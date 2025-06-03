# 🎮 Strategy Game Movement System

A modular, visual system for simulating unit movement in grid-based strategy games using Dijkstra’s algorithm.

This project is split into two parts:
- 🧠 A core algorithm module that calculates reachable tiles using Dijkstra’s algorithm
- 🕹️ An interactive browser-based tool that lets you experiment with terrain, movement range, and unit positioning

---

## 🕹️ Live Demo

Try the strategy game tool directly in your browser:

🔗 [**Live Demo**](https://quirkyqubits.github.io/strategy-game-tool/)

Explore how terrain affects movement range and see Dijkstra’s algorithm in action.

![demo](https://github.com/QuirkyQubits/strategy-game-djikstra-algorithm/blob/main/demo.png)

---

## 🧠 Core Algorithm Module

The logic for determining movement range is powered by a custom implementation of Dijkstra’s algorithm:

📂 [Dijkstra Algorithm Repository](https://github.com/QuirkyQubits/strategy-game-djikstra-algorithm)

This module:
- Models grid-based maps with variable terrain movement costs
- Computes all reachable tiles given a unit’s starting position and movement points
- Can be reused or extended for other turn-based game logic

---

## 💻 Source Code

- 🧠 [Dijkstra Algorithm (backend logic)](https://github.com/QuirkyQubits/strategy-game-djikstra-algorithm)
- 🕹️ [Frontend Tool (browser interface)](https://github.com/QuirkyQubits/strategy-game-tool)

---

## 🧾 Use Cases

This system is ideal for:
- Prototyping tactical game mechanics (Fire Emblem, Advance Wars, etc.)
- Teaching or learning pathfinding algorithms in a visual context
- Demonstrating modular game architecture

---

## 📚 Technical Breakdown

You can read a full breakdown of how the system works, including diagrams and usage details, in the accompanying GitBook:

📖 *Coming Soon* (optional link to GitBook here when it's ready)

---

## 🧑‍💻 Author

Jonathan Huang  
[quirkyqubits.dev@gmail.com](mailto:quirkyqubits.dev@gmail.com)  
