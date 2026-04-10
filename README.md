# MARL-GovSim: Multi-Agent Reinforcement Learning for Global Policy Simulation

![Python](https://img.shields.io/badge/python-3.10-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-brightgreen)

## Overview

MARL-GovSim is a sophisticated simulation environment designed to model complex global governance dynamics using **Multi-Agent Reinforcement Learning (MARL)**. The project simulates how diverse national stakeholders (Governments, Corporations, and NGOs) react to global policy proposals and learn, through Deep Q-Learning, to optimize their internal satisfaction and national stability.

## 🎯 Why MARL-GovSim Matters

Traditional policy models often fail because they treat nations as monolithic entities. In reality:

- **Real-world policy is complex and subjective:** Every decision involves internal friction between the public and private sectors.
- **Traditional models ignore multi-agent conflict:** MARL-GovSim explicitly models the internal disagreement (Conflict) that destabilizes governments.
- **Geopolitical Dynamic:** By using MARL, we simulate real negotiation dynamics where actors don't just "calculate" a result—they **learn to adapt and compromise** over hundreds of interactions.

## 🧠 How It Works (Simple Explanation)

1.  **Stakeholders:** Each country contains three unique agents (Government, Industry, and NGOs), each with their own ethical "compass" (a 3D vector).
2.  **Evaluation:** When a global policy is proposed, these agents evaluate how close it is to their compass.
3.  **Learning:** Agents use a **Deep Q-Network (DQN)** to decide whether to **Accept**, **Reject**, or **Adjust** their stance.
4.  **Convergence:** Over time, the agents learn that total rejection leads to global failure, while strategic adjustment leads to stability and higher long-term rewards.

---

## 📂 Project Structure

```text
MARL-GovSim/
│── AI_Gov.ipynb       # Main simulation notebook
│── README.md           # Documentation & Architecture
│── requirements.txt    # Dependency list
└── Results/            # Extracted performance graphs
    ├── Basic Level/    # Baseline performance (Fixed Policy)
    ├── Intermediate Level/   # Stability & Conflict metrics
    ├── Advanced Level/       # Power-weighted global scores
    └── Expert Level/         # Acceptance rates & Ethical alignment
```

---

## 🚀 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/AbeerRai/MARL-GovSim.git
cd MARL-GovSim
```

### 2. Install dependencies

It is recommended to use a virtual environment (Python 3.10+):

```bash
pip install -r requirements.txt
```

### 3. Launch the environment

```bash
jupyter notebook AI_Gov.ipynb
```

---

## ⚙️ How to Run

1.  Open the `AI_Gov.ipynb` notebook.
2.  Run all cells (`Cell > Run All`).
3.  Scroll to the bottom to view the **training logs** and **final performance visualizations**.
4.  The simulation will run for 200 episodes by default, showing how agents evolve from random behavior to strategic alignment.

---

## 📊 Evaluation Metrics

Success in the simulation is defined by three converging indicators:

- **Stability Index (↑):** Higher stability indicates that internal stakeholders have reached a consensus.
- **Internal Conflict (↓):** Success is measured by the reduction of "ethical distance" between a country's internal agents.
- **Global Score (↑):** An aggregation of national happiness weighted by the geopolitical power of each nation.

---

## 🖼️ Simulation Results

### 1. Global Performance (Basic vs Dynamic)

|             Fixed Global Policy (Baseline)             |                Dynamic Geopolitical Adaptation                |
| :----------------------------------------------------: | :-----------------------------------------------------------: |
| ![Fixed](Results/Basic%20Level/global_score_fixed.png) | ![Dynamic](Results/Advanced%20Level/global_score_dynamic.png) |

### 2. Internal Dynamics

|                    National Stability Over Time                    |                  Stakeholder Conflict Reduction                  |
| :----------------------------------------------------------------: | :--------------------------------------------------------------: |
| ![Stability](Results/Intermediate%20Level/stability_over_time.png) | ![Conflict](Results/Intermediate%20Level/conflict_over_time.png) |

### 3. Expert Alignment

|               Global Policy Acceptance Rate               |                Ethical Alignment Distance                 |
| :-------------------------------------------------------: | :-------------------------------------------------------: |
| ![Acceptance](Results/Expert%20Level/acceptance_rate.png) | ![Alignment](Results/Expert%20Level/ethical_distance.png) |

---

## 🔬 Mathematical Theoretical Model

### 1. Euclidean Ethical distance

$$dist(E, P) = \sqrt{\sum_{i=1}^3 (E_i - P_i)^2}$$

### 2. National Index ($I$)

$$I = 0.6(0.4s_{gov} + 0.4s_{comp} + 0.2s_{ngo}) + 0.4(\frac{1}{1 + Conflict})$$

### 3. Global Score Aggregation

$$GlobalScore = \sum_{c \in Countries} Power_c \times I_c$$

---

## 🧪 Hyperparameters

| Parameter       | Value | Description                  |
| :-------------- | :---- | :--------------------------- |
| `lr`            | 0.001 | Adam Optimizer Learning Rate |
| `gamma`         | 0.95  | Reward Discount Factor       |
| `epsilon_decay` | 0.995 | Exploration decay rate       |
| `episodes`      | 200   | Simulation length            |

---

## 🚀 Future Work

- [ ] **Real-world Datasets:** Integrate actual UN voting data to initialize stakeholder vectors.
- [ ] **Transformer Agents:** Move from Simple MLPs to Attention-based architectures for multi-stakeholder history.
- [ ] **Communication Protocols:** Allow agents to "negotiate" via message passing before taking actions.
- [ ] **Macro-Economic Feedback:** Link policy acceptance to GDP growth variables.

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the DQN architecture or add new stakeholder types, please fork the repo and submit a PR. For major changes, please open an issue first.

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Abeer Rai**  
_Aspiring AI/ML Engineer_

[LinkedIn](https://www.linkedin.com/in/theabeerrai/) | [GitHub](https://github.com/abeerrai01)
