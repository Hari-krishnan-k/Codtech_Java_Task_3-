# 💬 Task 3 – Multithreaded Chat Application

This Java project implements a **real‑time, multi‑user chat system** using **Sockets** and **Multithreading**. Multiple clients can connect to a central server, send messages, and receive broadcasts from all other connected users.

---

## ✅ Features

- **Server** accepts multiple client connections concurrently  
- **ClientHandler** threads manage each connected user  
- **Broadcast** mechanism delivers messages to all clients  
- Graceful handling of user join/leave events  

---

## 📦 Project Structure

Task-3_Chat_Application/
├── ChatServer.java # Server-side implementation
├── ChatClient.java # Client-side implementation
└── README.md # This file

yaml
Copy
Edit

---

## 🛠️ Prerequisites

- **Java SE 8** or above  
- Network access (clients connect via TCP/IP)  
- Terminal or IDE of your choice  

---

## 🔧 Setup & Run

### 1. Compile

Open a terminal in `Task-3_Chat_Application/` and run:
```bash
javac ChatServer.java ChatClient.java
2. Start the Server
In one terminal window:

bash
Copy
Edit
java ChatServer
You should see:

arduino
Copy
Edit
Server started. Waiting for clients...
3. Launch Clients
In separate terminal windows (or machines) within the same network:

bash
Copy
Edit
java ChatClient
When prompted, enter your username.

Start typing messages—each will be broadcast to all connected users.

📝 Sample Interaction
Server Console

sql
Copy
Edit
Server started. Waiting for clients...
New user connected: Socket[addr=/127.0.0.1,port=54321,localport=1234]
New user connected: Socket[addr=/127.0.0.1,port=54322,localport=1234]
Client 1

yaml
Copy
Edit
Enter your name:
Alice
Alice joined the chat.
Bob: Hi Alice!
Alice: Hello Bob!
Client 2

yaml
Copy
Edit
Enter your name:
Bob
Bob joined the chat.
Alice: Hello Bob!
Bob: Hi Alice!
📌 Notes
By default, the server listens on port 1234; you can change this in ChatServer.java.

Clients connect to localhost. To run over a network, replace "localhost" in ChatClient.java with the server’s IP address.
