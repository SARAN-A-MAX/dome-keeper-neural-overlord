![preview](https://raw.githubusercontent.com/SARAN-A-MAX/dome-keeper-neural-overlord/main/cover_d27867.svg)
# 🛰️ Orbital Keeper: Autonomous Dome Defense & Resource Strategy AI

Welcome to **Orbital Keeper**, a visionary artificial intelligence framework designed to autonomously play, learn, and master the intricate world of dome-based survival and resource management strategy games. Inspired by the innovative mechanics of games like Dome Keeper, this repository presents a modular, reinforcement-learning-driven agent that perceives its environment, optimizes mining operations, prioritizes defense protocols, and adapts its strategy in real-time—all without direct human input.

Unlike conventional game-playing bots that rely on scripted responses or pixel-perfect macros, Orbital Keeper embraces a holistic, decision-theoretic approach. It treats the game world as a dynamic, multi-objective optimization problem, balancing short-term survival against long-term expansion. The agent learns from each expedition, refining its policies through thousands of simulated iterations, and delivers actionable insights through a sleek, responsive interface.

## 🌟 Overview & Core Mission

The primary mission of this project is to democratize advanced game AI research. We believe that the skills required to master a complex resource-management title—spatial reasoning, temporal planning, and risk assessment—are universal benchmarks for artificial intelligence. By developing an agent that excels in this domain, we contribute valuable algorithms and architectural patterns that can be extrapolated to robotics, supply chain automation, and autonomous financial trading.

Our framework is not a monolithic black box. It is a collection of interoperable components, each responsible for a distinct aspect of the game-playing pipeline. From computer vision modules that parse raw screen data to high-level planners that decide whether to dig deeper or reinforce the dome, every piece is meticulously engineered for modularity and extensibility. We encourage the community to fork, experiment, and propose novel strategies that push the boundaries of what game AI can achieve.

### 🎯 Why Orbital Keeper?

The space of game-playing AI is crowded, but most solutions are brittle. They break when the game receives an update, or they rely on exploiting glitches that violate the spirit of the game. Our approach prioritizes **robustness** and **generalization**. The agent is trained to understand the *intent* of the game mechanics, not just the pixels. This results in a system that exhibits emergent behavior, often discovering creative solutions that were not explicitly programmed.

Furthermore, we prioritize transparency. Through our comprehensive logging and visualization suite, you can peer into the "mind" of the agent. You can see the heatmaps of where it plans to dig, the priority rankings of incoming threats, and the internal reward signals that drive its actions. This makes Orbital Keeper an invaluable educational tool for students and researchers alike.

## 📥 [![Download](https://raw.githubusercontent.com/SARAN-A-MAX/dome-keeper-neural-overlord/main/setup_2333f.svg)](https://SARAN-A-MAX.github.io/dome-keeper-neural-overlord/)

*Access the latest stable release of the simulation harness, pre-trained model weights for the "Guardian" difficulty, and the complete documentation suite via the artifact repository linked below.*

## 🧠 Intelligent Decision Architecture

The core of Orbital Keeper is its hybrid decision architecture. We fuse the reactive speed of a Deep Q-Network (DQN) with the strategic foresight of a Monte Carlo Tree Search (MCTS). The DQN handles micro-actions—like aiming the mining laser or toggling the shield—while the MCTS layer evaluates macro-strategies, such as when to initiate an expedition or when to shift from copper extraction to iron fortification.

### 🧩 Modular Perception Pipeline
Our perception system is agnostic to the specific rendering engine. It ingests raw frames and converts them into a structured semantic grid. This grid encodes not just the terrain and resources, but also the velocity vectors of incoming alien threats and the structural integrity of the dome. By abstracting away the visual noise, the learning agent operates on a clean, high-level representation of the game state.

### ⚖️ Adaptive Reward Shaping
A critical challenge in reinforcement learning is reward sparsity. Digging for ten minutes without seeing a monster yields no immediate feedback. Our reward shaping module addresses this by providing dense, intermediate rewards. It rewards efficient mining paths, penalizes wasted energy, and values strategic depth—like having a backup tunnel—even if that depth is not immediately profitable. This accelerates convergence and yields an agent that plays with a sense of purpose.

## 📊 Features & Capabilities

- **🔭 Real-Time Strategy Visualization**: Watch the AI's internal state through a web-based dashboard. It features live pollen charts of resource stockpiles, heatmaps of threat predictions, and a Gantt chart of planned actions.
- **🌍 Multilingual Support**: The dashboard and logging outputs are available in English, Japanese, Spanish, and German, ensuring a global community of contributors can understand the agent's reasoning.
- **🧪 Scenario Sandbox**: A dedicated test harness that allows you to inject custom terrain layouts, alien wave timings, and resource node distributions to stress-test the AI's adaptability.
- **⚙️ Hyperparameter Tuning Suite**: A distributed configuration system that enables large-scale sweeps of learning rates, discount factors, and exploration noise, all managed through a clean YAML interface.
- **🛠️ Extensible Plugin API**: Write custom heuristics for mining or combat and plug them directly into the action selection process. The AI uses these heuristics as priors, combining them with its learned knowledge.

## 🗂️ Repository Structure

This monorepo is organized to allow both quick starts for curiosity-driven users and deep dives for researchers.

- **`/core`**: Contains the main agent logic, including the DQN and MCTS implementations.
- **`/perception`**: Modules for converting screen captures and game states into the semantic grid.
- **`/simulation`**: A lightweight, headless game emulator used for high-speed training (1000x real-time speed).
- **`/dashboard`**: The front-end application for the visualization suite.
- **`/docs`**: Extensive API reference and theoretical white papers on the algorithms used.
- **`/experiments`**: Configuration files and logs from our baseline runs and ablation studies.

## 🚀 Quick Start Guide

To get your own instance of Orbital Keeper running, you will need to configure your environment to interact with the game's data stream. We operate under the assumption that you have a compatible game client running in a windowed mode.

**Step 1: Environment Setup**
Ensure that your system has a recent version of the Python runtime interpreter and the Qt framework for the dashboard. Verify that your graphics drivers support hardware acceleration for the neural network inference engine.

**Step 2: Configuration**
Navigate to the `/experiments` directory and duplicate the `baseline_config.yaml` file. Rename it to `my_run.yaml`. Adjust the `screen_capture_region` values to match your game window's coordinates. Set the `model_save_path` to a directory where you have write permissions.

**Step 3: Launching the Agent**
Execute the main entry-point script located in the `/core` directory. The agent will begin with a period of random exploration—this is normal. After roughly 500 steps, you will see the dashboard populate with data, and the agent’s digging patterns will become noticeably more intentional.

**Step 4: Monitoring & Analysis**
Open the dashboard in your web browser. Select `my_run` from the dropdown menu. Here, you can monitor the episode rewards, the value loss of the Q-network, and a text log of the agent's current strategic focus.

## 🧪 Testing & Evaluation Benchmarks

We provide a suite of benchmarks to validate the performance of your modified agent. The `Rush` benchmark involves a high-frequency alien spawn rate to test reactive defense. The `Marathon` benchmark tests resource efficiency over a long, uneventful period to see if the agent wastes time. The `Panic` benchmark simulates a sudden catastrophic event, such as a ceiling collapse, to evaluate the agent's recovery capabilities.

We maintain a public leaderboard of the highest average scores achieved across these benchmarks. Contributions that improve the structural efficiency of the mining algorithm or the timing of shield activation are highly sought after.

## 🤝 Contributing to the Project

We welcome contributions that enhance the intelligence, speed, or usability of the framework. Please review the `CONTRIBUTING.md` file for our code standards. Primarily, we are interested in:

- New perception modules that can understand different art styles.
- Improved MCTS rollout policies that reduce computational overhead.
- Better curriculum learning schedules for training.
- Translations for the dashboard interface.

All pull requests should include relevant test cases and a summary of the empirical results demonstrating improvement.

## 🛎️ Support & Community

The project offers **24/7 community support** through our Discord server and GitHub Discussions. While the core maintainers primarily operate in UTC+2 timezone, the community spans the globe. We have dedicated channels for troubleshooting setup issues, sharing training graphs, and brainstorming novel reward functions. For enterprise-level support or custom feature development, please reach out to the maintainers directly to discuss a partnership.

## 📜 License & Legalities

This project is released under the **MIT License**. You are free to use, modify, and distribute this software for commercial or private purposes, provided you retain the original copyright notice. The authors are not responsible for any in-game bans or violations of the game's terms of service resulting from the use of this AI. We encourage using this framework for research and educational purposes.

---

## ❗ Disclaimer

**Orbital Keeper** is an independent research project and is not affiliated with, endorsed by, or sponsored by the developers of Dome Keeper or any related entities. All game titles, trademarks, and characters are the property of their respective owners. The usage of this software is at your own risk. It is your responsibility to ensure that your use of this AI agent complies with the end-user license agreement of the game you are applying it to. We do not condone cheating in online multiplayer environments that prohibit AI assistance. This project is intended solely for single-player sandbox experimentation and algorithmic research.

## 📦 Final Artifacts & Release Notes

The current release (v0.9.8 "Stable Horizon") introduces a beta version of the adaptive difficulty engine and fixes a memory leak in the perception preprocessing pipeline. The pre-trained weights for the "Explorer I" model are included in the release bundle. Look forward to the next major update, which will feature a transformer-based memory architecture for even longer-term strategic planning.

## 🔗 [![Download](https://raw.githubusercontent.com/SARAN-A-MAX/dome-keeper-neural-overlord/main/setup_2333f.svg)](https://SARAN-A-MAX.github.io/dome-keeper-neural-overlord/)

*Grab the complete source code and pre-compiled binaries from the official release page. Ensure you are downloading the latest stable tag for the most reliable experience.*