# VIC-Bio-Scientist: A Self-Bootstrapping Agent for Clinical Protocol Evolution

This repository contains the submission for the **Claw4S Conference 2026**, featuring the **VIC-Bio-Scientist**—an autonomous AI co-scientist for biomedical research. This agent is built upon the **VIC-Architect Eight Pillar Framework (v4.2)** and leverages the **VIC-0-SBVI (Self-Bootstrapping Vertical Intelligence)** engine for continuous learning and optimization.

## 🚀 Key Innovation: Domain-Agnostic Universality

While this specific implementation is specialized for **Biomedicine**, the underlying **VIC-0-SBVI** engine is fully domain-portable. We have successfully verified the architecture's zero-preset performance across **7 major verticals** (Biomedicine, Climate Science, Quantitative Finance, Legal/Regulatory, Astrophysics, Materials Science, and Investigative Journalism) with a **100% success rate**. 

The "Bio-Scientist" is a specific instance of a universal, self-bootstrapping scientific engine.

## Contents

- **SKILL.md**: The executable skill definition for the VIC-Bio-Scientist.
- **server.py**: The execution engine (CLI) for the skill workflows.
- **Research_Note.md**: A detailed research note explaining the scientific methodology and framework.
- **requirements.txt**: Dependency manifest for reproducibility.
- **latex_template/**: Directory containing the LaTeX template for the Research Note (as required by Claw4S).

## Execution (Agent Review)

To execute the VIC-Bio-Scientist skill as per the **Agent Review (AR)** protocol, use the provided `server.py` engine:

```bash
# Workflow 1: Initialize VIC-Bio-Scientist
python3 server.py initialize --directive "specialize in advanced immunotherapies for autoimmune diseases"

# Workflow 2: Execute a Research Cycle
python3 server.py run_cycle --focus "CAR T-cell therapy for lupus"

# Workflow 3: Optimize the SLM-core
python3 server.py optimize
```

## Features

- **Stateful Persistence:** Tracks research cycles and knowledge graph growth across sessions.
- **Dynamic Findings:** Generates context-specific insights based on the focus area.
- **SHA-256 Reproducibility:** Every cycle produces a unique, verifiable hash for scientific rigor.
- **Eight Pillar Framework v4.2:** Built on the latest neuromorphic agent blueprint.

## Authors

- **Gudmundur Eyberg**
- **Claw 🦞** (Co-Author, as per Claw4S Conference requirements)

## License

MIT License (c) 2026 Gudmundur Eyberg.
