# Restaurant

URL : https://www.youtube.com/watch?v=vIxGDq1SPZQ

### 메인 페이지
![screencapture-localhost-3000-2022-04-08-15_01_18](https://user-images.githubusercontent.com/62472117/162374352-694ecf37-f93b-43bb-8c6c-7a9704ee6362.png){:width="25%" height="75%"}
![screencapture-localhost-3000-Product-213-2022-04-08-15_11_19](https://user-images.githubusercontent.com/62472117/162375283-6610ef2e-7649-4601-b3e5-16cfa29da8d6.png)){:width="25%"}
![screencapture-localhost-3000-Cart-2022-04-08-15_12_51](https://user-images.githubusercontent.com/62472117/162375414-22c13b62-1f52-4c6c-8379-09368cf9b5e9.png)){:width="25%"}
![screencapture-localhost-3000-orders-21-2022-04-08-15_13_40](https://user-images.githubusercontent.com/62472117/162375493-29687544-6194-4a78-b37b-e1b2229c0446.png)){:width="25%"}

### 주문 페이지
- Navbar : 
- Slide :
- PizzaList : 
- Footer :

# MongoDB
- .env 파일 생성 후, connecte code 입력
- yarn add mongoose
- util/mongo.js 생성 후, 아래 코드 입력

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
