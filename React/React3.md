

<br> 
<h1>React</h1>
<br>




#3


**TODO APP**

<br>

```javascript
import './App.css';
import { useState, useEffect, useRef } from 'react';

// 필터 조건
const FILTER_MAP = {
  All: () => true,
  Done: (task) => task.completed, // 완료된것만
  Active: (task) => !task.completed // 완료되지 않은 것만
}

// Object.keys(객체): 객체의 속성 이름을 문자열 배열로 리턴한다.
// all, done , active
const FILTER_NAMES = Object.keys(FILTER_MAP);

// 로컬 스토리지 동기화하는 함수
function saveDoc(tasks){
  localStorage.setItem("tasks", tasks); // tasks 라는 키를 가진 로컬 스토리지를 찾아서 동기화 함.
}

// tasks 변수의 초기값, localStorage tasks 으면 [] 가져옴
const initialTasks = localStorage.getItem("tasks") || "[]";


// 메인 컴포넌트
export default function App() {

  // JSON.parse JSON 포맷을 js 객체 형태로 반환 해줌.
    const [tasks, setTasks] = useState(JSON.parse(initialTasks)); // tasks 있으면 localStorage 저장된 값 가져옴
    const [filter, setFilter] = useState("All");
    console.log(tasks); // 추적
    console.log(filter); // all , 초기값 all 줘서

    // 할일 추가 함수
    function addTask(name){
      const newTask ={
        id: `todo-${Date.now()}`, // 현재 시간을 ms 로 나타내는 함수
        name,
        completed: false
      }

      // 업데이트 하는코드 , 최신 문법 기존의 tasks + newTask 해서 변수에 담는다.
      const updateTasks = [...tasks, newTask];

      setTasks(updateTasks);

      // 로컬스토리지 동기화, updateTasks 는 js 객체인데 로컬 스토리지에 js 객체는 저장 못 해서 json 으로 변환해줌.
      saveDoc(JSON.stringify(updateTasks));
    }

    // 할일 삭제 함수
    function deleteTask(id) {

      // 전달받은 id 와 일치하지 않는 id를 가진 task 만 리턴.
       // filter 메소드도 반복문 같음. 리턴값이 true 인 것을 기반으로 새로운 배열을 만드는 함수. 콜백함수
        const remainingTasks = tasks.filter(task => task.id !==id);
        setTasks(remainingTasks);
        saveDoc(JSON.stringify(remainingTasks));
    }

    // 할일의 완료 상태 다루는 함수
    function toggleTaskCompleted(id) {
      const updatedTasks = tasks.map(task => {
        if (task.id === id) {
          return { ...task, completed: !task.completed };
        }
        return task;
      });
    
      setTasks(updatedTasks);
      saveDoc(JSON.stringify(updatedTasks));
    }
    

    // 할일 수정 함수
    function editTask(id, newName){
      const editedTasks = tasks.map(task => {
        if(task.id === id){
          return {...task, name: newName}
        }
        return task;
      })
      setTasks(editedTasks);
      saveDoc(JSON.stringify(editedTasks));
    }


    // 필터버튼 , 리스트 출력할 때 컴포넌트 사용
    const filterButtons = FILTER_NAMES.map( name => (
      <FilterButton
      key={name}
      name={name}
      isPressed={filter == name}
      setFilter={setFilter} />
    ))

    // 할일 목록, 출력할 트리를 변수에 담아둠. map은 key가 꼭 필요함!
    // FILTER_MAP[filter]: 필터링 조건
    const taskList = tasks.filter(FILTER_MAP[filter]).map(task => (
      <Todo
        key={task.id}
        id={task.id}
        name={task.name}
        completed={task.completed}
        deleteTask={deleteTask}
        toggleTaskCompleted={toggleTaskCompleted}
        editTask={editTask} />
    ))

    return (
      <div className="app-container">
        {/* 제목 */}
        <h1 className="app-title"> 할일 목록 </h1>

        {/* 폼 */}
        <Form addTask={addTask} />

        {/* 필터 버튼 */}
        <div className="filter-btn-group">
          {filterButtons}
        </div>

        {/* 할일 목록 */}
        <h2 className="remaining"> {taskList.length} 개 남았습니다.</h2>
        <ul>
          {taskList}
        </ul>

      </div>
    )
}

// 폼 컴포넌트
function Form({addTask}) {

  // 컴포넌트 내에서만 접근 가능.
  const [name, setName] = useState("");

  function handleSubmit(e) {

    e.preventDefault();

    // app 메인 컴포넡트에 있는 함수
    addTask(name);

    setName(""); // 폼 제출시 input 비운다.

  }

  return (
    <form className="todo-form" onSubmit={handleSubmit}>
      <input
        type="text"
        className="add-input"
        value={name}
        onChange={(e) => setName(e.target.value)}
        autoComplete="off"
      />
      <button
        type="submit"
        disabled={!name.trim()} // 빈문자열이 아니면 활성화 됨.
        className="add-btn" > 추가 </button>
    </form>
  )
}

// 필터 버튼
// name, isPressed, setFilter 전달 받았음. map 으로 3개 불러 왔었음.
// 생성된 버튼 하나하나가 필터 컴포넌트
function FilterButton( { name, isPressed, setFilter}) {
  return (
    <button className={`filter-btn ${isPressed && "active"}`}
      onClick={() => setFilter(name)}>
      {name}
    </button>
  )

}

// Todo 컴포넌트
function Todo({id, name, completed, deleteTask, toggleTaskCompleted, editTask}) {


  // 템플릿 상태를 결정하는 변수
  const [isEditing, setIsEditing] = useState(false);
  // 새로운 할 일 이름
  const [newName, setNewName] = useState("");

  // useRef Hook : 엘리먼트 접근
  const inputEl = useRef(null); // 실제 값을 전달하기 전 까지 useRef 초기값은 null
  // 이벤트 효과
  useEffect(() => {
      // 수정중일때
      if(isEditing) {
        // useRef 는 current 속성에 엘리먼트를 담는다.
        // 가상의 엘리먼트가 실제 html 에 주입되고 난 뒤에 input 접근 가능.
          inputEl.current.focus(); // 수정 버튼 눌러서 수정상황이면 포커스 여기로.
      }
  })

  // 업데이트 폼 제출
  function handleSubmit(e) {
    
    e.preventDefault();

    editTask(id, newName);

    // 수정 후 다시 뷰 템플릿으로 이동.
    setIsEditing(false);
    setNewName("");
  }



  const viewTemplate = (
    <div className="view-template">
      {/* 할일 이름 */}
      <div className="todo-details">
        <input
          type="checkbox"
          id={id}
          className="todo-checkbox"
          // 이걸 추가해서 새로고침 해도 완료 결과 안 바뀌게
          checked={completed}
          onChange={() => toggleTaskCompleted(id)} />
          <label htmlFor={id} className="todo-name">
            {name}
          </label>
      </div>

      {/*  버튼 그룹 */}
      <div className="view-btn-group">
        <button className="edit-btn"
        onClick={() => setIsEditing(true)}>
          수정
        </button>
        <button className="delete-btn"
          onClick={() => deleteTask(id)}>
          삭제
        </button>
      </div>
    </div>
  );


  const editingTemplate = (
    <form onSubmit={handleSubmit} className="edit=template">
      <input 
        type="text"
        className="edit-input"
        onChange={(e) => setNewName(e.target.value)}
        ref={inputEl} />

      {/*  버튼 그룹 */}
      <div className="edit-btn-group">
        <button 
          className="cancel-btn"
          type="button"
          onClick={() => setIsEditing(false)}>
          취소
        </button>
        <button
          type="submit"
          className="save-btn"
          disabled = {!newName.trim()}>
          저장
        </button>
      </div>

    </form>
    
  )

  return (
    <li className="todo-item">
      {isEditing ? editingTemplate : viewTemplate}
    </li>
  )

}
```