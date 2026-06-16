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
부모요소에 적용하여 그 안에 자식요소들을 정렬하는 방식.
Flexbox를 사용하려면, 정렬하고 싶은 대상(자식들)을 감싸고 있는,
부모 태그에 display:flex;를 선언해야 한다.

부모가 결정하는 것 (주로 사용하는 속성들):

flex-direction: 가로로 정렬할까? 세로로 정렬할까?(column / low)
justify-content: 주축(주로 가로)으로 어떻게 정렬할까?(양옆으로? 중앙으로?)
align-items: 교차축(주로 세로)으로 어떻게 정렬할까? (위/중간/아래?)
gap: 자식들 사이의 간격은 얼마로 할까?



◆media query
css 디자인을 할때 하드코딩으로 맞을때 까지 조정하는 것보다 media query를 사용함.
- 화면 크기 변화에 대응하며, 20%를 설정한다고 가정했을때 큰화면이든 작은화면이든 20%에 똑같이 맞춰서 표시됨.