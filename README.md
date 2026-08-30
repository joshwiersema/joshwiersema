# 👋 Hi, I'm Josh Wiersema
### Computer Science Student

I'm a CS student, athlete, and freelance developer who loves building real, practical software. From full-stack apps for local businesses to algorithm-heavy C++ projects and machine learning experiments.

I know how to actually code, and I leverage AI to build both ambitious and real, applicable software.

I use GitHub to showcase clean, well-structured projects that reflect what I'm learning and what I can build.

---

## 🚀 Featured Projects (Pinned)

### 🤖 JARVIS 3

📌 A voice-first AI desktop presence for Windows, built with Tauri v2, React/TypeScript, and Python FastAPI.

Jarvis 3 talks back, remembers what you tell him, and writes his own abilities when he doesn't have one — tests them, hot-loads them, and uses them on the next sentence. It includes:

- On-device speech-to-text (faster-whisper + Silero VAD) so audio never leaves the machine
- A persistent brain: plain-markdown memory (Obsidian-compatible) wired into a weighted synapse graph, with neural-embedding recall and Hebbian-style strengthening
- A background trainer that consolidates, merges, and decays memory while idle
- Self-forging skills — no hardcoded capability list; Jarvis writes, tests, and loads new ones at runtime
- A phone client sharing the same backend, wire protocol, and brain over a token-gated TLS tunnel
- A 3D WebGL particle orb UI reflecting real-time voice state

📊 A full local/cloud hybrid architecture — voice and memory stay on-device, reasoning runs in the cloud — showcasing desktop app architecture, real-time audio pipelines, and agentic system design.

*This one took about four months and a lot of back-and-forth — I went through four different Claude Opus models over the life of the project plus Claude Fable 5, and ran Codex alongside as a second set of eyes for code review. It's the project that pushed me hardest on architecture decisions I actually had to defend, not just accept.*

🔗 Repo: Pinned below

---

### 🖥️ Render Fault Detector (Image Corruption Model)

📌 A 1.2M-parameter CNN that looks at a rendered game frame and tells you whether the GPU that drew it was misbehaving — and how — in ~12ms on CPU.

Built end-to-end with Claude Opus 5, run through the Claude Code harness: a labeled corpus that didn't previously exist, a dual-head classifier trained on it, an evaluation harness measuring what actually gates deployment, and a written report explaining what the model learned and where it still fails. It includes:

- A synthetic corruption pipeline built from ~1,550 real game captures across 10 titles, injecting 6 distinct hardware-failure signatures at seeded severities
- A dual-head CNN (binary fault / 7-way classification) trained jointly, evaluated on 1,240 held-out samples
- 97.2% detection accuracy, 96.1% correct-fault classification, **0 false positives** across 388 clean holdout frames
- A full latency-profiled inference benchmark (12.5ms mean / 80 FPS on laptop CPU)
- A self-contained HTML report with every figure, plus documented failure analysis and next steps

📊 A complete applied-ML arc — problem framing, data strategy, model, evaluation, and communication — not just a training script.

🔗 Repo: Pinned below

---

### 🎮 CliffWalk Q-Learning vs SARSA
*(Class Project: NO AI USED)*

📌 A reinforcement learning comparison project built with Python and Gymnasium.

Implements tabular Q-Learning and SARSA on the CliffWalking-v0 environment to explore off-policy vs on-policy learning. It includes:

- Training both agents over 1000 episodes
- Tracking and plotting key metrics (reward, cliff falls, steps)
- Real-time GUI visualization of agent success / ASCII policy visualization of learned strategies
- Clear demonstration of how exploration and update rules shape behavior

📊 Q-Learning favors higher-reward but riskier strategies, while SARSA learns safer paths — a showcase of RL fundamentals and empirical evaluation.

🔗 Repo: Pinned below

---

### ♠️ BlackJack Game
*(Class Project: NO AI USED)*

📌 A fully playable multiplayer Blackjack game built in C++ with no external dependencies — just the standard library.

Runs in the console, supports any number of players against a single dealer, with a play-again loop. Organized into six classes (Card, Deck, Hand, Player, BlackjackGame, plus a thin main). Key details:

- Deck shuffles using `std::mt19937` seeded from `std::random_device`
- Automatically reshuffles mid-round if the deck runs out
- Fully automatic Ace handling — treated as 11 when it helps, 1 when 11 would bust
- Dealer follows standard casino rules, hitting below 17 and standing otherwise
- Each player gets their own per-round result: win, lose, or push

**Tech:** C++
**Highlights:** OOP, game state management, randomness, data structures

🌐 Live Python Version: uiblackjack.onrender.com

🔗 Repo: Pinned below

---

### 🔢 ASCII Optimization (Huffman Trees)
*(Class Project: NO AI USED)*

A C++ implementation of Huffman Tree compression for ASCII text optimization.

Demonstrates algorithmic understanding, tree structures, recursion, and efficient encoding/decoding.

**Tech:** C++
**Highlights:** Priority queues, binary trees, recursive tree building, compression logic

🔗 Repo: Pinned below

---

### 🧠 Excess Machine Learning Projects

This project explores machine learning techniques using two datasets. The Linear Regression notebook loads and cleans Auto.csv, performs exploratory analysis, trains a regression model, visualizes MPG relationships, and evaluates performance with standard error metrics. The Tree-Based Modeling notebook uses forestfires.csv to train ensemble models (bagging, boosting, random forest), measure accuracy, and show how tree-based methods capture nonlinear patterns in data.

**Tech:** Python, Pandas, NumPy, Matplotlib, Scikit-learn
**Highlights:** Regression modeling, plotting

🔗 Repo: Pinned below

---

## 🛠️ Tech Stack

**Languages:**
Python • Java • C++ • JavaScript •

**Tools & Frameworks:**
Full Claude Suite/ Codex, multiple Claude Code projects
Git/GitHub
React (basic)
TensorFlow, Pytorch, NumPy, Pandas, scikit-learn, Matplotlib
Linux / Ubuntu / Kali, VS Code, PyCharm, CLion. Cursor

## 📫 Contact Me

Email: josh.wiersema06@gmail.com
LinkedIn: linkedin.com/in/josh-wiersema-526452377

Thanks for visiting my GitHub!

Feel free to explore the pinned repos below 👇
