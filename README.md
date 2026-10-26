# AI Model Arena

A single-file, zero-dependency data-visualization site for LLM benchmarks, built on the independent [Artificial Analysis](https://artificialanalysis.ai/) evaluation system (Intelligence Index v4.3.2). It gives you a full view of how **30 flagship models from 15 providers** compare on intelligence, speed, and cost. The new flagship **Claude Opus 5.5** tops the intelligence leaderboard at 58 points, with **Claude Sonnet 5.5** and Meta's **Muse Wonder Full** tied at 56 — while Xiaomi's **MiMo-V2.6-Pro** stands out at 46 points for just $0.13 per task.

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
- A dedicated color per provider (15 in total), linked across every chart on the site

## 📊 Data notes

- Source: Artificial Analysis Intelligence Index v4.3.2 (snapshot from Oct 26, 2026), which aggregates 10 benchmarks — AA-Briefcase v1.1, GDPval-AA v2.1, AutomationBench-AA, Terminal-Bench 4.0, SciCode, Humanity's Last Exam, GDP.pdf, CritPt, AA-Omniscience, and AA-LCR v1.1
- 1–4 flagship in-market models per provider; outdated, niche, and non-core models are excluded
- Speed / cost figures are shown only for models with officially published data; anything unpublished is marked `null` — nothing is made up
- Highlights of this snapshot: NVIDIA Nemotron 3.5 Super VL takes the speed crown at 458.8 t/s, followed by Claude Haiku 5.5 (234.2 t/s) and Step 5 Preview (220.2 t/s); the cheapest model is Xiaomi MiMo-V2.6-Flash ($0.06/task) and the most expensive is Claude Fable 5.1 ($7.63/task) — a 127× spread; the open-weights field is led by Kimi K3.1 Pro (55 points) and MiMo-V2.6-Pro (46 points / $0.13)
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
