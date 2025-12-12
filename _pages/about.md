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