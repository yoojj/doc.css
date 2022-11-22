# CSS Load


```
HTML 로드  -->  HTML 구문 분석  -------------->  DOM
                             CSS 로드 -->  구문 분석  -->  CSSOM


1. HTML 로드
2. HTML 구문 분석을 하면서 CSS 파일을 연결한 link 태그를 분리하고 이후 CSS 파일 로드
3. CSS는 두 단계를 통해 구문 분석
    1. CSS 파일을 위에서 아래로 스캔하며 CSS 충돌 해결 <-- Cascading
    2. 요소에 적용할 최종 값을 만듬 (상대 값은 절대 값으로 변환)
4. 구문 분석이 완료되면 CSSOM 생성
5. 이하 생략  
```


**종류**
- [Author CSS](#author-css)
- [User defined CSS](#user-defined-css)
- [Browser default CSS](#browser-default-css)



## Author CSS
: 작성자-개발자가 정의한 스타일 시트    


**Inline CSS**  
: 요소에 직접 스타일 속성 지정  
: 웹 문서에 포함되므로 우선 순위가 높음  
: 인라인 스타일 지정시 가상 클래스와 가상 엘리먼트 사용 불가   

```html
<div style=""></div>
```


**Internal(Embedded) CSS**  
```html
<style>
div {}
</style>

<div></div>
```


**External CSS**  
: link 태그를 사용해 웹 문서에 CSS 파일 연결  

```html
<head>
<link rel="stylesheet" href="style.css">
<link rel="stylesheet" href="base.css" media="all">
<link rel="stylesheet" href="small.css" media="(min-width:50em)">
<link rel="stylesheet" href="medium.css" media="(min-width:100em)">
<link rel="stylesheet" href="large.css" media="(min-width:150em)">
</head>
```



## User defined CSS
: 브라우저 기본 스타일을 유저가 수정하거나 정의한 CSS 파일을 브라우저의 기본 스타일로 등록  


**Firefox**
1. 주소창 about:config 입력
2. 검색창에 toolkit.legacyUserProfileCustomizations.stylesheets 검색하고 활성화

**Chrome**  
: stylish 확장 프로그램 설치



## Browser default CSS
= User-agent default CSS  
: 브라우저에서 미리 정의한 기본 스타일    
: 웹 문서에 작성한 CSS가 없는 경우에도 콘텐츠는 렌더링되어야 하므로 기본 스타일 존재   
: 브라우저마다 기본 스타일이 다르므로 사용자/작성자는 이를 재설정 함  


**ie 7,8,9**   
http://web.archive.org/web/20170122223926/http://www.iecss.com/


**Chrome (Blink)**    
https://cs.chromium.org/chromium/src/third_party/blink/renderer/core/html/resources/html.css  
https://chromium.googlesource.com/chromium/blink/+/master/Source/core/css/html.css


**Chrome/Safari (WebKit)**  
http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css


**Firefox**    
https://dxr.mozilla.org/mozilla-central/source/layout/style/res/html.css



[ [index](./README.md) | [top](#) ]
