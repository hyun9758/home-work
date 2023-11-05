## HOMEWORK MISSION-01
첫 번째 과제 진행

## 어려웠던 점

- 피그마 파일을 직접 따라하는 실습이 처음이라 피그마 파일을 여는 과정, 분석하는 과정, 파일을 추출하는 과정에서 시간이 오래 걸렸다.

- 또한 막상 css를 직접 입히니까 모르는 태그들이 많아서 알아보는 것도 무척이나 시간이 걸렸다.

- 뒤늦게 조원분께 여쭤봐서 flex 라는 속성을 사용하여 주요 이미지와 텍스트들을 배치한 후에 버튼을 따로 속성을 지정하여 만드는 것이 더 편리하다는 것을 깨달았지만 시간이 없어서 position: absolute로 진행하는 수 밖에 없었다.

- 현재 버튼 내에서 자꾸 배경이 겹쳐보이는 이슈가 발생하는데 그 이슈를 결국 해결하지 못해서 우선 제출하게 되었다. 해결하는 대로 다시 수정하여 제출할 생각이다. border는 이미 none 속성을 사용하여 감출 수 있었는데도 불구하고 배경이 자꾸만 사라지지 않는다..

(+)

2023.11.05.

겹쳐 보이는 속성이 버튼의 기본 패딩값이라는 것을 알게 되었다. 그래서 버튼의 기본 할당 패딩값을 padding: 0; 을 추가해서 오류를 수정하였다. 추후로 알게 된 것이 있다면 보통 버튼의 기본 할당값을 바꾸기 위해서 * { padding:0; margin:0} 을 추가하면 더욱 편하다는 것을 알게 되었다. 또한 하나 더 배운 게 있다면 flex 속성과 함께 wrap으로 감싸면 더욱 확대, 축소하였을 때 안 깨져서 좋다는 것 또한 다시 배울 수 있었다.

## 회고
처음으로 내 힘으로 제대로 작성한 이후에야 html이랑 css 감이 잡히는 것 같다. 초반에는 이미 배운 내용을 굳이 다시 배울 필요가 있을까 싶었는데 이렇게까지 깊게 공부해본 적은 처음이라 감회가 새롭다. 특히 피그마 파일을 잘 사용하면 디자인을 훌륭하게 뽑을 수 있어서 좋았다. 아쉬웠던 점은 이번주에 시간이 매우 촉박해서 과제에 목표 시간보다 덜 쏟을 수 밖에 없었는데, 그것이 아쉽다. 

코드를 작성할 때 우선 레이아웃을 그려보고, 들어가야 할 태그를 임의로 span, img, button 등을 다 넣어본 이후에야 하나씩 입력하기 시작했다. 그렇게 입력해야 조금 더 머릿속에 구조가 더욱 잘 잡히는 것 같다. 

## 사용한 도구 및 웹사이트
- 크롬 개발자 도구
- Figma
- Visual Studio Code
- https://wonit.tistory.com/314

## 과제 진행 시간 
- 2023.11.4 오전 12시~4시

## 코드 소개 

### HTML 코드

```
<!DOCTYPE html>
<html lang="ko">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="./css/mission-01.css">
  <title>1차 과제</title>
</head>

<body>
  <div class="box1">
    <img class="honey-logo" src="./images/logo.png" alt="Ottuki" />
    <span class="honey-text">따뜻한 차 향기</span>
    <button type="button" class="honeyB-arrow">
      <a href="./mission-01.html">
        <img src="images/button.png" alt="">
      </a>
    </button>
    <img class="honey-product" src="./images/product.png" alt="honey">
  </div>
  <div class="box2">
    <img class="handcream-logo" src="./images/logo (1).png" alt="kamil">
    <img class="handcream-product" src="./images/product (1).png" alt="handcream">
    <button type="button" class="button-buy">
      <a href="/mission-01/mission-01.html"></a>
      <span class="buy-text">구매하기</span>
      <img class="handcreamB-arrow" src="./images/angle-right.svg" alt="button-arrow">
    </button>
    <span class="handcream-text">핸드크림 모음</span>
  </div>
  <div class="box3">
    <img class="tea-logo" src="./images/logo (2).png" alt="gomgom">
    <img class="tea-product" src="./images/product (2).png" alt="tea">
    <button type="button" class="teaB-arrow">
      <a href="./mission-01.html">
        <img src="images/button.png" alt="">
      </a>
    </button>
    <span class="tea-text">고소한 보리차</span>
  </div>
</body>

</html>
```
### CSS 코드

```
/* 박스 정렬 */

.box1 {
  border: 1px solid var(--gray-500, #C4C4C4);
  background: var(--White, #FFF);
  width: 502px;
  height: 310px;
  position: relative;
}

.box2 {
  border: 1px solid var(--gray-500, #C4C4C4);
  background: var(--White, #FFF);
  width: 243px;
  height: 310px;
  position: relative;
}

.box3 {
  border: 1px solid var(--gray-500, #C4C4C4);
  background: var(--White, #FFF);
  width: 243px;
  height: 310px;
  position: relative;
}

/* 꿀 상품 */

.honey-text {
  color: var(--gray-800);
  text-align: center;
  font-family: Noto Sans;
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  line-height: 150%;
  position: absolute;
  top: 155px;
  right: 274px;
  width: 200px;
  height: 37px;
}

.honey-logo{
  width: 112px;
  height: 67px;
  flex-shrink: 0;
  position: absolute;
  top: 75px;
  right: 317px;
}

.honey-product{
  width: 222px;
  height: 270px;
  flex-shrink: 0;
  position: absolute;
  top: 20px;
  right: 28px;
}

.honeyB-arrow{
  width: 42px;
  height: 42px;
  flex-shrink: 0;
  position: absolute;
  top: 248px;
  right: 440px;
  border: none;
}

/* 핸드크림 */

.handcream-logo{
  width: 114px;
  height: 42px;
  flex-shrink: 0;
  position: absolute;
  right: 65px;
  top: 14px;
}

.handcream-text {
  color: var(--grayscale-gray-5, #555);
  text-align: center;
  font-family: Noto Sans;
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 150%; /* 27px */
  position: absolute;
  top: 66px;
  right: 22px;
  width: 200px;
  height: 27px;
}

.handcream-product {
  width: 195.005px;
  height: 196px;
  flex-shrink: 0;
  position: absolute;
  right: 24.99px;
  top: 100px;
}

.buy-text{
  color: var(--White, #FFF);
  /* Text/Medium/14 */
  font-family: Noto Sans;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%; /* 16.8px */
}

.button-buy{
  display: inline-flex;
  padding: 12px 18px 13px 20px;
  justify-content: center;
  align-items: center;
  gap: 16px;
  background: var(--blue-600, #0074E9);
  position: absolute;
  left: 20px;
  bottom: 20px;
}

.handcreamB-arrow {
  width: 6px;
  height: 10px;
  fill: var(--gray-100, #F3F3F3);
}

/* 보리차 */

.tea-logo{
  width: 114px;
  height: 42px;
  flex-shrink: 0;
  position: absolute;
  top: 14px;
  right: 65px;
}

.tea-text{
  color: var(--grayscale-gray-5, #555);
  text-align: center;
  font-family: Noto Sans;
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 150%; /* 27px */
  position: absolute;
  top: 66px;
  right: 22px;
  width: 200px;
  height: 27px;
}

.tea-product{
  width: 195.005px;
  height: 196px;
  flex-shrink: 0;
  position: absolute;
  top: 100px;
  right: 24.99px;
}

.teaB-arrow{
  position: absoolute;
  right: 181px;
  bottom: 20px;
  width: 42px;
  height: 42px;
  flex-shrink: 0;
  fill: var(--opacity-20, rgba(0, 0, 0, 0.20));
  position: absolute;
  left:20px;
  bottom: 20px;
  border: none;
}

/* 박스 위치 조정 */

.box1 {
  position: absolute; /* 절대 위치 지정 */
  top: 0; /* 맨 위에 위치 */
  /* 나머지 스타일은 그대로 유지 */
}

.box2 {
  position: absolute;
  top: 320px; /* box1의 height + 간격 등을 고려해 조절 */
}

.box3 {
  position: absolute;
  top: 320px; /* box1의 height + 간격 등을 고려해 조절 */
  left: 260px; /* box2의 width + 간격 등을 고려해 조절 */
}
```