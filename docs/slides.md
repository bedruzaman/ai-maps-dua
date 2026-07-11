---
layout: default
title: Presentation
nav_order: 2
---

# Workshop Presentation

<style>
  .presentation-container {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 20px;
    margin: 20px 0;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .presentation-frame {
    position: relative;
    width: 100%;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
    height: 0;
    overflow: hidden;
    border-radius: 6px;
    margin-bottom: 15px;
    display: none;
  }
  
  .presentation-frame.active {
    display: block;
  }
  
  .presentation-frame iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
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
  
  .btn-open {
    background-color: #ff8c42;
    color: white;
  }
  
  .btn-open:hover {
    background-color: #ff7a1f;
    transform: translateY(-2px);
  }
</style>

<div class="presentation-container">
  <h2 style="margin-top: 0; color: #1f2937;">Setup and Introduction to the Workshop</h2>
  
  <div class="button-group">
    <button onclick="toggleSlides()" class="btn btn-open">📊 View Slides</button>
  </div>
  
  <div class="presentation-frame" id="slideFrame">
    <iframe src="https://docs.google.com/presentation/d/1TL0Kd_gScbQyAuGOr4_wC408Q15dwNOwVwVcxf4DbSM/embed?start=false&loop=false&delayms=3000" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
  </div>
</div>

<script>
function toggleSlides() {
  const slideFrame = document.getElementById('slideFrame');
  slideFrame.classList.toggle('active');
  const button = event.target;
  button.textContent = slideFrame.classList.contains('active') ? '📊 Hide Slides' : '📊 View Slides';
}
</script>
