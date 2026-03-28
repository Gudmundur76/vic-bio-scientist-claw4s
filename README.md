# Claw4S Submission: VIC-Bio-Scientist

This repository contains the submission for the Claw4S Conference 2026, featuring the **VIC-Bio-Scientist**—an autonomous AI co-scientist for biomedical research. This agent is built upon the **VIC-Architect Eight Pillar Framework (v4.2)** and leverages the **VIC-0-SBVI (Self-Bootstrapping Vertical Intelligence)** engine for continuous learning and optimization of clinical trial protocols.

## Contents

-   `SKILL.md`: The executable skill definition for the VIC-Bio-Scientist.
-   `Research_Note.md`: A detailed research note explaining the scientific methodology and framework.
-   `latex_template/`: Directory containing the LaTeX template for the Research Note (as required by Claw4S).

## VIC-Bio-Scientist Overview

The VIC-Bio-Scientist is designed to:

-   **Autonomously acquire and integrate biomedical knowledge** from primary sources.
-   Apply the **VIC-Architect framework** to ensure rigorous, reproducible, and generalizable research.
-   Utilize **VIC-0-SBVI** to enable continuous learning and adaptation of its internal scientific world model.
-   **Generate optimized clinical trial protocols** based on real-world data and learned insights.

## How to Run the Skill

To execute the `VIC-Bio-Scientist` skill, an AI agent (such as Claw) would interact with it via its defined workflows:

```shell
# Initialize VIC-Bio-Scientist with a research directive
/vic-bio-scientist InitializeVICBio --research_directive "specialize in advanced immunotherapies for autoimmune diseases"

# Execute a research cycle focusing on a specific area
/vic-bio-scientist ExecuteResearchCycle --focus_area "CAR T-cell therapy for lupus"

# Optimize the SLM-core based on new knowledge
/vic-bio-scientist OptimizeSLM
```

## Authorship

-   Gudmundur Eyberg 
-   Claw 🦞 (Co-Author, as per Claw4S Conference requirements)

## License

[MIT License](LICENSE) (Placeholder - actual license to be determined)
