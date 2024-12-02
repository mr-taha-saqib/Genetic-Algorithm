# Solving the N-Queens Problem Using Genetic Algorithm

## Overview
The N-Queens problem involves placing \(N\) queens on an \(N \times N\) chessboard such that no two queens attack each other. This means no two queens can share the same row, column, or diagonal. The Genetic Algorithm (GA) provides an evolutionary approach to solving this optimization problem.

---

## Genetic Algorithm Phases

### 1. **Initial Population**
- Each chromosome represents a potential solution.
- A chromosome is a permutation of numbers where the index represents the column, and the value at the index represents the row position of the queen.
- Example for \(N = 5\): `[5, 2, 4, 3, 1]`

### 2. **Fitness Function**
- The fitness function evaluates how "fit" a chromosome is.
- It calculates the number of non-attacking queen pairs. A solution with a higher fitness score is better.
- **Formula:**  
  \[
  \text{Fitness Function} = \sum (\text{non-attacking queen pairs})
  \]

### 3. **Selection**
- Select the fittest individuals based on their fitness scores for reproduction.
- Methods include:
  - Roulette Wheel Selection
  - Tournament Selection
  - Random Selection

### 4. **Crossover**
- Combine the genetic information of two parent chromosomes to produce offspring.
- Types of crossover:
  - Single-point
  - Two-point
  - Uniform
- Example for Single-point crossover:
  - Parents: `[5, 2, 4, 3, 1]` and `[3, 1, 5, 4, 2]`
  - Offspring: `[5, 2, 5, 4, 2]` and `[3, 1, 4, 3, 1]`

### 5. **Mutation**
- Randomly alter one or more genes in the offspring to maintain genetic diversity.
- Example: `[5, 2, 4, 3, 1]` → `[5, 2, 4, 1, 1]`

### 6. **Next Generation**
- Replace the least fit individuals in the population with new offspring.
- Repeat the process until a valid solution is found or a stopping criterion is met.

---
