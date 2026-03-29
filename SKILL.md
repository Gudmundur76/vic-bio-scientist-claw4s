---
name: vic-bio-scientist
description: An autonomous, self-bootstrapping AI co-scientist for biomedical research, built on the VIC-Architect Eight Pillar Framework and VIC-0-SBVI principles. It autonomously acquires knowledge, analyzes clinical protocols, and generates optimized research designs with real-time web-search and CLG stratification.
allowed-tools: python3, requests, re, hashlib, shutil
---

# VIC-Bio-Scientist: A Self-Bootstrapping Agent for Clinical Protocol Evolution

This skill defines an advanced AI co-scientist capable of autonomously conducting biomedical research, specifically focusing on the evolution and optimization of clinical trial protocols. It integrates the foundational principles of the **VIC-Architect Eight Pillar Framework (v4.2)** and the **VIC-0-SBVI (Self-Bootstrapping Vertical Intelligence)** engine for continuous, zero-preset learning.

## Fixed v1.0 Features
The v1.0 implementation transitions from a simulation skeleton to a functional research engine:
- **Real Data Acquisition:** Active web-scraping of biomedical sources (PubMed/DuckDuckGo).
- **Dynamic Entity Extraction:** Pattern-based parsing of therapies, biomarkers, and protocols.
- **CLG Stratification:** Automated knowledge layering into ANCHORED, ACTIVE, GROWING, and ARCHIVE based on freshness.
- **TCE Scoring:** Source-aware temporal context scoring to manage knowledge decay.
- **GRPO Reward Calculation:** Real-time computation of factual, analytical, and temporal metrics.

## Installation & Setup

To execute the VIC-Bio-Scientist, the following environment is required:
1. **Python 3.10+**
2. **Dependencies:** `pip install -r requirements.txt`

The execution engine is provided in `server.py`.

## Workflows

### 1. `InitializeVICBio` - Initialize Self-Bootstrapping Biomedical Intelligence

**Description:** Sets up the VIC-Bio-Scientist agent, cleans the workspace, and establishes the foundational knowledge graph directories.

**Execution:**
```shell
python3 server.py initialize --directive "optimize clinical trial designs for novel oncology therapeutics"
```

### 2. `ExecuteResearchCycle` - Execute a Biomedical Research and Protocol Evolution Cycle

**Description:** Runs a single iteration of knowledge acquisition, entity extraction, and gap analysis.

**Execution:**
```shell
python3 server.py run_cycle --focus "CAR T-cell therapy for lupus"
```

**Workflow Steps:**
- **Acquisition:** Real-time search of scientific literature and clinical databases.
- **Extraction:** Automated parsing of structured entities (Therapies, Biomarkers).
- **Analysis:** Domain-specific protocol gap identification (Lupus/Oncology).
- **Stratification:** Knowledge layering based on the TCE (Temporal Context Engine) score.
- **Reproducibility:** SHA-256 hashing of the entire research entry for scientific rigor.

### 3. `OptimizeSLM` - Optimize Small Language Model Core

**Description:** Computes the GRPO (Generative Reward Policy Optimization) alignment scores based on the autonomously constructed corpus.

**Execution:**
```shell
python3 server.py optimize
```

**Metrics:**
- **Temporal Coherence:** Freshness weighted by source stability.
- **Factual Accuracy:** Derived from source diversity and entity density.
- **Analytical Depth:** Measured by extraction richness across cycles.

## Quality Standards (VIC-Architect v4.2)

- **Pillar 4 (CLG):** Rigorous categorization of knowledge into temporal layers.
- **Pillar 5 (TCE):** Active staleness detection for biomedical data.
- **Pillar 7 (Reproducibility):** Cryptographic verification of every research cycle.
- **GRPO Alignment:** Real-time reward signaling for model fine-tuning.

## Example Usage

```shell
# Initialize
python3 server.py initialize --directive "specialize in advanced immunotherapies"

# Run Research Cycle
python3 server.py run_cycle --focus "CAR T-cell therapy for lupus"

# Optimize Core
python3 server.py optimize
```
