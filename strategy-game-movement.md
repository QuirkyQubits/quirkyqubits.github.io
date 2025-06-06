# 🎮 Strategy Game Movement System

A two-part project designed to support rapid prototyping and simulation for grid-based strategy games.

This system combines:
- 🛠️ A browser-based **Strategy Game Level Creator** for fast map design and iteration
- 🧠 A C# console-based simulation engine for turn-based movement and combat logic

---

## 🧩 Overview

Designing levels for grid-based strategy games is often slow and fragmented - game designers may need to manually define tile maps, terrain types, and unit logic using engine-specific tools or handwritten data formats. This makes it harder to iterate on what "feels fun" during early development.

To bridge this gap, I built a two-part system:

- A **visual Level Creator**, allowing designers to quickly sketch out maps, assign terrain, and export them in a structured JSON format.
- A **minimal C# reference implementation**, which consumes that JSON to simulate movement and combat, demonstrating how the exported data can be used by a game engine or AI-powered translation workflow.

The C# implementation includes a clean, modular Dijkstra pathfinding algorithm that can be easily:
- Copied directly into engines like Unity
- Translated into other languages (e.g. JavaScript, C++, Rust) using LLMs or developer tooling

Together, these tools help speed up the early design loop: from **initial level design → prototype → test**. By decoupling level creation from engine constraints, this system gives teams a flexible, engine-agnostic foundation to build on - whether they're using Unity, Unreal, or something custom.

---

### 🛠️ Strategy Game Level Creator (Frontend)

A browser-based visual editor that functions like **MS Paint for strategy game levels**. It lets you:

- 🎨 Draw grid-based maps using your mouse, assigning different terrain types  
- 💾 Export maps as JSON for use in game engines or backend simulations  
- 📂 Re-import saved maps to continue editing or testing later  
- ⚡ Rapidly prototype level layouts and iterate on terrain balance and map feel  

#### 🖼️ Example Usage

![Demo Preview](/portfolio/strategy-game-tool-demo.png)

👉 **Try it here!** → [Strategy Game Level Creator](https://quirkyqubits.github.io/strategy-game-tool/)

---

### 🧠 Turn-Based Simulation Engine (Backend)

A C# console application that:

- Loads exported maps from the Level Creator  
- Simulates unit movement and combat using **a shortest-path algorithm that accounts for terrain cost and movement range**  
- Resolves victory conditions based on terrain and unit data  

The backend focuses on core **game logic and mechanics**, and is designed to serve as a foundation for integration with Unity, Unreal, or any game framework. For more details, please see the [README on GitHub](https://github.com/QuirkyQubits/strategy-game-dijkstra-algorithm).

---

## 📂 Source Code

- 🛠️ [Strategy Game Level Creator (JavaScript)](https://github.com/QuirkyQubits/strategy-game-tool)  
- 🧠 [Backend Simulation + Logic (C#)](https://github.com/QuirkyQubits/strategy-game-dijkstra-algorithm)  

Each repo includes documentation, code samples, and usage instructions.
