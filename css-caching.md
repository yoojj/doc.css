# CSS Caching
: 브라우저에 CSS 파일이 로드되면 (비활성화하지 않은 경우) 이를 캐시에 저장하고 재사용  
: CSS가 변경되어도 브라우저는 변경 전 CSS를 사용하므로 CSS 파일을 새로 로드해야 함 (캐시 무효화)  


**+ Caching**   
: 캐시에 데이터를 저장하고 이를 사용하는 프로세스

https://github.com/yoojj/doc.cs/computer/cache.md 


## HTTP Cache
= Site Cache, Page Cache > Browser Cache  
: 클라이언트 측 캐싱  
: 리소스를 클라이언트에 캐싱  
: 리소스의 Last-Modified, etag 값을 사용해 유효성 검사를 함  


**캐시 유효 기간**  
```
Cache-Control: no-store | no-cache | max-age | private | public | must-revalidate

// http header 
Cache-Control: max-age=84600, public

// apache
Header set Cache-Control "max-age=84600, public"

// nginx
expires 365d;
add_header Cache-Control "public";
```

\+ 캐싱 테스트  
https://cache-tests.fyi/


**Browser Cache**    
: 클라이언트 측 캐싱 (개인 캐시)    
: 최종 사용자(유저)가 브라우저 설정을 통해 캐시 제어  

\+ 크롬 캐시 분할  
https://developer.chrome.com/blog/http-cache-partitioning/



## Server Cache  
: Proxy Cache, CDN Cache, Edge Cache ...  
: 서버 측 캐싱 (공유 캐시)  
: 리소스를 여러 서버에 캐싱함 (프록시 서버, CDN, 엣지 서버 등에서 캐싱 기능을 지원)  



# Cache Busting
: 캐시 무효화  


**파일명이나 파일 패스 변경**
```
/css/style1.css
/css/style2.css

/css/v1/style.css
/css/v2/style.css
```


**쿼리스트링 추가**  
! 일부 브라우저에서 작동하지 않음  

```
style.css?v=20221010
style.css?v=20221111
style.css?v=20221212
```


**파일명 변경 + webpack**
```js
plugins: [
    new MiniCssExtractPlugin({
        filename: '[name].[hash | chunkhash | contenthash].css',
    })
]
```



[ [index](./README.md) | [top](#) ]