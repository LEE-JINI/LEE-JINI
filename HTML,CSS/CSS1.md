<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <!--     
    단위
    <style>
        ul {
            font-size: 1.5rem;
        }

        .px {
            font-size: 16px;
        }

        .rem {
            /* 1rem = 브라우저의 기본 글자크기 rem : root element*/
            font-size: 1rem;
        }

        .em {
            /* 1em = 부모 엘리먼트의 글자 크기 */
            font-size: 1em;
        }

        .percent {
            /* 100% = 부모 엘리먼트의 글자 크기 */
            font-size: 100%;
        }

        .vw {
            /* 100vm = view port의 넓이 (width) */
            font-size: 10vw;
        }

        .vh {
            /* 100vh = view port의 높이 (heigth) */
            font-size: 10vh;
        }
    </style>

    <ul>
        <li class="px">font-size: 16px</li>
        <li class="rem">font-size: 1rem</li>
        <li class="em">font-size: 1em;</li>
        <li class="percent">font-size: 100%</li>
        <li class="vw">font-size: 10vm;</li>
        <li class="vh">font-size: 10vh;</li>
    </ul> -->
    <!-- 

    <h1>css 색상 표기법</h1>
    <style>
        li:first-child {
            color: red;
        }

        li:nth-child(2) {
            color: rgb(255 0 0)
        }

        li:nth-child(3) {
            /* rgb+a opacity ( 투명도 0~1 까지 ) */
            color: rgba(255 0 0 / 0.5)
        }

        li:nth-child(4) {
            /* hex ( haxadecimal), 16진수 */
            color: #ff0000;
        }

        li:last-child {
            /* rr gg bb 각각 모두 같을 떄 사용 가능 */
            color: #f00;
        }
    </style>

    <ul>
        <li> list item</li>
        <li> list item</li>
        <li> list item</li>
        <li> list item</li>
        <li> list item</li>
    </ul> -->

    <!-- <h1> font style </h1>

    <style>
        .not-italic {
            font-style: normal;
        }
        .italic { 
            /* 이탈릭 = 기울기 */
            font-style: italic;
        }


    </style>
    
    <ul>
        <li>list item</li>
        <li class="not-italic">list item</li>
        <li class="italic">list item</li>
    </ul> -->

    <!-- <h1> font weight </h1>
    <style>
        .font-thin {font-weight: 100;}
        .font-normal { font-weight: 400;}
        .font-bold { font-weight: 700;}
    </style>
    <ul>
        <li class="font-thin">list item</li>
        <li class="font-normal">list item</li>
        <li class="font-bold">list item</li>
    </ul> -->
    <!-- 
    <h1>text align ( 정렬 ) </h1>
    <style>
        .text-left { text-align: left;}
        .text-center { text-align: center;}
        .text-right { text-align: right;}
    </style>
    <ul>
        <li class="text-left">list item</li>
        <li class="text-center">list item</li>
        <li class="text-right">list item</li>
    </ul> -->

    <!-- <h1>letter spacing ( 글자간격 )</h1>
    <style>
        .tracking-tightest { letter-spacing: -0.05em;}
        .tracking-normal { letter-spacing: 0em;}
        .tracking-widest { letter-spacing: 0.1em;}
    </style>
    <ul>
        <li class="tracking-tightest">list item</li>
        <li class="tracking-normal">list item</li>
        <li class="tracking-widest">list item</li>
    </ul> -->

    <!-- <h1>line height 줄간격</h1>
    <style>
       .leanding-none { line-height: normal;}
       .leanding-8 { line-height: 2rem;}
    </style>
    <p class="leanding-none">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum laboriosam tempora beatae error eaque expedita accusamus quae natus vel quidem? Nostrum consequatur quas sit provident? Autem soluta dicta aspernatur ex.</p>
    <p class="leanding-8">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Est at dolorum veritatis, in itaque aspernatur numquam quaerat omnis inventore nisi autem. Distinctio, consequuntur dignissimos. Officiis veritatis rerum dignissimos consequuntur repellat!</p> -->



    <!-- <h1></h1>
    <style>
       
    </style>
    <ul>
        <li>list item</li>
        <li>list item</li>
        <li>list item</li>
    </ul> -->

    <!-- <style>
        .text1 {letter-spacing: 0.1; text-align: center;}
        .text2 {line-height: 2rem; text-align: center;}
        .text3 {text-align: center; font-style: italic;}
    </style>
    
    <h1>Q. Typography</h1>
    <h3 class="text1" > GUINNESS </h3>
    <P class="text2">Lorem ipsum, dolor sit amet consectetur adipisicing elit. <br>
        Nihil error aspernatur illo eos sunt dicta adipisci qui deleniti sapiente, <br>
        nam minus, accusamus, <br>
         quam nemo fuga sit dolorem provident voluptas reiciendis.</P>
    <p class="text3">- Dublin, lreland </p> -->

    <!-- <h1>color / background </h1>
    <style>
        li{
            background-color: #333;
            color: #fff;
        }
    </style>
    <ul>
        <li>list item</li>
        <li>list item</li>
        <li>list item</li>
    </ul> -->
    <!-- 
    <h1> border </h1>
    <p> 엘리먼트의 경계선 </p>
    <style>
        .item{
            /* 엘리먼트가 옆으로 된다고 생각하면 됨. 아마 보더레이아웃처럼 */
            display: inline-block;
        }
        .border {
            border-width: 1px;
            border-style: solid;
            border-color: #000;
        }
        .border-t {
            border-top-width: 1px;
            border-top-style: solid;
            border-top-color: #000;
        }
        .border-x {
            border-left-width: 1px;
            border-left-style: solid;
            border-left-color: #000;
            border-right-width: 1px;
            border-right-style: solid;
            border-right-color: #000;
        }
    </style>

    <div class="item border">border</div>
    <div class="item border-t">border t</div>
    <div class="item border-x">border x</div> -->

    <!-- <style>
        .font-white {
            color: white;
        }

        .font-gray {
            color: gray;
        }

        .back {
            background-color: black;
        }

        p {
            background-color: black;
            color: gray;
        }

        .border-b {
            border-bottom: 3px solid orange;
        }
    </style>

    <h1> Q. background-color, border </h1>
    <div class="back">
        <h1 class="font-white border-b">GUINNESS</h1>
        <div class="border-t"></div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis eius voluptatum asperiores deleniti nihil
            aliquam debitis, eligendi aut consectetur provident sed recusandae laboriosam id ut accusamus consequatur
            quaerat soluta perferendis.</p>
    </div> -->

    <!-- <h1> padding </h1>
<p> 엘리먼트 내부 공간 </p>
<style>
    .item {
        display: inline-block;
        border: 1px dashed;
    }
    .p-2{
        padding: 0.5rem;
    }
    .pt-2{
        padding-top: 0.5rem;
    }
    .px-2{
        padding-left: 0.7rem;
        padding-right: 0.7rem;
    }
</style>

<div class="item">padding 0</div>
<div class="item p-2">padding all</div>
<div class="item pt-2">padding top</div>
<div class="item px-2">padding left/right</div> -->

    <!-- <h1>margin</h1>
    <p> 엘리먼트 외부의 공간 </p>
    <style>
        .item{
            border: 1px dashed;
            display: inline-block;
        }
        .m-2 { margin: 1rem;}
        .mt-2 { margin-top: 1rem;}
        .mx-2 { 
            margin-left: 1rem;
            margin-right: 1rem;
        }
    </style>

<div class="item"> margin 0</div>
<div class="item m-2"> margin all</div>
<div class="item mt-2"> margin top</div>
<div class="item mx-2"> margin left / right </div> -->

    <!-- <h1>Q. Buttons </h1>
    <h4>Are you sure to submit?</h4>
    <style>
        .btn {
            padding: 0.5rem;
            /* margin-left: 0.5rem; */
            margin-right: 0.5rem;
           
        }
    </style>
    <button class="btn">Submit</button>
    <button class="btn">cancle</button> -->

    <!-- <h1> box size </h1>
    <p> 엘리먼트 크기 조절</p>
    <style>
        .item {
            width: 100px;
            height: 100px;
            padding: 10px;
            background-color: white;
            border: 2px solid #888;
        }

        .content-box {
            /* 기본값 패딩과 보더가 w,h 밖으로 적용 됨 */
            box-sizing: content-box;
        }

        .border-box {
             /* 기본값 패딩과 보더가 w,h 안으로 적용 됨 */
            box-sizing: border-box;
        }
    </style>
    <h3> box-sizing: content-box</h3>
    <div class="item content-box">124 x 124</div>
    <h3> box-sizing: border-box</h3>
    <div class="item border-box">100 x 100</div>-->

    <!-- <h1>display</h1>
    <p> 엘리먼트를 어떻게 배치할 것인가</p>
    <p>block, inline-block, inline, none, ....</p>
    <style>
        .item {
            background-color: white;
            /* 부모의 넓이를 모두 차지 */
            /* body, div, p, nav, 기타 */
            display: block;
        }
    </style>

    <div class="item"> block </div>
    <div class="item"> block </div> -->
    <!-- block 하나씩 줄바꿈해서 배치 , inline flow layout 같은 -->

    <!-- <h1>display</h1>
    <p> inline-block</p>
    <style>
        .item {
            background-color: white;
           /* 컨텐츠 필요한 만큼만 넓이 차지 */
           /* button, input, img 등 */
            display: inline-block;
        }
    </style>

    <div class="item"> inline-block </div>
    <div class="item"> inline-block </div>  -->

    <!-- <h1>display</h1>
    <p> inline </p>
    <style>
        .item {
            background-color: white;
            /* 레이아웃 용으로 적합하지 않
            - width, height 가 적용되지 않
            - y 축 패딩과 마진이 적동되지 않
            span, a
            */
            display: inline;
        }
    </style>

    <div class="item"> inline </div>
    <div class="item"> inline </div>  -->

    <!-- <h1>display</h1>
    <p> none </p>
    <style>
        .item {
            background-color: white;
            display: none;
        }
    </style>

    <div class="item"> none </div> -->

    <!-- <h1>width</h1>

    <style>
        .item {
            background-color: #ddd;
            width: 100px;
        }
        .block {
            display: block;
        }
        .inline-block {
            display: inline-block;
        }

    </style>

    <h3>display block</h3>
    <div class="item block">item</div>
    <div class="item block">item</div>
    
    
    <h3>display inline-block</h3>
    <div class="item inline-block">item</div>
    <div class="item inline-block">item</div> -->

    <!-- <h1>max-w , max-h</h1>
    <style>
        .container {
            border: 1px dashed;
        }

        .item {
            background-color: #ddd;
            display: block;
        }

        .min-w-600px {
            min-width: 600px;
        }

        .max-w-600px {
            max-width: 600;
        }
    </style>

    <h3>min width</h3>
    <div class="item min-w-600px">min width 600px</div>
    <h3>max width</h3>
    <div class="item max-w-600px">max width 600px</div> -->

    <!-- <h1>height</h1>
    <style>
        .item {
            background-color: #ddd;
        }

      .h-auto {
        /* 기본값 */
        height: auto;
       }

       .h-100px {
            height: 100px;
        }
        </style>

        <h3>height auto</h3>
        <div class="item h-auto">item</div>

        <h3>height 100</h3>
        <div class="item h-100px">item</div> -->


    <!-- <h1>max-height</h1>
    <style>
        .item {
            background-color: #ddd;
        }

        .max-h-50px {
            max-height: 50px;
        }
    </style>
    <h3> max-height: 50px</h3>
    <div class="item max-h-50px"> item </div>

    <h3> max-height: 50px</h3>
    <div class="item max-h-50px">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Reprehenderit tempora doloremque voluptas impedit
        reiciendis voluptatum. Quaerat, temporibus, perspiciatis excepturi mollitia error provident ullam iste dolorum
        ipsa incidunt, laborum laudantium saepe?
    </div>

    <h1>min-height</h1>
    <style>
        .item {
            background-color: #ddd;
        }

        .min-h-50px {
            min-height: 50px;
        }
    </style>
    <h3> min-height: 50px</h3>
    <div class="item min-h-50px"> item </div>

    <h3> min-height: 50px</h3>
    <div class="item min-h-50px">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Reprehenderit tempora doloremque voluptas impedit
        reiciendis voluptatum. Quaerat, temporibus, perspiciatis excepturi mollitia error provident ullam iste dolorum
        ipsa incidunt, laborum laudantium saepe?
    </div> -->

    <!-- <h1>Q.display, widht/height</h1>
    <style>
        .item {
            display: inline-block;
        }
        .i_green {
            width: 50px;
            height: 100px;
            background-color: green;
        }
        .i_white {
            width: 50px;
            height: 100px;
            background-color: white;
        }
        .i_yellow {
            width: 50px;
            height: 100px;
            background-color: yellow;
        }
        .n_red {
            width: 150px;
            height: 50px;
            background-color: red;
        }
        .n_white {
            width: 150px;
            height: 50px;
            background-color: white;
        }
        .n_blue {
            width: 150px;
            height: 50px;
            background-color: blue;
        }

    </style>


    <h4>Ireland</h4>
    <div class="item i_green"></div>
    <div class="item i_white "></div>
    <div class="item i_yellow "></div>

    <h4>Netherlands</h4>
    <div class="n_red "></div>
    <div class="n_white "></div>
    <div class="n_blue "></div> -->

    <!-- <h1> overflow </h1>
    <p> 콘텐츠가 넘쳤을 때 </p>
    <style>
        .item {
            height: 50px;
            background-color: #ddd;
        }
        .hidden {
            overflow: hidden;
        }
        .scroll {
            overflow: scroll;
        }
        .auto {
            overflow: auto;
        }
        .visible {
            overflow: visible;
        }
    </style>

    <h3> hidden </h3>
    <div class="item hidden"> Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
    </div>
    <br>
    <h3> scroll x,y 둘 다 스크롤 생김 </h3>
    <div class="item scroll"> Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
    </div>
    <br>
    <h3> auto 오버플로우 축만 스크롤 생성  </h3>
    <div class="item auto"> Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
    </div>
    <br>
    <h3> visible </h3>
    <div class="item visible"> Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis ipsa quo id modi quia, excepturi aliquam temporibus assumenda quisquam nisi nulla aliquid ullam commodi, blanditiis accusamus saepe eos alias at.
    </div> -->

    <!-- <h3> transform </h3>
    <p> translate 이동, scale 크기 , rotate 회전 </p>

    <style>
        .item {
            background-color: #ddd;
            width: 100px;
            height: 100px;
        }
        .translate {
            transform: translate(1rem, 1rem);
        }
        .scale-110 {
            transform: scale(1.1);
        }
        .rotate-12 {
            transform: rotate(12deg);
        }


    </style>

<h3>none</h3>
<div class="item"></div>
<h3>translate</h3>
<div class="item translate"></div>
<h3>scale</h3>
<div class="item scale-110"></div>
<h3>rotate</h3>
<div class="item rotate-12"></div> -->
    <!-- 
    <h1>white space 여백처리 </h1>
    <style>
        .container {
            border: 1px dashed;
            overflow: auto;
        }

        .item {
            background-color: #ddd;
            display: inline-block;
            width: 200px;
        }

        .ws_nor {
            white-space: normal;
        }

        .ws_now {
            white-space: nowrap;
        }
    </style>
    <h3>nomal</h3>
    <div class="container ws_nor">
        <div class="item">item</div>
        <div class="item">item</div>
        <div class="item">item</div>
    </div>
    <h3>mowrap</h3>
    <div class="container ws_now">
        <div class="item">item</div>
        <div class="item">item</div>
        <div class="item">item</div>
    </div> -->

    <!-- <h1> float &#128519 </h1>
    <p> 엘리먼트를 왼쪽 또는 오른쪽으로 띄움 </p>

    <style>
        .container {
            border: 1px dashed;
        }

        .clear-both {
            clear: both;
        }

        .item {
            background-color: #ddd;
            padding: 0.5rem;
        }

        .float-l {
            float: left;
        }

        .folat-r {
            float: right;
        }
    </style>

    <h3>left</h3>
    <div class="item float-l">item</div>
    <div class="item float-l">item</div>
    <div class="item float-l">item</div>
    <div class="clear-both"></div>

    <h3>right</h3>
    <div class="item folat-r">item</div>
    <div class="item folat-r">item</div>
    <div class="item folat-r">item</div>
    <div class="item folat-r">item</div> -->

    <!-- <h1>flex &#129321;</h1>
    <style>
        .container {
            display: flex;
            border: 1px dashed;
        }

        .item {
            padding: 0.5rem;
            background-color: #ddd;
        }
    </style>

    <div class="container">
        <div class="item"> item </div>
        <div class="item"> item </div>
        <div class="item"> item </div>
    </div> -->

    <!-- <pre>
        flex container 속성

        - flex-direction(row) item 의 배열방향
        row, row-reverse, column, colunm-reverse

        - flex-wrap


    </pre> -->


    <!-- <h1>flex direction</h1>
<p> item의 배열방향</p>

<style>
    .con {
        display: flex;
        border: 1px dashed;
    }
    .item {
        background-color: #ddd;
        padding: 0.5rem;
    }
    .flex-row {
        flex-direction: row;
    }
    .flex-col{
        flex-direction: column;
    }


</style>

<h3>flex row</h3>
<div class="con flex-rov">
<div class="item"> item row 일 떄는 width 가 컨텐츠 맞춤 </div>
<div class="item"> item</div>
<div class="item"> item</div>
</div>

<h3>flex row</h3>
<div class="con flex-col">
<div class="item"> item</div>
<div class="item"> item</div>
<div class="item"> item</div>
</div> -->

    <!-- <h1>flex rap</h1>
<p>item 을 감쌀 것인지 여부</p>

<style>
    .con{
        display: flex;
        border: 1px dashed;
    }
    .item {
        background-color: #ddd;
        width: 200px;
        padding: 0.5rem;
    }
    .f-wrap {
        flex-wrap: wrap;
    }
    .f-nowrap {
        flex-wrap: nowrap;
    }
</style>

<h3>flex warp</h3>
<div class="con f-wrap">
    <div class="item"> item</div>
    <div class="item"> item</div>
    <div class="item"> item</div>
</div>

<h3>flex nowarp</h3>
<div class="con f-nowrap">
    <div class="item"> item 감싸지 않아서 아이템 크기가 줄어듦. 그래서
        width 200인데 200아니게 됨.
    </div>
    <div class="item"> item</div>
    <div class="item"> item</div>
</div> -->

    <!-- <h1>justify-content</h1>
<p>item의 수평방향</p>

<style>
.con {
    display: flex;
    flex-direction: row;
    border: 1px dashed;
}
.item{
    background-color: #ddd;
    padding: 0.5rem;
}
.j-start {
    justify-content: start;
}
.j-center{
    justify-content: center;
}
.j-between {
    justify-content: space-between;
}
.j-end {
    justify-content: flex-end;
}

</style>

<h3>justify-content flex-start(de)</h3>
<div class="con j-start">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div>

<h3>justify-content center</h3>
<div class="con j-center">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div>

<h3>justify-content space-between</h3>
<div class="con j-between">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div>

<h3>justify-content flex-end</h3>
<div class="con j-end">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div> -->
    <!-- 
<h1>justify-content</h1>
<p>item의 수직방향</p>

<style>
.con {
    display: flex;
    flex-direction: column;
    border: 1px dashed;
    height: 400px;
}
.item{
    background-color: #ddd;
    padding: 0.5rem;
}
.j-start {
    justify-content: start;
}
.j-center{
    justify-content: center;
}
.j-between {
    justify-content: space-between;
}
.j-end {
    justify-content: flex-end;
}

</style>

<h3>justify-content flex-start(de)</h3>
<div class="con j-start">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div>

<h3>justify-content center</h3>
<div class="con j-center">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div>

<h3>justify-content space-between</h3>
<div class="con j-between">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div>

<h3>justify-content flex-end</h3>
<div class="con j-end">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div> -->

    <!-- <h1>align items (row)</h1>
<style>
    .con {
        display: flex;
        : row;
        border: 1px dashed;
        height: 100px;
    }
    .item {
        background-color: #ddd;
        padding: 0.5rem;
    }
    .i-stretch{
        align-items: stretch;
    }
    .i-center{
        align-items: center;
    }
    .i-baseline{
        align-items: baseline;
    }
    .i-end{
        align-items: flex-end;
    }

</style>

<h3>stretch(default)</h3>
<div class="con i-stretch">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div>

<h3>center</h3>
<div class="con i-center">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div>

<h3>baseline</h3>
<div class="con i-baseline">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div>

<h3>end</h3>
<div class="con i-end">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div> -->
    <!-- 
<h1>align items (column)</h1>
<style>
    .con {
        display: flex;
        flex-direction: column;
        border: 1px dashed;
    }
    .item {
        background-color: #ddd;
        padding: 0.5rem;
    }
    .i-stretch{
        align-items: stretch;
    }
    .i-start{
        align-items: flex-start;
    }
    .i-center{
        align-items: center;
    }
    .i-end{
        align-items: flex-end;
    }

</style>

<h3>stretch(default)</h3>
<div class="con i-stretch">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div>

<h3>start</h3>
<div class="con i-start">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div>

<h3>center</h3>
<div class="con i-center">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div>

<h3>end</h3>
<div class="con i-end">
    <div class="item">item</div>
    <div class="item">item</div>
    <div class="item">item</div>
</div> -->

    <!-- <h1>Q. flex container </h1>
<style>
.con{
    display: flex;
    height: 100px;
    border: 1px dashed;
    flex-direction: row;
    justify-content:  space-between;
    align-items: flex-end;
}
.item{
background-color: #ddd;
padding: 0.5rem;
}

</style>
<div class="con">
    <div class="item">itme</div>
    <div class="item">itme</div>
    <div class="item">itme</div>
</div> -->

    <!-- <h1>flex gorw</h1>
    <p> 한 줄에서 아이템이 남은 공간 차지 </p>
    <style>
        .con {
            border: 1px dashed;
            display: flex;
        }

        .item {
            padding: 0.5rem;
        }

        .g-0 {
            background-color: #ddd;
            flex-grow: 0;
        }

        .grow {
            background-color: #0bf;
            flex-grow: 1;
        }
    </style>

    <div class="con">
        <div class="item g-0">item</div>
        <div class="item grow">item</div>
        <div class="item g-0">item</div>
    </div>  -->
<!-- 
<h1>flex shrink</h1>
    <p> itme 크기 축소, 설정한 크기 만큼 </p>
    <style>
        .con {
            border: 1px dashed;
            display: flex;
        }

        .item {
            width: 200px;
            padding: 0.5rem;
        }

        .shrink {
            background-color: #ddd;
            flex-shrink: 1;
        }

        .shrink-0 {
            background-color: #0bf;
            flex-shrink: 0;
        }
    </style>

    <div class="con">
        <div class="item shrink">item</div>
        <div class="item shrink-0">item (not shrink)</div>
        <div class="item shrink">item</div>
    </div> -->

    <!-- <h1>flex basis</h1>
    <p> itme 넓이 </p>
    <style>
        .con {
            border: 1px dashed;
            display: flex;
        }

        .item {
            background-color: #ddd;
            padding: 0.5rem;
        }

        .b-auto {
            /* default */
            flex-basis: auto; 
        }
        .b-100 {
            flex-basis: 100px; 
        }
        .b-50 {
            flex-basis: 50%; 
        }
    </style>
<h3>flex basis auto</h3>
    <div class="con">
        <div class="item b-auto">item</div>
        <div class="item b-auto">item</div>
    </div>
    <h3>flex basis 100px</h3>
    <div class="con">
        <div class="item b-100">item</div>
        <div class="item b-100">item</div>
    </div>

    <h3>flex basis 50% 퍼센트하면 고무 태그 기준?</h3>
    <div class="con">
        <div class="item b-50">item</div>
        <div class="item b-50">item</div>
    </div> -->

    <!-- <h1>order</h1>
    <p>item의 순서, none 부터 순서 지정되</p>
    <style>
        .con {
            border: 1px dashed;
            display: flex;
        }

        .item {
            background-color: #ddd;
            padding: 0.5rem;
        }
        .o-1{
            order: 1;
        }
        .o-2{
            order: 2;
        }
        .o-none{
            /* default */
            order: 0;
        }
    </style>

<div class="con">
<div class="item o-2">itme 1</div>
<div class="item o-1">itme 2</div>
<div class="item o-none">itme 3</div>
<div class="item o-none">itme 4</div>


</div> -->

<!-- <h1> 레이아웃 만들기 </h1>
<style>
    .con {
        border: 1px dashed;
        display: flex;
    }

    .item { 
        background-color: #ddd;
        padding: 0.5rem;
    }
    /* .g-0{ 
        flex-grow: 0;
        background-color: #ddd;
    } 기본값은 안해도 됨 */
    .g{
        flex-grow: 1;
        background-color: #0bf;
    }
</style>
    
<div class="con">
    <div class="item ">item</div>
    <div class="item g">item</div>
    <div class="item ">item</div>
</div> -->

<!-- <h1>grid</h1>
<p> 격자 모양의 레이아웃</p>
<style>
.grid{
    display: grid;
    gap: 0.5rem;
}
.g-cols-3{
    grid-template-columns: repeat(3,minmax(0,1fr));
    /* 첫번쨰인자가 최소값 두번쨰 최대값( 그냥 많이 통용 ) */
}
.g-cols-6{
    grid-template-columns: repeat(6,minmax(0,1fr));
    /* 첫번쨰인자가 최소값 두번쨰 최대값( 그냥 많이 통용 ) */
}
.item{
    background-color: #ddd;
    padding: 0.5rem;
}

/* 칼럼병힙 */
.col-span-2{
    grid-column: span 2/span 2;
}
.col-span-4{
    grid-column: span 4/span 4;
}
.col-start-1{
    grid-column-start: 1;
}
.col-start-2{
    grid-column-start: 2;
}
.col-end-3{
    grid-column-end: 3;
}
.col-end-4{
    grid-column-end: 4;
}
.col-end-7{
    grid-column-end: 7;
}

</style>

<div class="grid g-cols-3">
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
<div class="item">item</div>
</div>

<h3>colum span 병합</h3>
<div class="grid g-cols-3">
    <div class="item">item1</div>
    <div class="item">item2</div>
    <div class="item">item3</div>
    <div class="item col-span-2">item4</div>
    <div class="item">item5</div>
    <div class="item">item6</div>
    <div class="item col-span-2">item7</div>
    </div>
</body>

<h3>column strat, column end</h3>
<div class="grid g-cols-6">
    <div class="item col-start-2 col-span-4">item1</div> 2번째 열에서 4개가 병합됨
    <div class="item col-start-1 col-end-3">item2</div> 1번째 시작 3번째 끝이니까 2번까지 병합
    <div class="item col-end-7 col-span-2">item3</div> 뒤에 2개 병합
    <div class="item col-start-1 col-end-7">item4</div> 1시작 7이 끝이니까 6까지 병합
    </div>
</body> -->

<!-- <h1>grid</h1>
<p>격자 모양의 레이아웃</p>
<h1>Q. gird</h1>
<style>
    .g{
        display: grid;
        gap: 0.5rem; 
    }
    .g-cols-3{
    grid-template-columns: repeat(3,minmax(0,1fr));
    /* 첫번쨰인자가 최소값 두번쨰 최대값( 그냥 많이 통용 ) */
}
    .item{
        background-color: #ddd;
        padding: 0.5rem;
    }
    .span-2{
        grid-column: span 2;
    }
</style>
<div class="g g-cols-3">
    <div class="item">item</div>
    <div class="item span-2">item</div>
    <div class="item span-2">item</div>
    <div class="item">item</div>
</div> -->

<!-- <h1>position</h1>
<p> 엘리먼트의 위치 속성 <br>
    static , relative, absolute, fixed
</p>
<style>
    .item{
        display: inline-block;
        background-color: #ddd;
        padding: 0.5rem;
    }
    .static{
        /* default */
        position: static;
    }
    .relative {
        position: relative;
    }
    .t-2{
        top: 0.5rem;
    }
    .l-2{
        left: 0.5rem;
    }
</style>
<h3>position static </h3>
<div class="item static">item</div>
<div class="item static">item</div>
<div class="item static">item</div>

<h3>position relative</h3>
<div class="item static">item</div>
<div class="item relative t-2 l-2">item</div> 원래 자신의 위치를 기준으로 이동함
<div class="item static">item</div>

</div> -->

<!-- <h1>position absolute</h1>
<p>relative 부모를 기준으로 위치한다</p>
<style>
    .con{
        position: relative;
        width: 200px;
        height: 100px;
        border: 1px dashed;
    }
    .itme{
        background-color: #ddd;
        padding: 0.5rem;
    }
    .absolute{
        position: absolute;
    }
    .left-0{
        left: 0;
    }
    .bottom-0{
        bottom: 0;
    }
</style>
/* 이미지 위에 텍스트가 올 때 주로 사용함. (엘리먼트 겹ㅊ칠 때
컨테이너ㅡㄴ 그대로 두고 엘ㄹ먼트만 ㅇ이동) */
<div class="con">
<div class="itme absolute left-0 bottom-0" > itme</div>
</div> -->


<!-- <h1>position fixed</h1>
<p>viewport 기준으로 위치한다 ( 보이는 곳 기준 ( 계쏙 따라옴, 네비게이션같) </p>
<style>
    body{
        height: 100px;
    }
    .itme{
        background-color: #ddd;
        padding: 0.5rem;
    }
    .fixed{
        position: fixed;
    }
    .top-0{
        top: 0;
    }
    .right-0{
        right: 0;
    }
</style>

<div class="itme fixed top-0 right-0" > itme</div> -->

<!-- <h1>반응형 스타일</h1>
<style>
    .title::after{
        content: "Extra small devices";
    }
    /* 디바이스 크기를 기준으로 640 이하면 엑스트라 스몰 , 모바일 퍼스트 ( 기준임 )*/
    @media (min-width: 640px){
        .title::after{
            content: "Small devices";
        }
    }
    @media (min-width: 768px){
        .title::after{
            content: "Medium devices";
        }
    }
    @media (min-width: 1024px){
        .title::after{
            content: "Large devices";
        }
    }
    @media (min-width: 1280px){
        .title::after{
            content: "Extra Large devices";
        }
    }
    @media (min-width: 1536px){
        .title::after{
            content: "2 Extra Large devices";
        }
    }

</style>

<div class="container">
<h3 class="title">Devices : </h3>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit.
    Sequi explicabo iusto tempora distinctio fuga, pariatur
    sapiente accusamus cupiditate rem similique doloremque
    veniam ab non in veritatis deleniti, adipisci consequuntur saepe.</p>
</div> -->

<!-- <h1>이미지</h1>
<style>
    .item{
        width: 200px;
        height: 200px;
    }
    .o-cover{
        object-fit: cover;
        /* 이미지 비율 조정 */
    }
    .bg-img{
        background-image: url('https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMjExMjhfMjYz%2FMDAxNjY5NTk4NTU2MTk2.fiwTsT0FLLKRxGwYe4sObc2qmF1fkyAhWUHPyFzPZsog.btKP4kLZKyq2btIrhc-nWasulyZrSiLo5EhFOYs39nkg.JPEG.blueumio2%2F637c69a3187dd2738250.jpg&type=sc960_832');
        background-size: cover;
        background-position: center;
        센터 아닐때는 왼쪽부터 보여줌.
    }
</style>

<h3>img</h3>
<img src="https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMjExMjhfMjYz%2FMDAxNjY5NTk4NTU2MTk2.fiwTsT0FLLKRxGwYe4sObc2qmF1fkyAhWUHPyFzPZsog.btKP4kLZKyq2btIrhc-nWasulyZrSiLo5EhFOYs39nkg.JPEG.blueumio2%2F637c69a3187dd2738250.jpg&type=sc960_832" class="o-cover">
<h3>background img</h3>
<div class="item bg-img"></div> -->
</body>
</html>