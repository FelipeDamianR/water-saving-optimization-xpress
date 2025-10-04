# 💧 Water-Saving Optimization (Xpress/Mosel)

Deterministic **Linear Programming (Simplex)** model to **maximize annual water savings** by upgrading irrigation technologies (gravity → sprinkler/drip) under **budget** and **land-area** constraints.  
Implemented in **Xpress/Mosel** (`uses "mmxprs"`).  
Case study: **Cuauhtémoc aquifer (Chihuahua, MX)**.  

---

## 🔎 Problem Overview

Given agricultural areas by crop and irrigation method, per-hectare **water savings** for technology upgrades, and per-hectare **conversion costs**, the model chooses the number of hectares to convert for each crop/method to **maximize total m³/year saved**, respecting:
- maximum available hectares by crop/method,
- a total **budget cap**, and
- non-negativity of decision variables.

The model is solved using **Simplex** and includes a **sensitivity and duality analysis** with shadow prices, slacks, and ranges.

---

## 🧮 Mathematical Model

**Decision variables (hectares):**  
- \(x_1, \dots, x_9\) = hectares converted per crop/method pair.

**Objective (maximize yearly water savings):**  
\[
\max Z = \sum_i ahorro_i \cdot x_i
\]

**Constraints:**
- Land availability per crop and method (e.g. apples, maize, beans).  
- Budget constraint:  
  \[
  \sum_i costo_i \cdot x_i \leq \text{Presupuesto}
  \]  
- Non-negativity: \(x_i \geq 0\).

---

