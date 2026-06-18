.father {
    /* background-color: blueviolet; */
    /* 부모요소인 body에 flex를 줘야함. */
    display: flex;
    /* 자식요소들을 수평으로 정렬.. */
    /* justify-content: space-between;  */
    /* 각 자식 요소 간에 간격을 주고 싶을때는 gap을 사용한다. */
    /* 부모요소에게 gap을 설정해야함. */
    gap: 10px;

    /* flex container의 높이가 화면의 높이와 같게 함. */

    /* vh - 보여지는 화면(브라우저)의 전체높이를 기준으로 하는 단위... */
    핵심 개념
    1vh = 뷰포트 전체 높이의 1%

    100vh = 뷰포트 전체 높이의 100% (즉, 화면 전체 높이)
    height: 100vh;

    왜 쓰나요?
    보통 height: 100%를 사용하면 부모 요소의 높이에 영향을 받지만, 100vh를 사용하면 부모 요소가 무엇이든 상관없이 무조건 현재 보고 있는 브라우저 창의 전체 높이를 꽉 채우게 할 수 있습니다.


    /* flex-direction: row; 없어도 기본옵션임. row일 때는 오른쪽으로 가는 가로선임.. */
    /* 왼쪽에서 오른쪽으로 가로선. */
    flex-direction: row;


    /* justify-content는 flex container의 main axis(주축)에서 아이템을 정렬해준다. */
    /* justify-content: ; */
    /* align-items는 flex container의 교차축(cross axis)을 따라 flex-item들을 정렬해줌. align-items */
    align-items: center;
}

/* 지금 first-child는 h1이기때문에 주석처리. */
/* h1 {
    color: whitesmoke;
} */

.box {
    width: 200px;
    height: 200px;
    background-color: tomato;
    /* display: inline; - width or height를 사용하면사라짐. */
    /* display: block; */
    /* display: inline-block; */
}

.box:first-child {
    /* display: block; */
    /* margin-right: 25%; */
}

.box:last-child {
    /* display: block; */
    /* margin-left: 25%; */
}


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

1. 옮기고 싶은 물건을 찾는다.(예. class: box인 1,2,3,4,5)
2. 그 물건의 부모가 누구 인지 찾는다.(class: father)
3. 그 다음 그 부모에 display: flex를 넣으면 기본 flex container를 가질 수 있다.


부모가 결정하는 것 (주로 사용하는 속성들):

flex-direction: 가로로 정렬할까? 세로로 정렬할까?(column / row) 기본이 row로 설정되어 있음.
justify-content: 주축(주로 가로)으로 어떻게 정렬할까?(양옆으로? 중앙으로?)
align-items: 교차축(주로 세로)으로 어떻게 정렬할까? (위/중간/아래?)
gap: 자식들 사이의 간격은 얼마로 할까?
flex-direction

※row-reverse로 하고 flex-end로 하면 반대로 표시 123 →　321로 그리고 3끝이기 때문에 처음과 끝이 반대로 됨. 3의 위치가 end가 되어서 오른쪽 부터 왼쪽 순서대로 표시됨(왼쪽에 붙음).

flexbox의 axis(축)
・main axis(주축, 수평)
・cross axis(교차축, 수직)
→　그 축들이 있는 위치는 flex container의 direction에 따라 달라진다.

flex container가 row의 flex direction을 가질 때,
주축은 수평으로 왼쪽에서 오른쪽으로 이동하고,
교차축은 수직으로 위에서 아래로 이동한다.

flex박스의 규칙은 자식들이 아닌 부모랑만 얘기하는 거 였는데,
아주 드물게 부모뿐만이 아니고 자식과도 얘기할수 있음.

flex 속성 중 부모에만 줬던 속성들..
- 아이템 중앙 정렬 관련: justify-content / align-item
- row와 column의 gap지정 / row-gap && column-gap
- align-content, flex-direction && flex-wrap

◆flex 속성 중 자식들에 적용하는 속성들...
★order속성..
다른 자식들에게 상대적이다..




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

◆box-sizing: border-box;　vs box-sizing: content-box;

1. box-sizing: content-box
box의 width를 200px로 지정했다고 가정하고, 거기에 box에 padding-left를 50을 지정해주면

50 200*(총 250px)이 되버림..

2. box-sizing: border-box;
이 경우는 위와 같이 지정해주면...
50 150*(총 200px)이 되어서 추가한 50을 포함해서 전체 200px을 유지할 수 있음..


flex-wrap: nowrap의 문제.
css에서 box를 전부 width와 height를 200px로 설정했는데
html에서 box를 여러개 추가했을때, 위에서 설정한 넓이와 높이가 줄어들면서, 압축되면서 box가 한줄에 다 표시됨.(드래그 바가 생김.)

◆flex-wrap: wrap - Flex 컨테이너 내의 여러 아이템들이 한 줄에 배치될지, 공간이 부족할때 여러 줄로 나누어서 배치(줄 바꿈)될지를 결정함...
→ box의 width를 지정하고(200px) 그 width를 유지한 채로, 표시되다가 행이 꽉차면 다음줄로 줄바꿈시킴..*(박스들의 너비를 존중해줌..　fiex-direction: row일 경우한정)



그래서 flex-wrap을 사용하면 줄바꿈을 설정할 수 있음.*(기본 nowrap, 줄바꿈 하지 않음.)
※기본이 nowrap이기 때문에 지정을 안해도 상관 없지만, 굳이 명시하는 이유는,
1. 코드가 명확해지고*(이 코드는 줄바꿈이 일어나면 안되는구나를 파악)
2. 기존 스타일 덮어쓰기, 부모 스타일이나 라이브러리에서 이미 flex-wrap: wrap을 지정해 두었을 때, 이를 다시 줄 바꿈이 안되도록 기본값으로 강제 초기화해야 하는 경우 사용.
3. 반응형 웹 디자인: 화면 크기에 따라 미디어 쿼리(@media)를 쓸 때, 큰 화면에서는 한 줄로 보여 주고(nowrap), 작은 화면에서는 줄 바꿈을 하도록(wrap)유연하게 변경할 때 명시적으로 작성.



◆flex-flow(flex-direction + flex-wrap, 이 둘의 속성을 하나의 속성으로 설정 가능.)

사용 예. flex-wrap: row wrap; 이런식으로 가능.



◆align-content*(box사이의 여백을 조절하고 싶을때..)
※※여러 라인이 있을 때만 동작하고, 라인을 조절하고 싶을때 사용하면 됨!!!!!!!!!!

- 다중라인 flex 컨테이너에서 라인들의 정렬을 설정하는 데 유용하게 사용할 수 있다.

align-items는 항목들 전체를 위, 아래, 혹은 중앙으로 움직이는데,
각 라인은 못 움직임.. 그래서 커다란 여백이 생기게 됨...
교차축을 가로지르는 방향에서 항목을 이동시킴.

그래서 align-content을 이용하면 각 라인에서 발생한 여백도 조절할 수 있음.
align-content는 항목들을 움직이지 않음. 라인을 움직임..


◆gap을 줄때 서로 다른 gap 값을 주고 싶을때 사용.
- 만약에 행은 10px gap을 가지고 열은 20px gap을 가지게 하고 싶다면??

row-gap / column-gap 따로 지정이 가능함.



◆align-self
이것도 역시 flex 자식 항목의 속성임. 교차축 정렬을 정할 수 있게 한다.
하나의 자식에만 적용되는 align-items속성, 자식하나가 독립을 한다 생각하면 될듯.. 

◆직접 값을 설정하지 않고 플렉스 컨테이너로 크기를 정하기.

flex-grow(기본값 0) 
flex컨테이너 자식들에게 얼마만큼의 공간을 차지할 수 있는지 알려줌.
+ 남는 공간이 있을 때, 아이템을 얼마나 늘릴지(비율) 정함.

px이나 백분율을 사용하지 않고 비율만 사용함..!!

flex-shrink(flex-grow의 반대개념 / 이건 기본값이 1이다!!)
숫자가 높을수록 빨리 압축된다.
flex-grow와 마찬가지로 형제들에게 상대적으로 변함.

아이템이 얼마나 줄어들지 정할 수 있다.
+ 공간이 부족할 때, 아이템을 얼마나 줄일지(비율)을 정함.
어떤 비율로 어떤 순서로 먼저 줄어들지 정할수 있다.


flex basis - flex항목의 이상적인 크기인 초기 크기를 설정할 수 있다.
+ 아이템의 기본 크기 설정(width와 비슷하지만, 가로/세로 주축에 따라 자동으로 변함.)
그리고 그 크기에서 상자가 커지거나 줄어들지만 초기 시작 크기를 설정할 수 있다.

flex: grow shrink basis;로 한번에 쓸수 있다.

