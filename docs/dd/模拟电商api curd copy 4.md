下面是根据你提供的 FastAPI 接口的所有 `curl` 命令示例：

### 1. **登录接口**
```bash
curl -X 'POST' \
  'http://localhost:8000/login' \
  -H 'Content-Type: application/json' \
  -d '{
  "username": "zhangsan",
  "password": "123456"
}'
```

### 2. **创建商品接口**
```bash
curl -X 'POST' \
  'http://localhost:8000/api/v1/products' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <your_token>' \
  -d '{
  "name": "New Product",
  "price": 199.99
}'
```

### 3. **查询所有商品接口**
```bash
curl -X 'GET' \
  'http://localhost:8000/api/v1/products' \
  -H 'Authorization: Bearer <your_token>'
```

### 4. **查询单个商品接口**
```bash
curl -X 'GET' \
  'http://localhost:8000/api/v1/products/101' \
  -H 'Authorization: Bearer <your_token>'
```

### 5. **更新商品接口**
```bash
curl -X 'PUT' \
  'http://localhost:8000/api/v1/products/101' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <your_token>' \
  -d '{
  "name": "Updated Product",
  "price": 149.99
}'
```

### 6. **删除商品接口**
```bash
curl -X 'DELETE' \
  'http://localhost:8000/api/v1/products/101' \
  -H 'Authorization: Bearer <your_token>'
```

### 7. **添加购物车项接口**
```bash
curl -X 'POST' \
  'http://localhost:8000/api/v1/cart' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <your_token>' \
  -d '{
  "product_id": "101",
  "quantity": 2
}'
```

### 8. **查询购物车接口**
```bash
curl -X 'GET' \
  'http://localhost:8000/api/v1/cart' \
  -H 'Authorization: Bearer <your_token>'
```

### 9. **更新购物车项接口**
```bash
curl -X 'PUT' \
  'http://localhost:8000/api/v1/cart/1' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <your_token>' \
  -d '{
  "product_id": "101",
  "quantity": 3
}'
```

### 10. **删除购物车项接口**
```bash
curl -X 'DELETE' \
  'http://localhost:8000/api/v1/cart/1' \
  -H 'Authorization: Bearer <your_token>'
```

### 11. **创建订单接口**
```bash
curl -X 'POST' \
  'http://localhost:8000/api/v1/orders' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <your_token>' \
  -d '{
  "cart_id": "1"
}'
```

### 12. **查询所有订单接口**
```bash
curl -X 'GET' \
  'http://localhost:8000/api/v1/orders' \
  -H 'Authorization: Bearer <your_token>'
```

### 13. **查询单个订单接口**
```bash
curl -X 'GET' \
  'http://localhost:8000/api/v1/orders/1' \
  -H 'Authorization: Bearer <your_token>'
```

### 14. **更新订单接口**
```bash
curl -X 'PUT' \
  'http://localhost:8000/api/v1/orders/1' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer <your_token>' \
  -d '{
  "cart_id": "1",
  "quantity": 3
}'
```

### 15. **删除订单接口**
```bash
curl -X 'DELETE' \
  'http://localhost:8000/api/v1/orders/1' \
  -H 'Authorization: Bearer <your_token>'
```

在这些命令中，`<your_token>` 是需要替换成实际从登录接口获取的 `token`。
