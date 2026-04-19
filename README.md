# Agentic AI Evaluation

Research and publication assets for Alchedata's work on evaluating agentic AI systems, with both Markdown and LaTeX versions of the white paper.

## Overview

This repository documents a multi-dimensional framework for assessing the readiness, reliability, safety, and economic viability of autonomous AI agents. The central argument is that outcome-only benchmarks are inadequate for agentic systems because they hide process failures, policy violations, and cost inefficiencies that only appear when you inspect the full execution trajectory.

The repository currently includes:

- research notes and source material
- a long-form Markdown white paper
- a blog-oriented summary
- a production-style LaTeX manuscript with modular sections, bibliography, and technical figures
- a generated PDF build of the paper

## Repository Layout

- [Agentic AI Evaluation.md](Agentic%20AI%20Evaluation.md): research notes, outline evolution, and source collection
- [white-paper-agentic-ai-evaluation.md](white-paper-agentic-ai-evaluation.md): full white paper in Markdown
- [blog-agentic-ai-evaluation.md](blog-agentic-ai-evaluation.md): shorter blog-style version of the core ideas
- [latex/main.tex](latex/main.tex): main LaTeX entrypoint for the white paper
- [latex/references.bib](latex/references.bib): bibliography used by the LaTeX manuscript
- [latex/Makefile](latex/Makefile): local build targets for compiling and cleaning the LaTeX document
- [latex/main.pdf](latex/main.pdf): generated PDF output
- [latex/sections/sec3_cognitive.tex](latex/sections/sec3_cognitive.tex): cognitive diagnostics and reasoning trace analysis
- [latex/sections/sec4_evaluator.tex](latex/sections/sec4_evaluator.tex): judge reliability and Agent-as-a-Judge discussion
- [latex/sections/sec5_operational.tex](latex/sections/sec5_operational.tex): economics, safety, and latency
- [latex/sections/sec6_enterprise.tex](latex/sections/sec6_enterprise.tex): enterprise readiness and CLEAR framework
- [latex/sections/sec7_tooling.tex](latex/sections/sec7_tooling.tex): tooling landscape
- [latex/sections/sec89_future_conclusion.tex](latex/sections/sec89_future_conclusion.tex): future directions, conclusion, and recommendations
- [latex/figures/pillar_model.tex](latex/figures/pillar_model.tex): Four-Pillar Model diagram
- [latex/figures/success_masking.tex](latex/figures/success_masking.tex): outcome-only vs trajectory evaluation figure
- [latex/figures/agent_gpa.tex](latex/figures/agent_gpa.tex): Goal-Plan-Action framework figure
- [latex/figures/judge_comparison.tex](latex/figures/judge_comparison.tex): LLM-as-a-Judge vs Agent-as-a-Judge comparison
- [latex/figures/cna_comparison.tex](latex/figures/cna_comparison.tex): cost-normalized accuracy comparison
- [latex/figures/clear_radar.tex](latex/figures/clear_radar.tex): CLEAR radar chart
- [latex/figures/security_layers.tex](latex/figures/security_layers.tex): agentic AI security attack surface
- [latex/figures/measurement_imbalance.tex](latex/figures/measurement_imbalance.tex): measurement imbalance chart

## Core Ideas

### Four-Pillar Model

The framework evaluates agents across four architectural pillars:

- Core Model: instruction following, alignment, calibration
- Memory: retrieval accuracy, update quality, context retention
- Tool Use: tool selection, parameter fidelity, sequencing, recovery
- Environment: permissions, resource constraints, adaptation under change

### CLEAR Framework

The enterprise readiness model emphasizes five deployment dimensions:

- Cost: absolute cost and Cost-Normalized Accuracy (CNA)
- Latency: time to first token and end-to-end responsiveness
- Efficacy: trajectory-aware task success and reasoning quality
- Adherence: policy compliance, constraint handling, idempotency
- Resilience: failure recovery and long-session stability

### Agent-as-a-Judge

The white paper argues that evaluating agents increasingly requires evaluator systems that can inspect trajectories, verify intermediate steps, and reason about process quality rather than judging only final outputs.

## LaTeX Build

The LaTeX document is organized as a modular paper with section files under [latex/sections](latex/sections) and TikZ/PGFPlots figures under [latex/figures](latex/figures).

Build requirements:

- `pdflatex`
- `bibtex`
- `latexmk`

From the [latex](latex) directory:

```bash
make all
```

This compiles [latex/main.tex](latex/main.tex) and produces [latex/main.pdf](latex/main.pdf).

Other supported targets:

- `make clean`: remove LaTeX auxiliary files
- `make view`: open the generated PDF

## Suggested Use

- Read the Markdown white paper for content review and editing.
- Use the LaTeX manuscript for publication-quality export and layout.
- Use the figures as standalone conceptual assets when presenting the framework.
- Use the bibliography as the base reference set for further research and expansion.

---

© 2026 Alchedata. All rights reserved.
