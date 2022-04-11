# Restaurant

Next.js를 이용한 피자 주문 사이트 제작

URL : https://www.youtube.com/watch?v=vIxGDq1SPZQ

### 메인 페이지
##### Navbar / Silde / PizzaList / Footer
##### Slide
``` 
const [index, setIndex] = useState(0);
  const images = [
    "/img/featured.png",
    "/img/featured2.png",
    "/img/featured3.png",
  ];

  const handleArrow = (direction) => {
    if (direction === "l") {
      setIndex(index !== 0 ? index - 1 : 2);
    }
    if (direction === "r") {
      setIndex(index !== 2 ? index + 1 : 0);
    }
  };
  ```
![image](https://user-images.githubusercontent.com/62472117/162374352-694ecf37-f93b-43bb-8c6c-7a9704ee6362.png)
### 주문 페이지
##### Navbar / Pizza's Specifics / Footer 
##### Pizza's Specifics
```
 const [size, setSize] = useState(0);
  const pizza = {
    id: 1,
    img: "/img/pizza.png",
    name: "CAMPAGNOLA",
    price: [19.9, 23.9, 27.9],
    desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis arcu purus. rhoncus frigilla vestibulum vel, dignissim vel ante. Nulla facilsi. Nullam a urna sit amet tellus pellentesque egestas in in ante.",
  };
```
![image](https://user-images.githubusercontent.com/62472117/162375283-6610ef2e-7649-4601-b3e5-16cfa29da8d6.png)
### 장바구니 페이지
##### Navbar / Selected Pizza List / Cart Total / Footer
![image](https://user-images.githubusercontent.com/62472117/162375414-22c13b62-1f52-4c6c-8379-09368cf9b5e9.png)
### 주문현황 페이지
##### Navbar / Customer Info / Order Progress / Footer
##### Order Progress - animation
```
const status = 0;

  const statusClass = (index) => {
    if (index - status < 1) return styles.done;
    if (index - status === 1) return styles.inProgress;
    if (index - status > 1) return styles.undone;
  };
  ```
![image](https://user-images.githubusercontent.com/62472117/162375493-29687544-6194-4a78-b37b-e1b2229c0446.png)

# MongoDB
- .env 파일 생성 후, connect code 입력
- ```yarn add mongoose```
- util/mongo.js 생성 후, 아래 코드 입력
(https://github.com/vercel/next.js/blob/canary/examples/with-mongodb-mongoose/lib/dbConnect.js)

``` import mongoose from 'mongoose'

const MONGODB_URL = process.env.MONGODB_URL

if (!MONGODB_URI) {
  throw new Error(
    'Please define the MONGODB_URL environment variable inside .env.local'
  )
}

/**
 * Global is used here to maintain a cached connection across hot reloads
 * in development. This prevents connections growing exponentially
 * during API Route usage.
 */
let cached = global.mongoose

if (!cached) {
  cached = global.mongoose = { conn: null, promise: null }
}

async function dbConnect() {
  if (cached.conn) {
    return cached.conn
  }

  if (!cached.promise) {
    const opts = {
      bufferCommands: false,
    }

    cached.promise = mongoose.connect(MONGODB_URL, opts).then((mongoose) => {
      return mongoose
    })
  }
  cached.conn = await cached.promise
  return cached.conn
}

export default dbConnect
```
- models/Product.js ``` import mongoose from "mongoose"```
