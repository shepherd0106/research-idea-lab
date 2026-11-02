# Research Idea Lab

**English** | [简体中文](README.zh-CN.md)

Research Idea Lab is a Codex skill for exploring, developing, and assessing research ideas. It adapts to your stage: explore a field, develop an existing idea, or review a proposal before committing resources.

It is designed for researchers at different stages, from entering a broad field to evaluating an existing idea or exploring a transfer from another field.

## What it does

- **Frame the problem.** Identify the task, the difficulty, who it affects, and the conditions in which it matters.
- **Examine prior work.** Compare the closest studies by question, inputs, mechanism, supervision, assumptions, and evaluation; look for counterexamples and direct precedents.
- **Build from recent papers.** Investigate representative work, check open-source starting points, and compare unresolved problems across papers before developing an idea.
- **Explore candidate directions.** Explain the expected value, core assumptions, and trade-offs of a small number of ideas. Consider cross-domain transfer when it serves the problem.
- **Develop complete proposals.** Describe a coherent method and its assumptions, while allowing untested mechanisms and cooperating components to remain research hypotheses.
- **Compare and review constructively.** Distinguish shared problems or reused components from overlap with a complete prior method. Examine the strongest objections and potential improvements without dismissing a proposal merely for combining existing techniques.
- **Make the next step testable.** Suggest an appropriate comparison, needed evidence and resources, and results that would weaken or change the idea.

The skill distinguishes reported evidence, interpretation, hypotheses, and illustrative examples. It does not guarantee novelty, publication, or experimental results. Literature searches depend on the tools and access available in the session.

## Installation for Codex

Clone the repository into your personal Codex skills directory:

```bash
git clone https://github.com/shepherd0106/research-idea-lab.git ~/.codex/skills/research-idea-lab
```

Use this command only if `~/.codex/skills/research-idea-lab` does not already exist. If the skill is already installed, review and update the existing directory instead of overwriting it. Start a new Codex session if the skill is not immediately available.

## Usage

Invoke the skill explicitly in Codex:

```text
$research-idea-lab I am exploring [research field]. Help me identify a concrete,
testable research problem, compare the closest work, and evaluate a promising idea.
My resources and constraints are: [details or unknown].
```

Other examples:

```text
$research-idea-lab Evaluate this idea against its closest prior work.
What does the complete proposal potentially add? Identify the strongest relevant
prior work, concrete objections, and evidence needed to assess them.
```

```text
$research-idea-lab I want to adapt [source method] to [target problem].
Map the assumptions and variables, find relevant precedents, and assess whether
the transfer addresses a meaningful unmet need.
```

When possible, supply the task, relevant papers or links, data, compute, project stage, and hard constraints. Unknown resources can be marked as such; they do not need to be invented.

## Repository structure

```text
research-idea-lab/
├── SKILL.md                     Skill entry point and workflow
├── agents/openai.yaml           Codex interface configuration
└── references/
    ├── novelty-and-evaluation.md
    ├── paper-grounded-ideation.md
    ├── research-transfer.md
    ├── reviewer-stress-test.md
    ├── source.md
    └── techniques.md
```

The skill loads supporting guidance as needed. It is intended for research idea exploration and assessment; confirmed implementation work, ordinary translation, and standalone paper explanation may be better served by other workflows.

## Limitations

An assessment depends on the literature accessible at the time, the completeness of the search, and the quality of the available evidence. Treat the output as a starting point for research, not as proof of novelty or a substitute for domain expertise and experiments.
