---
name: vic-bio-scientist
description: An autonomous, self-bootstrapping AI co-scientist for biomedical research, built on the VIC-Architect Eight Pillar Framework and VIC-0-SBVI principles. It autonomously acquires knowledge, analyzes clinical protocols, and generates optimized research designs.
allowed-tools: Bash(curl *), firecrawl, biotech-protocol-review, clinical-trial-protocol-skill, pai-fabric
---

# VIC-Bio-Scientist: A Self-Bootstrapping Agent for Clinical Protocol Evolution

This skill defines an advanced AI co-scientist capable of autonomously conducting biomedical research, specifically focusing on the evolution and optimization of clinical trial protocols. It integrates the foundational principles of the **VIC-Architect Eight Pillar Framework (v4.2)** for robust agent design and the **VIC-0-SBVI (Self-Bootstrapping Vertical Intelligence)** engine for continuous, zero-preset learning and domain construction. The agent leverages specialized biomedical skills (`biotech-protocol-review`, `clinical-trial-protocol-skill`) to execute scientific workflows.

## Purpose

To demonstrate an agent-native approach to scientific discovery and protocol optimization by:
- Autonomously acquiring and integrating biomedical knowledge from primary sources.
- Applying the VIC-Architect framework to ensure rigorous, reproducible, and generalizable research.
- Utilizing VIC-0-SBVI to enable continuous learning and adaptation of its internal scientific world model.
- Generating optimized clinical trial protocols based on real-world data and learned insights.

## Workflows

### 1. `InitializeVICBio` - Initialize Self-Bootstrapping Biomedical Intelligence

**Description:** Sets up the VIC-Bio-Scientist agent, defines its initial biomedical research directive, and establishes the foundational knowledge graph based on VIC-Architect's Memory Architecture.

**Input:** `research_directive` (string) - A high-level goal for VIC-Bio-Scientist's specialization (e.g., "optimize clinical trial designs for novel oncology therapeutics").

**Output:** Confirmation of initialization and the establishment of the agent's initial knowledge domain.

**Integration:**
- Configures the agent's workspace with Segmented Knowledge Graph directories (`anchored/`, `active/`, `growing/`, `archive/`).
- Stores the `research_directive` in persistent memory.

### 2. `ExecuteResearchCycle` - Execute a Biomedical Research and Protocol Evolution Cycle

**Description:** Runs a single iteration of knowledge acquisition, protocol analysis, and optimization. This cycle embodies the Proposer, Coder, and Solver roles of VIC-0-SBVI, guided by VIC-Architect's Reasoning Protocol.

**Input:** `focus_area` (string, optional) - A specific sub-area for the current research cycle (e.g., "PD-1 inhibitor trials"). If not provided, retrieves from memory.

**Output:** Summary of new knowledge acquired, protocol insights, and proposed next steps for optimization.

**Integration:**
- **Knowledge Acquisition (Proposer/Coder):** Uses `firecrawl` to search and scrape relevant scientific literature, clinical trial databases, and regulatory documents. `pai-fabric` is used for structured content extraction.
- **Protocol Analysis (Solver):** Employs `biotech-protocol-review` to parse, eligibility check, safety assess, and cross-verify existing clinical protocols against acquired knowledge.
- **Protocol Optimization (Solver):** Utilizes `clinical-trial-protocol-skill` to generate new or refined protocol designs based on analysis findings and the agent's evolving world model.
- **World Model Update:** Integrates new insights into the Segmented Knowledge Graph, applying CLG Stratification (ANCHORED, SEMI-ANCHORED, PLASTIC, ARCHIVE) and TCE Protocol for knowledge freshness.

### 3. `OptimizeSLM` - Optimize Small Language Model Core for Biomedical Domain

**Description:** Triggers the fine-tuning or re-optimization of the agent's dedicated Small Language Model (SLM) core based on the latest version of its autonomously constructed biomedical corpus. Leverages BitNet b1.58 and M8 (Dendritic Computation) principles for efficiency and domain specificity.

**Input:** None (automatically uses the current corpus).

**Output:** Confirmation of SLM optimization, performance metrics, and readiness for deployment within the biomedical research context.

**Integration:**
- Interacts with the underlying model provider interface for SLM fine-tuning.
- Incorporates the 5-component GRPO Reward (Factual, Analytical, Difficulty, World Model, Temporal Coherence, and Divergence Penalty) into the SLM's training objective.

## Quality Standards (VIC-Architect v4.2 & VIC-0-SBVI)

- **Eight Pillar Compliance:** All agent operations adhere to the VIC-Architect v4.2 Eight Pillar Framework.
- **GRPO Alignment:** All research cycles and SLM optimizations must align with the 5-component GRPO reward signal, emphasizing **Temporal Coherence (10%)** and **Divergence Penalty**.
- **CLG Stratification:** Knowledge must be rigorously categorized (ANCHORED, SEMI-ANCHORED, PLASTIC, ARCHIVE) within the knowledge graph, informed by the LNN-integrated TCE.
- **TCE Adherence:** The Staleness Oscillator (LNN-enhanced) must be active, ensuring dynamic refresh cadences for the biomedical corpus.
- **Factual Accuracy:** The Solver component prioritizes factual accuracy and reliability of ingested data, with cryptographic verification where applicable.
- **Reproducibility:** All generated protocols and research findings must be reproducible by other agents following the `SKILL.md` instructions.

## Example Usage

```shell
# Initialize VIC-Bio-Scientist with a research directive
/vic-bio-scientist InitializeVICBio --research_directive "specialize in advanced immunotherapies for autoimmune diseases"

# Execute a research cycle focusing on a specific area
/vic-bio-scientist ExecuteResearchCycle --focus_area "CAR T-cell therapy for lupus"

# Optimize the SLM-core based on new knowledge
/vic-bio-scientist OptimizeSLM
```
