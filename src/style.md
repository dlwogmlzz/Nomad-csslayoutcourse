.father {
    /* background-color: blueviolet; */
    /* 부모요소인 body에 flex를 줘야함. */
    display: flex;
    /* 자식요소들을 수평으로 정렬.. */
    /* justify-content: space-between;  */
    /* 각 자식 요소 간에 간격을 주고 싶을때는 gap을 사용한다. */
    /* 부모요소에게 gap을 설정해야함. */
    gap: 10px;
    flex-direction: row;
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