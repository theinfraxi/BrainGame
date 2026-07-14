# Overall Development Roadmap

```
Stage 1
Planning
        ↓
Stage 2
Development Environment
        ↓
Stage 3
Learn Required Technologies
        ↓
Stage 4
Create Project
        ↓
Stage 5
Create UI Framework
        ↓
Stage 6
Create Game Engine
        ↓
Stage 7
Develop Individual Games
        ↓
Stage 8
Analytics Engine
        ↓
Stage 9
Testing
        ↓
Stage 10
Deployment
```

We are only going to do **Stage 1–4** first.

---

# STEP 1 — Install the Required Software

## 1. Visual Studio Code

Download

[https://code.visualstudio.com/](https://code.visualstudio.com/)

This is where you'll write all your code.

---

## 2. Node.js (Very Important)

Download

[https://nodejs.org/](https://nodejs.org/)

Install the **LTS version**, **not Current**.

Example

```
Node.js LTS
v24.x.x
```

During installation

✔ Add to PATH

✔ Install npm

Leave everything else default.

---

## 3. Git

Download

[https://git-scm.com/](https://git-scm.com/)

Git allows version control.

Later you'll upload to GitHub.

---

## 4. Google Chrome

We'll use Chrome Developer Tools.

---

# STEP 2 — Verify Installation

Open Command Prompt

Type

```bash
node -v
```

Example

```
v24.2.0
```

Then

```bash
npm -v
```

Example

```
11.5.0
```

Then

```bash
git --version
```

Example

```
git version 2.50.0
```

If all three work,

You're ready.

---

# STEP 3 — Install VS Code Extensions

Open VS Code

Install these extensions.

### Essential

✔ ESLint

✔ Prettier

✔ Auto Rename Tag

✔ Path Intellisense

✔ Error Lens

✔ Material Icon Theme

✔ GitLens

---

### React

✔ ES7+ React Snippets

✔ JavaScript Booster

---

### Optional

✔ Thunder Client

✔ Live Server

(Useful for testing HTML.)

---

# STEP 4 — Learn the Technology Stack

Since you're a beginner, don't try to learn everything at once. Focus on what you'll actually use.

```
HTML

↓

CSS

↓

JavaScript

↓

React

↓

Tailwind CSS

↓

Local Storage

↓

Canvas Animation (optional)

↓

Git

↓

GitHub
```

---

## Required Skill Levels

### HTML

You should understand:

```
div

button

img

span

header

footer

section

article

forms
```

---

### CSS

Know:

```
Flexbox

Grid

Animation

Transition

Transform

Variables

Media Queries
```

---

### JavaScript

Must know:

```
Functions

Arrays

Objects

Loops

if

Events

setTimeout

setInterval

Arrow Functions

Promises (basic)
```

---

### React

Must know:

```
Component

Props

State

useState

useEffect

Conditional Rendering

Mapping Arrays
```

---

# STEP 5 — Create GitHub Account

[https://github.com](https://github.com)

Create repository

```
BrainGame
```

Keep it public.

---

# STEP 6 — Create Project Folder

Example

```
Documents

    Projects

        BrainGame
```

Inside

```
BrainGame

    README.md

    Documentation

    Assets

    BrainGame-App
```

Notice

The React project is NOT the root folder.

---

# STEP 7 — Create Documentation Folder

This is something students often skip, but it makes a huge difference.

```
Documentation

    Game Design Document

    UI Sketches

    Algorithms

    Flowcharts

    Wireframes

    Meeting Notes

    References
```

You'll thank yourself later.

---

# STEP 8 — Make the Game Design Document (GDD)

This is the "blueprint" of the entire application.

```
Brain Trainer

Version 1.0

----------------------------------

Dashboard

Training

Evaluation

Analytics

Settings

----------------------------------

24 Games

----------------------------------

Speed

Alphabet Soup

Flash Glance

Math Blitz

...

----------------------------------

Attention

Clockwise

...

----------------------------------

Memory

...

----------------------------------

Reasoning

...

----------------------------------

Achievements

Statistics

Recommendation Engine
```

This document should answer:

* What is the goal of each game?
* How is it played?
* How is it scored?
* How does difficulty increase?
* What skills does it train?

---

# STEP 9 — Draw the UI

Don't code yet.

Use

* Figma (recommended)
* Excalidraw
* Pen & paper

Sketch:

```
Dashboard

Sidebar

Statistics

Today's Recommendation

Daily Challenge

Continue Training
```

Then

```
Memory Page
```

Then

```
Speed Page
```

Then

```
Analytics
```

Then

```
Settings
```

Wireframes don't need colors yet—focus on layout and functionality.

---

# STEP 10 — Prepare Assets Folder

```
Assets

images

icons

music

fonts

animations

sound

logo
```

Later

```
icons

memory.png

speed.png

attention.png

reasoning.png
```

---

# STEP 11 — Create the React Project

Open Command Prompt

```bash
cd Documents/Projects/BrainGame
```

Create project

```bash
npm create vite@latest
```

Choose

```
React

JavaScript
```

Name

```
braingame-app
```

Install

```bash
cd braingame-app

npm install
```

Run

```bash
npm run dev
```

Browser opens

```
http://localhost:5173
```

Congratulations.

Your app is running.

---

# STEP 12 — Learn the Initial React Structure

You'll see something like:

```
braingame-app

public/

src/

App.jsx

main.jsx

index.css

package.json

vite.config.js
```

Understand the purpose of each file before modifying anything.

---

# STEP 13 — Create a Professional Folder Structure

Inside `src`, organize your project from the beginning.

```
src
│
├── assets/
│
├── components/
│   ├── common/
│   ├── layout/
│   ├── dashboard/
│   └── charts/
│
├── pages/
│   ├── Dashboard/
│   ├── Speed/
│   ├── Attention/
│   ├── Memory/
│   ├── Reasoning/
│   ├── Analytics/
│   └── Settings/
│
├── games/
│   ├── speed/
│   │   ├── AlphabetSoup/
│   │   ├── FlashGlance/
│   │   ├── MathBlitz/
│   │   ├── Symbolism/
│   │   ├── WordAcrobat/
│   │   └── Wordsmith/
│   │
│   ├── attention/
│   │   ├── Clockwise/
│   │   ├── ColorCraze/
│   │   ├── Parita/
│   │   ├── QuickSwitch/
│   │   ├── FormFever/
│   │   └── QuantumLeap/
│   │
│   ├── memory/
│   │   ├── ChainReaction/
│   │   ├── MemoMart/
│   │   ├── Memoflow/
│   │   ├── Turnabout/
│   │   ├── WordMemobox/
│   │   └── PathFinder/
│   │
│   └── reasoning/
│       ├── FormFusion/
│       ├── Formula/
│       ├── Solitaria/
│       ├── LogiLadder/
│       ├── Rotator/
│       └── TrailTracker/
│
├── hooks/
├── utils/
├── services/
├── context/
├── data/
├── styles/
└── App.jsx
```

This structure scales cleanly as the project grows.

---

# STEP 14 — Create a Development Milestone Plan

Rather than trying to build all 24 games at once, build the platform first.

| Phase | Goal                                                     |
| ----- | -------------------------------------------------------- |
| 1     | Environment setup and React project                      |
| 2     | UI design system (sidebar, navigation, cards, buttons)   |
| 3     | Dashboard and routing                                    |
| 4     | User profile and local storage                           |
| 5     | Scoring engine and analytics framework                   |
| 6     | Build one complete game (e.g., **Chain Reaction**)       |
| 7     | Refine the game engine and reusable components           |
| 8     | Add the remaining 23 games using the shared framework    |
| 9     | Comfort Zone Detector and Daily Workout Recommendation   |
| 10    | Final polish, animations, sound, testing, and deployment |

---

## My Recommendation

Because this is a **large-scale project with 24 games**, we should approach it like a real software development project. Instead of immediately coding, we'll first create the **software architecture**, **UI design system**, and **game framework**. Once those foundations are in place, each new game becomes much easier to implement and maintain.

This approach also makes the project suitable for a university final-year project or portfolio piece, with clean organization, reusable code, and room for future expansion.

