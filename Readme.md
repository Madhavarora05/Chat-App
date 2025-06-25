# 💬 Real-Time Chat Application

A simple and responsive real-time chat app built using **Node.js**, **Express**, **Socket.IO**, and **React**. This was created as part of the full-stack development assignment to demonstrate WebSocket communication and UI interactivity.

---

## 📁 Project Structure

```

chat-app/
├── backend/                    # Backend code (Node.js + Express + Socket.IO)
│   ├── index.js                # Server + Socket.IO logic
│   └── package.json            # Backend dependencies
│
├── frontend/                   # Frontend code (React)
│   ├── src/
│   │   ├── App.js              # Main App with routes and logic
│   │   ├── App.css             # Stylesheet for the whole app
│   │   └── components/
│   │       ├── ChatWindow\.jsx  # Main chat interface
│   │       └── Login.jsx       # Login UI
│   └── package.json            # Frontend dependencies

````

---

## ⚙️ Technologies Used

- **Frontend**: React (via Create React App), HTML5, CSS3
- **Backend**: Node.js, Express.js
- **WebSocket**: Socket.IO
- **Dev Tools**: VS Code, npm, Chrome DevTools

---

## 📦 Dependencies

### Frontend

Installed via `npm install` inside the `frontend/` directory:

- `react`
- `react-dom`
- `react-scripts`
- `socket.io-client`

### Backend

Installed via `npm install` inside the `backend/` directory:

- `express`
- `socket.io`
- `cors`

---

## 🚀 How to Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/chat-app.git
cd chat-app
````

---

### 2. Start the Backend

```bash
cd backend
npm install 
node index.js
```

> Backend runs on: `http://localhost:5050`

---

### 3. Start the Frontend

Open a new terminal:

```bash
cd frontend
npm install 
npm start 
```

> Frontend runs on: `http://localhost:3000`

Make sure both servers are running in separate terminals.

---

## ✨ Features Implemented

* ✅ Simple login form (no auth, username only)
* ✅ Real-time chat using WebSockets
* ✅ Typing indicators (shows when a user is typing)
* ✅ Chat history display with system messages
* ✅ Responsive design for mobile and desktop
* ✅ Clean and readable UI with styled components

---

## 📊 Architecture & Flow

* When the React app loads, user submits a username via the login screen.
* After login, React connects to the Socket.IO server and sends/receives events like:

  * `send_message`: to broadcast a message
  * `typing`: to show typing indicators
  * `receive_message`: to update chat window for all users
* Server uses Socket.IO to broadcast messages and typing states to all clients in real-time.

---

