# Frontend Mentor - Single-page design portfolio solution

## 목차

- [개요](#개요)
  - [진행과제](#진행과제)
  - [스크린샷](#스크린샷)
  - [링크](#링크)
- [진행과정](#진행과정)
  - [사용언어와 라이브러리](#사용언어와-라이브러리)
  - [터득내용](#터득내용)


## 개요

### 진행과제

- 기기의 화면 크기에 따른 최적의 사이트 레이아웃 보기
- 페이지의 모든 대화형 요소에 대한 호버 상태 보기
- 마우스/트랙패드 또는 키보드를 사용하여 슬라이더 탐색

### 스크린샷

![1](https://user-images.githubusercontent.com/76725512/191451369-a600f059-c7bb-4742-955c-6d87950f72dc.JPG)
![2](https://user-images.githubusercontent.com/76725512/191451375-e6eeb504-82d6-4293-8d4e-557da348403a.JPG)
![3](https://user-images.githubusercontent.com/76725512/191451378-e4e952cc-d30f-4138-993c-c897847aff75.JPG)
![4](https://user-images.githubusercontent.com/76725512/191451383-5384c743-164e-4f6b-bb48-57aaa3dcf1ed.JPG)

### 링크
- [go-page](https://swiperjs.com/)

## 진행과정

### 사용언어와-라이브러리

- Semantic HTML5 markup
- SCSS
- Flexbox
- [Swiper](https://okhee-singlepage.netlify.app/) - slide library


### 터득내용

* 폰트사이즈를 rem으로 적용할 때, SCSS에 함수를 만들어 사용하였다. 그 과정에서 연산과 단위를 연결시켜주는 방법을 배웠습니다.
* 스와이퍼의 사용법과, 원하는 이미지사이즈에서 센터모드로 적용하는 법을 배웠습니다.


```scss
// rem 사이즈 구하는 함수
@function rem($pixSize, $context: $base-font-size) {
    @return $pixSize / $context * 1rem;
}
```
```javascript
new Swiper('.slide .swiper', {
        slidesPerView: "auto", // 슬라이드에 한번에 보여줄 개수
        spaceBetween: 30, // 슬라이드 사이 여백
        centeredSlides: true, // 1번 슬라이드가 가운데로 보여지기
        loop: true,
        autoplay: {
            delay: 5000
        },
        navigation: {
            prevEl: '.swiper-btn .swiper-prev',
            nextEl: '.swiper-btn .swiper-next',
        }
    });
```