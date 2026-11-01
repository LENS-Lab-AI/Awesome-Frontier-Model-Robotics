# Awesome Frontier Model Robotics

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

A curated list of **frontier language and multimodal models evaluated on robots**, covering research papers, official reports, independent studies, and community experiments.

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

- **[LIBERO-10: From Reasoning to Action](https://arxiv.org/abs/2610.30051v1)** (Oct 2026) — May Espinola, Qifan Zhang & Yu Xiang. Frontier-model manipulation in simulation. [Project](https://irvlutd.github.io/LLM-LIBERO/) · [Code](https://github.com/IRVLUTD/LLM_LIBERO)
- **[Claude Plays Robotics](https://www.anthropic.com/research/claude-plays-robotics)** (Jul 2026) — Shmuel Berman et al., Anthropic. Developer evaluation of control interfaces in simulation and on real robots.
- **[Robocurve Evaluations](https://robocurve.org/)** (Live) — Robocurve team. Independent real-robot comparisons of task scores, cost, and execution time.

## Embodied Perception and Reasoning

- **[RoboColiseum: A Cross-Model Evaluation](https://arxiv.org/abs/2610.27865v1)** (Oct 2026) — Da Huang et al. Instruction following, spatial reasoning, manipulation, and robustness in simulation, with real-robot case studies.

## Coding Agents and Tool Use

- **[EmbodiedSWE](https://arxiv.org/abs/2609.27308v2)** (Sep 2026) — Zeyu Shen, Haoxiang You, Yilang Liu et al. Coding agents for long-horizon simulation tasks and demonstration generation for robot-policy training. [Project](https://embodiedswe.github.io/) · [Code](https://github.com/EmbodiedSWE/EmbodiedSWE)
- **[Agent as Policy](https://arxiv.org/abs/2609.12541v3)** (Sep 2026) — Mengzhao Jia et al. Real-robot manipulation through runtime coding, visual feedback, and experience reuse. [Project](https://agent-as-policy-2026.github.io/) · [Code](https://github.com/agent-as-policy-2026/agent-as-policy)

## Safety and Reliability

- **[RoboHarm](https://robocurve.org/roboharm/)** (Sep 2026) — Edward Sun et al., Robocurve. Independent real-robot evaluation separating safety refusals from execution failures. [Code](https://github.com/robocurve/roboharm)
- **[DESPITE](https://arxiv.org/abs/2604.18463v2)** (May 2026 version) — Tao Zhang et al. Symbolic planning benchmark separating feasible plans from safe ones. [Project](https://despite-safety.github.io/) · [Code](https://github.com/taozhang1004/DESPITE)

## Benchmarks and Resources

- **[EmbodiedBench](https://arxiv.org/abs/2502.09560v3)** (ICML 2025) — Rui Yang et al. Simulation benchmark covering high-level planning, navigation, and manipulation. [Project](https://embodiedbench.github.io/) · [Code](https://github.com/EmbodiedBench/EmbodiedBench)
- **[Inspect Robots](https://github.com/robocurve/inspect-robots)** — Robocurve and contributors. Open-source evaluation tools for language models and VLAs in simulation and on real robots.

## Emerging Insights

- **Interfaces matter:** tools and controllers affect results alongside the model. [Study](https://www.anthropic.com/research/claude-plays-robotics)
- **Experience can help:** saved Astra experience improved Terra in AGP's small study of five trials per condition. [Results](https://agent-as-policy-2026.github.io/)
- **Compare cost within the same setup:** include runtime and retries. [Evaluations](https://robocurve.org/)
- **Measure safety separately from task completion.** [RoboHarm](https://robocurve.org/roboharm/) · [DESPITE](https://arxiv.org/abs/2604.18463v2)

## Contributing

Found a paper, report, or demo? **[Submit its title and link](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml)** — we'll handle the formatting. Or [add an entry by PR](CONTRIBUTING.md). Authors and first-time contributors are welcome!

[Report a correction](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=correction.yml).

## Acknowledgements

**Research and evaluation teams:** all findings, benchmarks, code, and demonstrations belong to their original authors. Thank you for making this work available to the community.

Maintained by [LENS Lab](https://github.com/LENS-Lab-AI) with community contributions. Inclusion is not an endorsement by a listed author or organization.

---

[Inspiration & template credits](CREDITS.md) · [CC0 license](LICENSE). Linked works retain their own licenses.
