---
layout: default
title: Code
parent: Lab
nav_order: 3
---

# Mapping Workflow Code

Execute the DUA mapping pipeline using one of the following options:

<style>
  .option-card {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 20px;
    margin: 20px 0;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .option-title {
    font-size: 18px;
    font-weight: 600;
    margin: 0 0 12px 0;
    color: #1f2937;
  }
  
  .option-description {
    color: #6b7280;
    margin-bottom: 15px;
    font-size: 14px;
    line-height: 1.6;
  }
  
  .button-group {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }
  
  .btn {
    display: inline-block;
    padding: 10px 20px;
    border-radius: 6px;
    border: none;
    font-size: 14px;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.3s ease;
  }
  
  .btn-primary {
    background-color: #ff8c42;
    color: white;
  }
  
  .btn-primary:hover {
    background-color: #ff7a1f;
    transform: translateY(-2px);
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
  
  .setup-section {
    margin: 15px 0;
  }
  
  .setup-subtitle {
    font-weight: 600;
    color: #1f2937;
    margin-top: 12px;
    margin-bottom: 8px;
    font-size: 14px;
  }
</style>

## Option 1: Run on Your Own Laptop

<div class="option-card">
  <div class="option-title">💻 Local Setup</div>
  <div class="option-description">
    Clone the repository and set up the environment on your machine using Conda or Docker.
  </div>
  
  <div class="setup-section">
    <strong>Step 1: Clone the Repository</strong>
    <div class="code-block">git clone https://github.com/IDEAtlas/ai-dua-mapping.git</div>
    <div class="code-block">cd ai-dua-mapping</div>
  </div>
  
  <div class="setup-section">
    <div class="setup-subtitle">Choose your environment setup:</div>
    
    <strong>Option A: Using Conda</strong>
    <div class="code-block">python setup.py --conda</div>
    <div class="code-block">conda activate ideatlas</div>
    
    <strong>Option B: Using Docker</strong>
    <div class="code-block">python setup.py --docker</div>
    <div class="code-block">docker exec -it ideatlas bash</div>
  </div>
  
  <div style="margin-top: 15px;">
    <a href="https://github.com/IDEAtlas/ai-dua-mapping" target="_blank" class="btn btn-primary">📖 View Setup Instructions</a>
  </div>
</div>

## Option 2: Launch in Binder

<div class="option-card">
  <div class="option-title">☁️ Interactive Environment</div>
  <div class="option-description">
    Run the notebooks in an interactive Jupyter environment directly in your browser. No installation required!
  </div>
  
  <div style="margin-top: 15px;">
    <a href="https://github.com/IDEAtlas/ai-dua-mapping/blob/main/DUA_mapping.ipynb" target="_blank" class="btn btn-primary">📓 View Notebook</a>
    <a href="https://mybinder.org/v2/gh/IDEAtlas/ai-dua-mapping/HEAD" target="_blank" class="btn btn-primary">🚀 Launch Binder</a>
  </div>
</div>

---

**Note:** Please ensure all required data is placed in the corresponding folders as outlined in the IDEAtlas user handbook.
