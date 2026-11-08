# claude-cirq-skill

A Claude Code skill for designing, simulating, optimizing, and evaluating quantum circuits with Cirq.

## Overview

Cirq is a Python framework for describing quantum circuits and running them on simulators or supported quantum hardware integrations. This skill provides guidance for circuit construction, simulation, noise modeling, compilation, hardware execution, and quantum experiment workflows.

## Main Capabilities

- Construct circuits from qubits, gates, and moments.
- Simulate ideal circuits and inspect measurement results.
- Model noise and evaluate circuit behavior under imperfect operations.
- Transform and optimize circuits for a target device.
- Prepare circuits for supported quantum hardware providers.
- Design experiments and benchmarks.
- Explore algorithms such as VQE, QAOA, and QPE.
- Compare circuit behavior across simulators and execution backends.

## Installation

Install the core package:

```bash
python -m pip install cirq
```

Optional provider integrations may require additional packages. Install only the integration needed for the target hardware.

Install the skill:

```bash
git clone https://github.com/Brajesh31/claude-cirq-skill.git ~/.claude/skills/cirq
```

## Usage

Invoke the skill for quantum computing tasks:

```text
/cirq
```

Include the target backend, number and type of qubits, algorithm, noise assumptions, and measurement requirements when they are known.

## Basic Circuit Example

```python
import cirq

qubits = cirq.LineQubit.range(2)
circuit = cirq.Circuit(
    cirq.H(qubits[0]),
    cirq.CNOT(qubits[0], qubits[1]),
    cirq.measure(*qubits, key="result"),
)

simulator = cirq.Simulator()
result = simulator.run(circuit, repetitions=1000)
print(result)
```

This example creates an entangled two-qubit state and measures it repeatedly on a simulator.

## Workflow

1. Define the problem and the expected quantum operation.
2. Select qubits and construct the circuit.
3. Inspect circuit moments and gate connectivity.
4. Run an ideal simulation to establish expected behavior.
5. Add a noise model when studying realistic device effects.
6. Apply transformations suitable for the target device.
7. Execute on the selected backend when access and credentials are available.
8. Analyze measurement results and document experimental settings.

## Reference Guide

| File | Focus |
|---|---|
| `references/building.md` | Circuit construction |
| `references/simulation.md` | Simulator workflows |
| `references/noise.md` | Noise models and simulation |
| `references/transformation.md` | Circuit transformations |
| `references/hardware.md` | Hardware execution considerations |
| `references/experiments.md` | Experiment design and evaluation |

## Validation Checklist

- Confirm qubit ordering and measurement keys.
- Check circuit depth and gate connectivity.
- Compare simulation results with expected outcomes.
- Record repetitions and random seeds where applicable.
- State the noise assumptions used.
- Verify hardware constraints before submission.
- Preserve experiment parameters for reproducibility.

## Repository Contents

- `SKILL.md`: Main skill instructions.
- `references/`: Focused guides for circuit construction, simulation, noise, hardware, transformations, and experiments.
- `README.md`: Installation, examples, and workflow overview.

## Notes

Quantum simulation results depend on circuit size, simulator configuration, and noise assumptions. Hardware execution may require provider-specific packages, credentials, access permissions, and device availability.
