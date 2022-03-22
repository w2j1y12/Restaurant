# Restaurant

url : https://www.youtube.com/watch?v=vIxGDq1SPZQ

##3월 22일

### 시작하기
- npx create-next-app

### 기본
1) logo(Navbar,Footer)가 every page에서 보이도록 pages/components/Navbar.js(x) & Footer.jsx & Layout.js 생성
2) import Navbar from "./components/Navbar"; 
+ Footer도
+ 메인 폴더로 옮겨지면 import Navbar from "./Navbar"; 🚬🚬🚬🚬
3) styles/Home.module.css all delete
4) pages/components -> main(=pizzaordering)/components 
5) _app.js의 component를 layout에 wrap, because out navbar and footer in every page
+ pages/about.js 생성 -> ``` <div>about page</div> ``` -> http://localhost:3000/about -> 모든 페이지에 navbar & footer 확인
6) Navbar의 css file 생성 (+ js에 import)
7) Navbar에 전화 아이콘 , 전화번호 등 추가
