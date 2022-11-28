# CSS Color

https://www.w3.org/TR/css-color  


**at-rule**
```css
/* @color-profile */
@color-profile --example {
    src:url('/css/style.css');
}

E {color:color(example 0 0 0);}
```


**property** 
- [color](#color)
- [opacity](#opacity)



## color 

- color keyword 
    - named color
- hex color 
- color functions
- system color (https://www.w3.org/TR/css-color/#typedef-system-color)



### color keyword  

```css
/*
transparent
= rgba(0,0,0,0) 
*/
E {color:transparent;}


/* 
currentcolor 
: 동일한 요소의 color 속성 값
*/
E {
    color:red;
    background-color:currentcolor;
}
```


**named color**  
https://www.w3.org/TR/css-color/#named-colors

```css
E {color:red;}
```



### hex color
: 16 진수 색상 표기법   
: 3, 4, 6, 8 자리 숫자로 색상 표현     


```css
E {color:#RRGGBB;}
E {color:#RGB;}

/* + alpha */
E {color:#RRGGBBCC;}
E {color:#RGBC;}
```



### color functions

```css
/* 
RGB 
- rgb(red green blue)
- rgba(red green blue alpha)

0 ~ 255  숫자 범위
0 ~ 100%  퍼센트 범위 

alpha 값을 생략하면 기본 값 100% 적용
*/
E {color:rgb(255 0 0 .5);color:rgb(100% 0% 0% .5);}
E {color:rgba(255 0 0 .5);}


/* 
HSL 
: 색상의 채도나 명도 변경 가능   

색상 = 0 ~ 359도 (0이면 빨강색, 120이면 초록색, 240이면 파란색)     
채도 = 0 ~ 100% (100%면 실제 색상, 0%면 회색)  
명도 = 0 ~ 100% (50%면 실제 색상, 0%면 검은색, 100%면 흰색)

- hsl(hue saturation lightness / alpha)
- hsla(hue saturation lightness alpha)
*/
E {color:hsl(0 100% 50% .5);}
E {color:hsla(0 100% 50% .5);}


/* HWB 
- hwb(hue whiteness blackness)
*/
E {color:hwb(0 0% 0%);}


/* 
- lab()
- lch()
- oklab()
- oklch()

lch
https://css.land/lch/
*/
E {color:lch();}


/* 
color() 

display-p3
https://webkit.org/blog/10042/wide-gamut-color-in-css-with-display-p3/
*/
E {color:color(display-p3 1 0 0);}
```



## opacity 
: 요소의 불투명도 지정   


```css
E {opacity:number | percentage;}
/*
number 
: 0 ~ 1 숫자 범위
: 모든 요소의 기본 값은 1
: 1보다 작은 opacity 값을 적용한 요소는 새로운 컨텍스트를 생성

! 해당 요소에만 투명도를 주려면 rgba() 사용 
background-color:rgba(red, green, blue, alpha);
*/
```


**+ stacking context**  
https://github.com/yoojj/doc.css/blob/main/css-context.md



[ [index](./README.md) | [top](#) ]