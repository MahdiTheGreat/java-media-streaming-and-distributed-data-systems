# Java Algorithmic Suite & Domain Models

Object-oriented implementations in Java, encompassing transactional retail store modeling, matrix linear algebra solvers, and discrete proximity grid evaluators.

---

## Directory Architecture

```
projects/SimpleProjects/
├── InternetShop.java      # Transactional retail inventory and accounting engine
├── matrixCalculator.java  # Core matrix linear algebra evaluator with dimensional error handling
└── mineGame.java          # Proximity matrix generator for discrete grid mine detection
```

---

## System Overviews

### 1. Retail Transaction & Order Management (`InternetShop.java`)
- Object-oriented retail inventory model tracking customer profiles, product SKUs, warehouse repositories, discount matrices, and aggregate revenue.
- Maintains fast $\mathcal{O}(1)$ lookup across entities via hash mappings while maintaining order history logs.

### 2. Matrix Linear Algebra Evaluator (`matrixCalculator.java`)
- Encapsulates discrete linear algebra operations within a dedicated `Matrix` data structure.
- Implements arithmetic addition, element-wise subtraction, and classical triple-loop matrix multiplication ($\mathcal{O}(R_1 \cdot C_2 \cdot C_1)$).
- Performs explicit inner-dimension compatibility assertions, rejecting invalid combinations with explicit error handling.

### 3. Grid Proximity Mine Sweeper (`mineGame.java`)
- Reads an $M \times N$ discrete character grid representing unmined spaces (`'0'`) and mines (`'*'`).
- Concurrently scans all spatial coordinates, replacing empty cells with character digits corresponding to the local mine density count.

---

## Build & Execution Instructions

Compile and run with OpenJDK:

```bash
# Build and run Matrix Calculator
javac matrixCalculator.java
java Matrix

# Build and run Retail Shop
javac InternetShop.java
java Shop
```
