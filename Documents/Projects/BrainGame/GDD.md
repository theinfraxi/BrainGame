# 📄 GAME DESIGN DOCUMENT: BRAIN TRAINER

**Project Name:** Brain Trainer

**Version:** 1.0

**Target Platform:** Web / HTML5 (Browser-based)

**Monetization & Ads:** 100% Free, Zero Ads

---

## 1. Executive Summary & Core Concept

**Brain Trainer** is a self-contained web application designed to combat cognitive stagnation ("brain rotting"), push users out of their daily comfort zones, and systematically unlock full mental potential.

Unlike traditional brain games that let users stick to what they are already good at, this game actively tracks player performance to detect their "Comfort Zone Trap." It then challenges them to face their weakest cognitive areas through an intelligent recommendation engine.

---

## 2. Interface & Architecture

The entire application operates as a single-page dashboard with clean sidebar navigation:

* **Dashboard:** The central hub. Displays the current daily streak, a prominent "Start Daily Workout" button, and a quick summary of recent scores.
* **Training Hub:** The master directory listing all 4 core cognitive categories and their respective games. All games are unlocked and playable for free from day one.
* **Evaluation Zone:** A specialized assessment mode that tests the player across all four domains in a single session to establish or update their cognitive baseline.
* **Analytics Panel:** Visualizes player progression using local graphs tracking Reaction Time (ms), Score Milestones, and Memory Accuracy.
* **Achievements:** A collection of unlockable badges highlighting cognitive milestones and moments where the user broke out of their comfort zone.
* **Settings:** Allows toggling sound effects, clearing local progress, and resetting data stored in the browser's `localStorage`.

---

## 3. The 24-Game Matrix

### ⚡ SPEED SECTION

*Focus: Enhancing information processing speed, visual scanning, and rapid muscle-memory response under pressure.*

1. **Alphabet Soup:** Letters are scattered randomly across a dynamic canvas. The player must locate and click them in alphabetical order ($A \rightarrow Z$) before a strict countdown timer hits zero.
2. **Flash Glance:** A chaotic cluster of shapes flashes on the screen for a mere 400 milliseconds. The player must instantly declare how many specific target items (e.g., green triangles) were displayed.
3. **Math Blitz:** Rapid-fire, basic arithmetic equations appear one after the other. The player must click True or False within a 1.5-second window per equation.
4. **Symbolism:** A master symbol is displayed at the top. A rapid conveyor belt of symbols moves across the bottom. The player must click whenever a matching symbol passes the target zone.
5. **Word Acrobat:** Words are displayed completely scrambled or upside down. The player must quickly type the correct word structure before the timer runs out.
6. **Wordsmith:** A 3x3 grid of letters appears alongside a clue. The player must swipe or click letters at high speed to spell out the target word before it vanishes.

---

### 🎯 ATTENTION SECTION

*Focus: Strengthening selective attention, focus sustainability, and the ability to ignore distracting secondary stimuli.*

1. **Clockwise:** Multiple analog clock faces spin at varying speeds. The player must click exactly when the clock hands cross a specific hour marker, requiring precise timing and divided focus.
2. **Color Craze:** A text color game based on cognitive interference. The word "BLUE" might be colored red; the game rapidly switches instructions between "Click the Word" and "Click the Color."
3. **Parita:** A continuous stream of pairs appears. The player must determine if the current pair matches the attributes (color, shape, or size) of the pair shown immediately before it, ignoring background color shifts.
4. **Quick Switch:** The screen splits into two distinct mini-tasks (e.g., sorting numbers on the left, sorting shapes on the right). The game forces the user to switch active tasks every few seconds without losing momentum.
5. **Form Fever:** A chaotic screen filled with moving shapes. The player must track a single "target shape" as it shifts colors, sizes, and blends into a dense crowd of moving decoy shapes.
6. **Quantum Leap:** A grid of nodes where a particle moves. The player must anticipate the particle's destination while dealing with random visual distortions and temporary grid blackouts.

---

### 💾 MEMORY SECTION

*Focus: Expanding working memory capacity, spatial recall, and short-term information retrieval.*

1. **Chain Reaction:** A sequence of buttons lights up on a panel accompanied by distinct tones. The player must perfectly replicate the sequence, which grows by one extra step with every successful round.
2. **Memo Mart:** A virtual shopping list of items is shown for 5 seconds. The player enters a store layout and must collect the exact items from the list from memory, dealing with changing store layouts.
3. **Memoflow:** An array of cards is revealed briefly and hidden. The cards don't just require classic matching; they form a sequential narrative or numerical flow that must be uncovered in precise order.
4. **Turnabout:** A spatial memory test. A pattern of blocks is displayed on a grid. The grid then closes, rotates 90 or 180 degrees, and the player must mark where the original blocks are located relative to the new orientation.
5. **Word Memobox:** A box displays a string of random words. The words vanish, and a new list appears. The user must identify which words are carry-overs from the previous box and which ones are entirely new.
6. **Path Finder:** A grid momentarily shows a safe pathway across a dangerous maze. The path disappears, and the player must navigate the avatar from start to finish entirely from structural memory.

---

### 🧩 REASONING SECTION

*Focus: Developing logical deduction, problem-solving, pattern recognition, and structural analysis.*

1. **Form Fusion:** The player is given two complex geometric wireframes and must mentally overlay or merge them to select the correct combined 3D shape from a multiple-choice list.
2. **Formula:** A math-logic puzzle. An equation balance sheet is presented with missing operators ($+, -, \times, \div$) or blank spaces. The player must place the right operators to make the final logic statement true.
3. **Solitaria:** A deductive puzzle where shapes must be sorted according to complex, hidden rules that the player must discover through trial and error (e.g., *stars cannot touch circles, green items must stay on the border*).
4. **Logiladder:** A word or number ladder puzzle where the player must figure out the underlying pattern of transformation to fill in the missing steps between the bottom and the top of the ladder.
5. **Rotator:** A gear and interlocking mechanics puzzle. The player is shown a series of connected cogs and must deduce which direction the final cog will rotate when the primary drive wheel turns clockwise.
6. **Trail Tracker:** A complex network of paths, intersections, and nodes. The player must use logical deduction to trace inputs to outputs under specific constraints, finding the only viable loop through the maze.

---

## 4. Systems & Data Logic

### The Evaluation & Suggestion Engine

To avoid requiring a backend server or external database, all performance metrics are calculated directly via client-side JavaScript and saved using `localStorage`.

* **Metrics Tracked:** For every single game session, the app logs the **Raw Score**, **Accuracy Percentage**, and **Average Reaction Time (ms)**.
* **The Comfort Zone Algorithm:** The engine aggregates performance data every 24 hours. If a player shows high engagement and high scores in *Speed* but low engagement or failing scores in *Reasoning*, the algorithm flags *Reasoning* as the user's **"Comfort Zone Trap."**
* **Dynamic Recommendations:** The main dashboard uses this flag to update the "Daily Workout." It will deliberately restrict access to the user's favorite category for the first game of the day, forcing them to play the flagged underperforming category to break their cognitive loop.

---

## 5. Technical Stack (Zero-Budget Specification)

* **Architecture:** Static Web Application (HTML5, CSS3, Vanilla JavaScript or lightweight frontend components).
* **Hosting Deployment:** Free distribution via **Itch.io** (as an interactive browser zip bundle) or hosted globally on **GitHub Pages**.
* **Asset Sourcing:** All visual assets, UI icons, and audio components utilize **CC0 (Public Domain)** assets sourced from creators like Kenney.nl or OpenGameArt.org to ensure zero asset overhead costs.
