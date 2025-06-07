# 🚇 Advanced Deep Reinforcement Learning Framework for Bus Transit Network Design Optimization

> **A next-generation solution for the Bus Transit Network Design Problem (BTNDP) using Transformer-based deep reinforcement learning, multi-objective reward shaping, and state-of-the-art evolutionary algorithms.**

---

## 📌 Project Overview

Welcome to an advanced, research-grade **Deep Reinforcement Learning (DRL) optimization system** for the **Bus Transit Network Design Problem (BTNDP)**. This framework is engineered to generate bus transit networks that are **efficient, sustainable, and scalable**, intelligently balancing complex trade-offs such as:

- ✅ Maximizing service area coverage  
- ✅ Minimizing passenger travel time  
- ✅ Reducing route length and transfer count  
- ✅ Lowering energy consumption and emissions  

**Key technological highlights:**
- **Transformer-inspired encoder-decoder policy networks** for sequence-based route generation
- **Multi-objective reward shaping** and Pareto front optimization via **NSGA-II**
- Seamless integration with the **Mandl BTNDP benchmark** and real-world datasets
- **Greedy Rollout** and **NSGA-II** baselines for robust comparative analysis
- Full-stack **API and web interface** for streamlined experimentation and deployment

---

## 🏆 Objectives

### 1. **Autonomous Policy Discovery**
Leverage DRL to autonomously learn optimal bus routing and scheduling strategies in dynamic, real-world transit environments.

### 2. **Hybrid Algorithmic Architecture**
Design a modular system combining:
- **Reinforcement Learning:** Advanced algorithms like PPO, SAC, and A2C
- **Transformer-based Sequence Modeling:** For effective route generation
- **Evolutionary Computation:** NSGA-II for powerful Pareto optimization

### 3. **Multi-Objective Optimization**
Simultaneously optimize conflicting objectives:
- Service coverage vs. route length
- Passenger travel time vs. number of transfers
- Energy and emissions minimization

### 4. **Rigorous Baseline Evaluation**
Benchmark against **Greedy Rollout** and **NSGA-II** to validate DRL's effectiveness.

---

## 🧱 System Architecture

### 🧠 Core Algorithms
- **DRL:** PPO, SAC, A2C (customized for sequence-based action spaces)
- **Hybrid Models:** DRL + Evolutionary (NSGA-II) for Pareto frontier discovery
- **Baseline:** Greedy Rollout, standalone NSGA-II

### 🌍 Environments
- **Gym-compatible wrapper** for Mandl BTNDP
- Support for custom, real-world city datasets
- **Reward shaping** with dynamic multi-objective balancing

### 🤖 Policy Networks
- **Transformer Encoder-Decoder**
  - 128-dimensional stop embeddings
  - 8-head Multi-Head Attention (MHA)
  - Deep feed-forward layers with ReLU
  - Output: Variable-length bus route sequences

### 📊 Evaluation Metrics
- Route length (km)
- Average and total travel time (min)
- Number of transfers
- Demand satisfied
- Load factor
- Energy consumption & emissions (CO₂, NOx, etc.)
- Service coverage (%)

### 📈 Visualization & Analysis
- Interactive Pareto frontier plots
- Route and network visualization
- Reward and performance curve analytics
- Algorithm comparison dashboards

---

## 📁 Folder Structure

```
btnd_optimization_framework/
├── configs/                # Algorithm and environment configs (YAML)
├── docs/                   # Documentation and design docs
├── models/                 # Trained model weights and checkpoints
├── src/
│   ├── envs/               # BTNDP environment implementations
│   ├── networks/           # Policy/value networks (Transformers, etc.)
│   ├── algorithms/         # RL and evolutionary algorithm modules
│   ├── scripts/            # Training, evaluation, simulation scripts
│   └── utils/              # Utilities and helpers
├── tests/                  # Unit and integration tests
├── requirements.txt
└── README.md
```

---

## 🔧 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/rafatoel/btnd_optimization_framework.git
cd btnd_optimization_framework
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### Train a DRL Model

```bash
python src/scripts/train.py --algo ppo --config configs/algorithm/ppo.yaml
```

### Evaluate Model Performance

```bash
python src/scripts/evaluate.py --model_path models/ppo_final.pt
```

### Run Simulation with Greedy Baseline

```bash
python src/scripts/simulate.py --baseline greedy_rollout
```

### Launch Backend & Frontend Servers

```bash
python src/scripts/run_server.py
```

---

## 📊 Sample Results

| Algorithm      | Avg. Route Length | Coverage (%) | Avg. Transfers | Emissions (kg) |
|----------------|-------------------|--------------|----------------|----------------|
| Greedy Rollout | 15.6 km           | 78%          | 2.1            | 2.4            |
| PPO            | 14.2 km           | 85%          | 1.7            | 2.1            |
| SAC            | 14.0 km           | 86%          | 1.6            | 2.0            |
| NSGA-II        | 13.9 km           | 87%          | 1.8            | 2.0            |

---

## 📄 Documentation

Comprehensive documentation and guides are available in the `/docs` directory:

- [User Guide](docs/user_guide.md)
- [API Reference (OpenAPI)](docs/api_docs/openapi.yaml)
- [Architecture Overview](docs/design_docs/architecture_overview.md)
- [Learning Policy Design](docs/design_docs/learning_policy.md)
- [Multi-Objective Optimization Strategy](docs/design_docs/multi_objective_optimization.md)

---

## 📚 References

- Vaswani, A., et al. (2017). *Attention Is All You Need*. arXiv.
- Mandl, C. E. (1980). *Evaluation of Urban Transit Systems and Their Applications*.
- Deb, K., Pratap, A., Agarwal, S., & Meyarivan, T. (2002). *A Fast and Elitist Multiobjective Genetic Algorithm: NSGA-II*.
- Schulman, J., et al. (2017). *Proximal Policy Optimization Algorithms*. arXiv.

---

## 🛡️ License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are highly encouraged! Please review the [contributing guidelines](CONTRIBUTING.md) before submitting a pull request.

---

## 📬 Contact

For inquiries, collaborations, or research partnerships, please contact:

- 📧 **Email:** [raafatoel@gmail.com](mailto:raafatoel@gmail.com)
- 🐙 **GitHub:** [@rafatoel](https://github.com/rafatoel)

---
