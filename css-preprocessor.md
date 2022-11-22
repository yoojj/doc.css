# CSS Preprocessor
: CSS 전처리기   
: CSS는 선언적 언어로 재사용이나 추상화가 어려운데 이를 보완하기 위해 생김   
: CSS 전처리기를 통해 코드를 재사용, 단순화, 추상화 함 (변수, 함수, 믹스인, 중첩 등)    
: 전처리기 문법을 사용해 생성한 파일은 컴파일러나 트랜스파일러를 통해 CSS 파일로 변환함      


**종류**   
- [SASS](#sass)
- [LESS](#less)
- Stylus
- ...


**도구**  
- [PostCSS](#postcss)


**CSS 전처리기 변수 vs CSS 변수**  
```css
/* CSS 전처리기 변수 */
$some-color:red;

div {background-color:$some-color;}


/* CSS 변수 */
:root {
    --some-color:red;
}

div {background-color:var(--some-color);}
```



## SASS
: ruby와 node 기반 컴파일러 지원   
: Sass와 SCSS 두 가지 문법 제공         


```bash
# ruby + sass
gem install sass
sass -v


# node + sass
npm install node-sass
node-sass -v
```



## LESS
: 변수, 함수, 연산, 중첩, 스코프 등 스크립트 언어 특징 지원    


```bash
npm install less

# less to css
lessc style.less style.css
```



## PostCSS
: node 기반 플러그인이나 전처리기처럼 사용 가능  
: 필요한 기능에 맞는 플러그인을 선택해 사용  


**플러그인 목록**  
https://github.com/postcss/postcss/blob/master/docs/plugins.md


```bash
npm install postcss postcss-cli

# autoprefixer 사용
postcss --use autoprefixer -o style.css ./css/*.css


# postcss + gulp + autoprefixer
npm install gulp-postcss autoprefixer

## postcss.config.js
var gulp = require('gulp');
var postcss = require('gulp-postcss');
var autoprefixer = require('autoprefixer');

gulp.task('css', () => {
    const plugins = [
        autoprefixer({browsers: ['last 1 version']}),
    ]
    return gulp.src('./css/*.css')
        .pipe(postcss(plugins))
        .pipe(gulp.dest('생성'));
});


# postcss + webpack + autoprefixer
$ npm install postcss postcss-loader autoprefixer   

## postcss.config.js
module.exports = {
    plugins: [
        require('autoprefixer')({
            'browsers': ['last 1 versions']
        })
    ]
}
```



[ [index](./README.md) | [top](#) ]
