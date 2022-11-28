# OS-API-Project

## There is 6 different API endpoints:

> ## `https://corner-mall.vercel.app/api/auth/signup`

**Description:**

This endpoint is used to register new users.

**Request:**

```http
POST /api/auth/signup HTTP/2
Host: corner-mall.vercel.app
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept: application/json, text/plain, */*
Content-Type: application/json
Content-Length: 68

{"name":"Mohamed","email":"mohamed@gmail.com","password":"12345678"}
```

**Response:**

```http
HTTP/2 201 Created
Content-Type: application/json; charset=utf-8
Date: Thu, 24 Nov 2022 19:53:34 GMT
Content-Length: 87

{"message":"User is created successfully","name":"Mohamed","email":"mohamed@gmail.com"}
```

> ## `https://corner-mall.vercel.app/api/auth/update`

**Description:**

This endpoint is used to update user profile.

**Request:**

```http
PUT /api/auth/update HTTP/2
Host: corner-mall.vercel.app
Cookie: __Host-next-auth.csrf-token=b813624e1cd219cdc2bef44ab585a57091f448d967e425fb9ef8fd110ee9c21f%7Cfd60862ea8c0556081986601511433ca7fe4ccba76985f8bd941318dd00b0ed9; __Secure-next-auth.callback-url=https%3A%2F%2Fcorner-mall.vercel.app%2Flogin; __Secure-next-auth.session-token=eyJhbGciOiJkaXIiLCJlbmMiOiJBMjU2R0NNIn0..fslH2EbX5D8wBhl0.pXbrAj0xkcAGJWYHD9eYOX4Fio1jHEbIE574VD1M-1BNUIvbAN_a9ubk9lXr0kbDe_vh-NQuLSVDbb1hpOhmlpQ4DMsFzwgYwHJEGoEnPzvF3qOqFuq_GQlEbYyuKL8aw6wv_lBbP0HpyMfuXOUA8ijNXGy7sQGtTc8faogx-ueVPB-2l1RlSFsa0UdNYvVJ0LVNCSiQsjJjX-NI2A-be0MJdGuwXV-2XMIB-A.SneFNrZLq3DQDQEfVOZOZg
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept: application/json, text/plain, */*
Content-Type: application/json
Content-Length: 69

{"name":"Mohamed","email":"mohamed2@gmail.com","password":"12345678"}
```

**Response:**

```http
HTTP/2 200 OK
Content-Type: application/json; charset=utf-8
Date: Thu, 24 Nov 2022 20:01:02 GMT
Content-Length: 42

{"message":"User is updated successfully"}
```

> ## `https://corner-mall.vercel.app/api/orders`

**Description:**

This endpoint is used to create an order.

**Request:**

```http
POST /api/orders HTTP/2
Host: corner-mall.vercel.app
Cookie: __Host-next-auth.csrf-token=b813624e1cd219cdc2bef44ab585a57091f448d967e425fb9ef8fd110ee9c21f%7Cfd60862ea8c0556081986601511433ca7fe4ccba76985f8bd941318dd00b0ed9; __Secure-next-auth.callback-url=https%3A%2F%2Fcorner-mall.vercel.app%2Fprofile; __Secure-next-auth.session-token=eyJhbGciOiJkaXIiLCJlbmMiOiJBMjU2R0NNIn0..S9jH9yHQg_6OKOeT.1-WlD6HO0nk6PTvTMpZIrs4_lTldJkJJgcq-h3P9ktIjOfHkYB6_e4rCIhwr-L4OG4KZBfDGntiHdSdgMTtW-npeigo5e7VnFJDQCGOv3hhOJSm4fpn50c-Q8OC-kdnMHlKj3bhsPIrXUYJSvewdA6otBa-UwCx1M8FzX6VfJoBm_UDgmh9Jl7dNOXO7M6ph3Ia3Q9FePQ8lmP_4lBk5xRJ7el_4jtM6U8qEzYQ.o6Koie26bVS6IzntFvPUOg; cart={%22cartItems%22:[{%22_id%22:%22637a451e248c68c59b054d54%22%2C%22name%22:%22Geo%20Print%20Polo%20Shirt%22%2C%22slug%22:%22polo-shirt%22%2C%22category%22:%22clothes%22%2C%22image%22:%22/images/clothes/tshirt-4.jpg%22%2C%22price%22:23%2C%22brand%22:%22Oliver%22%2C%22rating%22:4.8%2C%22numReviews%22:7%2C%22countInStock%22:10%2C%22description%22:%22A%20popular%20t-shirt%22%2C%22__v%22:0%2C%22createdAt%22:%22Sun%20Nov%2020%202022%2015:17:50%20GMT+0000%20(Coordinated%20Universal%20Time)%22%2C%22updatedAt%22:%22Sun%20Nov%2020%202022%2015:17:50%20GMT+0000%20(Coordinated%20Universal%20Time)%22%2C%22quantity%22:1}]%2C%22shippingAddress%22:{%22fullName%22:%22Mohamed%22%2C%22address%22:%226B%22%2C%22country%22:%22Egypt%22%2C%22city%22:%22Giza%22%2C%22postalCode%22:%2212345%22%2C%22mobileNumber%22:%220123456789%22}%2C%22paymentMethod%22:%22PayPal%22}
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept: application/json, text/plain, */*
Content-Type: application/json
Content-Length: 676

{"orderItems":[{"_id":"637a451e248c68c59b054d54","name":"Geo Print Polo Shirt","slug":"polo-shirt","category":"clothes","image":"/images/clothes/tshirt-4.jpg","price":23,"brand":"Oliver","rating":4.8,"numReviews":7,"countInStock":10,"description":"A popular t-shirt","__v":0,"createdAt":"Sun Nov 20 2022 15:17:50 GMT+0000 (Coordinated Universal Time)","updatedAt":"Sun Nov 20 2022 15:17:50 GMT+0000 (Coordinated Universal Time)","quantity":1}],"shippingAddress":{"fullName":"Mohamed","address":"6B","country":"Egypt","city":"Giza","postalCode":"12345","mobileNumber":"0123456789"},"paymentMethod":"PayPal","itemsPrice":23,"shippingPrice":20,"taxPrice":3.22,"totalPrice":46.22}
```

**Response:**

```http
HTTP/2 201 Created
Content-Type: application/json; charset=utf-8
Date: Thu, 24 Nov 2022 20:04:02 GMT
Content-Length: 564

{"user":"637fcbbe9fe3f0689c51e05e","orderItems":[{"name":"Geo Print Polo Shirt","quantity":1,"image":"/images/clothes/tshirt-4.jpg","price":23,"_id":"637a451e248c68c59b054d54"}],"shippingAddress":{"fullName":"Mohamed","address":"6B","country":"Egypt","city":"Giza","postalCode":"12345","mobileNumber":"0123456789"},"paymentMethod":"PayPal","itemsPrice":23,"shippingPrice":20,"taxPrice":3.22,"totalPrice":46.22,"isPaid":false,"isDelivered":false,"_id":"637fce329fe3f0689c51e073","createdAt":"2022-11-24T20:04:02.278Z","updatedAt":"2022-11-24T20:04:02.278Z","__v":0}
```

> ## `https://corner-mall.vercel.app/api/orders/[id]`

**Description:**

This endpoint is used to display details about specific order.

**Request:**

```http
GET /api/orders/637fce329fe3f0689c51e073 HTTP/2
Host: corner-mall.vercel.app
Cookie: __Host-next-auth.csrf-token=b813624e1cd219cdc2bef44ab585a57091f448d967e425fb9ef8fd110ee9c21f%7Cfd60862ea8c0556081986601511433ca7fe4ccba76985f8bd941318dd00b0ed9; __Secure-next-auth.callback-url=https%3A%2F%2Fcorner-mall.vercel.app%2Fprofile; __Secure-next-auth.session-token=eyJhbGciOiJkaXIiLCJlbmMiOiJBMjU2R0NNIn0..S9jH9yHQg_6OKOeT.1-WlD6HO0nk6PTvTMpZIrs4_lTldJkJJgcq-h3P9ktIjOfHkYB6_e4rCIhwr-L4OG4KZBfDGntiHdSdgMTtW-npeigo5e7VnFJDQCGOv3hhOJSm4fpn50c-Q8OC-kdnMHlKj3bhsPIrXUYJSvewdA6otBa-UwCx1M8FzX6VfJoBm_UDgmh9Jl7dNOXO7M6ph3Ia3Q9FePQ8lmP_4lBk5xRJ7el_4jtM6U8qEzYQ.o6Koie26bVS6IzntFvPUOg; cart={%22cartItems%22:[]%2C%22shippingAddress%22:{%22fullName%22:%22Mohamed%22%2C%22address%22:%226B%22%2C%22country%22:%22Egypt%22%2C%22city%22:%22Giza%22%2C%22postalCode%22:%2212345%22%2C%22mobileNumber%22:%220123456789%22}%2C%22paymentMethod%22:%22PayPal%22}
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept: application/json, text/plain, */*
```

**Response:**

```http
HTTP/2 200 OK
Content-Type: application/json; charset=utf-8
Date: Thu, 24 Nov 2022 20:11:52 GMT
Content-Length: 564

{"shippingAddress":{"fullName":"Mohamed","address":"6B","country":"Egypt","city":"Giza","postalCode":"12345","mobileNumber":"0123456789"},"_id":"637fce329fe3f0689c51e073","user":"637fcbbe9fe3f0689c51e05e","orderItems":[{"name":"Geo Print Polo Shirt","quantity":1,"image":"/images/clothes/tshirt-4.jpg","price":23,"_id":"637a451e248c68c59b054d54"}],"paymentMethod":"PayPal","itemsPrice":23,"shippingPrice":20,"taxPrice":3.22,"totalPrice":46.22,"isPaid":false,"isDelivered":false,"createdAt":"2022-11-24T20:04:02.278Z","updatedAt":"2022-11-24T20:04:02.278Z","__v":0}
```

> ## `https://corner-mall.vercel.app/api/orders/history`

**Description:**

This endpoint is used to show all previous order to the user.

**Request:**

```http
GET /api/orders/history HTTP/2
Host: corner-mall.vercel.app
Cookie: __Host-next-auth.csrf-token=b813624e1cd219cdc2bef44ab585a57091f448d967e425fb9ef8fd110ee9c21f%7Cfd60862ea8c0556081986601511433ca7fe4ccba76985f8bd941318dd00b0ed9; __Secure-next-auth.callback-url=https%3A%2F%2Fcorner-mall.vercel.app%2Fprofile; __Secure-next-auth.session-token=eyJhbGciOiJkaXIiLCJlbmMiOiJBMjU2R0NNIn0..S9jH9yHQg_6OKOeT.1-WlD6HO0nk6PTvTMpZIrs4_lTldJkJJgcq-h3P9ktIjOfHkYB6_e4rCIhwr-L4OG4KZBfDGntiHdSdgMTtW-npeigo5e7VnFJDQCGOv3hhOJSm4fpn50c-Q8OC-kdnMHlKj3bhsPIrXUYJSvewdA6otBa-UwCx1M8FzX6VfJoBm_UDgmh9Jl7dNOXO7M6ph3Ia3Q9FePQ8lmP_4lBk5xRJ7el_4jtM6U8qEzYQ.o6Koie26bVS6IzntFvPUOg; cart={%22cartItems%22:[]%2C%22shippingAddress%22:{%22fullName%22:%22Mohamed%22%2C%22address%22:%226B%22%2C%22country%22:%22Egypt%22%2C%22city%22:%22Giza%22%2C%22postalCode%22:%2212345%22%2C%22mobileNumber%22:%220123456789%22}%2C%22paymentMethod%22:%22PayPal%22}
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept: application/json, text/plain, */*
```

**Response:**

```http
HTTP/2 200 OK
Content-Type: application/json; charset=utf-8
Date: Thu, 24 Nov 2022 20:19:24 GMT
Content-Length: 566

[{"shippingAddress":{"fullName":"Mohamed","address":"6B","country":"Egypt","city":"Giza","postalCode":"12345","mobileNumber":"0123456789"},"_id":"637fce329fe3f0689c51e073","user":"637fcbbe9fe3f0689c51e05e","orderItems":[{"name":"Geo Print Polo Shirt","quantity":1,"image":"/images/clothes/tshirt-4.jpg","price":23,"_id":"637a451e248c68c59b054d54"}],"paymentMethod":"PayPal","itemsPrice":23,"shippingPrice":20,"taxPrice":3.22,"totalPrice":46.22,"isPaid":false,"isDelivered":false,"createdAt":"2022-11-24T20:04:02.278Z","updatedAt":"2022-11-24T20:04:02.278Z","__v":0}]
```

> ## `https://corner-mall.vercel.app/api/products/[id]`

**Description:**

This endpoint is used to send the details about specific product by its ID.

**Request:**

```http
GET /api/products/637a451e248c68c59b054d51 HTTP/2
Host: corner-mall.vercel.app
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept: application/json, text/plain, */*
```

**Response:**

```http
HTTP/2 200 OK
Content-Type: application/json; charset=utf-8
Date: Thu, 24 Nov 2022 20:26:12 GMT
Content-Length: 338

{"_id":"637a451e248c68c59b054d51","name":"Soft Graphic T-Shirt","slug":"soft-tshirt","category":"clothes","image":"/images/clothes/tshirt-1.jpg","price":35,"brand":"Nike","rating":4.5,"numReviews":14,"countInStock":10,"description":"A popular t-shirt","__v":0,"createdAt":"2022-11-20T15:17:50.602Z","updatedAt":"2022-11-20T15:17:50.602Z"}
```
