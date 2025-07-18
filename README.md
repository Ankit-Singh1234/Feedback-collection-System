# 📬 Feedback Collection System

A full-stack web application that allows authenticated users to create and send feedback surveys. Built using the **MERN** stack (MongoDB, Express, React, Node.js) with Google OAuth for authentication.

---

## 🚀 Features

- 🔐 Google OAuth Login using Passport.js
- ✉️ Send feedback surveys
- 📊 Track user responses
- 🍪 Cookie-based session handling
- ⚡ Run both client & server from one console
- ✅ Ready for production deployment

---

## 📁 Project Structure

```
/client         - React frontend
/config         - Configuration files (keys.js, prod.js, dev.js)
/middlewares    - Custom Express middleware
/models         - Mongoose models (User, Survey)
/routes         - Express route handlers
/services       - OAuth and mailer setup
index.js        - Express server entry point
```

---

## 🛠️ Tech Stack

- **Frontend**: React.js
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose)
- **Authentication**: Google OAuth 2.0 with Passport.js
- **Deployment**: Heroku / Render-ready
- **Other**: cookie-session, body-parser, concurrently

---

## 🔧 Setup Instructions

### Prerequisites

- Node.js (v16+)
- MongoDB URI (from MongoDB Atlas or local MongoDB)
- Google OAuth credentials (Client ID + Secret)

---

### 📥 Installation

```bash
# Clone the repository
git clone https://github.com/Ankit-Singh1234/feedback-collection-system.git
cd feedback-collection-system

# Install dependencies
npm install
cd client
npm install
cd ..
```

---

### ⚙️ Configuration

Create a file: `config/dev.js`

```js
module.exports = {
  googleClientID: "YOUR_GOOGLE_CLIENT_ID",
  googleClientSecret: "YOUR_GOOGLE_CLIENT_SECRET",
  mongoURI: "YOUR_MONGO_DB_URI",
  cookieKey: "RANDOM_COOKIE_KEY"
};
```

---

### ▶️ Run the App (Single Console)

```bash
# This will start both client and server
npm run dev
```

> Make sure `concurrently` is defined in `package.json`:
```json
"scripts": {
  "dev": "concurrently \"npm run server\" \"npm run client\"",
  "server": "nodemon index.js",
  "client": "npm start --prefix client"
}
```

---

## 🌐 Deployment

- Set environment variables in your production platform
- Run `npm run build` inside `/client`
- Express will serve React build automatically when in production

---

## 📄 License

MIT License © 2025 [Ankit Singh](https://github.com/Ankit-Singh1234)
