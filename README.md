1. npm create vite@latest
2. npm install



◆layout - block <-> inline

<div class="box"></div>
<div class="box"></div>
<div class="box"></div

「div는 기본적으로 display프로퍼티가 block으로 설정되어 있고, 자신 옆에 그 어떤 요소도  　오는 것을 허락하지 않는다.　그래서 box들이 위아래로 쌓인다.」

.box {
    width: 200px;
    height: 200px;
    background-color: tomato;
    display: inline;
}

diplay: inline은 width와 height프로퍼티를 지원하지 않아서 같이 쓰면 블록이 사라짐..

diplay: inline-block은 width와 height프로퍼티를 지원하고 옆으로 나란히 블록을 표시할수 있다.

◆flexbox
요소들을 가로/세로 정렬하거나 배치하는 레이아웃 도구.


◆media query
css 디자인을 할때 하드코딩으로 맞을때 까지 조정하는 것보다 media query를 사용함.
- 화면 크기 변화에 대응하며, 20%를 설정한다고 가정했을때 큰화면이든 작은화면이든 20%에 똑같이 맞춰서 표시됨.