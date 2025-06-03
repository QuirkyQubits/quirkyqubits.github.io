# 🎮 Strategy Game Movement System

A two-part project designed to support rapid prototyping and simulation for grid-based strategy games.

This system combines:
- 🛠️ A browser-based **Strategy Game Level Creator** for fast map design and iteration
- 🧠 A C# console-based simulation engine for turn-based movement and combat logic

---

## 🧩 About the Projects

This system includes two modular tools, designed to work independently or together:

---

### 🛠️ Strategy Game Level Creator (Frontend)

A browser-based visual editor that functions like **MS Paint for strategy game levels**. It lets you:

- 🎨 Draw grid-based maps using your mouse, assigning different terrain types  
- 💾 Export maps as JSON for use in game engines or backend simulations  
- 📂 Re-import saved maps to continue editing or testing later  
- ⚡ Rapidly prototype level layouts and iterate on terrain balance and map feel  

#### 🖼️ Example Usage

![Demo Preview](./demo.png)

👉 **Try it here!** → [Strategy Game Level Creator](https://quirkyqubits.github.io/strategy-game-tool/)

---

### 🧠 Turn-Based Simulation Engine (Backend)

A C# console application that:

- Loads exported maps from the Level Creator  
- Simulates unit movement and combat using **a shortest-path algorithm that accounts for terrain cost and movement range**  
- Resolves victory conditions based on terrain and unit data  

The backend focuses on core **game logic and mechanics**, and is designed to serve as a foundation for integration with Unity, Unreal, or any game framework.

---

## 📂 Source Code

- 🛠️ [Strategy Game Level Creator (JavaScript)](https://github.com/QuirkyQubits/strategy-game-tool)  
- 🧠 [Backend Simulation + Logic (C#)](https://github.com/QuirkyQubits/strategy-game-djikstra-algorithm)  

Each repo includes documentation, code samples, and usage instructions.
