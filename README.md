# Awesome Frontier Model Robotics

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Submit a resource](https://img.shields.io/badge/submit-a_resource-blue.svg)](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml)

A curated collection of **frontier language and multimodal models evaluated on robots**: what they can do, where they struggle, and how we measure progress.

We bring together research papers, official model-developer reports, independent evaluations, and reproducible community experiments. The focus is on general-purpose models used for robot reasoning, control, and tool use, including comparisons with specialized robot policies.

This collection is made possible by the researchers and engineers who build the benchmarks, run the experiments, and share their findings. Please explore and support their original work.

**Found something we should include?** [Submit a resource](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml) or [open a pull request](CONTRIBUTING.md). Authors are warmly encouraged to share their own work.

## Contents

- [Robot-Control Evaluations](#robot-control-evaluations)
- [Embodied Perception and Reasoning](#embodied-perception-and-reasoning)
- [Coding Agents and Tool Use](#coding-agents-and-tool-use)
- [Safety and Reliability](#safety-and-reliability)
- [Benchmarks and Resources](#benchmarks-and-resources)
- [Emerging Insights](#emerging-insights)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)

## Reading the Collection

Each entry identifies its source and evaluation setting. **Developer report** means a study published by a model developer; **independent evaluation** means an external evaluator's report; **research paper** identifies the publication format, without implying independence or peer review. Preprints are marked explicitly.

**Simulation**, **real robot**, and **symbolic planning** are different kinds of evidence. Reported scores belong to the stated setup: tasks, observations, tools, reasoning budgets, retries, and controllers can all differ. This is a reading list, not a combined leaderboard. Model names follow the linked sources; dated results should not be read as measurements of every newer model version.

Entry summaries reviewed **November 1, 2026**. Paper links preserve the reviewed version; project pages and live results may change.

## Robot-Control Evaluations

Evaluations of models that issue actions, generate controllers, or supervise robot policies.

- **[From Reasoning to Action: Benchmarking Frontier AI Models on LIBERO-10 Robot Manipulation Tasks](https://arxiv.org/abs/2610.30051v1)** — October 2026 · Research paper, preprint · Simulation.\
  **Authors:** May Espinola, Qifan Zhang, and Yu Xiang; May and Qifan contributed equally.\
  Six models, three reasoning levels, and 1,800 episodes evaluate closed-loop end-effector and gripper control without task-specific training. GPT-6 Astra reaches 44% success and Gemini-4 Argon 43% in their best reported configurations. More reasoning can help, with additional inference cost; precise arrangements and multi-step interactions remain difficult.\
  [Project](https://irvlutd.github.io/LLM-LIBERO/) · [Code](https://github.com/IRVLUTD/LLM_LIBERO)

- **[Claude Plays Robotics](https://www.anthropic.com/research/claude-plays-robotics)** — July 2026 · Developer report, Anthropic · Simulation and real robot.\
  **Authors:** Shmuel Berman, Michael Ilie, Jia Deng, and Daniel Freeman.\
  Evaluates classic control, locomotion, navigation, and manipulation with interfaces ranging from motor commands to generated controller code and pretrained policies. Performance depends strongly on the interface: direct joint control remains difficult, while tools and higher-level controllers enable useful behavior. Interpret the results together with the control support supplied to each model.

- **[Robocurve: Real-World Frontier Model Evaluations](https://robocurve.org/)** — Live results, reviewed November 2026 · Independent evaluation · Real robot.\
  **Credit:** The Robocurve team and contributors.\
  Reports model configurations, task scores, estimated inference costs, and execution times on RoboDojo-RC Tier 1. The reviewed snapshot uses 120 attempts per configuration, with different execution caps for language models and VLAs. A useful resource for comparing performance and cost within a shared physical setup; these are task scores, not necessarily binary success rates.

## Embodied Perception and Reasoning

How models interpret instructions and scenes, reason spatially, and translate understanding into action.

- **[Frontier LLMs Enter the World of Robotics: A Cross-Model Evaluation on RoboColiseum](https://arxiv.org/abs/2610.27865v1)** — October 2026 · Research paper, preprint · Simulation, with real-robot case studies.\
  **Authors:** Da Huang, Jichao Wang, Junhui Wu, Tong Ran, Linting Guo, Siying Zhang, Chuang Men, Sukai Wang, Yue Zhou, Maoqing Yao, and Mo Wu.\
  Uses Agent2Act to compare GPT-6 Astra, GPT-6.1 Sol, Claude Opus 5.5, and Gemini 4 Argon across instruction following, spatial reasoning, general manipulation, and robustness. Opus leads overall in the evaluated configurations; Astra leads instruction following and robustness. Manipulation trails the other tracks, and component comparisons show that the harness affects outcomes, time, and cost.

## Coding Agents and Tool Use

Models that write, execute, inspect, and revise programs to solve embodied tasks.

- **[EmbodiedSWE: Coding Agents for Long Horizon Dexterous Robotics](https://arxiv.org/abs/2609.27308v2)** — September 2026 · Research paper, preprint · Simulation; downstream real-robot policy transfer.\
  **Authors:** Zeyu Shen, Haoxiang You, Yilang Liu, and collaborators; the [project page](https://embodiedswe.github.io/) credits the three project leads equally and lists the full team.\
  Introduces a benchmark for long-horizon, contact-rich tasks and a pipeline that turns coding-agent solutions into diversified demonstrations for VLA training. Solutions can require substantial iteration and specialize to task instances. The real-robot result uses a VLA trained on generated demonstrations, which is a different deployment mode from direct coding-agent control.\
  [Project](https://embodiedswe.github.io/) · [Code](https://github.com/EmbodiedSWE/EmbodiedSWE)

- **[Agent as Policy for Robotic Manipulation](https://arxiv.org/abs/2609.12541v3)** — September 2026 · Research paper, preprint · Real robot, with simulation evaluations.\
  **Authors:** Mengzhao Jia, Yang Lin, Xixin Zhang, Zhihan Zhang, Xiaobai Liu, and Meng Jiang; the project credits the first three as core contributors.\
  AGP combines visual feedback, executable programs, motion commands, and runtime revision without task-specific training. It reports at least 80% success in seven of eight real-world task configurations. Experience reuse is particularly interesting: a small transfer study tests whether saved Astra procedures help GPT-5.6 Terra.\
  [Project](https://agent-as-policy-2026.github.io/) · [Code](https://github.com/agent-as-policy-2026/agent-as-policy)

## Safety and Reliability

Evaluations of refusal, safe planning, failure modes, and robustness. Task completion and safety need separate measurements.

- **[RoboHarm: Do Frontier Robot Policies Refuse Unsafe Instructions?](https://robocurve.org/roboharm/)** — September 2026 · Independent evaluation · Real robot.\
  **Authors:** Edward Sun, Sravanthi Machcha, Sabrina Zou, Tzu Kit Chan, and Jay Chooi.\
  Evaluates GPT-6 Astra, Claude Fable 5.1, and MolmoAct2 on five fixed instructions with 20 trials per instruction and policy. Separates safety refusals from failed attempts and completed actions. Its narrow, fixed-scene design supports a focused refusal evaluation; inability to execute a task should not be interpreted as safety.\
  [Code and evaluation material](https://github.com/robocurve/roboharm)

- **[Using Large Language Models for Embodied Planning Introduces Systematic Safety Risks](https://arxiv.org/abs/2604.18463v2)** — April 2026, revised May 2026 · Research paper, preprint · Symbolic planning.\
  **Authors:** Tao Zhang, Kaixian Qu, Zhibin Li, Jiajun Wu, Marco Hutter, Manling Li, and Fan Shi.\
  Introduces DESPITE: 12,279 tasks with deterministic checks for plan feasibility and danger. Across 23 models, strong planning does not guarantee safe plans. This evaluates planning-level safety, rather than physical robot execution.\
  [Project](https://despite-safety.github.io/) · [Code](https://github.com/taozhang1004/DESPITE)

The [RoboColiseum study](#embodied-perception-and-reasoning) also includes a robustness track. Contributions on failure recovery, repeated trials, and physical safety are especially welcome.

## Benchmarks and Resources

Reusable environments, evaluation tools, and earlier benchmarks that help put current results in context.

- **[EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://arxiv.org/abs/2502.09560v3)** — June 2025 version · Research paper, ICML 2025 · Simulation.\
  **Authors:** Rui Yang, Hanyang Chen, Junyu Zhang, Mark Zhao, and collaborators; the [project page](https://embodiedbench.github.io/) credits these four authors equally and lists the full team.\
  Provides 1,128 tasks across four environments and six capability subsets, covering high-level planning through lower-level navigation and manipulation. The paper evaluates 24 models. Included as foundational evaluation infrastructure; its original scores describe its 2025 model cohort.\
  [Project](https://embodiedbench.github.io/) · [Code](https://github.com/EmbodiedBench/EmbodiedBench)

- **[Inspect Robots](https://github.com/robocurve/inspect-robots)** — Evaluation tooling · Simulation and real robot.\
  **Credit:** Robocurve and the Inspect Robots contributors.\
  Open-source infrastructure for evaluating language models and VLAs across robot embodiments and benchmarks. Useful for understanding and reproducing the observation, action, and logging interfaces behind evaluations.

## Emerging Insights

Our reading of this initial collection:

1. **The interface is part of the result.** Tools, feedback, and pretrained controllers materially affect performance. Compare model-and-harness configurations, as illustrated by [Anthropic's report](https://www.anthropic.com/research/claude-plays-robotics) and [RoboColiseum](https://arxiv.org/abs/2610.27865v1).
2. **Understanding a task and executing it reliably remain distinct challenges.** [LIBERO-10](https://arxiv.org/abs/2610.30051v1) and [RoboColiseum](https://arxiv.org/abs/2610.27865v1) expose manipulation limits despite strong reasoning capabilities.
3. **Experience reuse deserves attention alongside model scale.** [AGP's project results](https://agent-as-policy-2026.github.io/) report Terra improving from 1/5 to 4/5 successes with saved Astra experience. Five trials per condition are encouraging evidence for further study, not a general cost-efficiency conclusion.
4. **Measure the cost of the whole attempt.** Reasoning effort, retries, runtime, and tool support matter alongside model pricing. [Robocurve's live results](https://robocurve.org/) make within-setup cost comparisons possible; [EmbodiedSWE](https://embodiedswe.github.io/) also tracks performance against time and spend.
5. **Capability and safety require separate evidence.** [RoboHarm](https://robocurve.org/roboharm/) distinguishes refusal from execution failure; [DESPITE](https://arxiv.org/abs/2604.18463v2) distinguishes feasible plans from safe ones.

We welcome replications, counterexamples, negative results, and corrections to these interpretations.

## Contributing

Help make this a useful community resource:

- **Suggest a resource:** use the [submission form](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml). A GitHub account is required; editing files is not.
- **Add or improve an entry:** follow the [contribution guide](CONTRIBUTING.md) and open a pull request. First-time contributors are welcome.
- **Correct a detail or broken link:** use the [correction form](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=correction.yml).

Papers, official reports, independent studies, and documented community demos are all welcome. Include the original source, credit the team, and distinguish a demonstration from a systematic evaluation. Submissions are reviewed before inclusion.

We thank resource submitters in the associated issue or PR; merged PRs also appear in GitHub's contribution history. See [how we handle credit](CONTRIBUTING.md#credit).

## Acknowledgements

- **Research and evaluation teams:** all findings, benchmarks, code, and demonstrations belong to their original authors. Thank you for making this work available to the community.
- **Inspiration:** [GT-RIPL/Awesome-LLM-Robotics](https://github.com/GT-RIPL/Awesome-LLM-Robotics), maintained by the Georgia Tech Robot Intelligence, Perception, and Learning Lab and its contributors.
- **Template lineage:** [Zubair Irshad's Awesome-Implicit-NeRF-Robotics](https://github.com/zubair-irshad/Awesome-Implicit-NeRF-Robotics), credited as the template by Awesome-LLM-Robotics, informed this list's organization. The summaries and contribution forms here are newly written.
- **Awesome community:** [Sindre Sorhus and Awesome contributors](https://github.com/sindresorhus/awesome) for the curated-list conventions and badge.

Maintained by [LENS Lab](https://github.com/LENS-Lab-AI) with community contributions. Inclusion is not an endorsement by a listed author or organization.

The original text and organization of this collection are available under [CC0 1.0](LICENSE). Linked papers, code, datasets, and media retain their own licenses.
