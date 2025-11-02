# QAOA-Based Extension of "Portfolio Asset Identification using Graph Algorithms on a Quantum Annealer"

This repository accompanies my academic report analyzing the paper:  

> **"Portfolio Asset Identification using Graph Algorithms on a Quantum Annealer"**  
> *by Angad Kalra, Faisal Qureshi, and Michael Tisi.*

While the original paper employs quantum annealing (via D-Wave's Quantum Annealer 2000Q) to encode financial graph problems such as the *Maximum Clique and Maximum Independent Set Problem (MISP)*, *Maximum Graph Coloring Problem* and *Structural Balance Portfolio (SBP)* into QUBO and Ising formulations, this project presents an alternative approach: Solving similar graph based portfolio problems using the **Quantum Approximate Optimization Algorithm (QAOA)**.  

---

## Overview

The original work demonstrated how portfolio asset identification can be formulated as a graph optimization problem, which is then encoded into a QUBO/Ising Model.
By encoding this structure into a QUBO model, they leveraged a quantum annealer to identify optimal, minimally correlated subsets of assets.

My project builds on this concept by:

- Reconstructing the **graph-based QUBO formulation** described in the paper.  
- Translating the model into an **Ising Hamiltonian** suitable for **QAOA**.  
- Implementing QAOA using **PennyLane's statevector simulator** and **Adam Optimizer** for classical parameter optimization.  
- Comparing the observed behavior with expectations from quantum annealing results.
- Applying various methodologies such as warm start, random restarts, etc, to improve the solution.

This work aims to utilize QAOA as an accessible alternative to hardware-based quantum annealers for solving QUBO/Ising models.

## Tools and Framework

**Libraries Used**: PennyLane, NumPy, NetworkX, yfinance, and matplotlib (refer to Requirement.txt).

**Dataset**: Asset data is obtained using yfinance; the assets chosen for this analysis are [APL, MSFT, NVDA, JPM, MA, XOM, JNJ, PG, KO, CAT, META, DUK].

## Methodology 

Please refer to the *project report* for details. 

## Result and Future Study

After multiple attempts to improve the solution, I have yet to achieve a satisfactory result. Due to the fundamental nature of the QAOA approach to solving QUBO problems, it is challenging to obtain a result of similar quality to that which can be obtained from a quantum annealer; however, there are ways to further optimize it. This is what I will look into to improve accuracy in the future.
