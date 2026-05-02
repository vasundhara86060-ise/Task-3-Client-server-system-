📨 Client–Server Chat System (Java)
A simple multi-client chat application built using Java Sockets, showcasing how client–server communication works in real time. This project is part of a networking lab / academic assignment and demonstrates the basic architecture of distributed communication.

🚀 Features
✅ Server
Accepts multiple client connections
Handles each client in a separate thread
Broadcasts messages to all connected clients
Logs client connections and disconnections

✅ Client
Connects to the server through sockets
Sends messages to the server
Receives broadcast messages from all other clients
Runs send/receive operations in parallel threads

📁 Project Structure

Task-3-Client-server-system/
│
├── ChatServer.java        # Main server program
├── ClientHandler.java     # Handles each connected client
├── ChatClient.java        # Client-side code
└── README.md              # Documentation

🏗️ How It Works
🔹 Step 1: Server Starts
The server opens a ServerSocket on a fixed port
(Example: port 12345) and waits for clients.

🔹 Step 2: Client Connects
Each client uses a Socket to connect to the server IP + port.

🔹 Step 3: Server Spawns a Thread
For every client, the server creates a ClientHandler thread.

🔹 Step 4: Messaging
Clients send messages → Server receives them → Server broadcasts to every connected client.

▶️ How to Run the Project
1. Start the Server
   
2.Bash
javac ChatServer.java ClientHandler.java
java ChatServer

3. Start Each Client (in new terminal windows)
Bash
javac ChatClient.java
java ChatClient

4. Start Chatting 🎉
Anything typed in a client window will appear in all other client windows.
