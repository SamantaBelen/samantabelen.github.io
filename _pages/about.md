---
permalink: /
title: "Samanta Rodriguez"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I’m a Ph.D. Candidate in Robotics at the University of Michigan, working in the [MMINT Lab](https://mmintlab.com), advised by [Prof. Nima Fazeli](https://www.mmintlab.com/people/nima-fazeli/) and co-advised by [Prof. Andrew Owens](https://andrewowens.com/). I successfully defended my doctoral dissertation on **November 21st, 2025**.

My research focuses on **tactile-centric robot learning**, including cross-sensor tactile generation, tactile representation learning, and visuo-tactile models for manipulation and in-hand state estimation.

I have led projects such as [Contrastive Touch-to-Touch Pretraining (CTTP)](https://arxiv.org/pdf/2410.11834) and [Cross-Sensor Touch Generation](https://openreview.net/pdf?id=oGcC8nMOit), where I developed methods for translating across heterogeneous tactile sensors and building generalizable tactile representations.

My research aims to enable robots to understand and interact with the physical world through **rich multimodal tactile perception**, supporting more adaptive and robust manipulation.

I am excited to continue advancing tactile sensing and robot learning, and to explore opportunities where robots can understand and interact with the physical world through touch.

# Highlights

<p style="float: left; position: relative; margin-right: 5px;">
  <a href="/publication/2024-08-01-cctp">
    <img src="/images/projects/cttp.png" width="250" style="border-radius:5%; cursor: pointer; transition: transform 0.2s ease-in-out;"/>
    <span class="image-text">Contrastive Touch-to-Touch Pretraining</span>
  </a>
</p>

<p style="float: left; position: relative; margin-right: 5px;">
  <a href="/publication/2024-07-01-touch2touch">
    <img src="/images/projects/touch2touch.gif" width="250" style="border-radius:5%; cursor: pointer; transition: transform 0.2s ease-in-out;"/>
    <span class="image-text">Touch2Touch</span>
  </a>
</p>

<p style="float: left; position: relative;">
  <a href="/publication/2025-08-01-cross-sensor-touch-generation">
    <img src="/images/projects/t2d2/t2d2_bc.gif" width="250" style="border-radius:5%; cursor: pointer; transition: transform 0.2s ease-in-out;"/>
    <span class="image-text">Cross-Sensor Touch Generation</span>
  </a>
</p>

<div style="clear: both;"></div>


<style>
  /* Hover effect for enlarging the image */
  a img:hover {
    transform: scale(1.1);
  }

  /* Text appearance settings */
  .image-text {
    position: absolute;
    bottom: 10px;
    left: 50%;
    width: 80%;
    transform: translateX(-50%);
    background-color: rgba(0, 0, 0, 0.6);
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    display: none;
    font-size: 14px;
    text-align: center;
  }

  /* Show text when hovering over the image */
  a:hover .image-text {
    display: block;
  }

  /* Apply shadowing and reduce opacity only when hovered */
  a img:hover {
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
    opacity: 1; /* Reset opacity to full */
  }

  /* Remove opacity and shadowing when not hovered */
  a img {
    opacity: 1; /* Ensure opacity is normal when not hovered */
    transition: opacity 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  }
</style>


<!-- Button to toggle content -->
<div style="text-align: center; margin-top: 1em;">
  <button 
    onclick="toggleContent()" 
    style="
      background-color: #007BFF; 
      color: white; 
      padding: 15px 30px; 
      font-size: 18px; 
      border: none; 
      border-radius: 25px; 
      cursor: pointer;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);"
  >
    Show More
  </button>
</div>

<!-- Content to toggle -->
<div id="moreContent" style="display: none; margin-top: 1em;">
  <h1> Publications </h1>
  
  {% include base_path %}

  {% for post in site.publications reversed %}
    {% include archive-single-publication.html %}
  {% endfor %}
</div>

<script>
  function toggleContent() {
    const content = document.getElementById("moreContent");
    const button = event.target;

    if (content.style.display === "none") {
      content.style.display = "block";
      button.innerText = "Show Less";
    } else {
      content.style.display = "none";
      button.innerText = "Show More Research Projects";
    }
  }
</script>


<!-- <h2>Featured GitHub Projects</h2>

<div style="display: flex; flex-wrap: wrap; gap: 20px; margin-top: 1em;">

  <!-- GitHub Repo 1 -->
  <a href="https://github.com/mr-mikmik/mik_tools" target="_blank" style="text-decoration: none; color: inherit;">
    <div style="
      width: 180px;
      border-radius: 10px;
      border: 1px solid #e1e4e8;
      padding: 16px;
      background-color: #f9f9f9;
      transition: transform 0.2s ease-in-out;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);">
      <!-- Header with icon -->
      <div style="display: flex; align-items: center; gap: 10px;">
        <svg height="20" viewBox="0 0 16 16" version="1.1" width="20" aria-hidden="true">
          <path fill="currentColor" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        <h3 style="margin: 0;">mik_tools</h3>
      </div>
      <!-- <h3 style="margin-top: 0;"></h3> -->
      <p style="margin-bottom: 0.5em; margin-top: 0.5em; margin-left: 0.5em">🔧 General coding tools.</p>
      <!-- <p style="font-size: 14px; color: #586069;">GitHub · ⭐ Stars · 🍴 Forks</p> -->
    </div>
  </a>

  <!-- GitHub Repo 2 -->
  <a href="https://github.com/UM-ARM-Lab/pytorch_mppi" target="_blank" style="text-decoration: none; color: inherit;">
    <div style="
      width: 180px;
      border-radius: 10px;
      border: 1px solid #e1e4e8;
      padding: 16px;
      background-color: #f9f9f9;
      transition: transform 0.2s ease-in-out;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);">
      <!-- Header with icon -->
      <div style="display: flex; align-items: center; gap: 10px;">
        <svg height="20" viewBox="0 0 16 16" version="1.1" width="20" aria-hidden="true">
          <path fill="currentColor" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        <h3 style="margin: 0;">pytorch_mppi</h3>
      </div>
      <p style="margin-bottom: 0.5em; margin-top: 0.5em; margin-left: 0.5em">🤖 MPPI on PyTorch</p>
      <!-- <p style="font-size: 14px; color: #586069;">GitHub · ⭐ Stars · 🍴 Forks</p> -->
    </div>
  </a>

  <!-- GitHub Repo 3 -->
  <a href="https://github.com/MMintLab/manipulation_via_membranes" target="_blank" style="text-decoration: none; color: inherit;">
    <div style="
      width: 320px;
      border-radius: 10px;
      border: 1px solid #e1e4e8;
      padding: 16px;
      background-color: #f9f9f9;
      transition: transform 0.2s ease-in-out;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);">
      <!-- Header with icon -->
      <div style="display: flex; align-items: center; gap: 10px;">
        <svg height="20" viewBox="0 0 16 16" version="1.1" width="20" aria-hidden="true">
          <path fill="currentColor" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        <h3 style="margin: 0;">manipulation_via_membranes</h3>
      </div>
      <p style="margin-bottom: 0.5em; margin-top: 0.5em; margin-left: 0.5em"> Soft-bubbles perception and control.</p>
      <!-- <p style="font-size: 14px; color: #586069;">GitHub · ⭐ Stars · 🍴 Forks</p> -->
    </div>
  </a>

</div>

<style> -->
  a div:hover {
    transform: scale(1.03);
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  }
</style>
