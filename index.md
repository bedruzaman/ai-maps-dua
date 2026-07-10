---
layout: default
title: Home
nav_order: 1
---

# AI-Driven Mapping of Deprived Urban Areas (DUA)

IDEAtlas is a research initiative focused on mapping the extent and spatial patterns of Deprived Urban Areas (DUA). This project leverages multi-branch deep learning and Earth Observation (EO) data to provide consistent, scalable spatial intelligence.

This site contains the technical training materials required to implement the mapping pipeline, transition from raw sensor data to classified outputs, and generate indicators aligned with SDG 11.1.1.

## Training Objectives

This training module provides the operational knowledge needed to execute the IDEAtlas workflow. Participants will learn to:
*   Configure the processing environment.
*   Manage input datasets (Sentinel-2, building footprints, and reference data).
*   Execute the multi-branch CNN (MB-CNN) pipeline for classification.
*   Adapt the model for specific city contexts using local reference data.
*   Compute SDG 11.1.1 statistics from classified DUA maps.

## Requirements

The mapping pipeline requires a computational environment capable of processing multi-modal EO data.

### Hardware
*   **GPU:** Recommended for efficient model training and fine-tuning.
*   **Storage:** Sufficient capacity for Sentinel-2 imagery stacks and intermediate patch files.

### Software
*   **Docker:** Recommended for maintaining consistent dependencies.
*   **Conda:** An alternative environment management system for managing Python packages.
*   **Git:** Required to clone the repository and manage version control.

## Workflow Overview

The system is managed via a centralized `main.py` script. The workflow follows a standard operational path:

1.  **Environment Setup:** Initialize the Docker or Conda environment as defined in the repository.
2.  **Data Acquisition:** The pipeline automatically retrieves city boundaries and spectral data based on the provided parameters.
3.  **Pipeline Execution:** Run the `main.py` script using the required arguments (`--task`, `--city`, `--country`, `--year`).
4.  **Validation & Stats:** Generate DUA extent maps and compute SDG 11.1.1 summary indicators.

---

## Contents

1. [Project Introduction](intro.md)
2. [Environment Setup](setup.md)
3. [Running the Pipeline](pipeline.md)
4. [Data Requirements](data.md)
5. [Validation & Reporting](validation.md)
```eof
