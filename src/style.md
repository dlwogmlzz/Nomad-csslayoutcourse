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