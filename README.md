
---

# ♟ Real-Time Multiplayer Chess Game

This is a web-based multiplayer chess game built with **Node.js**, **Express**, **Socket.IO**, and **chess.js**. Two players can play against each other in real-time while additional users can join as spectators.

## 🚀 Features

* Real-time multiplayer gameplay using WebSockets
* Auto assignment of roles: White, Black, or Spectator
* Drag-and-drop chess piece movement
* Legal move validation using `chess.js`
* Responsive UI with Unicode chess pieces
* Spectators can view the ongoing game live
* Automatic board flipping for Black player

## 🧰 Technologies Used

* **Frontend**: HTML, CSS, JavaScript (vanilla)
* **Backend**: Node.js, Express.js
* **Real-time Communication**: Socket.IO
* **Chess Logic**: [chess.js](https://github.com/jhlywa/chess.js)

## 📦 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/raj-kmr/chess.git
   cd chess
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Run the server**

   ```bash
   node server.js
   ```

4. **Visit the app**
   Open your browser and go to: [http://localhost:3000](http://localhost:3000)

## 🕹 How It Works

* The first user to connect becomes the **White** player.
* The second user becomes the **Black** player.
* Any further users are assigned the **Spectator** role.
* Players can drag and drop pieces only if it's their turn.
* The server validates each move using `chess.js` before broadcasting it.
* Board state is shared with all users in real-time.

## 🧠 Game Logic Highlights

* Chess rules are handled by the `chess.js` library.
* Socket events:

  * `playerRole`: Assigns role to new player
  * `spectatorRole`: Assigns role to spectators
  * `move`: Transmits moves and updates state
  * `boardState`: Syncs the full board (FEN string) to all clients


## ✅ To-Do (Optional Enhancements)

* Add move history display
* Highlight legal move squares
* Show game end status (Checkmate, Draw, etc.)
* Add player timers or clock
* User authentication and room system

---
