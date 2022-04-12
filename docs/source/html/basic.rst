BASIC
========


VSCODE
-------

1. Pretter HTML에서 제외하기

``F1 > format document with... 검색 > HTML 기본 선택한다``


CSS
-----------

`Flex Froggy <https://flexboxfroggy.com/#ko>`_

`CSS레이아웃 입문서 <https://developer.mozilla.org/ko/docs/Learn/CSS/CSS_layout/Introduction>`_

`Particle.js <https://github.com/VincentGarreau/particles.js>`_

`Chart.js <https://www.chartjs.org/>`_

``Css Tool Tip Disable- settings.json``

.. code-block::

    "editor.quickSuggestionsDelay": 1000,
    "editor.hover.enabled": false,
    "editor.parameterHints": false,


``HTML 파일의 CSS 주석이 이상할 때 <-- Live Sass compiler 충돌``

.. image:: https://user-images.githubusercontent.com/30430227/150738333-bd9ef207-2203-4554-8a37-82aa1118856b.png

.. image:: https://user-images.githubusercontent.com/30430227/150738676-3365ca27-3e68-45ac-9136-223544a98702.png


1. 가상요소 :before, after

.. code-block::

 .tab_type1 ul li a:before{
    content:"맛있는";
    width: 40px;
    padding: 3px 6px;
    margin: 0 5px;
    border-radius: 4px;
    background:red;
    text-align:center;
    color: white;
 }

.. image:: https://user-images.githubusercontent.com/30430227/73346127-b1142000-42c8-11ea-8db1-9b214669e73e.jpg


2. list-style: none

.. code-block::

 리스트 스타일
 *{
    padding:0;
    list-style: none;
 }


3. margin-left: auto

>>> 왼 쪽 마진을 공유한다 
 
.. image:: https://d2.naver.com/content/images/2018/12/helloworld-201811-flex_13.png

https://d2.naver.com/helloworld/8540176#ch2


4. flex border collapse Tip

.. code-block::

 ul      { border-width: 2px  0   0  2px }
 ul > li { border-width:  0  2px 2px  0  }

``border 속성 다음에 border-width가 놓어야 한다``

5. Div 속성 

``기본적으로 div는 가로너비(width가 100% 지만, width 속성을 지정하지 않고 margin과 padding을 지정했을 때 이를 포함한 너비가 100%``

.. image:: https://user-images.githubusercontent.com/30430227/150628505-3902efed-b557-4714-8bc4-22686d9f771f.png

.. code-block:: console

 <!DOCTYPE html>
 <html lang="en">
 <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            width: 500px;
            border: 1px solid #000;
        }
        .box div{
            width: 100%;
            margin: 20px;
            padding: 20px;
            background: dodgerblue;
        }
    </style>
 </head>
 <body>
    <div class="box">
        <div>width 를 지정하지 않고 margin 과 padding  을 지정하면</div>
    </div>
 </body>
 </html>

.. image:: https://user-images.githubusercontent.com/30430227/150628533-5e22c5e7-6734-43d2-b4a5-2cd91e7fc104.png


6. Inline 속성

``width, height 적용 불가, inline 요소 하위에 block 요소를 가질 수 없음, ``


7. Float 속성

.. code-block::

 어울림 효과 해지 - clear:both(left,right
 before와 :after에는 무조건 content:""; 속성이 들어가야 합니다.
 그리고 display:block을 해줘야 clear:both가 작동합니다.
 float은 "어울림" 이고 inline-block은 "글자처럼취급" 입니다. 

`이미지 <http://placeimg.com/640/480/any>`_

.. image:: http://placeimg.com/640/480/any


8. Modal Popup - target 선택자

.. image:: https://user-images.githubusercontent.com/30430227/150629353-a99c5d02-5952-446b-b59e-c4445d5fc1ff.png
.. image:: https://user-images.githubusercontent.com/30430227/150629348-afcb37e5-9368-472b-a4ad-bdc4c9b88c19.png

.. code-block:: console

 <!DOCTYPE html>
 <html lang="en">
 <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
            text-decoration: none;
        }
        #popup{
            display: none;
        }
        #popup:target{
            display: block;
        }
    </style>
 </head>
 <body>
    <a href="#popup" class="opener">클릭하세요</a>
    <div id="popup" class="layer">
        <h2>열려라</h2>
        <a href="#">닫혀라</a>
    </div>
 </body>
 </html>


9. 선택자 

..code-block::

 복합선택자
 + : 친구(friend 선택
 ~ : 친구들(friends 선택
 , : 다중(multi 선택
 :nth-child(n : n 번째 태그 선택
 :first-child : 첫번째(first 요소 선택
 :last-child : 마지막(last 요소 선택

 기타선택자
 * : 모든 태그(all 선택
 [attribute="value"] : 속성(attribute 선택
 가상 선택자
 :hover 마우스 올렸을 때
 :active 마우스 누르고 있을 때
 :before 태그 맨 앞에 가상 요소 추가
 :after 태그 맨 뒤에 가상 요소 추가
 a:visited 방문 했던 링크
 a:link 방문 하지 않은 링크
 :focus 입력 포커스가 있는 상태
 :checked input이 check 된 상태


10. 기타 

>>> 단어 - word-break: keep-all(단어가 분리되지 않는다

.. image:: https://user-images.githubusercontent.com/30430227/150629777-45e4399b-d176-48f0-a131-4859ddd1455c.png

.. code-block:: console

 <!DOCTYPE html>
 <html lang="en">
 <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
            text-decoration: none;
        }
        .layer{
            display: none;
            justify-content: center;
            align-items: center;
            background: dodgerblue;
            position: fixed;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
        }
        .layer .box{
            padding: 20px 20px 60px;
            width: 500px;
            background: white;
            position: relative;
        }
        .layer .close{
            position: absolute;
            right: 20px;
            bottom: 20px;
            display: block;
            background:#09F;
            color:#fff;text-align:center;
            padding:5px 20px;
            font-size:13px;
        }

        .layer:target{
            display: flex;
            animation: open 0.5s;
        }

        @keyframes open{
            from{opacity:0;} to {opacity:1;}
        }
    </style>
 </head>
 <body>
    <a href="#popup" class="opener">클릭하세요</a>
    <div id="popup" class="layer">
        <div class="box">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Inventore quibusdam nihil deserunt ratione optio nemo rem provident dicta facilis magni minima saepe,obcaecati eaque? Laudantium voluptatum iusto est beatae adipisci aliquam ex, doloribus blanditiis!
            <a href="#" class="close">닫혀라</a>
        </div>
    </div>
 </body>
 </html>


Pure CSS Parallax
-------------------


`출처 <https://www.hyungjoo.me/parallax-scroll원리](https://www.hyungjoo.me/parallax-scroll-%EC%9B%90%EB%A6%AC>`_

1. HTML

.. code-block:: console

 <div id="title" class="slide header">
  <h1>Pure CSS Parallax</h1>
 </div>

 <div id="slide1" class="slide">
  <div class="title">
    <h1>Slide 1</h1>
    <p>Lorem ipsum dolor sit amet, in velit iudico mandamus sit, persius dolorum in per, postulant mnesarchum cu nam. Malis movet ornatus id vim, feugait detracto est ea, eam eruditi conceptam in. Ne sit explicari interesset. Labores perpetua cum at. Id viris docendi denique vim.</p>
  </div>
 </div>

 <div id="slide2" class="slide">
  <div class="title">
    <h1>Slide 2</h1>
    <p>Lorem ipsum dolor sit amet, in velit iudico mandamus sit, persius dolorum in per, postulant mnesarchum cu nam. Malis movet ornatus id vim, feugait detracto est ea, eam eruditi conceptam in. Ne sit explicari interesset. Labores perpetua cum at. Id viris docendi denique vim.</p>
  </div>
  <img src="https://lorempixel.com/640/480/abstract/6/">
  <img src="https://lorempixel.com/640/480/abstract/4/"> 
 </div>

 <div id="slide3" class="slide">
  <div class="title">
    <h1>Slide 3</h1>
    <p>Lorem ipsum dolor sit amet, in velit iudico mandamus sit, persius dolorum in per, postulant mnesarchum cu nam. Malis movet ornatus id vim, feugait detracto est ea, eam eruditi conceptam in. Ne sit explicari interesset. Labores perpetua cum at. Id viris docendi denique vim.</p>
  </div> 
 </div>

 <div id="slide4" class="slide header">
    <h1>The End</h1>
 </div>



2. CSS

.. code-block:: console

 @import url(https://fonts.googleapis.com/css?family=Nunito;

 html {
  height: 100%;
  overflow: hidden;
 }

 body { 
  margin:0;
  padding:0;
	perspective: 1px;
	transform-style: preserve-3d;
  height: 100%;
  overflow-y: scroll;
  overflow-x: hidden;
  font-family: Nunito;
 }

 h1 {
   font-size: 250%
 }

 p {
  font-size: 140%;
  line-height: 150%;
  color: #333;
 }

 .slide {
  position: relative;
  padding: 25vh 10%;
  min-height: 100vh;
  width: 100vw;
  box-sizing: border-box;
  box-shadow: 0 -1px 10px rgba(0, 0, 0, .7;
	transform-style: inherit;
 }

 img {
  position: absolute;
  top: 50%;
  left: 35%;
  width: 320px;
  height: 240px;
  transform: translateZ(.25px scale(.75 translateX(-94% translateY(-100% rotate(2deg;
  padding: 10px;
  border-radius: 5px;
  background: rgba(240,230,220, .7;
  box-shadow: 0 0 8px rgba(0, 0, 0, .7;
 }

 img:last-of-type {
  transform: translateZ(.4px scale(.6 translateX(-104% translateY(-40% rotate(-5deg;
 }

 .slide:before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  box-shadow: 0 0 8px 1px rgba(0, 0, 0, .7;
 }

 .title {
  width: 50%;
  padding: 5%;
  border-radius: 5px;
  background: rgba(240,230,220, .7;
  box-shadow: 0 0 8px rgba(0, 0, 0, .7;
 }

 .slide:nth-child(2n .title {
  margin-left: 0;
  margin-right: auto;
 }

 .slide:nth-child(2n+1 .title {
  margin-left: auto;
  margin-right: 0;
 }

 .slide, .slide:before {
  background: 50% 50% / cover;  
 }

 .header {
  text-align: center;
  font-size: 175%;
  color: #fff;
  text-shadow: 0 2px 2px #000;
 }

 #title {
  background-image: url("https://placeimg.com/640/480/abstract/6/";
  z-index:2;
 }

 #title h1 {
 transform: translateZ(.25px scale(.75;
 transform-origin: 50% 100%;

 }

 #slide1:before {
  background-image: url("https://placeimg.com/640/480/abstract/4/";
  transform: translateZ(-1px scale(2;
 }

 #slide2 {
  background-image: url("https://lorempixel.com/640/480/abstract/3/";
  z-index:2;
 }

 #slide3:before {
  background-image: url("https://placeimg.com/640/480/abstract/5/";
  transform: translateZ(-1px scale(2;
 }

 #slide4 {
  background: #222;
 }


Animation 축약
---------------

.. code-block:: console

   div {
        animation-name: myShorthand;
        animation-duration: 3s;
        animation-timing-function: ease-in-out;
        animation-delay: 1s;
        animation-iteration-count: 3;
        animation-direction: alternate;
    }


  div { animation: myShorthand 3s ease-in-out 1s 3 alternate; }

	@keyframes movingPara {
        from { margin-left: 100%; }
        to { margin-left: 0%; }



이어서 메뉴
----------

.. code-block:: console

	<ul class="one">
    <li>메뉴1
        <ul class="two">
            <li>메뉴1-1</li>
            <li>메뉴1-2</li>
            <li>메뉴1-3</li>
        </ul>
    </li>
    <li>메뉴2
        <ul class="two">
            <li>메뉴2-1</li>
            <li>메뉴2-2</li>
            <li>메뉴2-3</li>
        </ul>
    </li>
    <li>메뉴3
        <ul class="two">
            <li>메뉴3-1</li>
            <li>메뉴3-2</li>
            <li>메뉴3-3</li>
        </ul>
    </li>
	</ul>
	
.. code-block::

 function handler(event{
    // 2단계. handler 의 함수를 작성. handler 함수가 호출이 되면 아래와 같은 행동을 하라.
    var $target = $(event.target;
        // 현재 클릭했던 요소가 뭔 요소인지 변수 $target 에 담는다.
    if($target.is("li"{
        // 만약에 $target 이 담고있었던 요소가 li 가 맞다면!
        $target.children(.toggle(;
            // 클릭했던 바로 그 li 의 자식 요소(.one li .two 을 토글 시켜라.
    }


  *{margin:0;padding:0;}
 li{list-style-type:none;text-align:center;}
 .one{background-color:#ffddd6;padding:10px;*zoom:1;}
 .one:after{content:'';display:block;clear:both;}
 .one>li{float:left;background-color:#ffffd6;margin-right:10px;cursor:pointer;}
 .two{background-color:#d6ffd9;padding:10px;}
 .two>li{background-color:#dad6ff;}
 }


.. code-block::

 $(".one".click(handler.find("ul".hide(;
    // 1단계. one 라는 클래스를 가진 요소를 클릭하게 되면 handler 라는 함수를 동작하게 하라
    // .one 가 자식으로 가지고 있는 요소들 중에 ul 을 찾아 숨겨라 <- 브라우저가 시작하마자 동작



팁 2
----------

1. border-radius 찌그러짐

``border-radius: 3%/10% //가로가 긴 경우 가로 % 값을 작게준다``


2. Fieldset
 
.. code-block::

 <form> <fieldset> <legend>개인정보:</legend>
    <label>이름: <input type="text"></label><br> 
    <label>주소: <input type="text">
    </label><br> <input type="submit"> </fieldset> </form>

 출처: https://webdir.tistory.com/318 [WEBDIR]


3. Input Type 선택

`` input[type=text] ``


4. clear both

.. code-block::

 div 블럭은 넓이를 얼마를 주던간에 아래로만 깔린다.//좌우 공간을 다 차지
 float 속성을 주면 옆으로 나란히 배열된다.//텍스트의 경우는 블럭을 둘러싸게된다
 블럭 줄바꿈(?을 하는 기능이 clear이다// left clear는 왼쪽에 붙는 것을 제거(안 붙는다
 #slide ul:after{content:"";display:block;clear:both;} //이렇게하면 ul 다음 블럭부터는 줄을 바꾸어 시작한다


5. radio 버튼

.. code-block::

 name은 같고 id(채널은 다르게한다
 <input type="radio" name="pos" id="pos1" checked>
 <input type="radio" name="pos" id="pos2">
 <input type="radio" name="pos" id="pos3">
 Label과 연동하기1 -for 사용
 <label for="pos1">일번 선택</label>

 Lable과 연동하기2 -라벨에 포함
 <label><input...>일번 선택</label>

 #pos1 :checked ~ ul // 라디오 채널(id pos1이 선택되었을 때 뒤의 태그 ul을 선택하여 속성 변경//이미지 슬라이드로


6. 전체 코드

.. code-block:: console

    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <title>Document</title>
    </head>
    <body>
    <style>
      *{margin:0;padding:0;}
      ul,li{list-style:none;}
      #slide{height:300px;position:relative;overflow:hidden;}
      #slide ul{width:400%;height:100%;transition:1s;}
      #slide ul:after{content:"";display:block;clear:both;}
      #slide li{float:left;width:25%;height:100%;}
      #slide li:nth-child(1{background:#faa;}
      #slide li:nth-child(2{background:#ffa;}
      #slide li:nth-child(3{background:#faF;}
      #slide li:nth-child(4{background:#aaf;}
      #slide input{display:none;}
      #slide label{display:inline-block;vertical-align:middle;width:10px;height:10px;border:2px solid #666;background:#fff;transition:0.3s;border-radius:50%;cursor:pointer;}
      #slide .pos{text-align:center;position:absolute;bottom:10px;left:0;width:100%;text-align:center;}
      #pos1:checked~ul{margin-left:0%;}
      #pos2:checked~ul{margin-left:-100%;}
      #pos3:checked~ul{margin-left:-200%;}
      #pos4:checked~ul{margin-left:-300%;}
      #pos1:checked~.pos>label:nth-child(1{background:#666;}
      #pos2:checked~.pos>label:nth-child(2{background:#666;}
      #pos3:checked~.pos>label:nth-child(3{background:#666;}
      #pos4:checked~.pos>label:nth-child(4{background:#666;}
    </style>
    <div id="slide">
      <input type="radio" name="pos" id="pos1" checked>
      <input type="radio" name="pos" id="pos2">
      <input type="radio" name="pos" id="pos3">
      <input type="radio" name="pos" id="pos4">
      <ul>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
      <p class="pos">
        <label for="pos1"></label>
        <label for="pos2"></label>
        <label for="pos3"></label>
        <label for="pos4"></label>
      </p>
    </div>
    </body>
    </html>



7. 자동슬라이드

.. code-block:: console

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
      <style>
        *{margin:0;padding:0;}
        ul,li{list-style:none;}
        .slide{height:300px;overflow:hidden;}
        .slide ul{width:calc(100% * 4;display:flex;animation:slide 8s infinite;} /* slide를 8초동안 진행하며 무한반복 함 */
        .slide li{width:calc(100% / 4;height:300px;}
        .slide li:nth-child(1{background:#ffa;}
        .slide li:nth-child(2{background:#faa;}
        .slide li:nth-child(3{background:#afa;}
        .slide li:nth-child(4{background:#aaf;}
        @keyframes slide {
          0% {margin-left:0;} /* 0 ~ 10  : 정지 */
          10% {margin-left:0;} /* 10 ~ 25 : 변이 */
          25% {margin-left:-100%;} /* 25 ~ 35 : 정지 */
          35% {margin-left:-100%;} /* 35 ~ 50 : 변이 */
          50% {margin-left:-200%;}
          60% {margin-left:-200%;}
          75% {margin-left:-300%;}
          85% {margin-left:-300%;}
          100% {margin-left:0;}
        }
      </style>
    </head>
    <body>
      <div class="slide">
        <ul>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
        </ul>
      </div>
    </body>
    </html>



8. Flex를 사용하는 방법

.. code-block:: console

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
      <style>
        *{margin:0;padding:0;}
        ul,li{list-style:none;}
        .slide{height:300px;overflow:hidden;position:relative;}
        .slide ul{width:calc(100% * 4;display:flex;transition:1s;}
        .slide li{width:calc(100% / 4;height:300px;}
        .slide li:nth-child(1{background:#ffa;}
        .slide li:nth-child(2{background:#faa;}
        .slide li:nth-child(3{background:#afa;}
        .slide li:nth-child(4{background:#aaf;}
        .slide input{display:none;}
        .slide .bullet{position:absolute;bottom:20px;left:0;right:0;text-align:center;z-index:10;}
        .slide .bullet label{width:10px;height:10px;border-radius:10px;border:2px solid #666;display:inline-block;background:#fff;font-size:0;transition:0.5s;cursor:pointer;}
        /* 슬라이드 조작 */
        #pos1:checked ~ ul{margin-left:0;}
        #pos2:checked ~ ul{margin-left:-100%;}
        #pos3:checked ~ ul{margin-left:-200%;}
        #pos4:checked ~ ul{margin-left:-300%;}
        /* bullet 조작 */
        #pos1:checked ~ .bullet label:nth-child(1,
        #pos2:checked ~ .bullet label:nth-child(2,
        #pos3:checked ~ .bullet label:nth-child(3,
        #pos4:checked ~ .bullet label:nth-child(4{background:#666;}
      </style>
    </head>
    <body>
      <div class="slide">
        <input type="radio" name="pos" id="pos1" checked>
        <input type="radio" name="pos" id="pos2">
        <input type="radio" name="pos" id="pos3">
        <input type="radio" name="pos" id="pos4">
        <ul>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
        </ul>
        <p class="bullet">
          <label for="pos1">1</label>
          <label for="pos2">2</label>
          <label for="pos3">3</label>
          <label for="pos4">4</label>
        </p>
      </div>
    </body>
    </html>



9. float:left 대신 요소 나란히 배열하고 화면 센터에 놓는 방법

.. code-block:: console

   .pagination a {
 -    display: block;
 +    display: inline-block;
     width: 30px;
     height: 30px;
 -    float: left;
     margin-left: 3px;
     background: url(/images/structure/pagination-button.png;
 }
 -대신 + 라인을 사용한다


비교 슬라이더
-------------
 
.. image:: https://user-images.githubusercontent.com/30430227/120735395-8291ff00-c525-11eb-8920-3865cbf69f4e.png

.. code-block:: console

 <style>
     *{
         margin: 0;
         padding: 0;
         box-sizing: border-box;
     }
     body{
         display: flex;
         justify-content: center;
         align-items: center;
         min-height: 100vh;
         background: #000;
     }
     .imgBox{
         position: relative;
         width: 442px;
         height: 500px;
         border: 3px solid white;
     }

     .imgBox textarea{
         position: absolute;
         top: 0;
         left: 0;
         width: 100%;
         max-width: 100%;
         height: 100%;
         background: url(../4g2.jpg ;
         background-size: cover;
         resize: none;
         opacity: 0.4;
         filter: grayscale(1 blur(5px;
         outline: none;
     }

     .imgBox textarea:nth-child(2{
         opacity: 1;
         filter: grayscale(0 blur(0;
         width: 150px;
         border-right: 2px solid yellow;
         resize: horizontal;
     }
 </style>
 </head>
 <body>

    <div class="imgBox">
        <textarea readonly></textarea>
        <textarea readonly></textarea>
    </div>



CSS 기초
----------

1. text-align 은 inline 속성에만 된다. 

2. &nbsp - no-break space

3. 반응형 높이값 - vw사용  height: 30vw;

4. disply:none 적용 안될 때 -  display: none !important;

5. css 파일 변경 

6. inline javascript open window

``<li><a href="#" onclick="window.open('https://www.mediace3d.com/','_blank'">MediACE3D.com</a></li>``

7. 기타

.. code-block::

 <link rel="icon" type="image/x-icon" href="./images/favicon_mediace3d.png">

 <link rel="stylesheet" id="changeStyle" href="./style.css">

 <a href="javascript:changeStyle(">Can't </a>

 function changeStyle({
    document.querySelector("#changeStyle".href="./styleTemp.css"
 }

.. image:: https://user-images.githubusercontent.com/30430227/149711123-244c71df-e787-424f-9c25-01de42b0941e.png

.. code-block:: console

 <!DOCTYPE html>
 <html lang="ko">
 <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
 </head>
 <body>
    <h1>나는 고양이를 사랑한다.</h1>

    <ul class="wrapper">
        <li>고양이 먹이 사세요</li>
        <li>운동</li>
        <li>기운내 친구야</li>
    </ul>

    <div class="container">
        <div class="box">부동</div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores excepturi sequi minima tenetur ad, enim laudantium deserunt odio nostrum. Numquam, tempora. Quia, minima. Totam sunt reiciendisexpedita explicabo doloremque perferendis tempore pariatur ex, illo exercitationem non, cupiditate assumenda ea est corrupti voluptate dolores eius neque dolor, quisquam odio nobis fugit sit sapiente. Optio animi saepe voluptates dicta neque dignissimos nulla ipsam, laboriosam, ducimus ipsa enim, reprehenderit temporibus debitis odio quod nisi? Sequi, eveniet sapiente.</p>
    </div>
    <br>

    <div class="position">
        <p>여기가 시작!</p>
        <p class="positioned">여기가 포지션!</p>
        <p>여기가 끝!</p>
    </div>

    <br>

    <form action="">
        <p>우선, 이름과 나이를 말씀해주세요</p>
        <div>
            <label for="이름">이름:</label>
            <input type="text" id="이름">
        </div>
        <div>
            <label for="성">성</label>
            <input type="text" id="성">
        </div>
        <div>
            <label for="나이">나이</label>
            <input type="text" id="나이">
        </div>
        
    </form>
 </body>
 </html>


.. code-block:: console

 *{
    list-style: none;
    margin: 0;
    padding: 0;
    font-size: 1em;
 }

 body{
    width: 900px;
    height: 2000px;
    margin: 0 auto;
 }

 h1{
    font-size: 2rem;
    font-size: 6vw;
    color: red;
 }


 .wrapper{
    display: flex;
    justify-content: space-around;
 }

 .wrapper li{
    flex: 1;
 }

 .wrapper li:first-child{
    display: block;
    flex: 3;
    width: 200px;
    height: 100px;
    background: yellow;
    border: 1px solid #000;
 }

 /* 컬럼 */

 .container{
    margin: 0;
 }

 .container p{
    /* column-width: 200px; */
    column-count: 2;
 }

 .box{
    width: 100px;
    height: 100px;
    border: 1px solid #000;
    float: left;
    margin-right: 5px;
 }

 .position p{
    padding: 10px;
    margin: 10px;
    background: tomato;
    border: 1px solid slateblue;
 }

 .position .positioned{
    position: relative;
    position: absolute;
    position: fixed;
    position: sticky;
    top: 30px;
    left: 30px;
 }
 /* r은 현재 위치를 기준 a는 부모의 위치를, fix는 절대위치-스크롤해도 고대로 */
 /* s은 스크롤 되다가 top에 도달하면 상단에 붙는다*/

 form{
    display: table;
    margin: 0 auto;
 }

 form p{
    display: table-caption;
    caption-side: bottom;
    width: 300px;
    color: #999;
 }

 form div{
    display: table-row;
 }

 form label, form input{
    display: table-cell;
    margin-bottom: 10px;
 }

 form label{
    width: 200px;
    padding-right: 5%;
    text-align: right;
 }

 form input{
    width: 300px;
 }

 /* 반응형 */

 @media screen and (min-width: 1000px{
    .container{
        margin: 1em 2em;
    }
    .container p{
        column-count: 3;
        
    }
 }

 @media (min-width: 700px{
    h1{
        font-size: 4rem;
    }
 }

 @media (max-width:500px{
    h1{
        font-size: 2em;
    }
 }




Header
------

1. Sticky Navbar on Scroll

.. image:: https://user-images.githubusercontent.com/30430227/149715453-289af4af-77e3-45bb-9543-f06e6d42a834.png

.. code-block:: console

 <!DOCTYPE html>
 <html lang="ko">
 <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
 </head>
 <body>
    <header>
        <a href="#" class="logo">Logo</a>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Team</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </header>

    <section class="banner"></section>
    
    <script type="text/javascript">
        window.addEventListener("scroll",(=>{
            const header = document.querySelector("header"
            header.classList.toggle("sticky", window.scrollY > 0
        }
    </script>

 </body>
 </html>


 @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100;300;400;500;700;900&display=swap';

 *{
    list-style: none;
    text-decoration: none;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-size: 1em;
    font-family: 'Noto Sans KR', sans-serif;
 }

 body{
    min-height: 200vh;
 }

 header{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: 0.6s;
    padding: 10px 100px;
    background: rgba(255,255,255,0;
 }

 /* 자바스크립트 연동 */

 header.sticky{
    padding: 5px 100px;
    background: rgba(255,255,255,1 ;
 }

 header .logo{
    position: relative;
    font-weight: 700;
    color: #000;
    font-size: 2em;
    text-transform: uppercase;
    letter-spacing: 2px;
    transition: 0.6s;
 }

 header ul{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
 }

 header ul li{
    position: relative;
 }

 header ul li a{
    position: relative;
    margin: 0 15px;
    color: #000;
    letter-spacing: 2px;
    font-weight: 500px;
    transition: 0.6s;
 }

 .banner{
    /* position: relative; */
    width: 100%;
    height: 100vh;
    background: url(images/main1.jpg;
    background-size: contain;
 }
 .wrapper{
    display: flex;
    justify-content: space-around;
 }


 .wrapper li{
    flex: 1;
 }

 .wrapper li:first-child{
    display: block;
    flex: 3;
    width: 200px;
    height: 100px;
    background: yellow;
    border: 1px solid #000;
 }

 /* 컬럼 */

 .container{
    margin: 0;
 }

 .container p{
    /* column-width: 200px; */
    column-count: 2;
 }

 .box{
    width: 100px;
    height: 100px;
    border: 1px solid #000;
    float: left;
    margin-right: 5px;
 }

 .position p{
    padding: 10px;
    margin: 10px;
    background: tomato;
    border: 1px solid slateblue;
 }

 .position .positioned{
    position: relative;
    position: absolute;
    position: fixed;
    position: sticky;
    top: 30px;
    left: 30px;
 }
 /* r은 현재 위치를 기준 a는 부모의 위치를, fix는 절대위치-스크롤해도 고대로 */
 /* s은 스크롤 되다가 top에 도달하면 상단에 붙는다*/

 form{
    display: table;
    margin: 0 auto;
 }

 form p{
    display: table-caption;
    caption-side: bottom;
    width: 300px;
    color: #999;
 }

 form div{
    display: table-row;
 }

 form label, form input{
    display: table-cell;
    margin-bottom: 10px;
 }

 form label{
    width: 200px;
    padding-right: 5%;
    text-align: right;
 }

 form input{
    width: 300px;
 }

 /* 반응형 */

 @media screen and (min-width: 1000px{
    .container{
        margin: 1em 2em;
    }
    .container p{
        column-count: 3;
        
    }
 }

 @media (min-width: 700px{
    h1{
        font-size: 4rem;
    }
 }

 @media (max-width:500px{
    h1{
        font-size: 2em;
    }
 }


Menu
------

1. TAB Table

.. image:: https://user-images.githubusercontent.com/30430227/149853528-1e32bb86-9bf5-4039-a332-ba4f6ba122b3.png

.. code-block:: console

        <input type="radio" name="tab" id="maf" checked>
        <input type="radio" name="tab" id="stl">
        <nav>
            <label for="maf" class="maf">MAF Files</label>
            <label for="stl" class="stl">STL Files</label>
        </nav>
        <table class="table mafTable">
            <thead>
                <tr>
                    <th>
                        <input type="checkbox" name="maf" id="allMaf" unchecked>
                    </th>
                    <th>No.</th>
                    <th>File</th>
                    <th>File Size</th>
                    <th>Date</th>
                    <th>Expires</th>
                    <th>File Check</th>
                    <th>User</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><input type="checkbox" name="maf" checked></td>
                    <td>1</td>
                    <td>test.MAF</td>
                    <td>8.5MB</td>
                    <td>2022-01-07 16:02</td>
                    <td>8 days left</td>
                    <td>Valid</td>
                    <td>Donald Trump</td>
                </tr>


.. code-block:: console

 #maf:checked ~ nav label.maf,
 #stl:checked ~ nav label.stl{
    color: teal;
    font-weight: 700;
 }

 section.mylist .table{
    display: none;
 }

 #maf:checked ~ table.mafTable{
    display: block;
 }

 #stl:checked ~ table.stlTable{
    display: block;
 }

 input[type=radio]{
    display: none;
 }


 section.mylist table{
    width: 100%;
    border-collapse: collapse;
 }

 section.mylist td, th{
    padding: 12px 15px;
    border: 1px solid #000;
    text-align: center;
    font-size: 1rem;
 }

 section.mylist th{
    background: teal;
    color: white;
 }

 section.mylist tbody tr:nth-child(even{
    background:azure;
 }



2. 전체 Check Box 선택

.. image:: https://user-images.githubusercontent.com/30430227/149853226-32e0ffa3-a565-4b80-97aa-12858f37e6c2.png

.. code-block:: console


            <thead>
                <tr>
                    <th>
                        <input type="checkbox" name="stl" id="allStl" unchecked>
                    </th>
                    <th>No.</th>

                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><input type="checkbox" name="stl" unchecked></td>
                    <td>1</td>
               </tr>


.. code-block:: console

        const allMaf = document.querySelector("#allMaf"

        allMaf.addEventListener('change', (=>{
            const checkboxes = document.getElementsByName("maf"

            checkboxes.forEach((i=>{
                i.checked = allMaf.checked
            }
        }



그림자 이미지
------------

.. image:: https://user-images.githubusercontent.com/30430227/151507338-8aa5b1b6-5b77-4019-9698-c5d1664bfbf0.png

.. code-block:: console

 <!DOCTYPE html>
 <html lang="ko">
 <head>
  <meta charset="UTF-8">
  <title>Document</title>
  <style>
    *{
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }
    body{
      width: 100%;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    section{
      width: 400px;
      height: 300px;
      display: flex;
      flex-direction: column;
    }
    section .top{
      border: 1px solid rgba(0,0,0,0.3;
      padding: 10px;
      text-align: justify;
    }
    section .btm{
      width: 100%;
      height: 15px;
      display: flex;
      justify-content: space-between;
    }
    .shadowl{
      background: url(./images/best-shadow-left.png no-repeat;
      background-size: cover;
      width: 200px;
      height: 15px;
    }
    .shadowr{
      background: url(./images/best-shadow-right.png no-repeat;
      background-size: cover;
      width: 200px;
      height: 15px;
    }
  </style>
 </head>
 <body>
  <section>
    <div class="top">Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio facere pariatur architecto esse modi voluptas sit consectetur, ab a non ullam. Error commodi atque inventore assumenda numquam quod doloremque sequi.</div>
    <div class="btm">
      <div class="shadowl"></div>
      <div class="shadowr"></div>
    </div>
  </section>
 </body>
 </html>


Bootstrap
------------

1. 로그인 폼

**form-floating - 레이블을 폼박스 안에 넣는다**

.. image:: https://user-images.githubusercontent.com/30430227/153338277-c5932ad7-c2f5-4e99-bcdc-856c24d07186.png
.. image:: https://user-images.githubusercontent.com/30430227/153338344-1b69b088-6241-484d-bd10-f1e027393f3b.png

.. code-block:: console

      <form action="">
        <div class="form-floating mb-5"> //mb(0~5 - margin-bottom
          <input type="email" id="form1example" class="form-control" placeholder=" " /> //placeholder 위치에
          <label for="form1example" class="form-label">Email address</label>
        </div>
      </form>


 **textarea에도 사용**

  <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea"></textarea>
  <label for="floatingTextarea">Comments</label>

.. image:: https://user-images.githubusercontent.com/30430227/153341657-bc11ae7f-a659-40f5-b9af-4cd4bb3049ed.png



**인풋 그룹**

.. code-block:: console

 <div class="input-group mb-5">
    <div class="input-group-text">@</div>
    <input type="text" class="form-control" id="inlineFormInputGroupUsername" placeholder="Username" />
 </div>

.. image:: https://user-images.githubusercontent.com/30430227/153344241-9ff52c01-68ce-49a1-b920-aa24adcc2275.png


2. 그리드

.. image:: https://user-images.githubusercontent.com/30430227/153340238-361c7211-1e83-481e-82d5-bef075f8b065.png


.. code-block:: console

            <div class="row mb-4"> // 열 시작
                <div class="col d-flex justify-content-center"> // 첫 번째 행
                    <div class="form-check">
                        <input type="checkbox" id="form1example3" class="form-check-input" checked />
                        <label for="form1example3" class="form-check-label">Remember me</label>
                    </div>
                </div>
                <div class="col"> // 두 번째 행
                    <a href="#!">Forget password?</a>
                </div>
            </div>


``<div class="form-check form-switch"> // form-switch 클래스``

.. image:: https://user-images.githubusercontent.com/30430227/153343546-85db7dba-cc5c-4f49-a2c2-bc7b6b4f33f3.png


3. 버튼

.. image:: https://user-images.githubusercontent.com/30430227/153342369-17c4c898-dff1-4087-aabd-72f6df9482a3.png

.. code-block:: console

            <div class="row">
                <button type="submit" class="btn btn-primary btn-block shadow">Sign in</button> //btn-block 가로100% 채운다
            </div>


.. image:: https://user-images.githubusercontent.com/30430227/153342595-18764884-a2b3-4768-89b2-45ef8a639140.png



**셀렉트**

.. code-block:: console

                <div class="col">
                    <select class="form-select">
                        <option value="1">One</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>

.. image:: https://user-images.githubusercontent.com/30430227/153345048-cfd39830-6ea3-485f-9bbe-0edbd46ee398.png


**버튼 그룹 - 접착**

.. code-block:: console

            <div class="btn-group mt-4"> 
                <button class="btn btn-primary">1</button>
                <button class="btn btn-primary">2</button>
                <div class="btn-group" role="group"> // 그룹 네스팅
                    <button type="button" id="btnGroupDrop" class="btn btn-primary dropdown-toggle" //dropdown-toggle
                        data-bs-toggle="dropdown" aria-expanded="false"> // dropdown 은 부트스트랩 자바스크립트 필요
                        Dropdown
                    </button>
                    <ul class="dropdown-menu" aria-labelledby="btnGroupDrop">
                        <li><a href="#" class="dropdown-item">Dropdown1</a></li>
                        <li><a href="#" class="dropdown-item">Dropdown2</a></li>
                        <li>
                            <hr class="dropdown-divider">
                        </li>
                        <li><a href="#" class="dropdown-item">Dropdown3</a></li>
                    </ul>
                </div>
            </div>


.. image:: https://user-images.githubusercontent.com/30430227/153348397-54c4ca4b-71bc-4cdb-a01c-207fdaa7877e.png

**페이지네이션**

.. code-block:: console

        <nav>
            <ul class="pagination">
                <li class="page-item"><a href="#" class="page-link">Previous</a></li>
                <li class="page-item"><a href="#" class="page-link">1</a></li>
                <li class="page-item active"><a href="#" class="page-link">2</a></li>
                <li class="page-item"><a href="#" class="page-link">3</a></li>
                <li class="page-item"><a href="#" class="page-link">Next</a></li>
            </ul>
        </nav>

.. image:: https://user-images.githubusercontent.com/30430227/153349286-2a2d48a2-df12-48c2-8f75-051e028fbd6a.png


4. Navbar

.. image:: https://user-images.githubusercontent.com/30430227/153352698-faa8af58-48ca-468d-877f-01d29da7f46f.png

.. image:: https://user-images.githubusercontent.com/30430227/153352645-064e5172-8d03-43f9-a32b-e2499804d223.png

.. code-block:: console

 * #navbarSupportedContent 토글(<button>/ <div>
    <header>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <!-- navbar-expand-lg: lg 즉 992px 이상일 때 펼친다 -->
            <div class="container-fluid">
                <a href="#" class="navbar-brand">Navbar</a>
                <button type="button" class="navbar-toggler" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0"> //marginend(좌/우정렬의 끝-2, margin-large-0
                        <li class="nav-item">
                            <a href="#" class="nav-link active" aria-current="page">Home</a>
                        </li>
                        <li class="nav-item">
                            <a href="#" class="nav-link">Link</a>
                        </li>
                        <li class="nav-item dropdown">
                            <a href="#" id="navbarDropdown" class="nav-link dropdown-toggle" role="button"
                                data-bs-toggle="dropdown" aria-expanded="false">
                                Dropdown
                            </a>
                            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                                <li><a href="#" class="dropdown-item">Action</a></li>
                                <li><a href="#" class="dropdown-item">Something else here</a></li>
                            </ul>
                        </li>
                        <li class="nav-item">
                            <a href="#" class="nav-link disabled">Disabled</a>
                        </li>
                    </ul>
                    <form action="" class="d-flex">
                        <input type="search" class="form-control me-2" placeholder="Search" aria-label="Search">
                        <button type="submit" class="btn btn-outline-success">Search</button>
                    </form>
                </div>
            </div>
        </nav>
    </header>




PHP
------


1. bitnami WAMP 설치 

``윈도우 환경 Path 에 등록``

.. image:: https://user-images.githubusercontent.com/30430227/149702592-dd000f72-e6e5-4a6c-8354-21e0042def11.png

``VSCode Extensions``

.. image:: https://user-images.githubusercontent.com/30430227/149688036-983b3dc8-d59a-4164-8b25-50b95c670cc0.png


2. 실행

.. image:: https://user-images.githubusercontent.com/30430227/149687744-2737f0e4-ece1-45de-92c5-9ce4f4b3b05f.png

``VSCode > XAMPP/htdocs 내 폴더 생성 > Setting 'F1', 'user setting'검색, 'php'검색 >Edit Setting Json``

.. image:: https://user-images.githubusercontent.com/30430227/149702200-969d0d62-6bb6-4ddb-a3fa-0e8192646077.png

.. image:: https://user-images.githubusercontent.com/30430227/149702318-eb79c18f-7069-488c-99b9-a974bf0764a1.png

.. code-block:: console

    ],
    "php.debug.executablePath":"C:\\php\\php.exe",
    "window.zoomLevel": 1
 }


``tasks.json 생성``

.. code-block:: console

 {
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "command": "chrome",

    "windows": {

    "command": "C:\\Program Files (x86\\Google\\Chrome\\Application\\chrome.exe"

    },

 

    "args": ["localhost\\${workspaceRootFolderName}\\${fileBasename}"]

 }

``서버 실행 > VSCode 'Ctrl-Shift-B'``

.. image:: https://user-images.githubusercontent.com/30430227/149702733-18a83a85-cf32-44d4-b4c5-c0fa39ae7a9b.png

``서버 주소 바꾸기 > Config 버튼 > Listen 주소 입력 > 서버 재시동 ``

.. image:: https://user-images.githubusercontent.com/30430227/149762552-d7b3141c-8ddd-4ed7-abc7-eb4369045b0f.png

.. image:: https://user-images.githubusercontent.com/30430227/149762929-ba9acbf0-6415-42ac-84a5-4459b6797fde.png

.. image:: https://user-images.githubusercontent.com/30430227/149762889-391d2b8b-2864-4969-8092-62846e4025ba.png


3. PHP include(partial

``기초``

.. image:: https://user-images.githubusercontent.com/30430227/149773138-8c70a567-23b8-49ea-93c5-72d8e3787939.png


``menu.php``

.. image:: https://user-images.githubusercontent.com/30430227/149773336-5c59db3e-2fd7-4778-bd7c-f31aec5dccb0.png

``default.php``

.. image:: https://user-images.githubusercontent.com/30430227/149773623-43dfc92d-2109-45d7-bc5b-800aa6058128.png


``레이아웃 표``

`참조사이트 <https://www.kimsq.com/docs/c/dev/extension/layout>`_

.. image:: https://user-images.githubusercontent.com/30430227/149775041-7ff04642-aada-4160-8b28-ed50ec238a7a.png
