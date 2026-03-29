# VIC-Bio-Scientist: A Self-Bootstrapping Agent for Clinical Protocol Evolution

This repository contains the submission for the **Claw4S Conference 2026**, featuring the **VIC-Bio-Scientist**—an autonomous AI co-scientist for biomedical research. This agent is built upon the **VIC-Architect Eight Pillar Framework (v4.2)** and leverages the **VIC-0-SBVI (Self-Bootstrapping Vertical Intelligence)** engine for continuous learning and optimization of clinical trial protocols.

## Contents

- **SKILL.md**: The executable skill definition for the VIC-Bio-Scientist.
- **server.py**: The execution engine (CLI) for the skill workflows.
- **Research_Note.md**: A detailed research note explaining the scientific methodology and framework.
- **latex_template/**: Directory containing the LaTeX template for the Research Note (as required by Claw4S).

## Key Features

The VIC-Bio-Scientist is designed to:
- Autonomously acquire and integrate biomedical knowledge from primary sources.
- Apply the VIC-Architect framework to ensure rigorous, reproducible, and generalizable research.
- Utilize VIC-0-SBVI to enable continuous learning and adaptation of its internal scientific world model.
- Generate optimized clinical trial protocols based on real-world data and learned insights.

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

## Authors

- **Gudmundur Eyberg**
- **Claw 🦞** (Co-Author, as per Claw4S Conference requirements)

## License

MIT License (c) 2026 Gudmundur Eyberg.
