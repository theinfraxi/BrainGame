
## 🧭 Improved Navigation Tree Blueprint

```text
📁 Dashboard (Main App Container)
 ├── 🏠 Home / Overview (Streak counter, daily quote)
 ├── ⚡ Daily Workout [LOCKED UNTIL EVALUATION]  <-- Highly recommended addition!
 ├── 📝 Baseline Evaluation (The initial/weekly full cognitive test)
 │
 ├── 🎮 Training Hub (Collapsible Dropdown Menu)
 │    ├── ⚡ Speed (6 Games)
 │    ├── 🎯 Attention (6 Games)
 │    ├── 💾 Memory (6 Games)
 │    └── 🧩 Reasoning (6 Games)
 │
 ├── 📊 Analytics & Insights (Cognitive breakdown graphs)
 ├── 🏆 Achievements & Badges (Milestone tracking)
 └── ⚙️ Settings & Local Data (Audio, clear localStorage data)

```

---

## 🚀 Why These Improvements Make the App Better

### 1. Separation of "Home" vs. "Daily Workout"

In your original concept, "Home" and "Dashboard" are somewhat redundant. By using **Home** as a passive landing page (showing streaks or levels), you can add a dedicated **Daily Workout** button. This button is what the *Recommendation Engine* intercepts to force users out of their comfort zone.

### 2. Collapsible "Training Hub"

Instead of letting the 4 categories take up a massive amount of vertical sidebar space at all times, make **Training** a toggleable dropdown menu. When clicked, it expands to reveal the 4 domains, keeping the layout clean.

### 3. Smart Status Badges (Visual Polish)

When you render this layout into HTML/CSS using Vite, add dynamic visual badges next to the text. For example:

| Navigation Item | Dynamic Badge Idea |
| --- | --- |
| **Home** | `🔥 5 Days` *(Shows their current daily streak)* |
| **Daily Workout** | `⚠️ Forced Task` *(Flashing indicator when a weak category is assigned)* |
| **Training $\rightarrow$ Speed** | `📈 Level 4` * (Shows domain ranking status)* |
| **Achievements** | `🔴 2 New` *(Appears when a new badge is unlocked but not yet viewed)* |

## Next Steps for Production

Since you are using a tool like **Vite**, you can easily build this sidebar component using flexbox or a CSS grid layout, utilizing icons (like Lucide Icons or FontAwesome) to represent the emojis shown in the tree layout above!
