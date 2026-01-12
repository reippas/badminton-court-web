# 🏸 badminton-court-web

A minimal web app for badminton clubs featuring Skill-Based Matchmaking (SBMM) and fairness-weighted rotations.

Live App: https://reippas.github.io/badminton-court-web/

# Key Features

**Dashboard:** Manage players, matches, rankings, and history in one view.

**Fixed Teams:** Lock partners to ensure they always play on the same side.

**SBMM Tiering:** Automatically groups players by skill (Elite vs. Developing).

**Fairness Engine:** Prioritizes players based on rest time.

**Data Export:** LocalStorage persistence with JSON export.

# The Engine

## 1. Priority Weight ($W$)

Determines who plays next:


$$W = (RestCount \times 10,000) + Points$$


Resting is the primary priority; points break ties.

## 2. Court Tiers & Snake Pairing

Tiering: Top players are assigned to Court 1, next to Court 2.

Balancing: Doubles teams are "snaked" to ensure even matches:

Team A: Rank #1 + #4

Team B: Rank #2 + #3

## 3. Scoring

Win: $+3$ Pts

Rest: $+2$ Pts

Loss: $+1$ Pt

# Usage

Setup: Activate players from the pool.

Generate: Click to create balanced matches.

Score: Tap the winning team and click Register Results.

Built with HTML5, Tailwind CSS, and Vanilla JavaScript.
