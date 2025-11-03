# Читать обязательно

## Команды и стек
- **frontend** (Вова, Марк): Next.js → порт 3000
- **backend** (Макс, Даня): Nest.js → порт 4000
- **ai-backend** (Илья): FastAPI → порт 8000

---

## Пошаговый workflow

### 1️⃣ Клонировать репу
```bash
git clone <url>
cd hackathon-2025
```

### 2️⃣ Создать свою ветку (НЕ пушьте в main!)
```bash
git checkout -b feature/<your-name>
# например: git checkout -b feature/vova-frontend
```

### 3️⃣ Писать код
- код пишете в своей папке: `frontend/`, `backend/` или `ai-backend/`
- ваш Dockerfile уже готов, не трогайте порты

### 4️⃣ Проверить что контейнер собирается (ПЕРЕД пушем!)
```bash
cd <your-folder>  # например: cd backend
docker build -t hackathon-backend .
docker run -p 4000:4000 hackathon-backend
```
Если контейнер запустился без ошибок — всё окей.

### 5️⃣ Закоммитить и запушить
```bash
git add .
git commit -m "ваше описание"
git push origin feature/<your-name>
```

### 6️⃣ Создать Pull Request
- идите на GitHub, создайте PR в main
- Макс проверит и смержит

### 7️⃣ Запустить всё вместе
```bash
docker-compose up --build
```
Откроется: фронт на localhost:3000, бек на localhost:4000, ии бек на localhost:8000

---

## Важные моменты
- **node_modules/, .venv/, .env** — уже в .gitignore, не коммитьте
- **приватные ключи** — пушьте смело в репу, она приватная (OPEN_AI_KEY и т.д.)
- **Docker networking:** в docker-compose контейнеры общаются по имени сервиса, НЕ по localhost
  - backend общается с ai-backend по: `http://ai-backend:8000` (не localhost!)
  - localhost работает только когда ты запускаешь контейнер локально и обращаешься с хоста
- **логи контейнеров:** `docker-compose logs -f`
- **остановить контейнеры:** `docker-compose down`

## Общее напутствие
- команда не ждёт что вы будете рвать жопу, вы также не ждёте этого от других
- всем похер на то как написан код
- задача — криво косо сделать минимально рабочий прототип
- пишите код через ии — он умнее чем все мы, быстрее через терминал, например [Gemini CLI](https://github.com/google-gemini/gemini-cli?tab=readme-ov-file#-installation) (бесплатно)


Test-main commit