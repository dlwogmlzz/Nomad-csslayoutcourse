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
flex컨테이너는 그 안에서 요소들이 움직이는 방향을 바꾸는 프로퍼티를 기본으로 가지고 있다.



부모가 결정하는 것 (주로 사용하는 속성들):

flex-direction: 가로로 정렬할까? 세로로 정렬할까?(column / row) 기본이 row로 설정되어 있음.
justify-content: 주축(주로 가로)으로 어떻게 정렬할까?(양옆으로? 중앙으로?)
align-items: 교차축(주로 세로)으로 어떻게 정렬할까? (위/중간/아래?)
gap: 자식들 사이의 간격은 얼마로 할까?
flex-direction


flexbox의 axis(축)
・main axis(주축, 수평)
・cross axis(교차축, 수직)
→　그 축들이 있는 위치는 flex container의 direction에 따라 달라진다.

flex container가 row의 flex direction을 가질 때,
주축은 수평으로 왼쪽에서 오른쪽으로 이동하고,
교차축은 수직으로 위에서 아래로 이동한다.


◆media query
css 디자인을 할때 하드코딩으로 맞을때 까지 조정하는 것보다 media query를 사용함.
- 화면 크기 변화에 대응하며, 20%를 설정한다고 가정했을때 큰화면이든 작은화면이든 20%에 똑같이 맞춰서 표시됨.





text-align: center vs justify-content: center의 차이
1. text-align: center; (텍스트 정렬)
╰ 이 속성은 블록 요소 안에 있는 '인라인 요소(글자, 이미지등)'를 정렬할 때 사용.
╰ 사용해도 가로 정렬은 되는데, 세로 정렬은 안된다.

2. justify-content: center; (박스 배치)
╰ 이 속성은 Flexbox 레이아웃에서 사용하며, '박스들(아이템들)'을 배치할 때 사용.

・적용 대상: display: flex;가 설정된 부모 요소에 설정한다!!
・부모 박스 안에 들어있는 자식 요소(박스들)들을 가로축(기본값) 기준으로 중앙으로 정렬한다.
・핵심!! 글자를 정렬하는 게 아니라, '덩어리(자식 박스)' 자체를 이동시켜서 중앙에 배치한다.

※display: flex / justify-content: center; / align-items 조합을 사용하면,
1. 가로 정렬(justify)과 세로 정렬(align)을 한 번에 제어할 수 있고,
2. 텍스트가 몇 줄이든 상관없이,
3. 박스 크기가 변해도 항상 완벽하게 정중앙에 위치 시킬 수 있다.


justify-content && align-items를 둘다 flex-start로 했을 때, 가로축과 세로축 둘다 처음이 왼쪽과 위에서 시작하기 때문에 이렇게 지정하면 왼쪽 위에 붙어서 표시됨..

Flex Direction이 row일때, 주축은 가로, column일 때는 세로.

Flex Direction이 row일때, 교차축은 세로(세로로움직임.), column일 때는 가로(가로로움직임.)

