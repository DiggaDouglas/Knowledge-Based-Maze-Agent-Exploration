# Knowledge-Based Maze Agent Exploration

## Description

This project implements a Knowledge-Based Agent (KBA) that navigates a 4×4 maze environment, demonstrating foundational principles of Artificial Intelligence knowledge representation and reasoning.

The notebook simulates an intelligent agent exploring a maze by:
- Representing the environment as a grid (0 = free path, 1 = wall)
- Building a Knowledge Base (KB) that stores logical facts about the world
- Dynamically updating knowledge as the agent perceives and moves through the maze

## 🧠 Core Concepts

The agent’s knowledge evolves through two key mechanisms:

### Visited Facts
Each time the agent moves to a new cell `(x, y)`, it records:
```
Visited(x, y)
```
This allows the agent to remember explored areas and avoid redundancy.

### NextToWall Facts
The agent checks surrounding cells for walls and adds facts such as:
```
NextToWall(x, y)
```
indicating proximity to obstacles — crucial for reasoning about safe moves.

## 🚀 Functional Highlights

- **Dynamic Fact Learning:** The agent continuously updates and prints newly learned facts as it moves.
- **Knowledge Base Summary:** Displays total facts learned during exploration (e.g., 47 facts).
- **Decision Logic:** Movement decisions are made using the `can_move()` function, which checks both logical and spatial constraints.
- **Visualization:** The `show_maze()` function visually displays the maze, marking:
  - `A` → Agent’s current position
  - `G` → Goal position
  - `#` → Walls

## 🧩 Learning Outcomes

Through this lab, the notebook demonstrates how:
- An agent can represent its world symbolically
- Logical facts can be used to drive movement decisions
- Perception and reasoning interact in building adaptive intelligence

## 🏁 Results


## ⚙️ Setup & Installation

To run this notebook on your own machine, follow these steps:

### 1. Install Python
Ensure you have Python 3.8 or newer installed. You can download it from [python.org](https://www.python.org/downloads/).

### 2. Install Required Packages
Open a terminal and run:
```bash
pip install numpy matplotlib
```

### 3. Run the Notebook
You can use Jupyter Notebook or VS Code:

- **Jupyter Notebook:**
  - Install Jupyter: `pip install notebook`
  - Start Jupyter: `jupyter notebook`
  - Open `Agent exploration.ipynb` and run all cells.

- **VS Code:**
  - Open the folder in VS Code
  - Install the Python and Jupyter extensions if prompted
  - Open `Agent exploration.ipynb` and run all cells

---
By the end of execution:
- The agent explores multiple valid moves using its knowledge base
- It successfully adds both Visited and NextToWall facts
- If unable to reach the goal, it identifies being stuck based on logical reasoning — mimicking real-world AI limitations
