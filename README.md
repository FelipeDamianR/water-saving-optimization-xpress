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

## 🌐 Data Collection Challenge

One of the **biggest difficulties** in this project was the **data collection process**.  
We had to **research, clean, and compile the data from scratch** using official sources such as:
- **Mexican government websites** (CONAGUA, SIAP, and others),
- public statistics about water usage and agricultural areas,
- irrigation efficiency reports.

This meant going beyond coding:  
- Identifying reliable data sources,  
- Standardizing heterogeneous formats,  
- Making assumptions where information was incomplete.  

👉 This step was **time-consuming and challenging**, but it added significant value to the project, ensuring that the optimization model was based on **realistic and government-backed data**.  

## 🧮 Mathematical Model

We applied **deterministic optimization** using the **Simplex method** to design our **linear programming model**.  
The objective was to maximize annual water savings by upgrading irrigation technologies under land and budget constraints.  

The model considers:  
- Available surface area per crop and irrigation method.  
- Investment costs for each conversion.  
- A total budget limit.  
- Non-negativity of decision variables.  

This approach allowed us to obtain not only the **optimal water-saving strategy** but also perform **sensitivity and duality analysis** (shadow prices, slacks, and ranges) to better understand the robustness of the solution.

