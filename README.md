# 💬 Real-Time Chat App with WebSockets (Socket.IO)

A real-time, two-way chat application built using **Node.js**, **Express**, and **Socket.IO**, supporting:

- 🔐 User login with username
- 🗨️ Public and private messaging
- 🖼️ Image sharing
- 💾 Session persistence (saved chat history)
- 👥 Dynamic online user list

---

## 📦 Features

| Feature              | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Login**            | Prompt for a username before entering the chat                              |
| **Real-time Chat**   | Send and receive messages instantly using WebSockets                        |
| **Private Messaging**| Send messages directly to a specific user                                   |
| **Image Upload**     | Upload and send images via `<input type="file">` and base64 encoding        |
| **Session Persistence** | Chat history saved to a JSON file (or MongoDB with optional upgrade)     |
| **User List**        | See who is online in real time                                               |

---

![project](https://github.com/user-attachments/assets/9d002df9-8263-4e05-b6b1-b5c82c52d27f)


## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, Vanilla JavaScript
- **Backend**: Node.js, Express.js
- **WebSockets**: Socket.IO
- **Persistence**: `messages.json` (can be upgraded to MongoDB)

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/chat-app.git
cd chat-app
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run the server

```bash
node server.js
```

The app will be available at:  
🌐 **http://localhost:3000**

---

## 📁 Project Structure

```
chat-app/
├── public/
│   ├── index.html        # Main frontend UI
│   ├── client.js         # Socket.IO client logic
│   ├── style.css         # Basic styles
├── messages.json         # Message history (for session persistence)
├── server.js             # Express + Socket.IO server
├── package.json
```

---

## 💬 How It Works

### User Flow:

1. User visits `localhost:3000`
2. Enters their name in the **login screen**
3. Enters the chat room with:
   - Full message history
   - User list
4. Can:
   - Send messages to everyone
   - Send private messages by specifying a recipient
   - Upload an image to share
5. Message history is stored and reloaded on reconnect.

---

## 🖼️ Image Upload

- Users can upload images using `<input type="file">`.
- Images are sent as base64-encoded strings via WebSocket.
- Images are displayed directly in the chat window.

---

## 🔐 Private Messaging

To send a private message:
1. Enter the username of the recipient in the `Private to` field.
2. Type your message.
3. Click **Send Private**.

Only the sender and recipient will see the private message.

---

## 🗃️ Session Persistence

- Messages are saved to `messages.json` file on the server.
- On reconnect or new login, full history is loaded for all users.
---

## 🔧 Optional MongoDB Integration (Advanced)

To use MongoDB instead of a JSON file:

1. Install MongoDB and `mongoose`:

```bash
npm install mongoose
```

2. Replace file-based storage in `server.js` with MongoDB logic.

3. Use Mongoose models to store and retrieve messages and users.


---

## 📌 TODO / Future Enhancements

- [ ] Upgrade message storage to MongoDB or Firebase
- [ ] Add typing indicators
- [ ] Enable user avatars via RandomUser API
- [ ] Use authentication (e.g. JWT) for secure login
- [ ] Create rooms or channels
- [ ] Deploy to Heroku/Vercel/Render

---

## 🧑‍💻 Author

Developed by Sairin and Sheenu  


