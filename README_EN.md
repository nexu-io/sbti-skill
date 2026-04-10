# 🧠 SBTI Cyber Personality Test Skill

> *"Congratulations, you've unlocked the rarest personality in all of China"*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![nexu](https://img.shields.io/badge/nexu-Skill-blueviolet)](https://github.com/nexu-io/nexu)

<br/>

The most viral personality test on the Chinese internet, now playable inside your AI agent.

30 questions, 15 dimensions, 27 personality types — test yourself, or test your AI 🦞

<br/>

[Install](#install) · [How to Play](#how-to-play) · [27 Personalities](#27-personalities) · [How It Works](#how-it-works) · [中文](README.md)

<br/>

---

> 🧠 **SBTI** is part of the [nexu](https://github.com/nexu-io/nexu) ecosystem — the open-source OpenClaw desktop client.

---

## What You Get

| Output | Description |
|--------|-------------|
| 🏷️ **Personality Code** | 27 absurd-but-accurate codes like CTRL, BOSS, SEXY, DEAD |
| 📊 **15-Dimension Radar** | 5 models × 3 dimensions, visualized with progress bars |
| 💬 **Opening Line** | A soul-crushing one-liner unique to your personality |
| 📖 **Deep Reading** | 200-300 word roast-style personality description |
| 🏆 **Top 3 Matches** | Your closest 3 personality types with match percentages |
| 🍺 **Hidden Easter Egg** | Trigger conditions classified. Involves baijiu in a thermos... |
| 🌐 **Shareable Landing Page** | One-click deploy to nexu.space, get a link to share |

---

## 27 Personalities

### 25 Standard Personalities

| # | Code | Name | One-liner |
|---|------|------|-----------|
| 1 | **CTRL** | The Controller | Got you right where I want you. |
| 2 | **ATM-er** | The Giver | You think I'm made of money? |
| 3 | **Dior-s** | The Underdog | Just wait for my comeback. |
| 4 | **BOSS** | The Leader | Give me the wheel. I'll drive. |
| 5 | **THAN-K** | The Grateful | I thank the heavens! I thank the earth! |
| 6 | **OH-NO** | The Worrier | Oh no! How am I this personality?! |
| 7 | **GOGO** | The Doer | Go go go~ Let's move! |
| 8 | **SEXY** | The Charmer | You are a natural-born stunner! |
| 9 | **LOVE-R** | The Romantic | Too much love, reality feels barren. |
| 10 | **MUM** | The Caretaker | Can I... call you mom? |
| 11 | **FAKE** | The Shapeshifter | There are no real humans left. |
| 12 | **OJBK** | The Whatever | When I say whatever, I mean it. |
| 13 | **MALO** | The Monkey | Life's a dungeon, and I'm just a monkey. |
| 14 | **JOKE-R** | The Clown | Turns out we're all clowns. |
| 15 | **WOC!** | The Reactor | WTF, how is this my personality? |
| 16 | **THIN-K** | The Thinker | Deep thinking for 100 seconds... |
| 17 | **SHIT** | The Cynic | This world is a pile of... |
| 18 | **ZZZZ** | The Hibernator | I'm not dead, just sleeping. |
| 19 | **POOR** | The Focused | I'm broke, but I'm specialized. |
| 20 | **MONK** | The Ascetic | No worldly desires here. |
| 21 | **IMSB** | The Self-Doubter | Am I really... an idiot? |
| 22 | **SOLO** | The Lone Wolf | I'm crying. How am I an orphan? |
| 23 | **FUCK** | The Rebel | F***! What kind of personality is this? |
| 24 | **DEAD** | The Void | Am I... still alive? |
| 25 | **IMFW** | The Fragile | Am I really... useless? |

### 2 Special Personalities

| # | Code | Name | Trigger |
|---|------|------|---------|
| 26 | **HHHH** | The Giggler | All matches < 60%, system fallback |
| 27 | **DRUNK** | The Drinker | Hidden easter egg (author's way of telling a friend to quit drinking) |

---

## Install

### nexu (Recommended)

Send the GitHub link to your nexu agent:

```
Install this skill: https://github.com/nexu-io/sbti-skill
```

### Manual

```bash
git clone https://github.com/nexu-io/sbti-skill <your agent skills directory>
```

No dependencies — pure prompt skill, ready to use.

---

## How to Play

### 🧑 Test Yourself

Tell your agent:

```
Take the SBTI test
```

The agent will ask 30 questions one by one. Pick A/B/C for each. Results auto-calculated at the end.

### 🦞 Test Your Agent

```
Give my AI agent the SBTI test
```

The agent answers all 30 questions from its own AI perspective, then reveals its cyber personality.

---

## How It Works

```
30 questions → Dimension scoring → Level conversion → Personality matching → Results
                                          ↓
                                  Compare against 25 patterns
                                          ↓
                                  Similarity ranking → Your type 🎯
```

### 5 Models × 15 Dimensions

| Model | Dimensions | Measures |
|-------|-----------|----------|
| **Self (S)** | S1 Self-esteem · S2 Self-clarity · S3 Core values | How you see yourself |
| **Emotion (E)** | E1 Attachment · E2 Emotional depth · E3 Boundaries | How you love |
| **Attitude (A)** | A1 Worldview · A2 Rules flexibility · A3 Life meaning | How you see the world |
| **Action (Ac)** | Ac1 Motivation · Ac2 Decision style · Ac3 Execution | How you act |
| **Social (So)** | So1 Social initiative · So2 Interpersonal boundaries · So3 Authenticity | How you connect |

### Matching Algorithm

1. 2 questions per dimension × 1-3 points → Total 2-6
2. Convert to level: 2-3=**L**, 4=**M**, 5-6=**H**
3. Generate 15-char level code (e.g. `HHL-HMH-MMH-HHM-LHH`)
4. Manhattan distance against all 25 personality patterns
5. Similarity = (1 - distance/30) × 100%
6. Highest match wins; < 60% → fallback to HHHH

---

## Project Structure

```
sbti-skill/
├── SKILL.md              # Agent Skill entry point
├── README.md             # Chinese docs
├── README_EN.md          # English docs
├── LICENSE               # MIT License
├── deploy/               # Deploy channel (nexu.space)
│   ├── deploy_skill.js
│   └── deploy_skill_core.js
├── templates/
│   └── sbti-result/
│       └── template.html # Result page HTML template
└── references/
    ├── personalities.md  # All 27 personality profiles
    └── questions.md      # All 30 + 2 questions with scoring
```

---

## Credits

SBTI was originally created by a Bilibili creator:

- Original test: https://sbti.unun.dev/
- Creator: https://space.bilibili.com/417038183
- Video: https://www.bilibili.com/video/BV1LpDHByET6/

This Skill adapts the publicly available test rules into an AI Agent-interactive format.

---

## Contributing

PRs welcome! You can contribute:
- 🧠 New personality types (need full dimension pattern + description)
- 🌐 Translations
- 🎨 Result display improvements
- 🐛 Matching algorithm fixes

---

<br/>

MIT License © [nexu](https://github.com/nexu-io)

Made with 🧠 by [nexu](https://github.com/nexu-io/nexu)

**Find out what cyber personality your AI has 🦞**

⭐ [Star this repo](https://github.com/nexu-io/sbti-skill) · ⭐ [Star nexu](https://github.com/nexu-io/nexu)

<br/>
