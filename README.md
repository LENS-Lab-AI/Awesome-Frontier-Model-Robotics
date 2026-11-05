# Awesome Frontier Model Robotics

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

A curated list of **frontier language and multimodal models evaluated on robots**, covering research papers, official reports, independent studies, and community experiments.

Last source check: **November 2, 2026**. Paper links point to reviewed versions.

**Have something to add?** [Submit a title and link](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml) or [open a PR](CONTRIBUTING.md).

## Contents

- [Robot-Control Evaluations](#robot-control-evaluations)
- [Embodied Perception and Reasoning](#embodied-perception-and-reasoning)
- [Coding Agents and Tool Use](#coding-agents-and-tool-use)
- [Safety and Reliability](#safety-and-reliability)
- [Benchmarks and Resources](#benchmarks-and-resources)
- [Emerging Insights](#emerging-insights)
- [Contributing](#contributing)

## Robot-Control Evaluations

- **[From Reasoning to Action: Benchmarking Frontier AI Models on LIBERO-10 Robot Manipulation Tasks](https://arxiv.org/abs/2610.30051v1)** (Oct 2026) — May Espinola, Qifan Zhang & Yu Xiang. Frontier-model manipulation in simulation. [Project](https://irvlutd.github.io/LLM-LIBERO/) · [Code](https://github.com/IRVLUTD/LLM_LIBERO)
- **[Large Multimodal Models for Direct Robot Control: GPT-6 as a Beginning](https://arxiv.org/abs/2610.28259v1)** (Oct 2026) — Youwei Zhou et al. Astra manipulation evaluations in simulation and on real robots, including geometry-constrained LIBERO-GeoMotion tasks.
- **[Has GPT-6-Astra Achieved Embodied Intelligence?](https://arxiv.org/abs/2610.22471v2)** (Oct 2026) — SenseNova Joint Research Team. Evaluates demonstrations, execution budgets, and hybrid control across 12 benchmarks and eight real-robot configurations. [Project](https://sensenova.ai/has-gpt-6-astra-achieved-embodied-intelligence)
- **[Systematically Exploring the Capabilities of GPT-6 Astra as Embodied Policies](https://arxiv.org/abs/2609.38537v1)** (Sep 2026) — Galbot Team. Simulation study of direct and learned-policy-assisted control across manipulation, navigation, and locomotion. [Project](https://galaxygeneralrobotics.github.io/astra-policy/index.html)
- **[An Unexpected Robot Policy: Early Evaluations of GPT-6 Astra on RoboDojo and Beyond](https://arxiv.org/abs/2609.24170v1)** (Sep 2026) — Wenbo Zhang et al. Compares Astra, GPT-5.5, and DeepSeek-Flash on RoboDojo simulation tasks, highlighting precision and coordination limits.
- **[Claude plays robotics](https://www.anthropic.com/research/claude-plays-robotics)** (Jul 2026) — Shmuel Berman et al., Anthropic. Developer evaluation of control interfaces in simulation and on real robots.
- **[FOCA: Future-Oriented Conditioning for Data-Efficient Vision-Language-Action Adaptation](https://arxiv.org/abs/2606.20867v1)** (ICML 2026) — Duc Minh Nguyen et al. Evaluates few-shot VLA adaptation with future-oriented conditioning in LIBERO and RoboCasa simulation and on real robots, including action-free co-training on generated videos. [Project](https://focavla.github.io/) · [Code](https://github.com/cair-vinuni/FOCA)
- **[How Far Does a Frontier Agent Get as an Embodied Policy?](https://internrobotics.github.io/EBench-Astra-Tech-Report/)** (Technical report) — Yifei Yao et al. Astra evaluation on EBench simulation tasks with one demonstration per task and analysis of execution failures.
- **[Robocurve](https://robocurve.org/)** (Live) — Robocurve team. Independent real-robot comparisons of task scores, cost, and execution time.

## Embodied Perception and Reasoning

- **[EmbodiedLab: Benchmarking Embodied Agents That Act to Know](https://arxiv.org/abs/2610.35385v1)** (Oct 2026) — Hongcheng Gao et al. Evaluates frontier agents conducting experiments and reading instruments in a simulated laboratory. [Code](https://github.com/HexaFuture/EmbodiedLab)
- **[Frontier LLMs Enter the World of Robotics: A Cross-Model Evaluation on RoboColiseum](https://arxiv.org/abs/2610.27865v1)** (Oct 2026) — Da Huang et al. Instruction following, spatial reasoning, manipulation, and robustness in simulation, with real-robot case studies.
- **[GPT-6-Astra Lights Up Embodied Navigation: Evaluation in Zero-Shot Vision-and-Language Navigation in Continuous Environments](https://arxiv.org/abs/2609.29861v2)** (Sep 2026) — Guangzhao Dai et al. Zero-shot navigation in simulation using monocular RGB, basic movement actions, and no pre-built map. [Project](https://daiguangzhao.github.io/gpt-6-astra-for-vln/)

## Coding Agents and Tool Use

- **[Astranomy: An empirical study of GPT-6 Astra as a native robot policy](https://research.nvidia.com/labs/srl/projects/astranomy/)** (Oct 2026, report) — Jenai Xuning Yang, Ashna Khetan & Shun Zhang, NVIDIA. Compares direct, coding-agent, and policy-orchestration interfaces on RoboLab-120 simulation tasks, including latency and token costs.
- **[EmbodiedEvo: Self-Evolving Coding Agent For Physical Intelligence](https://arxiv.org/abs/2610.18867v2)** (Oct 2026) — Wenyi Li et al. Tests reusable code skills and lessons across unseen RoboDojo-Sim scenes without updating model weights.
- **[SEAR: Self-Evolving Agentic Robotics](https://arxiv.org/abs/2610.18792v1)** (Oct 2026) — Xinyi Wang et al. Evaluates retained experience versus repeated attempts across coding, live control, and policy-training workflows in simulation and on real robots.
- **[Fewer Tokens, Better Action: GPT-6 Astra Robot Agents with 14% Higher Success Rate but 65% Fewer Tokens](https://arxiv.org/abs/2610.01939v2)** (Oct 2026) — Ruiyang Si et al. PyRUA-Lean compares code execution with tool calling for simulated manipulation using the same Astra planner and robot primitives. [Project](https://dagroup-pku.github.io/PyRUA-Lean/) · [Code](https://github.com/DAGroup-PKU/PyRUA-Lean)
- **[RLE-Bench: A Qualifying Exam for Coding Agents as Robot Learning Engineers](https://arxiv.org/abs/2609.34210v2)** (Sep 2026) — Haitong Ma et al. Evaluates coding agents on robot control, policy learning, perception, and mechanical design using simulation feedback. [Project](https://rle-bench.github.io/) · [Code](https://github.com/RLE-Bench/RLE-Bench)
- **[EmbodiedSWE: Coding Agents for Long Horizon Dexterous Robotics](https://arxiv.org/abs/2609.27308v2)** (Sep 2026) — Zeyu Shen, Haoxiang You, Yilang Liu et al. Long-horizon coding agents in simulation, with generated demonstrations used to train a VLA tested on a real robot. [Project](https://embodiedswe.github.io/) · [Code](https://github.com/EmbodiedSWE/EmbodiedSWE)
- **[Agent as Policy for Robotic Manipulation](https://arxiv.org/abs/2609.12541v3)** (Sep 2026) — Mengzhao Jia et al. Real-robot manipulation through runtime coding, visual feedback, and experience reuse. [Project](https://agent-as-policy-2026.github.io/) · [Code](https://github.com/agent-as-policy-2026/agent-as-policy)
- **[ENPIRE: Agentic Robot Policy Self-Improvement in the Real World](https://arxiv.org/abs/2606.19980v2)** (CoRL 2026) — Wenli Xiao et al. Coding agents improve robot policies through repeated physical trials, outcome verification, and code revisions. [Project](https://research.nvidia.com/labs/gear/enpire/) · [Code](https://github.com/NVlabs/ENPIRE)
- **[CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://arxiv.org/abs/2603.22435v2)** (Jul 2026 version) — Letian Fu et al. Benchmarks code-generating robot agents under different tool abstractions, with simulation and real-robot evaluations. [Project](https://capgym.github.io/)

## Safety and Reliability

- **[Probing Collision Grounding in Vision-Language Models for Safe Human-Robot Collaboration](https://arxiv.org/abs/2605.31196v2)** (CoRL 2026) — Jun Wang, Xiaohao Xu & Xiaonan Huang. TouchSafeBench tests VLM recognition of current and imminent robot collisions in Habitat simulation. [Project](https://jun25336-bit.github.io/TouchSafeBench/)
- **[Refuses in Chat, Complies with Arms: LLM Refusal Does Not Survive Robot Control](https://arxiv.org/abs/2610.14043v1)** (Oct 2026) — Edward Sun et al. RoboHarm compares refusal across text, code, and robot-control interfaces in simulation and on physical arms. [Earlier report](https://robocurve.org/roboharm/) · [Code](https://github.com/robocurve/roboharm)
- **[Using large language models for embodied planning introduces systematic safety risks](https://arxiv.org/abs/2604.18463v2)** (May 2026 version) — Tao Zhang et al. DESPITE is a symbolic planning benchmark separating feasible plans from safe ones. [Project](https://despite-safety.github.io/) · [Code](https://github.com/taozhang1004/DESPITE)
- **[AGENTSAFE: Benchmarking the Safety of Embodied Agents on Hazardous Instructions](https://arxiv.org/abs/2506.14697v3)** (Oct 2025 version) — Zonghao Ying et al. Simulation benchmark tracing hazardous instructions through embodied agents' perception, planning, and execution.

## Benchmarks and Resources

- **[ScaleEvals: Scaling Generalist Policy Evaluation through Reset-Free Autonomous Play](https://scaleevals.github.io/Scale_Eval_CORL_2026.pdf)** (CoRL 2026) — Amitoj Sandhu et al. VLM-guided task generation and grading for reset-free evaluation of generalist policies on real robots. [Project](https://scaleevals.github.io/)
- **[RoboGaze: Evaluating Robot World Models via Structured Vision-Language Analysis](https://arxiv.org/abs/2606.28385v2)** (Oct 2026 version) — Minh-Loi Nguyen et al. Evaluates eight VLM backbones for structured failure diagnosis in generated robot-manipulation videos, with RoboGazeBench covering simulated and real-world conditioning data. [Project](https://robogaze-eval.github.io/) · [Code](https://github.com/cair-vinuni/RoboGaze)
- **[RoboWorM: Evaluating Movement Realism, Consistency and Acceleration Affects in Embodied Video World Models](https://arxiv.org/abs/2610.33807v1)** (Oct 2026) — Doanh Le Thien et al. Evaluates generated robot videos conditioned on 1,605 real-robot episodes, comparing kinematic and multi-view consistency metrics with the evaluated VLM judges and auditing nine acceleration methods. [Project](https://roboworm.github.io/roboworm/) · [Code](https://github.com/cair-vinuni/roboworm)
- **[Gym-Anything for Robotics: Scaling physical simulations with digital agents](https://arxiv.org/abs/2610.40565v1)** (Oct 2026) — Pranjal Aggarwal & Sean Welleck. Agent-created simulations and the RoboWorld benchmark of 25 physical-work test tasks. [Project](https://gym-anything.github.io/robotics/) · [Code](https://github.com/gym-anything/robotics)
- **[RobotAgentBench: Towards Open-world Robot Autonomy](https://arxiv.org/abs/2610.34649v1)** (Oct 2026) — Lingjun Mao et al. Evaluates task discovery, execution, recovery, and open-ended autonomy in simulated households. [Project](https://aetherlabsai.github.io/RobotAgentBench/) · [Code](https://github.com/AetherLabsAI/RobotAgentBench)
- **[RobotWorld: Benchmarking Multimodal Agents for Robot Use Across Diverse Tasks and Embodiments](https://arxiv.org/abs/2610.10409v1)** (Oct 2026) — Zhiqin Yang et al. Tests multimodal agents on 84 simulation tasks spanning manipulation, locomotion, driving, and aerial control. [Project](https://robotworldai.github.io/) · [Code](https://github.com/robotworldai/robotworld)
- **[RoboLab: A High-Fidelity Simulation Benchmark for Analysis of Task Generalist Policies](https://arxiv.org/abs/2604.09860v4)** (RSS 2026) — Jenai Xuning Yang et al. Simulation infrastructure and 120 tasks for evaluating generalist robot policies under controlled variations.
- **[EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://arxiv.org/abs/2502.09560v3)** (ICML 2025) — Rui Yang et al. Simulation benchmark covering high-level planning, navigation, and manipulation. [Project](https://embodiedbench.github.io/) · [Code](https://github.com/EmbodiedBench/EmbodiedBench)
- **[Inspect Robots](https://github.com/robocurve/inspect-robots)** — Robocurve and contributors. Open-source evaluation tools for language models and VLAs in simulation and on real robots.

## Emerging Insights

- **Interfaces matter:** tools and controllers affect results alongside the model. [Study](https://www.anthropic.com/research/claude-plays-robotics)
- **Experience can help:** saved Astra experience improved Terra in AGP's small study of five trials per condition. [Results](https://agent-as-policy-2026.github.io/)
- **Compare cost within the same setup:** include runtime and retries. [Evaluations](https://robocurve.org/)
- **Real-time responsiveness needs its own test:** Astranomy pauses simulation during inference, so task success alone does not establish real-time control. [Report](https://research.nvidia.com/labs/srl/projects/astranomy/)
- **Measure safety separately from task completion.** [RoboHarm](https://arxiv.org/abs/2610.14043v1) · [DESPITE](https://arxiv.org/abs/2604.18463v2)

## Contributing

Found a paper, report, or demo? **[Submit its title and link](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml)** — we'll handle the formatting. Or [add an entry by PR](CONTRIBUTING.md). Authors and first-time contributors are welcome!

[Report a correction](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=correction.yml).

## Acknowledgements

**Research and evaluation teams:** all findings, benchmarks, code, and demonstrations belong to their original authors. Thank you for making this work available to the community.

Maintained by [LENS Lab](https://github.com/LENS-Lab-AI) with community contributions. Inclusion is not an endorsement by a listed author or organization.

---

[Inspiration & template credits](CREDITS.md) · [CC0 license](LICENSE). Linked works retain their own licenses.
