<h1 align="center">🔗 Shortify - Ultra Advanced URL Shortener Platform 🚀</h1>

<p align="center">
  <strong>Scalable | Secure | Analytics-Driven | API Ready</strong> <br>
  <em>Transform long URLs into sleek, trackable links.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-production--ready-brightgreen?style=for-the-badge" />
 
  <img src="https://img.shields.io/badge/PRs-welcome-blueviolet?style=for-the-badge" />
</p>

---

## ⚡ Overview

**Shortify** is a modern, full-featured URL shortening platform built for speed, scalability, and insights. It provides developers and users with:

- Shortened, trackable URLs
- Expiry control, analytics, and device/IP tracking
- REST API support
- Cloud deployment support (Docker, Render, Vercel)
- Security measures for abuse prevention
- Optional admin dashboard for link management

---

## 🧠 Key Features

✅ Create short URLs with unique codes  
📈 Real-time click tracking and analytics *(optional)*  
⏳ Set expiration times on links  
🛡️ Rate limiting, sanitization & security middleware  
📱 Responsive frontend (React/Vite or HTML/JS)  
⚙️ Full REST API for programmatic access  
🔐 Role-based authentication (admin/user) *(optional)*  
🧾 QR code generation for easy sharing *(optional)*  
💬 URL preview metadata (OG scraping) *(optional)*  

---

## 🧱 Tech Stack

| Layer            | Technology                        |
|------------------|------------------------------------|
| **Language**     | Node.js (JavaScript)              |
| **Framework**    | Express.js                        |
| **Database**     | MongoDB with Mongoose             |
| **Short Code**   | `nanoid`                          |
| **Env Config**   | `dotenv`                          |
| **Analytics**    | Redis or MongoDB aggregations *(optional)* |
| **Rate Limiting**| `express-rate-limit`              |
| **Security**     | `helmet`, `cors`, `xss-clean`     |
| **Logging**      | `morgan`, `winston` *(optional)*  |
| **Frontend**     | React.js / Tailwind / Bootstrap *(optional)* |
| **CI/CD**        | GitHub Actions / Render / Railway |
| **Container**    | Docker, Docker Compose            |

---

## 🔧 Setup Instructions

### 🔹 1. Clone & Install

```bash
git clone https://github.com/Sarvesh2783/Shortify.git
cd ShareShort/backend
npm install
```

### 🔹 2. Configure Environment

```bash
cp .env.example .env
```

Example `.env`:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/shortener
BASE_URL=http://localhost:5000
RATE_LIMIT_WINDOW_MS=60000
RATE_LIMIT_MAX=100
```

---

## 📦 API Reference

### ➕ Create Short URL

**POST** `/api/shorten`

```json
{
  "longUrl": "https://example.com",
  "expiryHours": 72
}
```

Returns:

```json
{
  "shortUrl": "http://localhost:5000/xyz123",
  "code": "xyz123",
  "expiry": "2025-06-30T12:00:00Z"
}
```

---

### 📥 Redirect to Original

**GET** `/:code`  
➡️ Redirects to the original `longUrl`.

---

### 📊 Get Analytics (Optional)

**GET** `/api/analytics/:code`

Returns:

```json
{
  "clicks": 143,
  "devices": { "desktop": 90, "mobile": 53 },
  "countries": { "US": 45, "IN": 72 }
}
```

---

## 🐳 Docker Setup

```bash
# Build & start containers
docker-compose up --build
```

Docker will spin up:

- Backend on `localhost:5000`
- MongoDB on default port `27017`

---

## 🧪 Testing

```bash
npm run test
```

Uses `Jest` + `Supertest` for testing endpoints.

---

## 🛡️ Security

- Rate limiting (prevent abuse)
- CORS & Helmet headers
- Input sanitization (XSS, NoSQL injection)
- Optional API key auth or JWT auth

---

## 🌍 Deployment

✅ **Render** – Free Node.js hosting  
✅ **Vercel/Netlify** – Frontend deployment  
✅ **MongoDB Atlas** – Cloud MongoDB  
✅ **Railway** – Fullstack deployment  
✅ **Docker** – Containerize the full app

---

## 🙌 Contributing

```bash
# Fork the repo
# Create a new branch
git checkout -b feature/your-feature
# Commit changes
git commit -m "Add: your feature"
# Push and open PR
```

We follow conventional commits and clean code. PRs are reviewed regularly.

---

## 📄 License

Licensed under the MIT License.

---

## 👤 Author

**Sarvesh Charpe**  
📫 sarveshcharpe27@gmail.com  
🌐 [GitHub](https://github.com/Sarvesh2783) • [LinkedIn]([https://linkedin.com/in/sarveshcharpe](https://www.linkedin.com/in/sarvesh-charpe-486076286/)

---

## 🌟 Star This Repo

If this project helped you or you liked it — show your support by starring ⭐️ the repo.
