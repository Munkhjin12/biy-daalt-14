# А хэсэг — API Setup

## Сонгосон API: JSONPlaceholder

### Товч тайлбар
JSONPlaceholder нь хөгжүүлэгчдэд зориулсан үнэгүй, нээлттэй REST API юм.
Prototype болон тест хийхэд зориулагдсан хуурамч (fake) өгөгдөл буцаадаг.
CRUD үйлдэл бүгд дэмжигддэг ч өгөгдөл бодитоор хадгалагддаггүй.

### Base URL
```
https://jsonplaceholder.typicode.com
```

### Authentication
Шаардлагагүй. API key, token байхгүй.

### Үндсэн Endpoint-ууд
| Endpoint                | Тайлбар                          |
|-------------------------|----------------------------------|
| GET /posts              | Бүх нийтлэл авах (100 ширхэг)    |
| GET /posts/:id          | Тодорхой нийтлэл авах            |
| POST /posts             | Шинэ нийтлэл үүсгэх              |
| PUT /posts/:id          | Нийтлэл бүрэн шинэчлэх           |
| DELETE /posts/:id       | Нийтлэл устгах                   |
| GET /users/:id          | Тодорхой хэрэглэгч авах          |
| GET /posts/:id/comments | Нийтлэлийн сэтгэгдэл авах        |

### Rate Limit
Тодорхой хязгааргүй.

### Workspace
- **Workspace нэр:** `F.CSM311 — Lab14`
- **Collection нэр:** `<Овог> — JSONPlaceholder`
- **Environment:** `dev` → `baseUrl = https://jsonplaceholder.typicode.com`

### Тэмдэглэл
- Response нь үргэлж JSON формат буцаадаг
- POST/PUT/DELETE нь бодитоор өгөгдөл өөрчилдөггүй — хариу нь симуляц
- Auth шаардлагагүй тул Authorization header хэрэггүй
