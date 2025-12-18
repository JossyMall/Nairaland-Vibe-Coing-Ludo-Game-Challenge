# 🎲 NairalandLudo - Ultimate 3D Edition

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

> 🚀 **Official Entry: Nairaland Forum Ludo Game Vibe Coding Challenge** > 👨‍💻 **Developer:** **mushroomfarm** (Nairaland)

**NairalandLudo** is a fully interactive, browser-based 3D Ludo game inspired by the classic board game. Built entirely with vanilla HTML, CSS, and JavaScript, it features a physics-simulated 3D dice, a rotatable board, intelligent AI opponents, and a robust local multiplayer mode.

---

## 🙌 Appreciation

A huge shoutout to **Seun Osewa** (the founder of Nairaland) for creating the platform that brought us all together.

It is an absolute honour to participate in this coding challenge alongside so many talented developers. **Win or not**, the joy of building this for the culture and contributing to the community is the real prize.

---

## ✨ Features

### 🎮 Game Modes
* **Vs AI Mode:** Play solo against 1, 2, or 3 computer-controlled bots. The AI intelligently prioritizes capturing opponents and moving tokens out of base.
* **Local Multiplayer (Hotseat):** Play with friends on the same device.
    * **Custom Selection:** Choose exactly which colors (Red, Green, Yellow, Blue) are active players.
    * **Minimum 2 Players:** The game enforces a valid setup before starting.

### 🎨 Visuals & Immersion
* **True 3D Board:** Built using CSS 3D transforms. Hold `Click + Drag` to rotate the camera angle.
* **3D Dice Rolling:** A tumbling 3D cube that lands on the generated random number.
* **Animations:**
    * **"Kick" Animation:** When a piece is captured, it spins and shrinks before teleporting back to base.
    * **Celebrations:** Confetti explosions and overlay text ("GBAM! 6!") for high rolls and victories.
    * **Smooth Movement:** Tokens glide across the board and sit perfectly centered in their cells.

### ⚙️ Game Mechanics
* **Classic Rules:** Roll a **6** to leave the home base.
* **The "Chop" Rule (Displacement):** Landing on an opponent's occupied square sends them back to the start (unless it is a Safe Zone).
* **Safe Zones:** Starred squares (and colored starting tracks) are safe havens where pieces cannot be captured.
* **The "Three 6s" Rule:** Rolling three 6s in a row forfeits your turn (prevents infinite loops).
* **Winning:** The first player to get all 4 tokens to the center "Snake Land" wins.

---

## 🚀 How to Run

No installation, build tools, or servers are required!

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/NairalandLudo.git](https://github.com/yourusername/NairalandLudo.git)
    ```
2.  **Open the file:**
    Navigate to the folder and double-click `index.html` (or `ludo_v2.html`) to open it in any modern web browser (Chrome, Firefox, Edge, Safari).

**That's it!**

---

## 🕹️ Controls

| Action | Control |
| :--- | :--- |
| **Roll Dice** | Click the **ROLL** button (or wait for AI). |
| **Move Token** | Click on a glowing/bouncing token to move it. |
| **Rotate Board** | `Left Click + Drag` anywhere on the background. |
| **Select Color** | Click color circles in the Setup Menu. |

---

## 🛠️ Technical Implementation

### The 3D Engine
The game uses `perspective` and `transform-style: preserve-3d` in CSS to create the depth. The board is a grid of `div`s, and the dice is a constructed cube. No WebGL or Canvas libraries (like Three.js) were used—this is pure CSS power!

### The Logic (`game.js`)
* **State Management:** A central `gameState` object tracks turn order, token positions (0-57), and dice values.
* **Pathfinding:** A mapping system converts a linear path index (1-52) into specific Grid Row/Column coordinates for visual placement.
* **AI Logic:** A decision tree that prioritizes moves:
    1.  *Can I capture an enemy?* (Highest Priority)
    2.  *Can I leave home base?*
    3.  *Can I score/win?*
    4.  *Just move forward.*

---

## 📸 Screenshots

*(Add your screenshots here)*

> **Start Screen:** Choose between AI or Multiplayer setup.
>
> **The Board:** Highlighting the 3D perspective and safe zones.
>
> **Victory:** Confetti raining down on the winner.

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for:
* Online Multiplayer (WebSockets).
* Sound Effects.
* Save/Load functionality.

Feel free to fork the repo and submit a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<p align="center">
  Built with ❤️ for the Nairaland Community
</p>
