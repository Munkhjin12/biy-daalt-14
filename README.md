# Бие даалт 14 — API Testing: Postman + Newman

## API
JSONPlaceholder — https://jsonplaceholder.typicode.com

## Шаардлага
- Node.js 18+
- Newman: `npm install -g newman newman-reporter-htmlextra`

## Local-д ажиллуулах

### 1. Repo clone хийх
```bash
git clone https://github.com/<username>/bie-daalt-14.git
cd bie-daalt-14
```

### 2. Newman тест ажиллуулах
```bash
newman run postman/collection.json -e postman/env.dev.json
```

### 3. HTML report үүсгэх
```bash
newman run postman/collection.json \
  -e postman/env.dev.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export reports/api.html
```
Дараа нь `reports/api.html` файлыг browser-т нээж харна.

## CI/CD
GitHub Actions автоматаар push болгонд тест ажиллуулдаг.
Actions tab → "API tests" workflow-оос харна.

## Бүтэц
```
bie-daalt-14/
├── .github/
│   └── workflows/
│       └── api-tests.yml
├── partA/
│   ├── SETUP.md
│   └── screenshot.png
├── postman/
│   ├── collection.json
│   ├── env.dev.json
│   └── env.ci.json
├── reports/
│   └── api.html
├── README.md
└── REFLECTION.md
```

## Environment хувьсагчид
| Хувьсагч     | Тайлбар                              |
|--------------|--------------------------------------|
| baseUrl      | API-ийн үндсэн URL                   |
| postId       | GET /posts-аас chain хийгдэн орно    |
| userId       | GET /posts-аас chain хийгдэн орно    |
| newPostId    | POST /posts-аас chain хийгдэн орно   |
| randomTitle  | Pre-request script-аар үүсгэгдэнэ    |
