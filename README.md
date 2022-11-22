# CSS
Cascading Style Sheets   
: 마크업 언어로 작성된 요소에 시각적 표현을 적용하기 위한 명령어 집합 (스타일 시트 언어)   
: 문서와 프레젠테이션을 분리하도록 설계   
: 처음 웹 문서는 텍스트 기반 구조만 제공해 사용자는 테이블 태그로 문서의 레이아웃을 제어했는데 이를 보완하기 위해 발전  
: 현재 CSS는 약 60여개의 모듈로 제공   
: CSS 스펙은 W3C CSSWG에서 관리   


- [CSSWG](#csswg)
    - WHATWG : CSS Book (https://books.idea.whatwg.org/)
- [CSS Level](#css-level)
- [CSS Module](./css.module/)
    - [CSS Syntax](./css.module/css-syntax.md)
- [CSS Context](./css-context.md)
- [CSS Load](./css-load.md)
    - [CSS Caching](./css-caching.md)
    - Critical CSS  
    - [Load CSS Async](./css-load-async.md)
- CSS Solutions
    - CSS Modules
    - [CSS in JS](./css-in-js.md)
    - Constructable Stylesheets
    - [CSS Module Scripts](./css-module-scripts.md)
- CSS Tools
    - [CSS Methodologies](./css-methodologies.md)
    - [CSS Preprocessor](./css-preprocessor.md)
    - [CSS Framework](./css-framework.md)
- [CSS Performance Optimization](./css-optimization.md)
- [CSS GPU Accelerated](./css-gpu.md)


```html
<!-- HTML1 -->
<h1><font size="5">제목</font></h1>

<!--
Håkon Wium Lie 초기 제안 (1994)
Cascading HTML Style Sheets -> Cascading Style Sheets

텍스트와 스타일 분리  
Cascading 도입
-->
h1.font.size = 24pt 100%
h2.font.size = 20pt 40%

<!-- IE3 CSS1 최초 구현 (1996) -->
h1 {font-size:24px;}
```


**+ CSS 영향**   
RRP, PWP, FOSI, DSSSL, PSL, CHSS, JSSS   
https://eager.io/blog/the-languages-which-almost-were-css/


**+ 마크업 언어**



## CSSWG
CSS Working Group  
: CSS 규격-명세-스펙 정의    
: 여러 단계의 프로세스를 걸쳐 표준화 진행   


**스펙**  
https://drafts.csswg.org/


**프로세스**  
https://www.w3.org/2021/Process-20211102/#rec-track



## CSS Level
: CSS는 버전이 존재하지 않고 레벨이 존재  
: CSS2 이후 빠른 표준화 진행과 브라우저 지원을 위해 CSS 사양을 모듈화하여 개별 정의  
: CSS3은 모듈화된 CSS를 지칭하고 모듈은 각각 업데이트되므로 CSS4 레벨은 존재하지 않음   
: 현재는 레벨이 없으며 CSS2와 구분을 위해 CSS3이라는 용어 사용  


레벨 | 특징 | 스펙
---|---|---
css1   | 초기 사양으로 현재 폐기 | https://www.w3.org/TR/CSS1/
css2.x | monolithic | https://www.w3.org/TR/CSS2/
css3   | component, module | https://www.w3.org/TR/CSS/



[top](#)
