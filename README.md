# 🌀 Quantum Computing Hackathon 2025: Advanced Optimization & Network Routing

### 📌 Project Overview
This repository contains the core algorithms developed during the **III All-Russian Quantum Hackathon (Quant-NN)**. The project addresses high-complexity computational challenges by combining classical heuristics (inspired by quantum annealing) with advanced graph theory for telecommunication infrastructure.

---

### 🚀 Key Components

#### 1. High-Performance QUBO Solver (`task1_solver.py`)
* **Problem:** Finding the minimum energy state for **QUBO (Quadratic Unconstrained Binary Optimization)** problems: $E(x) = x^T Q x$.
* **Solution:** A custom-built **Simulated Annealing** algorithm designed for high-speed execution.
* **Technical Highlights:**
    * **Time-Critical Logic:** Implemented a dynamic loop that ensures the best possible solution is returned within a strict **9.5-second** window.
    * **Sparse Data Handling:** Integrated `scipy.sparse` (CSR format) to efficiently process large-scale matrices, significantly reducing memory overhead.
    * **Adaptive Hyperparameters:** The solver automatically scales temperature ($T_0$, $\alpha$) and relaxation parameters based on the problem size ($N \le 1000$ to $N > 5000$).
    * **Hybrid Escape Mechanism:** Uses continuous relaxation with sigmoid activation to help the algorithm jump out of local minima.



#### 2. RWA: Optical Network Optimizer (`task2_rwa.py`)
* **Problem:** Solving the **Routing and Wavelength Assignment (RWA)** problem to ensure survivability in all-optical WDM networks.
* **Solution:** A greedy **BFS-based pathfinding algorithm** that calculates optimal primary and link-disjoint backup paths.
* **Technical Highlights:**
    * **Survivable Routing:** Guarantees a backup path for every request that shares zero physical links with the primary path.
    * **Wavelength Continuity:** Ensures the same wavelength is used across the entire path while strictly avoiding spectral clashing on shared links.
    * **Quantum Readiness:** The solution is architected for submission to the **QBoard CloudOS** quantum simulation platform.



---

### 🛠 Tech Stack
* **Language:** Python 3.10+
* **Libraries:** `NumPy` (Vectorized math), `SciPy` (Sparse matrices), `Collections` (Optimized queues).
* **Target Platforms:** Local simulation & QBoard Quantum Cloud.

### 📈 Results & Impact
* Successfully implemented a functional RWA solver that handles complex request lists with 100% path disjointedness.
* Developed a competitive QUBO solver capable of processing thousands of variables within rigorous competition time limits.

---
*Developed as part of the III All-Russian Quantum Hackathon.*
