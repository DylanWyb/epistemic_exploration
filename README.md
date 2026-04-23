
<h1 align="center">🔥 Awesome-Epistemic-Exploration

"Epistemic Exploration Toward Artificial General Intelligence"  (ArXiv 2026) </h2>




<p align="center">
  <b>◇ Responder → Reasoner → Agent → Prospector → Ecosystem ◇</b>
    <br>
   <i><b>🚀 Exploration as the Transition Mechanism 🚀</b></i>
</p>

<p align="center"><img src="fig/5levels.png" width="900"/></p>



<p align="center">
  <!-- <a href="#"><img src="https://img.shields.io/badge/📄_Paper-ArXiv-red" alt="Paper"></a> -->
  <!-- <a href="#"><img src="https://img.shields.io/badge/🌐_Website-Project_Page-blue" alt="Website"></a> -->
  <a href="https://github.com/banyikun/epistemic_exploration"><img src="https://img.shields.io/badge/GitHub-Repository-181717?logo=github" alt="GitHub"></a>
  <a href="#"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"></a>
  <a href="#"><img src="https://img.shields.io/badge/Maintained%3F-Yes-brightgreen.svg" alt="Maintained"></a>
  <a href="#"><img src="https://img.shields.io/badge/PRs-Welcome-orange.svg" alt="PRs Welcome"></a>
  </a>
  <a href=""><img src="https://img.shields.io/github/last-commit/banyikun/epistemic_exploration?color=lightgrey"></a>
</p>

<p align="center">
  <a href="https://github.com/banyikun/epistemic_exploration/stargazers"><img src="https://img.shields.io/github/stars/banyikun/epistemic_exploration?style=social" alt="GitHub stars"></a>
  <a href="https://github.com/banyikun/epistemic_exploration/network/members"><img src="https://img.shields.io/github/forks/banyikun/epistemic_exploration?style=social" alt="GitHub forks"></a>
</p>

<h4 align="center">If you find our survey helpful, please give it a star ⭐ to show your support！Thank you:)

</h4>




---

## 📣 Notices

> 🔥 This is a curated paper list for the survey **"Epistemic Exploration Toward Artificial General Intelligence"**, covering exploration mechanisms across reasoning, embodied AI, world models, and multi-agent systems.

> 🔥 **Stay tuned for our full paper release, incorporating the latest developments.**

> **[Always] [Add your papers]** We welcome all related papers! If you find any missed or new work, please open a Pull Request or contact us.

> **[Always] [Maintain]** We will keep this list updated frequently!

---


<br>



## 📑 Table of Contents

- [1. Overview](#1-overview)
  - [1.1 What is Epistemic Exploration?](#11-what-is-epistemic-exploration)
  - [1.2 Three Criteria](#12-three-criteria)
  - [1.3 Five-Level Trajectory Toward AGI](#13-five-level-trajectory-toward-agi)
  - [1.4 3×5 Taxonomy](#14-3×5-taxonomy)
- [2. Level 1–2: Responder → Reasoner (Reasoning-Space Exploration)](#2-levels-12-responder--reasoner--reasoning-space-exploration)
  - [2.1 Uncertainty-Driven Exploration](#21-uncertainty-driven-exploration)
  - [2.2 Competence-Driven Exploration](#22-competence-driven-exploration)
  - [2.3 Reachability-Driven Exploration](#23-reachability-driven-exploration)
- [3. Level 3: Reasoner → Agent (Perception- & Action-Space Exploration)](#3-level-3-reasoner--agent--perception--action-space-exploration)
  - [3.1 Digital Agents](#31-digital-agents)
    - [3.1.1 Uncertainty-Driven Exploration](#311-uncertainty-driven-exploration)
    - [3.1.2 Competence-Driven Exploration](#312-competence-driven-exploration)
    - [3.1.3 Reachability-Driven Exploration](#313-reachability-driven-exploration)
  - [3.2 Embodied Agents](#32-embodied-agents)
- [4. Level 4: Agent → Prospector (Imagination-Space Exploration)](#4-level-4-agent--prospector--imagination-space-exploration)
- [5. Level 5: Prospector → Ecosystem (Coordination-Space Exploration)](#5-level-5-prospector--ecosystem--coordination-space-exploration)
- [6. Cross-Cutting Topics](#6-cross-cutting-topics)
- [7. Citation](#7-citation)

---



## 1. Overview

### 1.1 What is Epistemic Exploration?

> **Epistemic exploration** is the agent's capacity to actively acquire information that reduces its uncertainty about the world, convert that reduction into durable policy improvement, and keep future acquisition possible.

Unlike undirected exploration (e.g., ε-greedy), epistemic exploration is *intentional*, *belief-driven*, and *multi-scale*: the agent reasons about which actions are most informative and plans multi-step information-gathering strategies across reasoning trajectories, tool-use policies, embodied sensorimotor loops, world-model rollouts, and multi-agent coordination protocols.

### 1.2 Three Criteria

<p align="center"><img src="fig/3criteria.png" width="800"/></p>
<p align="center"><i>Figure: Foundation of Epistemic Exploration — Why, What, and How.</i></p>

We ground epistemic exploration in **three jointly necessary criteria**, each addressing a distinct failure mode of static optimisation:

| Criterion | What It Does | Failure Mode Addressed | Explores... |
|:---------:|:-------------|:-----------------------|:------------|
| **C1: Information Gain** | Actively reduces epistemic uncertainty via belief-updating observations | *Belief Stagnation* — frozen internal model under distribution shift | ...where it knows least |
| **C2: Value Improvement** | Converts new information into durable policy improvement | *Value Stagnation* — local optima lock-in, surrogate misalignment | ...what it cannot yet do well |
| **C3: Epistemic Reachability** | Preserves positive visitation over belief-consistent regions | *Reachability Collapse* — irreversible contraction of behavioural diversity | ...where it might otherwise never go |

These form a closed loop: **gain information → convert to value → keep the capacity to gain information alive → ...**

### 1.3 Five-Level Trajectory Toward AGI

We propose exploration as the **transition mechanism** between five levels of increasing agent sophistication. Each level introduces a qualitatively new exploration space that the previous level cannot access:

| Transition | Exploration Space | What Becomes Explorable |
|:-----------|:------------------|:------------------------|
| **L1→L2: Responder → Reasoner** | **Reasoning space** | Hypotheses, reasoning trajectories, latent thought representations |
| **L2→L3: Reasoner → Agent** | **Perception & action space** | Tool invocation, sensorimotor loops, memory management |
| **L3→L4: Agent → Prospector** | **Imagination space** | Counterfactual futures in learned world models, dual real-imagined exploration |
| **L4→L5: Prospector → Ecosystem** | **Coordination space** | Communication topologies, role assignments, shared world models |

### 1.4 3×5 Taxonomy

Our survey is organized as a **3×5 taxonomy** crossing three signal-driven methodologies with the five levels:

|  | **L1 Responder** | **L2 Reasoner** | **L3 Agent** | **L4 Prospector** | **L5 Ecosystem** |
|:-|:---|:---|:---|:---|:---|
| **Uncertainty-Driven** | Token entropy | Ensemble disagreement, semantic uncertainty | Active SLAM, prediction variance | Epistemic disagreement in latent space | Joint-belief uncertainty |
| **Competence-Driven** | Input difficulty | Iterative curricula, self-play | Skill bootstrapping, RL-VLA | Imagination-based skill discovery | Multi-agent self-play curricula |
| **Reachability-Driven** | Anti-repetition | Beam diversity, reasoning-path anti-foreclosure | Go-Explore, coverage curricula | Latent-space diversity bonuses | Role-diversity, anti-specialisation |

---

<br>

## 2. Levels 1–2: Responder → Reasoner — Reasoning-Space Exploration

The transition from **Responder** to **Reasoner** requires exploration in *reasoning space*: branching over token sequences, reasoning trajectories, and latent thought representations. The agent must search for informative hypotheses rather than simply produce reactive outputs.

<p align="center"><img src="fig/level1_reasoner.png" width="850"/></p>
<p align="center"><i>Figure: Levels 1–2 Reasoning-Space Exploration — Why (entropy escalation & reward stagnation), Where (tokens → turns → latent trajectories), and How (uncertainty / competence / reachability-driven).</i></p>

### 2.1 Uncertainty-Driven Exploration

Methods that prioritise exploration at high-uncertainty branching points in the reasoning process:

| Method | Strategy | Paper |
|:-------|:---------|:------|
| **CURE** | High-entropy tokens as re-branching anchors | Uncertainty-aware Reasoning Enhancement (2025) |
| **SPINE** | Concentrates updates on high-entropy branching points | Sparse Inference with Entropy (2025) |
| **TreeRL** | On-policy tree search from high-entropy steps | Tree-Structured RL for Reasoning (2025) |
| **CE-GPPO** | Coordinating entropy-gradient preservation | CE-GPPO (2025) |
| **SIREN** | Top-p & peak-entropy masks for meaningful exploration | Rethinking Entropy in LLM Reasoning (2025) |
| **AEPO** | Anchors entropy to user-specified target level | Arbitrary Entropy Policy Optimization (2025) |
| **ICPO** | Intrinsic confidence from relative generation probabilities | Intrinsic Confidence Policy Optimization (2025) |
| **REAL** | Categorical labels replacing scalar rewards | Rewards as Labels (2026) |

### 2.2 Competence-Driven Exploration

Methods that match problem difficulty to the model's evolving competence frontier:

| Method | Strategy | Paper |
|:-------|:---------|:------|
| **E2H** | Easy-to-hard curriculum with gradual fade-out | Easy to Hard Curriculum (2025) |
| **RLAAR** | Ability-gated curriculum with abstention reward | RL with Abstention-Aware Rewards (2025) |
| **Online Difficulty Filtering** | Selects medium-difficulty samples by current success rate | Dynamic Difficulty Filtering (2025) |
| **CDAS** | Historical performance gaps for robust difficulty estimation | Competence-Driven Adaptive Sampling (2025) |
| **HA-DW** | Tracks evolving competence, reweights difficulty | Hardness-Aware Dynamic Weighting (2026) |
| **SvS** | Self-synthesized harder variants from solved examples | Solve via Self-play (2025) |
| **Absolute Zero** | Reinforced self-play with zero external data | Absolute Zero Reasoner (2025) |

### 2.3 Reachability-Driven Exploration

Methods that prevent irreversible contraction of reasoning trajectory distributions:

| Method | Strategy | Paper |
|:-------|:---------|:------|
| **Trust-region methods** | KL penalties, PPO clipping to preserve pre-trained breadth | Various (2025) |
| **Anti-degeneration penalties** | Repetition penalties, length-budget constraints | Welleck et al. (2020), various (2025) |
| **SPO / KTAE** | Step-level credit assignment preserving alternative trajectories | Step Policy Optimization / KTAE (2025) |
| **VRPRM** | Process-level dense supervision for intermediate steps | Verifiable Reward PRM (2025) |
| **RLVRR** | Content coverage + style constraints for denser rewards | RL with Verifiable & Reward-Rich feedback (2026) |

---

<br>

## 3. Level 3: Reasoner → Agent — Perception- & Action-Space Exploration

At Level 3, the agent crosses from internal reasoning into **situated interaction with external environments**. Exploration unfolds in perception and action space, where every step incurs real cost.

### 3.1 Digital Agents

Agents operating in software-mediated environments (web, APIs, code interpreters):

#### 3.1.1 Uncertainty-Driven Exploration

Methods that acquire information under partial observability by prioritising uncertain states, tool calls, or capability boundaries:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------|:---------|:------|:---:|
| 2026-01 | **JitRL** | Uses count-based uncertainty bonuses to explore unseen state-action pairs | [Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates](https://arxiv.org/abs/2601.18510) | [![GitHub Stars](https://img.shields.io/github/stars/liushiliushi/JitRL?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/liushiliushi/JitRL) |
| 2023-05 | **RAP** | Explores alternative reasoning paths with MCTS and UCB guidance | [Reasoning with Language Model is Planning with World Model](https://doi.org/10.18653/v1/2023.emnlp-main.507) | [![GitHub Stars](https://img.shields.io/github/stars/Ber666/RAP?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/Ber666/RAP) |
| 2024-08 | **Agent Q** | Expands high-value action trajectories via MCTS-guided exploration | [Agent Q: Advanced Reasoning and Learning for Autonomous AI Agents](https://arxiv.org/abs/2408.07199) | - |
| 2023-10 | **LAST** | Explores reasoning-action branches through language-agent tree search | [Language Agent Tree Search Unifies Reasoning Acting and Planning in Language Models](https://arxiv.org/abs/2310.04406) | [![GitHub Stars](https://img.shields.io/github/stars/lapisrocks/LanguageAgentTreeSearch?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/lapisrocks/LanguageAgentTreeSearch) |
| 2025-04 | **KnowSelf** | Explores capability boundaries by detecting uncertain self-knowledge | [Agentic Knowledgeable Self-awareness](https://arxiv.org/abs/2504.03553) | [![GitHub Stars](https://img.shields.io/github/stars/zjunlp/KnowSelf?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/zjunlp/KnowSelf) |
| 2025-01 | **Search-o1** | Explores external evidence when reasoning exposes knowledge uncertainty | [Search-o1: Agentic Search-Enhanced Large Reasoning Models](https://doi.org/10.18653/v1/2025.emnlp-main.276) | [![GitHub Stars](https://img.shields.io/github/stars/RUC-NLPIR/Search-o1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/RUC-NLPIR/Search-o1) |

#### 3.1.2 Competence-Driven Exploration

Methods that tame combinatorial tool-use spaces through curricula, process-level credit assignment, and self-generated training tasks:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------|:---------|:------|:---:|
| 2025-08 | **PilotRL** | Stages curricula to expand agent exploration from planning to tool use | [PilotRL: Training Language Model Agents via Global Planning-Guided Progressive Reinforcement Learning](https://arxiv.org/abs/2508.00344) | - |
| 2025-09 | **ReSum-GRPO** | Sustains long-horizon search exploration through context summarization | [ReSum: Unlocking Long-Horizon Search Intelligence via Context Summarization](https://arxiv.org/abs/2509.13313) | - |
| 2024-03 | **ETO** | Optimizes exploratory trial-and-error trajectories for agent learning | [Trial and Error: Exploration-Based Trajectory Optimization for LLM Agents](https://arxiv.org/abs/2403.02502) | [![GitHub Stars](https://img.shields.io/github/stars/Yifan-Song793/ETO?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/Yifan-Song793/ETO) |
| 2025-09 | **Planner-R1** | Uses dense process rewards to steer exploration toward feasible plans | [Planner-R1: Reward Shaping Enables Efficient Agentic RL with Smaller LLMs](https://arxiv.org/abs/2509.25779) | - |
| 2025-08 | **RLTR** | Rewards complete tool-use processes to improve exploratory planning | [Encouraging Good Processes Without the Need for Good Answers: Reinforcement Learning for LLM Agent Planning](https://arxiv.org/abs/2508.19598) | - |
| 2025-05 | **GiGPO** | Assigns state-level credit across grouped rollouts for exploration | [Group-in-Group Policy Optimization for LLM Agent Training](https://arxiv.org/abs/2505.10978) | [![GitHub Stars](https://img.shields.io/github/stars/langfengQ/verl-agent?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/langfengQ/verl-agent) |
| 2025-11 | **Agent0-VL** | Evolves tool-integrated exploration through repeated reasoning cycles | [Agent0-VL: Exploring Self-Evolving Agent for Tool-Integrated Vision-Language Reasoning](https://arxiv.org/abs/2511.19900) | [![GitHub Stars](https://img.shields.io/github/stars/aiming-lab/Agent0?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/aiming-lab/Agent0) |
| 2025-05 | **Absolute Zero** | Uses proposer-solver self-play to explore new reasoning tasks | [Absolute Zero: Reinforced Self-play Reasoning with Zero Data](https://arxiv.org/abs/2505.03335) | [![GitHub Stars](https://img.shields.io/github/stars/LeapLabTHU/Absolute-Zero-Reasoner?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/LeapLabTHU/Absolute-Zero-Reasoner) |

#### 3.1.3 Reachability-Driven Exploration

Methods that preserve behavioural flexibility by regulating entropy or injecting useful off-policy experience:

| Date | Method | Key Idea | Paper | Github |
|:---:|:-------|:---------|:------|:---:|
| 2025-08 | **EGPO** | Adds entropy bonuses to encourage exploration in function-call reasoning | [Reasoning through Exploration: A Reinforcement Learning Framework for Robust Function Calling](https://arxiv.org/abs/2508.05118) | [![GitHub Stars](https://img.shields.io/github/stars/BingguangHao/RLFC?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/BingguangHao/RLFC) |
| 2025-09 | **EPO** | Regularizes entropy to sustain exploration in multi-turn agent RL | [EPO: Entropy-regularized Policy Optimization for LLM Agents Reinforcement Learning](https://arxiv.org/abs/2509.22576) | [![GitHub Stars](https://img.shields.io/github/stars/WujiangXu/EPO?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/WujiangXu/EPO) |
| 2025-09 | **ENTROPO** | Uses entropy-enhanced preferences to diversify coding-agent exploration | [Building Coding Agents via Entropy-Enhanced Multi-Turn Preference Optimization](https://arxiv.org/abs/2509.12434) | - |
| 2026-03 | **RAPO** | Expands policy exploration with retrieval-augmented experience | [RAPO: Expanding Exploration for LLM Agents via Retrieval-Augmented Policy Optimization](https://arxiv.org/abs/2603.03078) | - |
| 2026-04 | **E³-TIR** | Branches from high-entropy prefixes to exploit exploratory experience | [E3-TIR: Enhanced Experience Exploitation for Tool-Integrated Reasoning](https://arxiv.org/abs/2604.09455) | [![GitHub Stars](https://img.shields.io/github/stars/yuki-younai/E3-TIR?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/yuki-younai/E3-TIR) |

### 3.2 Embodied Agents

<p align="center"><img src="fig/level3_embodied.png" width="850"/></p>
<p align="center"><i>Figure: Level 3 Embodied Agent Exploration — Uncertainty-driven active perception, competence-driven RL & test-time compute, and reachability-driven safety & reward engineering.</i></p>

Agents operating in physical/simulated environments with continuous action spaces:

| Paradigm | Method | Key Idea | Project |
|:---------|:-------|:---------|:--------|
| **Uncertainty-Driven** | | | |
| *Geometric & high-fidelity reconstruction* | [ActiveSplat](https://arxiv.org/abs/2410.21955) | Gaussian splatting for information-maximizing viewpoint selection | [🔗](https://github.com/Li-Yuetao/ActiveSplat) |
| | [APT](https://arxiv.org/abs/2103.04551) | Unsupervised active pre-training with every transition | [🔗](https://github.com/rll-research/url_benchmark) |
| | [MAX](https://arxiv.org/abs/1810.12162) | Model-based active exploration via ensemble disagreement | [🔗](https://github.com/nnaisense/MAX) |
| | [Active Neural SLAM](https://arxiv.org/abs/2004.05155) | Learning to explore using active neural SLAM | [🔗](https://github.com/devendrachaplot/Neural-SLAM) |
| *Semantic active inference* | [Conan](https://arxiv.org/abs/2311.02018) | Active reasoning in open-world environments | [🔗](https://github.com/ariesssxu/Conan-Active-Reasoning) |
| | [ActiveRIR](https://arxiv.org/abs/2404.16216) | Cross-modal audio-visual exploration | - |
| | [Active Semantic Perception](https://arxiv.org/abs/2510.05430) | Active semantic perception for embodied agents | [🔗](https://github.com/grasp-lyrl/active_semantic_perception) |
| *Active mapping & path planning* | [Fisher-info planning](https://arxiv.org/abs/2410.17422) | MLLM-guided exploration via Fisher information | [🔗](https://github.com/JiangWenPL/multimodal-active) |
| **Objective-Driven** | | | |
| *Language-guided navigation* | [SayCan](https://arxiv.org/abs/2204.01691) | Grounding language in robotic affordances | [🔗](https://github.com/google-research/google-research/tree/master/saycan) |
| | [Inner Monologue](https://arxiv.org/abs/2207.05608) | Embodied reasoning through planning with language models | - |
| | [LM-Nav](https://arxiv.org/abs/2207.04429) | Robotic navigation with large pre-trained models | [🔗](https://github.com/blazejosinski/lm_nav) |
| | [VLMaps](https://arxiv.org/abs/2210.05714) | Visual language maps for robot navigation | [🔗](https://github.com/vlmaps/vlmaps) |
| | [LFG](https://arxiv.org/abs/2310.10103) | Semantic guesswork as a heuristic for planning | [🔗](https://github.com/Michael-Equi/lfg-nav) |
| **Competence-Driven** | | | |
| *Offline RL-VLA* | [Q-Transformer](https://arxiv.org/abs/2309.10150) | Scale value learning to static trajectories | - |
| | [Cal-QL](https://arxiv.org/abs/2303.05479) | Calibrated offline RL for robot manipulation | - |
| *Online RL-VLA* | [VLA-RL](https://arxiv.org/abs/2505.18719) | PPO-based online RL for VLA | [🔗](https://github.com/GuanxingLu/vlarl) |
| | [FLaRe](https://arxiv.org/abs/2409.16578) | Fine-tuning language models for autonomous RL | [🔗](https://github.com/JiahengHu/FLaRe) |
| | [SimpleVLA-RL](https://arxiv.org/abs/2509.09674) | GRPO-based online RL for VLA | [🔗](https://github.com/PRIME-RL/SimpleVLA-RL) |
| | [SOP](https://arxiv.org/abs/2601.03044) | Scalable online post-training for VLA | - |
| *Hybrid (Offline+Online)* | [ConRFT](https://arxiv.org/abs/2502.05450) | Offline-to-online with Cal-QL + BC | [🔗](https://github.com/cccedric/conrft) |
| | [SRPO](https://arxiv.org/abs/2511.15605) | Self-refined policy optimization | [🔗](https://github.com/SUSTechBruce/SRPO_MLLMs) |
| | [Dual-Actor FT](https://arxiv.org/abs/2509.13774) | Dual-actor fine-tuning for offline-to-online | - |
| *Test-time compute & cognitive search* | [VLA-Reasoner](https://arxiv.org/abs/2509.22643) | MCTS-based planning for VLA | - |
| | [DeepThinkVLA](https://arxiv.org/abs/2511.15669) | Slow-thinking VLA via GRPO | [🔗](https://github.com/OpenBMB/DeepThinkVLA) |
| | [Hume](https://arxiv.org/abs/2505.21432) | System-2 thinking for embodied agents | [🔗](https://github.com/hume-vla/hume) |
| | [TT-VLA](https://arxiv.org/abs/2601.06748) | On-the-fly VLA adaptation at test-time | - |
| | [TACO](https://arxiv.org/abs/2512.02834) | Steering VLA via anti-exploration | [🔗](https://github.com/breez3young/TACO) |
| **Reachability-Driven** | | | |
| *Automated reward engineering* | [Eureka](https://arxiv.org/abs/2310.12931) | LLM-driven reward code synthesis | [🔗](https://github.com/eureka-research/eureka) |
| | [Language to Rewards](https://arxiv.org/abs/2306.08647) | Language-conditioned robotic reward synthesis | [🔗](https://github.com/google-deepmind/language_to_reward_2023) |
| | [TeViR](https://arxiv.org/abs/2505.19769) | Text-to-video reward for efficient RL | - |
| *Curiosity & curriculum* | [RND](https://arxiv.org/abs/1810.12894) | Exploration by random network distillation | [🔗](https://github.com/openai/random-network-distillation) |
| | [CurricuLLM](https://arxiv.org/abs/2409.18382) | Automatic task curricula via LLMs | [🔗](https://github.com/labicon/CurricuLLM) |
| *Constrained safety* | [Recovery RL](https://arxiv.org/abs/2010.15920) | Safe RL with learned recovery zones | [🔗](https://github.com/abalakrishna123/recovery-rl) |
| | [RECOVER](https://arxiv.org/abs/2404.00756) | Neuro-symbolic failure detection and recovery | - |
| | [SafeVLA](https://arxiv.org/abs/2503.03480) | Safe VLA with constrained policy optimization | [🔗](https://github.com/PKU-Alignment/SafeVLA) |

---

<br>

## 4. Level 4: Agent → Prospector — Imagination-Space Exploration

<p align="center"><img src="fig/level4_worldmodel.png" width="850"/></p>
<p align="center"><i>Figure: Level 4 Imagination-Space Exploration — Why (the dual exploration problem), Where (simulated rollouts, hazard zones, latent value landscapes), and How (MBRL, video generation, autonomous driving, social dynamics).</i></p>

The Prospector internalises a **world model** and faces a **dual exploration problem**: simultaneously gathering real data to refine the model AND searching imagined trajectories to extract policies.
The Prospector internalises a **world model** and faces a **dual exploration problem**: simultaneously gathering real data to refine the model AND searching imagined trajectories to extract policies.


### 4.1 Surveys & Overviews



- **A survey of learning in multiagent environments: Dealing with non-stationarity** (2017) <a href="https://arxiv.org/abs/1707.09183"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Model-based reinforcement learning: A survey** (2023) <a href="https://arxiv.org/abs/2006.16712"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **An Information-Theoretic Perspective on Intrinsic Motivation in Reinforcement Learning: A Survey** (2023) <a href="https://arxiv.org/abs/2209.08890"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A Survey on Model-based Reinforcement Learning** (2024) <a href="https://arxiv.org/abs/2206.09328"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A survey of world models for autonomous driving** (2025) <a href="https://arxiv.org/abs/2501.11260"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A Survey of Embodied World Models** (2025) <a href="https://arxiv.org/abs/2507.02790"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Reward Models in Deep Reinforcement Learning: A Survey** (2025) <a href="https://arxiv.org/abs/2506.15421"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A Survey of Safe Reinforcement Learning and Constrained MDPs: A Technical Survey on Single-Agent and Multi-Agent Safety** (2025) <a href="https://arxiv.org/abs/2505.17342"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A Comprehensive Survey on Physical Risk Control in the Era of Foundation Model-enabled Robotics** (2025) <a href="https://arxiv.org/abs/2505.12583"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **The role of world models in shaping autonomous driving: A comprehensive survey** (2026) <a href="https://arxiv.org/abs/2502.10498"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Latent World Models for Automated Driving: A Unified Taxonomy, Evaluation Framework, and Open Challenges** (2026) <a href="https://arxiv.org/abs/2603.09086"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Towards Generalist Embodied AI: A Survey on World Models for VLA Agents** (2026) <a href="https://arxiv.org/abs/2503.18942"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.2 Foundations & Classic MBRL


- **What uncertainties do we need in bayesian deep learning for computer vision?** (2017) <a href="https://arxiv.org/abs/1703.04977"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Recurrent world models facilitate policy evolution** (2018) <a href="https://arxiv.org/abs/1809.01999"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **World Models** (2018) <a href="https://arxiv.org/abs/1803.10122"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **When to Trust Your Model: Model-Based Policy Optimization** (2019) <a href="https://arxiv.org/abs/1906.08253"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Learning to poke by poking: Experiential learning of intuitive physics** (2019) <a href="https://arxiv.org/abs/1606.07419"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Mastering atari with discrete world models** (2020) <a href="https://arxiv.org/abs/2010.02193"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Planning to Explore via Self-Supervised World Models** (2020) <a href="https://arxiv.org/abs/2005.05960"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A Generalist Agent** (2022) <a href="https://arxiv.org/abs/2205.06175"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Model-Based Imitation Learning for Urban Driving** (2022) <a href="https://arxiv.org/abs/2210.07729"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Language models represent space and time** (2023) <a href="https://arxiv.org/abs/2310.02207"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Geollm: Extracting geospatial knowledge from large language models** (2023) <a href="https://arxiv.org/abs/2310.06213"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Leveraging pre-trained large language models to construct and utilize world models for model-based task planning** (2023) <a href="https://arxiv.org/abs/2305.14909"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Self-supervised learning from images with a joint-embedding predictive architecture** (2023) <a href="https://arxiv.org/abs/2301.08243"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Language models meet world models: Embodied experiences enhance language models** (2023) <a href="https://arxiv.org/abs/2305.10626"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Uncertainty-Aware Model-Based Offline Reinforcement Learning for Automated Driving** (2023) <a href="https://arxiv.org/abs/2212.04123"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Driving into the Future: Multiview Visual Forecasting and Planning** (2024) <a href="https://arxiv.org/abs/2311.17918"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Revisiting feature prediction for learning visual representations from video** (2024) <a href="https://arxiv.org/abs/2404.08471"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Learning and leveraging world models in visual representation learning** (2024) <a href="https://arxiv.org/abs/2403.00504"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Efficient and scalable reinforcement learning for large-scale network control** (2024) <a href="https://arxiv.org/abs/2410.17221"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Training agents inside of scalable world models** (2025) <a href="https://arxiv.org/abs/2509.24527"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Thinking in space: How multimodal large language models see, remember, and recall spaces** (2025) <a href="https://arxiv.org/abs/2412.14171"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Smart Exploration in Reinforcement Learning using Bounded Uncertainty Models** (2026) <a href="https://arxiv.org/abs/2504.05978"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **MEM: Multi-Scale Embodied Memory for Vision Language Action Models** (2026) <a href="https://arxiv.org/abs/2603.03596"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.3 Dreamer Family (Latent World Models)

- **Dream to control: Learning behaviors by latent imagination** (2019) <a href="https://arxiv.org/abs/1912.01603"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Learning latent dynamics for planning from pixels** (2019) <a href="https://arxiv.org/abs/1811.04551"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Planet: Model-based reinforcement learning for multi-goal visual control** (2020) <a href="https://arxiv.org/abs/2003.00370"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Daydreamer: World models for physical robot learning** (2023) <a href="https://arxiv.org/abs/2206.14176"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DreamerV3: Mastering Diverse Domains through World Models** (2023) <a href="https://arxiv.org/abs/2301.04104"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DriveDreamer: Towards Real-World-Driven World Models for Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2309.09777"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DriveDreamer-2: LLM-enhanced world models for diverse driving video generation** (2025) <a href="https://arxiv.org/abs/2403.06845"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.4 Uncertainty-Driven Exploration in World Models

- **Model-based active exploration** (2019) <a href="https://arxiv.org/abs/1810.12162"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **RIDE: Rewarding Impact-Driven Exploration for Procedurally-Generated Environments** (2020) <a href="https://arxiv.org/abs/2002.12292"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Curiosity in Hindsight: Intrinsic Exploration in Stochastic Environments** (2022) <a href="https://arxiv.org/abs/2211.10515"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


- **Active Exploration in Bayesian Model-based Reinforcement Learning for Robot Manipulation** (2024) <a href="https://arxiv.org/abs/2404.01867"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **World Model Robustness via Surprise Recognition** (2025) <a href="https://arxiv.org/abs/2512.01119"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Beyond Noisy-TVs: Noise-Robust Exploration Via Learning Progress Monitoring** (2025) <a href="https://arxiv.org/abs/2509.25438"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Curiosity-Driven Imagination: Discovering Plan Operators and Learning Associated Policies for Open-World Adaptation** (2025) <a href="https://arxiv.org/abs/2503.04931"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **The Impact of Intrinsic Rewards on Exploration in Reinforcement Learning** (2025) <a href="https://arxiv.org/abs/2501.11533"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Latent Reasoning in LLMs as a Vocabulary-Space Superposition** (2025) <a href="https://arxiv.org/abs/2510.15522"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Exploring Representation-Aligned Latent Space for Better Generation** (2025) <a href="https://arxiv.org/abs/2502.00359"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **ActSafe: Active Exploration with Safety Constraints for Reinforcement Learning** (2025) <a href="https://arxiv.org/abs/2410.09486"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **General Exploratory Bonus for Optimistic Exploration in RLHF** (2025) <a href="https://arxiv.org/abs/2510.03269"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


- **SuS: Strategy-aware Surprise for Intrinsic Exploration** (2026) <a href="https://arxiv.org/abs/2601.10349"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.5 Competence-Driven MBRL & Safe Exploration







- **Deep exploration via bootstrapped DQN** (2016) <a href="https://arxiv.org/abs/1602.04621"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Learning and policy search in stochastic dynamical systems with bayesian neural networks** (2016) <a href="https://arxiv.org/abs/1605.07127"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Mastering the game of Go with deep neural networks and tree search** (2016) <a href="https://arxiv.org/abs/1712.01815"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Mastering chess and shogi by self-play with a general reinforcement learning algorithm** (2017) <a href="https://arxiv.org/abs/1712.01815"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Prediction and control with temporal segment models** (2017) <a href="https://arxiv.org/abs/1703.04070"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Algorithmic framework for model-based deep reinforcement learning with theoretical guarantees** (2018) <a href="https://arxiv.org/abs/1807.03858"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Sample-Efficient Reinforcement Learning with Stochastic Ensemble Value Expansion** (2018) <a href="https://arxiv.org/abs/1807.01675"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Lipschitz Continuity in Model-based Reinforcement Learning** (2018) <a href="https://arxiv.org/abs/1804.07193"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Deep Reinforcement Learning in a Handful of Trials using Probabilistic Dynamics Models** (2018) <a href="https://arxiv.org/abs/1805.12114"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Model-ensemble trust-region policy optimization** (2018) <a href="https://arxiv.org/abs/1802.10592"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Convergence of learning dynamics in stackelberg games** (2019) <a href="https://arxiv.org/abs/1906.01217"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A game theoretic framework for model based reinforcement learning** (2020) <a href="https://arxiv.org/abs/2004.07804"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Stochastic latent actor-critic: Deep reinforcement learning with a latent variable model** (2020) <a href="https://arxiv.org/abs/1907.00953"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Offline reinforcement learning as one big sequence modeling problem** (2021) <a href="https://arxiv.org/abs/2106.02039"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Model-based reinforcement learning with multi-hop reasoning** (2023) <a href="https://arxiv.org/abs/2309.12412"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Differentiable Information Enhanced Model-Based Reinforcement Learning** (2025) <a href="https://arxiv.org/abs/2503.01178"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Long-Horizon Model-Based Offline Reinforcement Learning Without Conservatism** (2025) <a href="https://arxiv.org/abs/2512.04341"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A Unified Uncertainty-Aware Exploration: Combining Epistemic and Aleatory Uncertainty** (2025) <a href="https://arxiv.org/abs/2401.02914"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Better World Models Can Lead to Better Post-Training Performance** (2025) <a href="https://arxiv.org/abs/2512.03400"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **The Reality Gap in Robotics: Challenges, Solutions, and Best Practices** (2025) <a href="https://arxiv.org/abs/2510.20808"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Accelerating Model-Based Reinforcement Learning with State-Space World Models** (2025) <a href="https://arxiv.org/abs/2502.20168"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


- **World model architectures in reinforcement learning: an exploration of strengths and limitations** (2025) <a href="https://arxiv.org/abs/2406.00483"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.6 Video Generation as World Models

- **Video Diffusion Models** (2022) <a href="https://arxiv.org/abs/2204.03458"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Scalable Diffusion Models with Transformers** (2023) <a href="https://arxiv.org/abs/2212.09748"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Video Generation Models as World Simulators** (2024) <a href="https://arxiv.org/abs/2402.17177"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **V-JEPA: Latent Video Prediction with Joint-Embedding Predictive Architecture** (2024) <a href="https://arxiv.org/abs/2404.08471"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Genie: Generative Interactive Environments** (2024) <a href="https://arxiv.org/abs/2402.15391"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **VBench: Comprehensive Benchmark Suite for Video Generative Models** (2024) <a href="https://arxiv.org/abs/2311.17982"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Worldgpt: Empowering llm as multimodal world model** (2024) <a href="https://arxiv.org/abs/2404.18202"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **V-jepa 2: Self-supervised video models enable understanding, prediction and planning** (2025) <a href="https://arxiv.org/abs/2506.09985"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Huvidpo: Enhancing video generation through direct preference optimization for human-centric alignment** (2025) <a href="https://arxiv.org/abs/2502.01690"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Video-t1: Test-time scaling for video generation** (2025) <a href="https://arxiv.org/abs/2503.18942"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Videodpo: Omni-preference alignment for video diffusion generation** (2025) <a href="https://arxiv.org/abs/2412.14167"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **TAGRPO: Boosting GRPO on Image-to-Video Generation with Direct Trajectory Alignment** (2026) <a href="https://arxiv.org/abs/2601.05729"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Inference-time Physics Alignment of Video Generative Models with Latent World Models** (2026) <a href="https://arxiv.org/abs/2601.10553"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.7 Autonomous Driving World Models


- **CARLA: An Open Urban Driving Simulator** (2017) <a href="https://arxiv.org/abs/1711.03938"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **nuScenes: A Multimodal Dataset for Autonomous Driving** (2020) <a href="https://arxiv.org/abs/1903.11027"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Scalability in Perception for Autonomous Driving: Waymo Open Dataset** (2020) <a href="https://arxiv.org/abs/1912.04838"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **FIERY: Future Instance Prediction in Bird's-Eye View from Surround Monocular Cameras** (2021) <a href="https://arxiv.org/abs/2104.10490"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **MILE: Model-Based Imitation Learning in Dot-Product Latent Spaces** (2022) <a href="https://arxiv.org/abs/2210.07729"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Ego4D: Around the World in 3,000 Hours of Egocentric Video** (2022) <a href="https://arxiv.org/abs/2110.07058"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **GAIA-1: A Generative AI for Autonomous Driving** (2023) <a href="https://arxiv.org/abs/2309.17080"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **OccWorld: Learning a Visual World Model for Autonomous Driving** (2023) <a href="https://arxiv.org/abs/2311.16038"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **UniWorld: Autonomous Driving World Model as a Foundation Model** (2023) <a href="https://arxiv.org/abs/2308.01538"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **TrafficBots: Towards World Models for Autonomous Driving Simulation and Motion Prediction** (2023) <a href="https://arxiv.org/abs/2303.04116"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Planning-oriented Autonomous Driving** (2023) <a href="https://arxiv.org/abs/2212.10156"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **UniSim: A neural closed-loop sensor simulator** (2023) <a href="https://arxiv.org/abs/2308.01898"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **OpenScene: The Largest Up-to-Date 3D Occupancy Prediction Benchmark in Autonomous Driving** (2023) <a href="https://arxiv.org/abs/2304.14365"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Gaia-1: A generative world model for autonomous driving** (2023) <a href="https://arxiv.org/abs/2309.17080"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **BEVControl: Accurately controlling street-view elements with multi-perspective consistency via bev sketch layout** (2023) <a href="https://arxiv.org/abs/2308.01661"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Language Conditioned Traffic Generation** (2023) <a href="https://arxiv.org/abs/2307.07947"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Drive-WM: Multi-view World Model for Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2311.17918"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **VAD-v2: End-to-End Vectorized Autonomous Driving via Probabilistic Planning** (2024) <a href="https://arxiv.org/abs/2402.13204"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **MagicDrive: Street View Generation with Diverse 3D Geometry Control** (2024) <a href="https://arxiv.org/abs/2310.02601"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **VADv2: End-to-End Vectorized Autonomous Driving via Probabilistic Planning** (2024) <a href="https://arxiv.org/abs/2402.13243"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Copilot4D: Learning Unsupervised World Models for Autonomous Driving via Discrete Diffusion** (2024) <a href="https://arxiv.org/abs/2311.01017"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **SimGen: Simulator-conditioned Driving Scene Generation** (2024) <a href="https://arxiv.org/abs/2406.09386"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Think2Drive: Efficient Reinforcement Learning by Thinking with Latent World Model for Autonomous Driving (in CARLA-V2)** (2024) <a href="https://arxiv.org/abs/2402.16720"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DriveWorld: 4D Pre-trained Scene Understanding via World Models for Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2405.04390"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **OccSora: 4D Occupancy Generation Models as World Simulators for Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2405.20337"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DrivingDiffusion: Layout-Guided Multi-view Driving Scenarios Video Generation with Latent Diffusion Model** (2024) <a href="https://arxiv.org/abs/2310.07771"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DriveArena: A Closed-Loop Generative Simulation Platform for Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2408.00415"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **UMAD: Unsupervised Mask-Level Anomaly Detection for Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2406.06370"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **UniPAD: A universal pre-training paradigm for autonomous driving** (2024) <a href="https://arxiv.org/abs/2310.08370"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DrivingWorld: Constructing World Model for Autonomous Driving via Video GPT** (2024) <a href="https://arxiv.org/abs/2412.19505"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Vista: A Generalizable Driving World Model with High Fidelity and Versatile Controllability** (2024) <a href="https://arxiv.org/abs/2405.17398"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Panacea: Panoramic driving scene generation with collaborative view diffusion** (2024) <a href="https://arxiv.org/abs/2404.12345"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **RealGen: Retrieval Augmented Generation for Controllable Traffic Scenarios** (2024) <a href="https://arxiv.org/abs/2312.13303"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Delphi: Unleashing Generalization of End-to-End Autonomous Driving with Controllable Long Video Generation** (2024) <a href="https://arxiv.org/abs/2406.01349"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **LimSim++: A Closed-Loop Platform for Deploying Multimodal LLMs in Autonomous Driving** (2024) <a href="https://arxiv.org/abs/2402.01246"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **AD-L-JEPA: Self-Supervised Spatial World Models with Joint Embedding Predictive Architecture for Autonomous Driving with LiDAR Data** (2025) <a href="https://arxiv.org/abs/2501.04969"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **GenAD: Generative End-to-End Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2402.11502"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Driving in the Occupancy World: Vision-Centric 4D Occupancy Forecasting and Planning via World Models for Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2408.14197"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **OccWorld: Learning a 3D Occupancy World Model for Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2311.16038"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DynamicCity: Large-Scale 4D Occupancy Generation from Dynamic Scenes** (2025) <a href="https://arxiv.org/abs/2410.18084"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Gaussian World: Gaussian World Model for Streaming 3D Occupancy Prediction** (2025) <a href="https://arxiv.org/abs/2412.10373"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DrivingSphere: Building a High-Fidelity 4D World for Closed-Loop Simulation** (2025) <a href="https://arxiv.org/abs/2411.11252"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Raw2Drive: Reinforcement Learning with Aligned World Models for End-to-End Autonomous Driving (in CARLA-V2)** (2025) <a href="https://arxiv.org/abs/2505.16394"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **World4Drive: End-to-End Autonomous Driving via Intention-Aware Physical Latent World Model** (2025) <a href="https://arxiv.org/abs/2507.00603"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **GeoDrive: 3D Geometry-Informed Driving World Model with Precise Action Control** (2025) <a href="https://arxiv.org/abs/2505.22421"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **VL-SAFE: Vision-Language Guided Safety-Aware Reinforcement Learning with World Models for Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2505.16377"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **World Model-based End-to-End Scene Generation for Accident Anticipation in Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2507.12762"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **UncAD: Towards Safe End-to-end Autonomous Driving via Online Map Uncertainty** (2025) <a href="https://arxiv.org/abs/2504.12826"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **AdaWM: Adaptive World Model based Planning for Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2501.13072"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **An Anatomy of Vision-Language-Action Models: From Modules to Milestones and Challenges** (2025) <a href="https://arxiv.org/abs/2512.11362"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **MindDrive: An All-in-One Framework Bridging World Models and Vision-Language Model for End-to-End Autonomous Driving** (2025) <a href="https://arxiv.org/abs/2512.04441"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Latent-WAM: Latent World Action Modeling for End-to-End Autonomous Driving** (2026) <a href="https://arxiv.org/abs/2603.24581"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.8 World Action Models & VLA

- **RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control** (2023) <a href="https://arxiv.org/abs/2307.15818"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **OpenVLA: An Open-Source Vision-Language-Action Model** (2024) <a href="https://arxiv.org/abs/2406.09246"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **RLVR-World: Training World Models with Reinforcement Learning** (2025) <a href="https://arxiv.org/abs/2505.13934"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>



- **Next-Latent Prediction Transformers Learn Compact World Models** (2025) <a href="https://arxiv.org/abs/2511.05963"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Act2Goal: From World Model To General Goal-conditioned Policy** (2025) <a href="https://arxiv.org/abs/2512.23541"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


- **WorldVLA: Towards Autoregressive Action World Model** (2025) <a href="https://arxiv.org/abs/2506.21539"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **10 Open Challenges Steering the Future of Vision-Language-Action Models** (2025) <a href="https://arxiv.org/abs/2511.05936"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning** (2025) <a href="https://arxiv.org/abs/2601.16163"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **DM0: An Embodied-Native Vision-Language-Action Model towards Physical AI** (2025) <a href="https://arxiv.org/abs/2602.14974"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Large Video Planner Enables Generalizable Robot Control** (2025) <a href="https://arxiv.org/abs/2512.15840"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **mimic-video: Video-Action Models for Generalizable Robot Control Beyond VLAs** (2025) <a href="https://arxiv.org/abs/2512.15692"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Evaluating Gemini Robotics Policies in a Veo World Simulator** (2025) <a href="https://arxiv.org/abs/2512.10675"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Ctrl-World: A Controllable Generative World Model for Robot Manipulation** (2025) <a href="https://arxiv.org/abs/2510.10125"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **WorldGym: World Model as An Environment for Policy Evaluation** (2025) <a href="https://arxiv.org/abs/2506.00613"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Ctrl-World: Action-Conditioned World Models for Vision-Language-Action Policies** (2026) <a href="https://arxiv.org/abs/2510.10125"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Do World Action Models Generalize Better than VLAs? A Robustness Study** (2026) <a href="https://arxiv.org/abs/2603.22078"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **GigaWorld-Policy: An Efficient Action-Centered World-Action Model** (2026) <a href="https://arxiv.org/abs/2603.17240"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **World Action Models are Zero-shot Policies** (2026) <a href="https://arxiv.org/abs/2602.15922"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Fast-WAM: Do World Action Models Need Test-time Future Imagination?** (2026) <a href="https://arxiv.org/abs/2603.16666"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **PlayWorld: Learning Robot World Models from Autonomous Play** (2026) <a href="https://arxiv.org/abs/2603.09030"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.9 Multi-Agent & Social World Models

- **Machine theory of mind** (2018) <a href="https://arxiv.org/abs/1802.07740"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **M $\^ 3$ RL: Mind-aware Multi-agent Management Reinforcement Learning** (2018) <a href="https://arxiv.org/abs/1810.00147"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Theory of minds: Understanding behavior in groups through inverse planning** (2019) <a href="https://arxiv.org/abs/1901.06085"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Social-STGCNN: A Social Spatio-Temporal Graph Convolutional Neural Network** (2020) <a href="https://arxiv.org/abs/2002.11927"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **The societal implications of deep reinforcement learning** (2021) <a href="https://arxiv.org/abs/2108.12427"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Model-based multi-agent reinforcement learning: Recent progress and prospects** (2022) <a href="https://arxiv.org/abs/2203.10603"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Models as agents: Optimizing multi-step predictions of interactive local models in model-based multi-agent reinforcement learning** (2023) <a href="https://arxiv.org/abs/2303.17984"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **World Models Should Prioritize the Unification of Physical and Social Dynamics** (2025) <a href="https://arxiv.org/abs/2510.21219"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Social world model-augmented mechanism design policy learning** (2025) <a href="https://arxiv.org/abs/2510.19270"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Agent learning via early experience** (2025) <a href="https://arxiv.org/abs/2510.08558"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.10 Causal & Hierarchical World Models



- **Hierarchical deep reinforcement learning: Integrating temporal abstraction and intrinsic motivation** (2016) <a href="https://arxiv.org/abs/1604.06057"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Feudal networks for hierarchical reinforcement learning** (2017) <a href="https://arxiv.org/abs/1703.01161"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Learning independent causal mechanisms** (2018) <a href="https://arxiv.org/abs/1712.00961"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Learning functional causal models with generative neural networks** (2018) <a href="https://arxiv.org/abs/1709.05321"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Data-efficient hierarchical reinforcement learning** (2018) <a href="https://arxiv.org/abs/1805.08296"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


- **Time-agnostic prediction: Predicting predictable video frames** (2018) <a href="https://arxiv.org/abs/1808.07784"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Neural-Symbolic Descriptive Action Model from Images: The Search for STRIPS** (2019) <a href="https://arxiv.org/abs/1912.05492"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **A meta-transfer objective for learning to disentangle causal mechanisms** (2019) <a href="https://arxiv.org/abs/1901.10912"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **CLEVRER: Collision events for video representation and reasoning** (2019) <a href="https://arxiv.org/abs/1910.01442"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


- **Causal discovery in physical systems from videos** (2020) <a href="https://arxiv.org/abs/2007.00631"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Reasoning about physical interactions with object-oriented prediction and planning** (2020) <a href="https://arxiv.org/abs/2008.03269"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **ACRE: Abstract causal reasoning beyond covariation** (2021) <a href="https://arxiv.org/abs/2103.14232"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Distilling critical paths of transformers for explainable natural language inference** (2021) <a href="https://arxiv.org/abs/2106.11340"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Skill-based meta-reinforcement learning** (2021) <a href="https://arxiv.org/abs/2107.06995"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Hierarchical world models for exploration and control** (2022) <a href="https://arxiv.org/abs/2206.04114"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Towards causal representation learning** (2022) <a href="https://arxiv.org/abs/2102.11107"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>



- **Exploring the limits of hierarchical world models in reinforcement learning** (2024) <a href="https://arxiv.org/abs/2406.00483"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


### 4.11 Benchmarks, Simulators & Datasets


- **The arcade learning environment: An evaluation platform for general agents** (2013) <a href="https://arxiv.org/abs/1207.4708"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Deepmind control suite** (2018) <a href="https://arxiv.org/abs/1801.00690"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **RT-1: Robotics Transformer for Real-World Control at Scale** (2022) <a href="https://arxiv.org/abs/2212.06817"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **SayCan: Do As I Can, Not As I Say: Grounding Language in Robotic Affordances** (2022) <a href="https://arxiv.org/abs/2204.01691"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Open x-embodiment: Robotic learning datasets and rt-x models** (2023) <a href="https://arxiv.org/abs/2310.08864"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **PaLM-E: An Embodied Multimodal Language Model** (2023) <a href="https://arxiv.org/abs/2303.03378"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **VIMA: General Robot Manipulation with Multimodal Prompts** (2023) <a href="https://arxiv.org/abs/2210.03094"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **RoboCat: A Self-Improving Generalist Agent for Robotic Manipulation** (2023) <a href="https://arxiv.org/abs/2306.11706"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **Octo: An Open-Source Generalist Robot Policy** (2023) <a href="https://arxiv.org/abs/2312.11592"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **VC-1: A Visual Foundation Model for Embodied AI** (2023) <a href="https://arxiv.org/abs/2303.18240"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>

- **ManiGaussian: Dynamic Gaussian Splatting for Manipulation** (2024) <a href="https://arxiv.org/abs/2403.08321"><img src="https://img.shields.io/badge/Paper-red?logo=arxiv&logoColor=white"></a>


---

<br>

## 5. Level 5: Prospector → Ecosystem — Coordination-Space Exploration

<p align="center"><img src="fig/level5_ecosystem.png" width="850"/></p>
<p align="center"><i>Figure: Level 5 Coordination-Space Exploration — Why (single-agent limitations), Where (communication, collaboration, role, deployment), and How (orchestration, ensemble, MARL, self-evolving agents).</i></p>

At the highest level, exploration enters **coordination space**: heterogeneous agents discover communication topologies, role specialisations, shared representations, and collaborative strategies.

| Challenge | Description |
|:----------|:------------|
| **Scalable Coordination Exploration** | The search space is combinatorial, hierarchical, and dynamic—which agents to activate, what communication to establish, how information flows |
| **Ecosystem-Level Credit Assignment** | Disentangling behavioural contribution from structural contribution under sparse, delayed feedback |
| **Diversity vs. Convergence Tension** | Balancing ecological diversity against system-level coherence |
| **Role–Communication Co-evolution** | Jointly evolving functional specialisation and information exchange protocols |

**Key Systems & Methods:**

| Method | Key Contribution |
|:-------|:-----------------|
| **MetaGPT** | Structured multi-agent coordination with role-based workflows |
| **AutoGen** | Flexible conversational multi-agent framework |
| **CAMEL** | Communicative agents for mind exploration |
| **Multi-agent Debate** | Structured deliberation improving collective reasoning (Du et al.) |
| **Learnable orchestration** | RL-evolved coordination topologies, optimisable agent graphs |






### 5.2 Agentic Ensemble Papers




#### 5.2.1 Ensemble-During-Inference Papers



| Date | Name | Title | Paper | Github |
|:---:|:---:|---|:---:|:---:|
| 2025-10 | `SAFE` | When to Ensemble: Identifying Token-Level Points for Stable and Fast LLM Ensembling | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/pdf/2510.15346) | - |
| 2025-10 | `CoRe` | Harnessing Consistency for Robust Test-Time LLM Ensemble | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://www.arxiv.org/abs/2510.13855) | - |
| 2025-05 | `Transformer Copilot` | Transformer Copilot: Learning from The Mistake Log in LLM Fine-tuning | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.16270) | [![GitHub Stars](https://img.shields.io/github/stars/jiaruzouu/TransformerCopilot?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/jiaruzouu/TransformerCopilot) |
| 2025-02 | `ABE` | Token-level Ensembling of Models with Different Vocabularies | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.21265) | [![GitHub Stars](https://img.shields.io/github/stars/mjpost/abe?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/mjpost/abe) |
| 2025-02 | `CITER` | CITER: Collaborative Inference for Efficient Large Language Model Decoding with Token-Level Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.01976) | [![GitHub Stars](https://img.shields.io/github/stars/aiming-lab/CITER?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/aiming-lab/CITER) |
| 2025-02 | `Speculative Ensemble` | Speculative Ensemble: Fast Large Language Model Ensemble via Speculation | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.01662) | [![GitHub Stars](https://img.shields.io/github/stars/Kamichanw/Speculative-Ensemble?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/Kamichanw/Speculative-Ensemble/) |
| 2024-10 | `UniTe` | Determine-Then-Ensemble: Necessity of Top-k Union for Large Language Model Ensembling | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.03777) | - |
| 2024-06 | `GaC` | Breaking the Ceiling of the LLM Community by Treating Token Generation as a Classification for Ensembling | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2406.12585) | [![GitHub Stars](https://img.shields.io/github/stars/yaoching0/GaC?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/yaoching0/GaC) |
| 2024-04 | `DeePEn` | Ensemble Learning for Heterogeneous Large Language Models with Deep Parallel Collaboration | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.12715) | [![GitHub Stars](https://img.shields.io/github/stars/OrangeInSouth/DeePEn?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/OrangeInSouth/DeePEn) |
| 2024-04 | `PackLLM` | Pack of LLMs: Model Fusion at Test-Time via Perplexity Optimization | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.11531) | [![GitHub Stars](https://img.shields.io/github/stars/cmavro/PackLLM?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/cmavro/PackLLM) |
| 2024-04 | `EVA` | Bridging the Gap between Different Vocabularies for LLM Ensemble | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.09492) | [![GitHub Stars](https://img.shields.io/github/stars/xydaytoy/EVA?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/xydaytoy/EVA) |
| 2024-02 | `-` | Purifying large language models by ensembling a small language model | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2402.14845) | - |


| Date | Name | Title | Paper | Github |
|:---:|:---:|---|:---:|:---:|
| 2025-06 | `RLAE` | RLAE: Reinforcement Learning-Assisted Ensemble for LLMs | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.00439) | - |
| 2024-12 | `SpecFuse` | SpecFuse: Ensembling Large Language Models via Next-Segment Prediction | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.07380) | - |
| 2024-09 | `SweetSpan` | Hit the Sweet Spot! Span-Level Ensemble for Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.18583) | - |
| 2024-07 | `Cool-Fusion` | Cool-Fusion: Fuse Large Language Models without Training | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2407.19807) | - |


| Date | Name | Title | Paper | Github |
|:---:|:---:|---|:---:|:---:|
| 2025-11 | `CBS` | Collaborative Beam Search: Enhancing LLM Reasoning via Collective Consensus | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://aclanthology.org/2025.emnlp-main.574/) | - |
| 2024-12 | `LE-MCTS` | Ensembling Large Language Models with Process Reward-Guided Tree Search for Better Complex Reasoning | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.15797) | - |



#### 5.2.2  Ensemble-After-Inference Papers


| Date | Name | Title | Paper | Github |
|:---:|:---:|---|:---:|:---:|
| 2025-12 | `LLM-PeerReview` | Scoring, Reasoning, and Selecting the Best! Ensembling Large Language Models via a Peer-Review Process | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.23213) | [![GitHub Stars](https://img.shields.io/github/stars/zeyuji/LLM-PeerReview?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/zeyuji/LLM-PeerReview) |
| 2025-10 | `LLMartini` | LLMartini: Seamless and Interactive Leveraging of Multiple LLMs through Comparison and Composition | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.19252) | - |
| 2025-10 | `-` | Beyond Consensus: Mitigating the Agreeableness Bias in LLM Judge Evaluations | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.11822) | [![GitHub Stars](https://img.shields.io/github/stars/ai-cet/paper-arxiv-llm-judge-calibration?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ai-cet/paper-arxiv-llm-judge-calibration) |
| 2025-10 | `OW/ISP` | Beyond Majority Voting: LLM Aggregation by Leveraging Higher-Order Information | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://www.arxiv.org/abs/2510.01499) | - |
| 2025-09 | `FLAME` | Explainable Fault Localization for Programming Assignments via LLM-Guided Annotation | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/pdf/2509.25676v1) | [![GitHub Stars](https://img.shields.io/github/stars/FLAME-FL/FLAME?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/FLAME-FL/FLAME) |
| 2025-09 | `CARGO` | CARGO: A Framework for Confidence-Aware Routing of Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.14899) | - |
| 2025-07 | `LENS` | LENS: Learning Ensemble Confidence from Neural States for Multi-LLM Answer Integration | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2507.23167) | - |
| 2025-05 | `EL4NER` | EL4NER: Ensemble Learning for Named Entity Recognition via Multiple Small-Parameter Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.23038) | - |
| 2025-03 | `Symbolic-MoE` | Symbolic Mixture-of-Experts: Adaptive Skill-based Routing for Heterogeneous Reasoning | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.05641) | [![GitHub Stars](https://img.shields.io/github/stars/dinobby/Symbolic-MoE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/dinobby/Symbolic-MoE/) |
| 2025-01 | `DFPE` | DFPE: A Diverse Fingerprint Ensemble for Enhancing LLM Performance | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2501.17479) | [![GitHub Stars](https://img.shields.io/github/stars/nivgold/DFPE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/nivgold/DFPE) |
| 2025-01 | `DMoA` | Balancing Act: Diversity and Consistency in Large Language Model Ensembles | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://openreview.net/pdf?id=Dl6nkKKvlX) | - |
| 2024-12 | `Smoothie` | Smoothie: Label Free Language Model Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.04692) | [![GitHub Stars](https://img.shields.io/github/stars/HazyResearch/smoothie?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/HazyResearch/smoothie) |
| 2024-10 | `LLM-Forest` | LLM-Forest: Ensemble Learning of LLMs with Graph-Augmented Prompts for Data Imputation | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.21520) | [![GitHub Stars](https://img.shields.io/github/stars/Xinrui17/LLM-Forest?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/Xinrui17/LLM-Forest) |
| 2024-10 | `LLM-TOPLA` | LLM-TOPLA: Efficient LLM Ensemble by Maximising Diversity | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.03953) | [![GitHub Stars](https://img.shields.io/github/stars/git-disl/llm-topla?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/git-disl/llm-topla) |
| 2024-10 | `MLKF` | Two Heads are Better than One: Zero-shot Cognitive Reasoning via Multi-LLM Knowledge Fusion | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://dl.acm.org/doi/abs/10.1145/3627673.3679744) | [![GitHub Stars](https://img.shields.io/github/stars/trueBatty/MLKF?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/trueBatty/MLKF) |
| 2024-08 | `URG` | URG: A Unified Ranking and Generation Method for Ensembling Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://aclanthology.org/2024.findings-acl.261/) | - |
| 2024-02 | `Agent-Forest` | More Agents Is All You Need | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2402.05120) | [![GitHub Stars](https://img.shields.io/github/stars/MoreAgentsIsAllYouNeed/AgentForest?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/MoreAgentsIsAllYouNeed/AgentForest) |
| 2023-06 | `LLM-Blender` | LLM-Blender: Ensembling Large Language Models with Pairwise Ranking and Generative Fusion | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2306.02561) | [![GitHub Stars](https://img.shields.io/github/stars/yuchenlin/LLM-Blender?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/yuchenlin/LLM-Blender) |
| 2023-05 | `MoRE` | Getting MoRE out of Mixture of Language Model Reasoning Experts | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2305.14628) | [![GitHub Stars](https://img.shields.io/github/stars/NoviScl/MoRE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/NoviScl/MoRE) |


#### 5.2.3 Ensemble-Before-Inference Papers


| Date | Name | Title | Paper | Github |
|:---:|:---:|---|:---:|:---:|
| 2025-10 | `DiSRouter` | DISROUTER: Distributed Self-Routing for LLM Selections | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.19208) | - |
| 2025-10 | `WebRouter` | WebRouter: Query-specific Router via Variational Information Bottleneck for Cost-sensitive Web Agent | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.11221) | - |
| 2025-10 | `LLMRank` | LLMRank: Understanding LLM Strengths for Model Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.01234) | - |
| 2025-06 | `TagRouter` | TAGROUTER: Learning Route to LLMs through Tags for Open-Domain Text Generation Tasks | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.12473) | - |
| 2025-06 | `Router-R1` | Router-R1: Teaching LLMs Multi-Round Routing and Aggregation via Reinforcement Learning | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.09033) | [![GitHub Stars](https://img.shields.io/github/stars/ulab-uiuc/Router-R1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ulab-uiuc/Router-R1) |
| 2025-06 | `RadialRouter` | RadialRouter: Structured Representation for Efficient and Robust Large Language Models Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://www.arxiv.org/abs/2506.03880) | - |
| 2025-05 | `Avengers` | The Avengers: A Simple Recipe for Uniting Smaller Language Models to Challenge Proprietary Giants | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.19797) | [![GitHub Stars](https://img.shields.io/github/stars/ZhangYiqun018/Avengers?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ZhangYiqun018/Avengers) |
| 2025-05 | `RTR` | Route to Reason: Adaptive Routing for LLM and Reasoning Strategy Selection | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.19435) | [![GitHub Stars](https://img.shields.io/github/stars/goodmanpzh/Route-To-Reason?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/goodmanpzh/Route-To-Reason) |
| 2025-05 | `InferenceDynamics` | InferenceDynamics: Efficient Routing Across LLMs through Structured Capability and Knowledge Profiling | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.16303) | - |
| 2025-05 | `-` | Rethinking Predictive Modeling for LLM Routing: When Simple kNN Beats Complex Learned Routers | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.12601) | - |
| 2025 | `RELM` | Co-optimizing Recommendation and Evaluation for LLM Selection | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://openreview.net/pdf?id=gWi4ZcPQRl) | - |
| 2025-02 | `-` | LLM Bandit: Cost-Efficient LLM Generation via Preference-Conditioned Dynamic Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.02743) | - |
| 2024-12 | `PickLLM` | PickLLM: Context-Aware RL-Assisted Large Language Model Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.12170) | - |
| 2024-12 | `Bench-CoE` | Bench-CoE: a Framework for Collaboration of Experts from Benchmark | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.04167) | [![GitHub Stars](https://img.shields.io/github/stars/ZhangXJ199/Bench-CoE?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ZhangXJ199/Bench-CoE) |
| 2024-10 | `GraphRouter` | GraphRouter: A Graph-based Router for LLM Selections | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.03834) | [![GitHub Stars](https://img.shields.io/github/stars/ulab-uiuc/GraphRouter?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ulab-uiuc/GraphRouter) |
| 2024-09 | `Eagle` | Eagle: Efficient Training-Free Router for Multi-LLM Inference | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.15518) | - |
| 2024-08 | `TO-Router` | TensorOpera Router: A Multi-Model Router for Efficient LLM Inference | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2408.12320) | - |
| 2024-08 | `SelectLLM` | SelectLLM: Query-Aware Efficient Selection Algorithm for Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2408.08545) | - |
| 2024-07 | `MetaLLM` | MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2407.10834) | [![GitHub Stars](https://img.shields.io/github/stars/mail-research/MetaLLM-wrapper?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/mail-research/MetaLLM-wrapper/) |
| 2024-06 | `RouteLLM` | RouteLLM: Learning to Route LLMs with Preference Data | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2406.18665) | [![GitHub Stars](https://img.shields.io/github/stars/lm-sys/RouteLLM?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/lm-sys/RouteLLM) |
| 2024-06 | `HomoRouter` | Query Routing for Homogeneous Tools: An Instantiation in the RAG Scenario | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2406.12429) | - |
| 2024-05 | `-` | Harnessing the Power of Multiple Minds: Lessons Learned from LLM Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2405.00467) | [![GitHub Stars](https://img.shields.io/github/stars/kvadityasrivatsa/llm-routing?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/kvadityasrivatsa/llm-routing) |
| 2024-04 | `Hybrid-LLM` | Hybrid LLM: Cost-Efficient and Quality-Aware Query Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.14618) | [![GitHub Stars](https://img.shields.io/github/stars/m365-core/hybrid_llm_routing?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/m365-core/hybrid_llm_routing) |
| 2024-03 | `ETR` | An Expert is Worth One Token: Synergizing Multiple Expert LLMs as Generalist via Expert Token Routing | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2403.16854) | [![GitHub Stars](https://img.shields.io/github/stars/zjunet/ETR?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/zjunet/ETR) |
| 2024-01 | `Routoo` | Routoo: Learning to Route to Large Language Models Effectively | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2401.13979) | - |
| 2024-01 | `Blending` | Blending Is All You Need: Cheaper, Better Alternative to Trillion-Parameters LLM | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2401.02994) | - |
| 2024 | `RouterDC` | RouterDC: Query-Based Router by Dual Contrastive Learning for Assembling Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7a641b8ec86162fc875fb9f6456a542f-Abstract-Conference.html) | [![GitHub Stars](https://img.shields.io/github/stars/shuhao02/RouterDC?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/shuhao02/RouterDC) |
| 2023-11 | `ZOOTER` | Routing to the Expert: Efficient Reward-guided Ensemble of Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.08692) | - |
| 2023-08 | `FORC` | Fly-Swat or Cannon? Cost-Effective Language Model Choice via Meta-Modeling | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2308.06077) | [![GitHub Stars](https://img.shields.io/github/stars/epfl-dlab/forc?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/epfl-dlab/forc) |
| 2023 | `-` | LLM Routing with Benchmark Datasets | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://openreview.net/forum?id=k9EfAJhFZc) | - |


#### 5.2.4 Cascaded-Based Papers


| Date | Name | Title | Paper | Github |
|:---:|:---:|---|:---:|:---:|
| 2025-12 | `RoBoN` | RoBoN: Routed Online Best-of-n for Test-Time Scaling with Multiple LLMs | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://www.arxiv.org/abs/2512.05542) | [![GitHub Stars](https://img.shields.io/github/stars/j-geuter/RoBoN?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/j-geuter/RoBoN) |
| 2025-09 | `-` | Semantic Agreement Enables Efficient Open-Ended LLM Cascades | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://www.arxiv.org/abs/2509.21837) | - |
| 2025-04 | `EMAFusionTM` | EMAFusionTM: A Self-Optimizing System for Seamless LLM Selection and Integration | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.10681) | - |
| 2025-04 | `ModelSwitch` | Do We Truly Need So Many Samples? Multi-LLM Repeated Sampling Efficiently Scales Test-Time Compute | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.00762) | [![GitHub Stars](https://img.shields.io/github/stars/JianhaoChen-nju/ModelSwitch?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/JianhaoChen-nju/ModelSwitch) |
| 2024-12 | `DER` | Dynamic Ensemble Reasoning for LLM Experts | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.07448) | - |
| 2024-10 | `Cascade Routing` | A Unified Approach to Routing and Cascading for LLMs | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.10347) | [![GitHub Stars](https://img.shields.io/github/stars/eth-sri/cascade-routing?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/eth-sri/cascade-routing) |
| 2024-04 | `-` | Language Model Cascades: Token-level uncertainty and beyond | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.10136) | - |
| 2023-10 | `AutoMix` | AutoMix: Automatically Mixing Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.12963) | [![GitHub Stars](https://img.shields.io/github/stars/automix-llm/automix?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/automix-llm/automix) |
| 2023-10 | `neural caching` | Cache & Distil: Optimising API Calls to Large Language Models | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.13561) | [![GitHub Stars](https://img.shields.io/github/stars/guillemram97/neural-caching?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/guillemram97/neural-caching) |
| 2023-10 | `-` | Large Language Model Cascades with Mixture of Thoughts Representations for Cost-efficient Reasoning | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.03094) | [![GitHub Stars](https://img.shields.io/github/stars/MurongYue/LLM_MoT_cascade?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/MurongYue/LLM_MoT_cascade) |
| 2023-10 | `EcoAssistant` | EcoAssistant: Using LLM Assistant More Affordably and Accurately | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.03046) | [![GitHub Stars](https://img.shields.io/github/stars/JieyuZ2/EcoAssistant?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/JieyuZ2/EcoAssistant) |
| 2023-05 | `FrugalGPT` | FrugalGPT: How to Use Large Language Models While Reducing Cost and Improving Performance | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2305.05176) | - |
| 2023-01 | `-` | When Does Confidence-Based Cascade Deferral Suffice? | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/1f09e1ee5035a4c3fe38a5681cae5815-Abstract-Conference.html) | - |
| 2022-10 | `Model Cascading` | Model Cascading: Towards Jointly Improving Efficiency and Accuracy of NLP Systems | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2210.05528) | - |

---

<br>


## 6. Exploration Evaluation

### Foundations
- **Three failure modes of static optimisation**: Belief Stagnation, Value Stagnation, Reachability Collapse
- **Unified Epistemic Exploration Objective**: Combines Bayes-optimal value (C2), cumulative information gain bonus (C1), and reachability constraint (C3)
- **Convergence**: As beliefs converge to truth, exploration automatically gives way to exploitation

### Biological Exploration Parallels
- **Sensory-motor embodiment** → Lévy flights, whisking, saccades
- **Intrinsic curiosity** → Dopaminergic information prediction errors
- **Meta-control** → Locus coeruleus-norepinephrine regulation
- **Cognitive simulation** → Hippocampal preplay sequences
- **Social exploration** → Swarm intelligence, Theory of Mind

### Evaluation Principles
- Benchmarks for epistemic exploration across reasoning, embodied AI, world models, and multi-agent settings
- Design principles for exploration-centric evaluation

### Open Challenges
- Open-domain scalable exploration for reasoning beyond verifiable tasks
- Safe exploration with predictive world action models
- Causal and counterfactual reasoning in imagination space
- Dynamic temporal abstraction for long-horizon planning
- Epistemic uncertainty quantification in imagination
- Scalable coordination-space exploration without combinatorial explosion

---

<br>

## 7. Citation

If you find this survey useful, please cite:

```bibtex
@article{ban2026epistemic,
  title={Epistemic Exploration Toward Artificial General Intelligence},
  author={Ban, Yikun and others},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2026}
}
```

---

<p align="center">
  <i>This repository is actively maintained. If you find any errors or have new papers to suggest, please open an issue or submit a pull request!</i>
</p>
