

<br> 
<h1>React</h1>
<br>




#3


**TODO APP**

<br>

```javascript
import React, { useEffect, useRef, useState } from 'react';
import Chart from 'chart.js/auto';

const apiUrl = `http://apis.data.go.kr/B552584/ArpltnInforInqireSvc/getCtprvnRltmMesureDnsty`;
const serviceKey = 'S9dwnUfVwm8%2FDBGjdL7fJ78YXnxqwUdIpBCU3RwTlTiJ7pEjm0eWlVN3JRdM9Xaj5RJNh1zyjyJAYfw7ZOXREw%3D%3D';
const TType = 'json';
const numOfRows = 100;
const pageNo = 1;
const ver = 1.0;

export default function App() {
  const chartRef = useRef(null);
  const [selectedRegion, setSelectedRegion] = useState('서울');
  const [chartType, setChartType] = useState('line');
  const [dataTime, setDataTime] = useState('');
  const [chartData, setChartData] = useState({ labels: [], values: [] });
  const chartInstance = useRef(null);

  useEffect(() => {
    fetchData(selectedRegion)
      .then(data => {
        const labels = data.map(item => item.stationName);
        const values = data.map(item => item.pm10Value);

        setChartData({ labels, values });
        setDataTime(data[0].dataTime); // 첫 번째 항목의 dataTime 값을 설정
      })
      .catch(error => {
        console.log('Error:', error);
      });
  }, [selectedRegion]);

  function handleRegionChange(event) {
    setSelectedRegion(event.target.value);
  }

  function handleChartTypeChange(event) {
    setChartType(event.target.value);
  }


  // api 요청
  function fetchData(region) {
    const url = `${apiUrl}?sidoName=${encodeURIComponent(region)}&pageNo=${pageNo}&numOfRows=${numOfRows}&returnType=${TType}&serviceKey=${serviceKey}&ver=${ver}`;

    return fetch(url)
      .then(response => response.json())
      .then(result => {
        if (result.response.header.resultCode === '00') {
          return result.response.body.items;
        } else {
          throw new Error(result.response.header.resultMsg);
        }
      });
  }

  useEffect(() => {
    if (chartRef.current && chartData.labels.length > 0) {
      // 이전 차트 제거
      if (chartInstance.current) {
        chartInstance.current.destroy();
      }

      // 새로운 차트 생성
      const ctx = chartRef.current.getContext('2d');
      chartInstance.current = new Chart(ctx, {
        type: chartType,
        data: {
          labels: chartData.labels,
          datasets: [
            {
              label: 'PM10',
              data: chartData.values,
              backgroundColor: chartType === 'bar' ? 'rgba(54, 162, 235, 0.5)' : 'rgba(255, 99, 132, 0.5)',
              borderColor: chartType === 'bar' ? 'rgba(54, 162, 235, 1)' : 'rgba(255, 99, 132, 1)',
              borderWidth: 1,
            },
          ],
        },
        options: {
          responsive: true,
          scales: {
            y: {
              beginAtZero: true,
            },
          },
        },
      });
    }
  }, [chartData, chartType]);

  return (
    <div>
      <h1>미세먼지(PM10) 농도</h1>
      <div>
        <select value={selectedRegion} onChange={handleRegionChange}>
          <option value="서울">서울</option>
          <option value="부산">부산</option>
          <option value="대구">대구</option>
          <option value="인천">인천</option>
          {/* 추가적인 지역 옵션을 필요에 따라 추가 */}
        </select>
      </div>
      <div>
        <select value={chartType} onChange={handleChartTypeChange}>
          <option value="line">선 차트</option>
          <option value="bar">바 차트</option>
        </select>
      </div>
      <div> 측정 일시 : {dataTime}</div>
      <div>
        <canvas ref={chartRef}></canvas>
      </div>
    </div>
  );
}

```