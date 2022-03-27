# Restaurant

url : https://www.youtube.com/watch?v=vIxGDq1SPZQ

### 시작하기
- npx create-next-app

### 기본
- logo(Navbar,Footer)가 every page에서 보이도록 pages/components/Navbar.js(x) & Footer.jsx & Layout.js 생성
- import Navbar from "./components/Navbar"; 
+ Footer도
+ 메인 폴더로 옮겨지면 import Navbar from "./Navbar"; 🚬🚬🚬🚬
- styles/Home.module.css all delete
- pages/components -> main(=pizzaordering)/components 
- _app.js의 component를 layout에 wrap, because out navbar and footer in every page
+ pages/about.js 생성 -> ``` <div>about page</div> ``` -> http://localhost:3000/about -> 모든 페이지에 navbar & footer 확인

### Navbar (21:40)
- Navbar의 css file 생성 (+ js에 import)
- Navbar에 전화 아이콘 , 전화번호 등 추가

### Slider
- components/Featured.jsx 생성
- public/styles/Featured.module.css 생성
- index.js에 featured 불러오기
- 양 옆에 padding이 있어서 가장자리 빈 공간이 생김
+ styles/Home.module.css에서 ```container { padding : 0 2 rem}``` -> ```container { padding : 0 0 rem}``` 
