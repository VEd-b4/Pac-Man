# 🎮 Pac-Man Console Game – Open Source Project Analysis

**Authors:**

- Ved Bhoraniya: 202401242  
- Sukun Dalal: 202401217  
- Tanishk Dhawan: 202401224  
- Uma Sainitin Burra: 202401487  

---

## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Key Questions & Findings](#key-questions--findings)
- [Conclusion](#conclusion)
- [Repository Link](#repository-link)

---

## 📌 Project Overview

This project is a C++ implementation of the classic Pac-Man game, designed to run entirely within the command-line interface (CMD) without any external graphics libraries. The game features ASCII-based rendering, real-time user input, basic AI-driven ghost movement, and a simple scoring system with persistent leaderboard functionality.

GitHub Repo: [Farid-Karimi/Pac-Man](https://github.com/Farid-Karimi/Pac-Man)

---

## 🎯 Objectives

- Clone and understand the structure and logic of the open source project.
- Analyze code using modern LLM tools to identify design patterns and improvements.
- Investigate possible bugs and propose or contribute fixes.
- Present findings through a structured set of questions and answers.

---

## ❓ Key Questions & Findings

### 1. What is the primary goal and scope of this open source project?
**Answer:**  
The project replicates Pac-Man using ASCII graphics in C++ for CMD. It demonstrates real-time gameplay mechanics without graphical libraries, focusing on game logic and system-level control.

---

### 2. How is the game logic architected in code, and what are the key modules?
**Answer:**  
Key modules include:
- Map rendering and storage
- Player movement via `getch()`
- Ghost AI (using BFS)
- Scoring and file-based high score persistence
- Main game loop handling logic and collisions

---

### 3. How is real-time interactivity achieved in a command-line environment?
**Answer:**  
Using `getch()` for non-blocking input, and `gotoxy()` to control cursor position. Only necessary parts of the screen are updated to simulate real-time animation and avoid flicker.

---

### 4. What data structures and algorithms are used?
**Answer:**  
- 2D arrays for map representation  
- BFS for ghost pathfinding  
- Basic file I/O for high score storage and retrieval  

---

### 5. What issues or bugs are present in the current code?
**Answer:**  
- No framerate control (speed varies per device)  
- Ghosts may overlap or behave inconsistently  
- Collision issues near borders  
A bug fix PR was considered for ghost resetting logic.

---

### 6. What design or gameplay improvements could be proposed?
**Answer:**  
- Add levels and increasing difficulty  
- Use OOP for better code structure  
- Implement smoother movement using timers  
- Add configurable controls

---

### 7. How is the maze structure printed and updated on the screen?
**Answer:**  
The maze is a 2D char array rendered with ASCII. It’s printed using nested loops and `gotoxy()` for positioning, which updates only affected characters, reducing flicker.

---

### 8. Where and how are player names and high scores stored?
**Answer:**  
Stored in a file (`highscore.txt`) using standard file I/O. Names and scores are read at startup and written post-game, enabling a persistent leaderboard.

---

### 9. What methods are used to prevent screen flicker during rendering?
**Answer:**  
Only modified screen regions are redrawn using `gotoxy()`. Full screen clearing is avoided, keeping transitions smooth in the console.

---

### 10. How does the game handle invalid or unexpected user inputs?
**Answer:**  
Non-directional key inputs are ignored using `getch()` filtering. This avoids undefined behavior or crashes due to unexpected keypresses.

---

### 11. What are the limitations of using file-based storage for score tracking?
**Answer:**  
File I/O is simple but not scalable or secure. Data corruption, lack of concurrency support, and minimal formatting (plain text) are key drawbacks.

---

## 🧠 Conclusion

The Pac-Man console game demonstrates solid foundational game design using C++ for CLI. While technically limited, it's impressive for its scope, making it ideal for system programming and educational demonstrations. With a few improvements and better modular design, it could be a robust retro gaming demo.

---

## 🔗 Repository Link

[https://github.com/Farid-Karimi/Pac-Man](https://github.com/Farid-Karimi/Pac-Man)
