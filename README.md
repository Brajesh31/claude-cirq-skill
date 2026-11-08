# Cirq

Quantum computing framework for building, simulating, optimizing, and executing quantum circuits. Use this skill when working with quantum algorithms, quantum circuit design, quantum simulation (noiseless or noisy), running on quantum hardware (Google, IonQ, AQT, Pasqal), circuit optimization and compilation, noise modeling and characterization, or quantum experiments and benchmarking (VQE, QAOA, QPE, randomized benchmarking).

## Overview

This repository preserves the original AITMPL skill definition, reference documentation, reusable assets, and scripts at their original relative paths.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-cirq-skill.git ~/.claude/skills/cirq
```

On Windows, use `%USERPROFILE%\.claude\skills\cirq` as the destination.

## Usage

Claude Code can load this skill when a request matches its description. Invoke directly with `/cirq` when appropriate.

## Repository structure

```text
cirq/
├── SKILL.md
├── references/building.md
├── references/experiments.md
├── references/hardware.md
├── references/noise.md
├── references/simulation.md
├── references/transformation.md
├── README.md
└── LICENSE
```

## Runtime requirements

- No build step is required for the instruction file.
- Check the scripts for package imports and API requirements before execution.
- Network-backed citation lookups may require external connectivity and service availability.
- No scripts or tests are claimed as executed.
