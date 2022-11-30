# CSS Module Scripts
: JS import 구문을 사용해 CSS 파일을 로드


**+ import assertions**  
: import 문에 모듈 타입을 지정하는 구문 추가

https://v8.dev/features/import-assertions   



**ex. js**
```js
import style from "/css/styles.css" assert { type: "css" };

document.adoptedStyleSheets = [style];
shadowRoot.adoptedStyleSheets = [style];


// dynamic import
const style = await import('/css/style.css', { assert: { type: 'css' } });

document.adoptedStyleSheets = [style.default];
shadowRoot.adoptedStyleSheets = [style.default];
```


**ex. html**
```html
<script type="module">
import style from "/css/styles.css" assert { type: "css" };
</script>
```



[ [index](./README.md) | [top](#) ]
