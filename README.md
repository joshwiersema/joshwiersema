# 👋 Hi, I'm Josh Wiersema

### Computer Science Student

I'm a CS student, athlete, and freelance developer who loves building real, practical software. From full-stack apps for local businesses to algorithm-heavy C++ projects and machine learning experiments.

I know how to actually code, and I leverage AI to build both ambitious and real, applicable software.

I use GitHub to showcase clean, well-structured projects that reflect what I'm learning and what I can build.

---

## 🚀 Featured Projects (Pinned)

### 🤖 **JARVIS 1.0**

📌 A voice-first AI desktop assistant for Windows, built with Tauri v2, React/TypeScript, and Python FastAPI.

This project is a personalized Jarvis prototype that lets you talk to your computer naturally — ask questions, control apps, run automations, and generate code through conversation. It includes:

- On-device **speech-to-text** with faster-whisper and VAD for privacy
- **Dual-model intelligence** using Claude Sonnet for conversation and Haiku for fast intent routing
- **Streaming TTS** via Fish Audio or ElevenLabs, targeting <2s end-to-end latency
- System control, app launching, web search, Playwright browser automation, and Claude Code generation
- Speaker voice authentication and a SQLite + FTS5 memory store with semantic embeddings
- A 3D WebGL particle orb UI that visualizes voice state in real time

📊 *A full hybrid local/cloud pipeline — audio and storage stay on-device while the heavy reasoning runs in the cloud — showcasing desktop app architecture, real-time audio processing, and practical LLM integration.*

🔗 **Repo:** *Pinned below*

---

### 🎮 **CliffWalk Q-Learning vs SARSA**

📌 A reinforcement learning comparison project built with Python and Gymnasium.

This project implements **tabular Q-Learning** and **SARSA** on the `CliffWalking-v0` environment to explore differences between off-policy and on-policy learning. It includes:

- Training both agents over 1000 episodes
- Tracking and plotting key metrics (reward, cliff falls, steps)
- Real-Time GUI Visualization of Agent success / ASCII policy visualization of learned strategies
- Clear demonstration of how exploration and update rules shape behavior

📊 *Q-Learning favors higher-reward but riskier strategies, while SARSA learns safer paths — a great showcase of RL fundamentals and practical empirical evaluation.*

🔗 **Repo:** *Pinned below*

---

### ♠️ **BlackJack Game**

📌 A fully playable multiplayer Blackjack game built in C++ with no external dependencies — just the standard library.

The game runs in the console and supports any number of players against a single dealer, with a play-again loop so you can run round after round. The codebase is organized into six classes, each in its own header/source pair: `Card`, `Deck`, `Hand`, `Player`, `BlackjackGame`, and a thin `main` entry point. Key details:

- Deck shuffles using `std::mt19937` seeded from `std::random_device`
- Automatically reshuffles mid-round if the deck runs out
- Fully automatic Ace handling — treated as 11 when it helps, 1 when 11 would bust
- Dealer follows standard casino rules, hitting below 17 and standing otherwise
- Each player gets their own per-round result against the dealer: win, lose, or push

**Tech:** C++

**Highlights:** OOP, game state management, randomness, data structures

🔗 **Repo:** *Pinned below*

🌐 **Live Python Version:** [uiblackjack.onrender.com](https://uiblackjack.onrender.com)

---

### 🔢 **ASCII Optimization (Huffman Trees)**

A C++ implementation of Huffman Tree compression for ASCII text optimization.

Demonstrates algorithmic understanding, tree structures, recursion, and efficient encoding/decoding.

**Tech:** C++

**Highlights:** Priority queues, binary trees, recursive tree building, compression logic

🔗 **Repo:** *Pinned below*

---

### 🧠 **Machine Learning Project**

This project explores machine learning techniques using two datasets. The Linear Regression notebook loads and cleans `Auto.csv`, performs exploratory analysis, trains a regression model, visualizes MPG relationships, and evaluates performance with standard error metrics. The Tree-Based Modeling notebook uses `forestfires.csv` to train ensemble models (bagging, boosting, random forest), measure accuracy, and show how tree-based methods capture nonlinear patterns in data.

**Tech:** Python, Pandas, NumPy, Matplotlib, Scikit-learn

**Highlights:** Regression modeling, plotting

🔗 **Repo:** *Pinned below*

---

### 🎯 **Networked Connect 4 Game**

A client–server implementation of Connect 4 built from my CS2 final. Being from my CS2 Final, that does make it a little sloppy.

Regardless, it still features real-time gameplay between two players over TCP sockets, server-side game state management, turn handling, and win/draw detection.

**Tech:** Java (Socket Programming, OOP)

**Highlights:** Networking fundamentals, client/server architecture, game logic, practical systems programming

🔗 **Repo:** *Pinned below*

---

## 🛠️ Tech Stack

**Languages:**

- Python • Java • C++ • JavaScript • HTML/CSS • Anything, to be honest

**Tools & Frameworks:**

- Full Claude Suite, multiple Claude Code projects
- Git/GitHub
- React (basic)
- NumPy, Pandas, scikit-learn, Matplotlib
- Linux / Ubuntu / Kali, VS Code, PyCharm, CLion

---

## 📫 Contact Me

- **Email:** josh.wiersema06@gmail.com
- **LinkedIn:** [linkedin.com/in/josh-wiersema-526452377](https://www.linkedin.com/in/josh-wiersema-526452377/)

---

Thanks for visiting my GitHub!

Feel free to explore the pinned repos below 👇
