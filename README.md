# 🃏 Memory Match

Lightweight, beginner-friendly **Memory Match** built with **HTML, CSS, and JavaScript**.

Teach DOM manipulation, basic state handling, and event-driven logic.

---

## 🧰 Tools & Setup

**You’ll Need:**
- **VS Code** (recommended editor)
  - Extension: `Live Server` (for instant browser preview)
  - Optional: `Prettier` (auto-formatting)
- **Modern Browser:** Chrome, Edge, or Firefox

**Project Folder Structure**
```
memory-match/
├── index.html
├── style.css
├── app.js
└── assets/   # optional (if you use images instead of emoji)
```

**Run It**
1. **Download or Clone**
   ```bash
   git clone https://github.com/ALopez90/Cycle19-Lesson-MemoryMatch.git
   ```

2. **Open in VS Code** → Right-click `index.html` → “Open with Live Server”

3. The app should open automatically in your browser at something like:
   ```
   http://127.0.0.1:5500/
   ```

---

## How It Works

- **Data:** an array of 6 emojis duplicated into 12 cards.
- **Shuffle:** Fisher–Yates algorithm randomizes card order each game.
- **Render:** JS dynamically creates `<button>` cards and attaches click events.
- **State:** tracks `firstCard`, `secondCard`, `lockBoard`, `turns`, and `matches`.
- **Logic Flow:**
  1. First flip → store reference.
  2. Second flip → compare icons.
  3. Match → lock as “matched”.
  4. No match → briefly lock board, then unflip both.

---

## Mini Quizzes

**Q1:** Why do we duplicate the emoji array before shuffling?
**Q2:** What does `lockBoard` prevent during the flip delay?
**Q3:** What’s the difference between `textContent` and `innerHTML`?
**Q4:** How could you add difficulty levels without breaking existing logic?

---

## Challenges

1) **Dynamic Row Handling** — Add another row of cards!
2) **Image Handling** — Create a new directory called "assets" to use image files instead of hardcoded icons
3) **Difficulty Modes** — Add difficulty levels (more cards or time limits)
4) **Scoreboard** — Include a timer and “best score” using `localStorage`
6) **Accessibility** — Add theme switching (emoji → image mode)
7) **UI/UX Improvement** — Display a small **confetti effect** on win
8) **UI/UX Improvement and Accessibility**  — Add sound effects for flips or matches

---

## 🧯 Troubleshooting

| Symptom | Likely Fix |
|----------|-------------|
| Cards won’t flip | Check `.card` gets `.flipped` and `.card-inner` rotates via CSS |
| Matches never trigger | Compare `firstCard.dataset.icon === secondCard.dataset.icon` |
| Win never shows | Increment `matches` properly and check `matches === icons.length` |
| All cards identical | Confirm shuffle runs before rendering (`deck = shuffle([...icons,...icons])`) |
