# Learning Fair Demand Models

This repository contains the official source code to reproduce the empirical findings and simulations presented in the research paper **"Learning Fair Demand Models"**. 

For a deep dive into the methodology, proofs, and framework, please refer to the [Full Paper](https://arxiv.org/abs/2606.06830).

---

## 🛠️ Experimental Setup & Solvers

The scripts in this repository are optimized to run out-of-the-box in **Google Colab**, but they can also be executed in a local Python environment. 
The codebase uses `Pyomo` (`Ipopt` and `Couenne`) and `SciPy` to model and solve optimization problems.
---

## 📊 Notebook Directory

### 1. Theoretical Insights & Propositions
These notebooks reproduce the theoretical visualizations discussed in the paper.

| Figure / Proposition | Notebook | Description                                                                |
| :--- | :--- |:---------------------------------------------------------------------------|
| **Figure 1** | `Parity_wise_Loss_Fairness.ipynb` | Visualizes parity-wise loss fairness (Proposition 1).                      |
| **Figure 2 & 3** | `Proposition2.ipynb` | Validates properties outlined in Proposition 2.                            |
| **Figure 4** | `Rawlsian_Price_Demand_Fairness.ipynb` | Explores Rawlsian fairness under price/demand constraints (Proposition 4). |

### 2. Synthetic Data Experiments
`Linear_Demand_Synthetic.ipynb` includes simulations evaluating model performance under linear demand.

### 3. Empirical Case Study
Evaluations using real-world vaccine pricing data to analyze both well-specified and misspecified model assumptions.

| Paper Section | Notebook | Estimation Model | True Demand |
| :--- | :--- | :--- | :--- |
| **Section 5.2** | `Logistic Demand Estimation with Logistic True Demand.ipynb` | Logistic | Logistic |
| **Appendix C.1** | `Linear Demand Estimation with Linear True Demand.ipynb` | Linear | Linear |
| **Appendix C.2** | `Linear Demand Estimation with Logistic True Demand.ipynb` | Linear | Logistic |
| **Appendix C.3** | `Logistic Demand Estimation with Linear True Demand.ipynb` | Logistic | Linear |

---

## 💾 Case Study Data Setup

The empirical case study relies on real-world vaccine pricing data from *Slunge (2015)*.
Before running the case study notebooks, create a `Dataset` directory at the project root and place the Excel data file inside it:

```text
├── code.ipynb
└── Dataset/
    └── SND 0987.xlsx
