---
layout: default
title: Data
parent: Hands On
nav_order: 2
---

# Dataset Download

<style>
  .resource-card {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 20px;
    margin: 20px 0;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .resource-title {
    font-size: 16px;
    font-weight: 600;
    margin: 0 0 10px 0;
    color: #1f2937;
  }
  
  .resource-description {
    color: #6b7280;
    margin-bottom: 15px;
    font-size: 14px;
  }
  
  .dataset-list {
    list-style: none;
    padding: 0;
    margin-bottom: 15px;
  }
  
  .dataset-list li {
    padding: 8px 0;
    color: #4b5563;
    font-size: 14px;
    border-bottom: 1px solid #e5e7eb;
  }
  
  .dataset-list li:last-child {
    border-bottom: none;
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
    background-color: #ff8c42;
    color: white;
  }
  
  .btn:hover {
    background-color: #ff7a1f;
    transform: translateY(-2px);
  }
</style>

<div class="resource-card">
  <div class="resource-title">Required Geospatial Datasets</div>
  <div class="resource-description">
    Download all necessary datasets for the case study city to complete the DUA mapping workflow:
  </div>
  <ul class="dataset-list">
    <li><strong>Sentinel-2 Imagery:</strong> Multi-spectral stacks for the selected Area of Interest (AOI)</li>
    <li><strong>Building Footprints:</strong> Standardized building vectors</li>
    <li><strong>GHSL Data:</strong> Built-up fraction layers for generating binary masks</li>
    <li><strong>AOI Boundary:</strong> Shapefile defining the city limits</li>
    <li><strong>Reference Polygons:</strong> Pre-digitized DUA polygons for training data</li>
  </ul>
  <a href="https://drive.google.com/drive/u/0/folders/1RaaN0s6PXwAkDleOlr6FjZNLHDvCZ_PN" target="_blank" class="btn">⬇️ Download Data Archive</a>
</div>
