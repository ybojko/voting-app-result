# voting-app-result

Node.js frontend для відображення результатів голосування. Частина Docker Voting App.

## Сервіс

- Мова: Node.js (Express)
- Порт: 80
- Залежності: PostgreSQL (сховище результатів), Socket.IO (реальний час)

## Docker

```bash
docker build -t voting-app-result .
docker run -p 8081:80 voting-app-result
```

## Multi-arch збірка

```bash
docker buildx build --platform linux/amd64,linux/arm64 \
  -t <registry>/voting-app-result:latest --push .
```
