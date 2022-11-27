# CSS Load Asynchronously
: CSS 파일을 로드하고 구문을 해석하는 동안 웹 문서의 렌더링이 중단되어 일시적으로 지연되는데(렌더링 차단 리소스)), 웹 문서의 렌더링이 지연되지 않도록 중요하지 않은 CSS 파일을 비동기식으로 로드함   


**rel 속성 사용**

1. rel 속성을 사용해 CSS 파일 다운로드
2. CSS 파일 다운로드 후 rel 속성 수정  

```html
<link rel="preload" href="example.css" as="style" onload="this.rel='stylesheet'">
```


**media 속성 사용**

1. media 속성을 사용해 CSS 파일 다운로드
2. CSS 파일 다운로드 후 media 속성을 유효한 값으로 수정  

```html
<link rel="stylesheet" href="example.css" media="none" onload="if(media!='all') media='all'">
```



[top](#)
