# 👋 Hi, I'm Josh Wiersema
### Computer Science Student

I'm a CS student, athlete, and freelance developer who loves building real, practical software. From full-stack apps for local businesses to algorithm-heavy C++ projects and machine learning experiments.

I know how to actually code, and I leverage AI to build both ambitious and real, applicable software.

I use GitHub to showcase clean, well-structured projects that reflect what I'm learning and what I can build.

---

## 🚀 Featured Projects (Pinned)

### 🤖 JARVIS v3  

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
Project Display: https://joshwiersema.github.io/Jarvisv3/ 
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
Project Display: https://joshwiersema.github.io/Image-Corruption-Model/ 

---


### ⚙️ RiscSim (RISC-V Processor Simulator & IDE)

📌 A from-scratch RISC-V simulator that answers the question Ripes and other tools leave you to guess: for the instruction currently in the pipeline, *why* is this exact wire, mux, or control signal on right now.

Built in TypeScript, React, and Electron as a native desktop app for Windows, macOS, and Linux: a real two-pass assembler, two full processor models, a configurable memory hierarchy, and a datapath that explains itself instead of just lighting up. It includes:

- Two processors — single-cycle RV32IMC and a 5-stage in-order pipeline (IF/ID/EX/MEM/WB) with EX/MEM and MEM/WB forwarding, a load-use hazard unit, branch resolution in EX with flush, and full reverse execution of every cycle
- A two-pass RV32I/M/C assembler with pseudo-instruction expansion, automatic 16-bit compression with branch relaxation, an ELF32 loader, and native compilation/loading of real C programs via installed RISC-V GCC
- Configurable L1 instruction/data caches (LRU/FIFO/random, write-back/write-through, write-allocate) with live hit/miss stats, evictions, and a tag/index/offset breakdown of every access
- Memory-mapped I/O (LED matrix, switches, d-pad, character output) alongside an explain-on-hover datapath giving a plain-English reason for every wire and control signal's value, plus a stage-by-stage walk mode
- Shipped cross-platform installers for Windows, macOS, and Linux via GitHub Actions CI with automated releases and in-app auto-update, backed by a Vitest suite covering the assembler, both processor models, caches, ELF, and I/O

📊 A complete systems-programming arc — ISA design, pipelining, memory hierarchy, and developer tooling — built to teach computer architecture more clearly than existing tools like Ripes.

🔗 Repo: Pinned below
Installers: <https://github.com/joshwiersema/RiscVSim-Editor/releases>

---

### ⚙️ AsyncFIFO (Dual-Clock FIFO in Verilog)
📌 A small, readable asynchronous FIFO that moves data safely between two clocks that have nothing to do with each other.

Written in plain Verilog-2001 and simulated with Icarus Verilog. Two files and no frameworks: the FIFO module and a self-checking testbench. It includes:

Gray-code read and write pointers, passed across the clock boundary through two-flop synchronizers so the other side never sees a half-updated value
Full and empty flags that stay correct across the crossing (they can be a little conservative, but never wrong)
Parameterized data width and depth, defaulting to 8-bit data and 16 entries
A testbench that runs the write and read sides on two different clock periods, randomly stalls and bursts each side, forces the full and empty corner cases, and checks every value comes out exactly once and in order

📊 A focused digital-design exercise in clock-domain crossing, the problem behind every real FIFO that sits between two clock domains.

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

### 🏀 2026 March Madness ML Bracket Predictor

📌 A multi-model ensemble that predicts the full NCAA Tournament bracket from real efficiency data instead of gut picks, and ranks exactly which stat is driving each one.

Built in Python with scikit-learn: four independently-trained models vote on every matchup, features engineered from two decades of tournament history, and twelve full bracket variants generated from different model-weighting strategies. It includes:

- A 4-model ensemble (Gradient Boosting, Random Forest, Logistic Regression, Neural Network/MLP) cross-validated at 64.5–67.0% game-level accuracy, voting jointly on every matchup
- 28 engineered features per matchup across five research-backed tiers (efficiency, Dean Oliver's Four Factors, shooting profile, seed/conference context, champion-similarity), built from Barttorvik T-Rank data across all 365 D-I teams
- A training set spanning 40 tournaments (1985–2025) plus every NCAA champion's advanced-stat profile from 2002–2025, cross-referenced against KenPom/BPI/NET
- 12 distinct bracket variants generated by re-weighting the same four models toward different strategies (chalk/favorites, upset-hunting, defense-first, pure efficiency), each producing an independent champion pick
- An interactive HTML bracket visualization rendering all 12 variants' predictions and round-by-round win probabilities

📊 Feature-importance analysis surfaced Barthag (expected win %) as the single strongest predictor at 37.4% importance, and the data itself confirmed a real basketball prior: no champion since 2001 has entered the tournament outside the KenPom top 25.

🔗 Repo: https://github.com/joshwiersema/March-Madness-Model-2026 

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
