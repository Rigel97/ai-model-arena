# AI Model Arena

A single-file, zero-dependency data-visualization site for LLM benchmarks, built on the independent [Artificial Analysis](https://artificialanalysis.ai/) evaluation system (Intelligence Index v4.3). It gives you a full view of how **30 representative models from 17 providers** compare on intelligence, speed, and cost. The new flagship **GPT-6 Astra** lands straight at the top of the intelligence leaderboard, tied with **Claude Fable 5.1** at 53 points — but at only 43% of the latter's per-task cost.

🌐 **Live site**: <https://rigel97.github.io/ai-model-arena/>

## ✨ Features

- **Intelligence Index leaderboard** — a 3D tilted podium for the top three (with a parallax effect on hover); the full ranking as gradient bars with a shimmer-sweep animation
- **Generation speed chart** — tokens-per-second comparison
- **Per-task cost chart** — weighted average cost per Intelligence Index task (USD)
- **Value-for-money quadrant** — a hand-drawn Canvas scatter plot of intelligence × cost (log scale), where bubble size encodes speed; the Pareto frontier is drawn automatically, and hovering shows details
- **Head-to-head 1v1** — pick any two models for a three-axis radar comparison (intelligence / speed / cost efficiency), with overall-power weights that switch by task scenario:
  - Balanced general use (intelligence 40% · speed 25% · cost 35%)
  - Everyday chat (intelligence 20% · speed 40% · cost 40%)
  - Large-scale engineering (intelligence 65% · speed 10% · cost 25%)
  - Research projects (intelligence 90% · speed 5% · cost 5%)

## 🎨 Visual effects

- Full-screen interactive particle-network background (particles are pushed away as the cursor approaches)
- Floating nebula glows, a cursor-following halo, and a tech-grid overlay
- Scroll-triggered reveal animations, rolling number counters, staggered bar-chart growth
- A dedicated color per provider (17 in total), linked across every chart on the site

## 📊 Data notes

- Source: Artificial Analysis Intelligence Index v4.3 (snapshot from Sep 9, 2026), which aggregates 10 benchmarks — AA-Briefcase, GDPval-AA v2, AutomationBench-AA, Terminal-Bench v4.0, SciCode, Humanity's Last Exam, GDP.pdf, CritPt, AA-Omniscience, and AA-LCR v1.1
- 1–4 representative models per provider; overly niche and low-intelligence models are excluded
- Speed / cost figures are shown only for models with officially published data; anything unpublished is marked `null` — nothing is made up
- Highlights of this snapshot: Gemini 3.5 Flash-Lite keeps the speed crown at 356 t/s, with InclusionAI Ling 3.0 Flash (298 t/s) entering the top three for the first time; the cheapest model is Xiaomi MiMo-V2.5-Pro ($0.05/task) and the most expensive is Claude Fable 5 ($8.75/task) — a 175× spread
- "Overall power" is this site's own weighted score (not an official metric); the weights change with the task scenario

## 🚀 Run locally

No build step whatsoever — just open it in a browser:

```bash
open index.html        # macOS
# or simply double-click index.html
```

## 🛠 Tech stack

A single file of plain HTML / CSS / JavaScript — no frameworks, no build dependencies. Every chart is hand-drawn on Canvas (scatter, radar, particle background); fonts load from the Google Fonts CDN (with automatic system-font fallback offline).

## 📁 Project structure

```
ai-model-arena/
└── index.html    # all page structure, styles, and logic
```

## ⚠️ Disclaimer

This page is a data-visualization demo. All scores are third-party independent results from Artificial Analysis and are for reference only.
