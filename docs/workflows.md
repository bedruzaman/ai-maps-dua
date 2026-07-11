---
layout: default
title: Workflows
parent: Code
nav_order: 2
---

# DUA Mapping Workflows

This section provides the commands to execute the four core workflows of the DUA mapping pipeline. Make sure your environment is set up before running these commands (see [Environment Setup](environment.md)).

All commands follow this general pattern, with variations for each task:
```
python main.py --task <task_name> --city <city_name> --country <country_name> --year <year>
```

<style>
  .workflow-card {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 20px;
    margin: 20px 0;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .workflow-title {
    font-size: 18px;
    font-weight: 600;
    margin: 0 0 12px 0;
    color: #1f2937;
  }
  
  .workflow-description {
    color: #6b7280;
    margin-bottom: 15px;
    font-size: 14px;
    line-height: 1.6;
  }
  
  .code-block {
    background-color: #f5f5f5;
    border-left: 4px solid #ff8c42;
    padding: 12px;
    margin: 10px 0;
    border-radius: 4px;
    font-family: 'Courier New', monospace;
    font-size: 13px;
    overflow-x: auto;
  }
  
  .workflow-section {
    margin: 12px 0;
  }
  
  .subsection-title {
    font-weight: 600;
    color: #1f2937;
    margin-top: 10px;
    margin-bottom: 8px;
    font-size: 14px;
  }
</style>

## 1. Training from Scratch

<div class="workflow-card">
  <div class="workflow-title">🛠️ Training from Scratch</div>
  <div class="workflow-description">
    Train a new model on your complete dataset. This is useful when you have sufficient labeled data for your specific city or region.
  </div>
  
  <div class="workflow-section">
    <div class="code-block">python main.py --task train --city nairobi --country kenya --year 2024</div>
  </div>
</div>

## 2. Fine-tuning with Pre-trained Weights

<div class="workflow-card">
  <div class="workflow-title">🎚️ Fine-tuning with Pre-trained Weights</div>
  <div class="workflow-description">
    Adapt the global IDEAtlas pre-trained model to your specific geographic context. Use this when you have limited local reference data.
  </div>
  
  <div class="workflow-section">
    <div class="subsection-title">Using default global model weights:</div>
    <div class="code-block">python main.py --task finetune --city nairobi --country kenya --year 2024</div>
  </div>
  
  <div class="workflow-section">
    <div class="subsection-title">Using custom weights:</div>
    <p style="color: #6b7280; font-size: 14px; margin-bottom: 8px;">Replace <code style="background-color: #f5f5f5; padding: 2px 4px; border-radius: 3px;">{custom}</code> with the actual name of the model weight file:</p>
    <div class="code-block">python main.py --task finetune --city nairobi --country kenya --year 2024 --weights checkpoint/custom.h5</div>
  </div>
</div>

## 3. Classification/Inference

<div class="workflow-card">
  <div class="workflow-title">🗺️ Classification/Inference</div>
  <div class="workflow-description">
    Generate segmentation maps from a trained or fine-tuned model. This creates the DUA classification output for your study area.
  </div>
  
  <div class="workflow-section">
    <div class="subsection-title">Using city-specific weights:</div>
    <div class="code-block">python main.py --task classify --city nairobi --country kenya --year 2024</div>
  </div>
  
  <div class="workflow-section">
    <div class="subsection-title">Using custom weights:</div>
    <p style="color: #6b7280; font-size: 14px; margin-bottom: 8px;">Replace <code style="background-color: #f5f5f5; padding: 2px 4px; border-radius: 3px;">{custom}</code> with the actual name of the model weight file:</p>
    <div class="code-block">python main.py --task classify --city nairobi --country kenya --year 2024 --weights checkpoint/custom.h5</div>
  </div>
</div>

## 4. SDG Statistics

<div class="workflow-card">
  <div class="workflow-title">📊 SDG Statistics</div>
  <div class="workflow-description">
    Compute SDG 11.1.1 statistics from classified rasters. This calculates the percentage and extent of deprived urban areas in your study region.
  </div>
  
  <div class="workflow-section">
    <div class="code-block">python main.py --task sdg_stats --city nairobi --country kenya --year 2024</div>
  </div>
</div>

---

**Note:** Ensure all required input data is placed in the corresponding folders as outlined in the IDEAtlas user handbook before running these workflows.
