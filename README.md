# Restaurant

url : https://www.youtube.com/watch?v=vIxGDq1SPZQ

### 시작하기
- npx create-next-app

### 기본
* logo(Navbar,Footer)가 every page에서 보이도록 pages/components/Navbar.js(x) & Footer.jsx & Layout.js 생성
* import Navbar from "./components/Navbar"; 
  + Footer도
  + 메인 폴더로 옮겨지면 import Navbar from "./Navbar"; 🚬🚬🚬🚬
* styles/Home.module.css all delete
* pages/components -> main(=pizzaordering)/components 
* _app.js의 component를 layout에 wrap, because out navbar and footer in every page
  + pages/about.js 생성 -> ``` <div>about page</div> ``` -> http://localhost:3000/about -> 모든 페이지에 navbar & footer 확인

### Navbar (21:40)
* Navbar의 css file 생성 (+ js에 import)
* Navbar에 전화 아이콘 , 전화번호 등 추가

### Slider(36:30)
#### 별다른 library 없이 슬라이더 만들기
* components/Featured.jsx 생성
* public/styles/Featured.module.css 생성
* index.js에 featured 불러오기
* 양 옆에 padding이 있어서 가장자리 빈 공간이 생김
  + styles/Home.module.css에서 ```container { padding : 0 2 rem}``` -> ```container { padding : 0 0 rem}```

### PizzaList(44:27)
* components/PizzaList.jsx 생성
* styles/PizzaList.module.css 생성
* components/PizzaCard.jsx 생성
* styles/PizzaCard.module.css 생성

### Footer
* styles/Footer.module.css 생성
* pages/Product/[id].jsx 생성
* styles/Product.module.css 생성

### Order Page - http://localhost:3000/Cart
* pages/Cart.jsx 생성
* styles/Cart.module.css 생성

### Paid Page - http://localhost:3000/orders/21 (01:29:27)
* pages/orders/[id].jsx 생성
* styles/Order.module.css 생성

### 휴대폰 화면크기 맞추기
## http://localhost:3000
* PizzaCard.module.css 
  - 피자 하나씩 나오게 (width:100%)
  - 피자 종류, 가격 폰트 사이즈 늘리기
* Footer.module.css
  - 가로 두 줄이였던 설명을 세로로 늘리기
  - 그만큼 검은 상자 auto로 늘리기 (+ 글자 가운데 정렬)
## http://localhost:3000/products/213
* Product.module.css
  - 전체 길이, 글지 늘리고 가운데 정렬
  - 
