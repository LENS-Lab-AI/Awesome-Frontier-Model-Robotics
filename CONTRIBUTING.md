# Contributing

Thank you for helping researchers and practitioners find useful evaluations of frontier models in robotics. Authors are welcome to submit their own work, and first-time GitHub contributors are welcome here.

## Two Ways to Contribute

**Use the [submission form](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=submit-resource.yml)** to suggest a paper, report, benchmark, tool, or documented demo. You need a GitHub account, but do not need to edit Markdown or open a PR. A maintainer will review the suggestion and help turn it into an entry.

**Open a pull request** if you would like to add the entry yourself:

1. Check the README and open issues for an existing entry or submission.
2. Fork the repository and create a branch, or use GitHub's editor on `README.md`.
3. Add the resource to the most relevant of the five sections, newest first where dates are available. Cross-link related sections instead of duplicating entries.
4. Use the format below and preview the Markdown.
5. Open a PR with a brief explanation and a link to any related submission issue. Maintainers can help with formatting.

## What Fits

Include work that evaluates general-purpose language or multimodal models in robot control, embodied reasoning, coding/tool use, or safety, as well as infrastructure that makes those evaluations possible. Comparisons with specialized robot policies are useful when connected to this scope.

Official model-developer reports, academic studies, independent evaluations, and community experiments are welcome. Earlier benchmarks are useful context when clearly dated. A demo can be included when its setup is documented; label it as a demo and avoid presenting it as a benchmark.

Prefer a primary source: the authors' paper, project page, repository, or original report. A social post can be an original source for a community experiment if it explains the model, task, interface, and limitations. Link accessible supporting material when available. Avoid promotional links without substantive technical evidence.

## Entry Format

```markdown
- **[Title](primary-source-url)** — Month Year · Source type · Evaluation setting.\
  **Authors:** Author names, with a link to the full team when abbreviated.\
  Two or three sentences on what was evaluated, what was learned, and an important limitation.\
  [Project](project-url) · [Code](code-url)
```

Omit unavailable links. Use a backslash at the end of a line for a line break inside an entry, as in the README.

- **Source type:** research paper (preprint or venue), developer report, independent evaluation, community demo, or evaluation tooling. Do not assume that a paper is peer reviewed or independent of a model developer.
- **Setting:** simulation, real robot, symbolic planning, or a clearly described combination. Distinguish direct agent control from a downstream policy trained on agent-generated data.
- **Models:** preserve the versions and reasoning settings from the source when reporting model-specific results.
- **Results:** include the metric, task set, and sample size where reported. Distinguish task score from success rate, and refusal from inability to execute. Do not infer an unreported number.
- **Efficiency:** retain the source's assumptions about inference cost, runtime, retries, tools, and hardware. A lower API price alone does not establish a lower cost per successful task.
- **Versions:** link the reviewed paper version. For a live leaderboard or changing report, state the date checked. Explain material changes when updating an existing summary.

Keep summaries concise and in your own words. Add links to the supporting evidence beside claims and preserve the authors' stated limitations. We do not aggregate incompatible benchmarks into a single ranking.

## Credit

Credit the original researchers or team in each entry. Preserve equal-contribution notes when available, and link the full author list if using “and collaborators.” Do not invent social handles or imply that listed authors endorse this collection.

For a resource suggested through an issue, the maintainer should link that issue from the resulting PR and thank the submitter by their GitHub handle in the PR description. The submitter may also open the PR themselves. An issue submission alone does not create a Git commit or a place in GitHub's code-contributor list; merged PR authors receive credit through the repository's history.

If adapting another list's wording or structure, acknowledge it and respect its license. New original contributions to this collection are made available under the repository's [CC0 1.0 dedication](LICENSE); linked works keep their own licenses.

## Corrections and Review

Use the [correction form](https://github.com/LENS-Lab-AI/Awesome-Frontier-Model-Robotics/issues/new?template=correction.yml) for an incorrect summary, missing credit, broken link, or out-of-date result. Include a source for the correction where possible.

Maintainers check relevance, source access, authorship, category, and whether each claim matches the evidence. We may ask for more context or suggest edits before merging. Constructive disagreements and negative findings are welcome; discuss the evidence with respect for the people doing the work.
