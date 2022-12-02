# CSS Media Query

https://www.w3.org/TR/mediaqueries/


```html 
<!-- HTML4 에서 다양항 장치에 스타일 시트를 지원하기 위해 media 속성 정의 -->
<link rel="stylesheet" href="style.css" media="all | print | screen">


<!-- CSS는 @media나 @import로 정의 -->
<style>
@media print {}
@media screen {}

@import "styles.css" print;
@import "styles.css" screen;
</style>   
```



## media condition

> @media modifier type (feature) {}



### 1. media query modifier
: 키워드 앞/뒤로 공백 필요

- not 
- and
- or



### 2. media type

- all : 타입을 지정하지 않은 경우 기본 값으로 생략되어 있음
- print
- screen : print를 제외한 모든 장치 화면 



### 3. media feature
: 기능이 참인 경우 CSS 적용     

>(feature name : value)  
(feature name range value)  
(range-feature name : value)  
(feature name : value) modifier (feature name : value)  


**feature name**
```css
/* 
뷰포트 너비와 높이
: 스크롤바의 크기를 포함해 계산  
: 값에 단위를 사용 할 수 있음 (ex. px, cm, em...)
*/
@media (width : value) {}
@media (min-width < value) {}
@media (max-width > value) {}
@media (value <= width <= value) {}

@media (height : value) {}
@media (min-height < value) {}
@media (max-height > value) {}

@media (device-width : value) {}
@media (device-height : value) {}


/* 너비와 높이의 비율 */
@media (aspect-ratio : value) {}


/*
디스플레이 가로/세로 모드 

- portrait : 세로 모드 (뷰포트 높이 > 뷰포트 너비)
- landscape : 가로 모드 (뷰포트 너비 > 뷰포트 높이)
*/
@media (orientation : portrait | landscape) {}


/* 디스플레이 해상도 */
@media (resolution : value) {}
@media (min-resolution < value) {}  
@media (max-resolution > value) {}    


/* 디스플레이 타입 */
@media (scan : interlace | progressive) {}    


/* 콘솔 디스플레이 감지 */
@media (grid) {}


/* 디스플레이 업데이트 빈도 */
@media (update : none | slow | slow) {}  


@media (overflow-block : none | scroll | paged) {}    
@media (overflow-inline : none | scroll) {}   


/* 컬러 미디어 */
@media (color) {}
@media (color : integer) {}
@media (color-index) {}
@media (color-index : integer) {}

@media (monochrome) {}
@media (monochrome : integer) {}
@media (monochrome >= integer) {}


/* 
컬러 디스플레이 
: 유저 에이전트의 대략 적인 색상 범위 

rec2020 > p3 > sRGB
*/
@media (color-gamut : srgb | p3 | rec2020) {}


/* 
인터랙션 미디어 

https://googlechrome.github.io/samples/media-hover-pointer/
*/
@media (pointer : none | coarse | fine) {}
@media (hover : none | hover) {}

@media (any-pointer : none | coarse | fine) {}
@media (any-hover : none | hover) {}


/* deprecated */
@media (device-width : value) {}
@media (device-height : value) {}

@media (device-aspect-ratio : value/value) {}
```



[ [index](./README.md) | [top](#) ]