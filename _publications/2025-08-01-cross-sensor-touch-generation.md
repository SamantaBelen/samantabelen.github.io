---
title: "Cross-Sensor Touch Generation"
collection: publications
permalink: /publication/2025-08-01-cross-sensor-touch-generation
excerpt: 'We prenset a method for tansferring manipulation policies between different tactile sensors by generating cross-sensor tactile signals. Using either a paired diffusion model (T2T) or an unpaired depth-based approach (T2D2), the method enables zero-shot policy transfer without retraining. We demonstrate it on a marble rolling task, where policies learned with one sensor are successfully applied to another.'
date: 2025-08-01
venue: '9th Conference on Robotic Learning (CoRL)'
image: "/images/projects/t2d2/t2d2_bc.gif"
paperurl: 'https://openreview.net/pdf?id=oGcC8nMOit'
website: 'https://samantabelen.github.io/cross_sensor_touch_generation'
authors: '<b>Samanta Rodriguez*</b>, Yiming Dou*, Miquel Oller, Andrew Owens, Nima Fazeli'
citation: "{{ authors }} &quot;{{ title }}&quot;.<i> {{venue}} {{ date | date: '%Y' }}</i>."
videourl: 'https://www.mmintlab.com/wp-content/uploads/2024/07/Touch2Touch-CoRL_2024_video.mp4'
---


<img src="{{ page.image }}" alt="{{ page.title }}" style="border-radius: 20px;">

The constant evolution of tactile sensors makes it challenging to transfer policies across different tactile sensors. We aim to enable tactile policy reutiliztion by generating tactile signals cross-sensors. This is achieved via two main approaches: (1) Touch2Touch (T2T) -- a one-stage diffusion-based model trained on paired sensor data to directly translate tactile images between sensors, and (2) Touch-to-Depth-to-Touch (T2D2) a two-stage unpaired method that uses a shared depth representation to bridge the gap between sensors. These approaches allow existing models—whether learned via Reinforcement Learning (RL) or Imitation Learning (IL)—to be reused with new sensors without retraining.

The effectiveness of the proposed framework is demonstrated on a marble rolling task, where policies trained using one sensor are successfully executed using another through the generated tactile signals. This validates that the generative translation accurately preserves the contact information critical for manipulation. The study also evaluates performance using both visual metrics (PSNR, SSIM, FID) and functional outcomes (e.g., object pose estimation), showing that the method, enables zero-shot policy transfer across heterogeneous tactile hardware in real-world tasks like cup stacking and insertion.


<img src="/images/projects/t2d2/t2d2_method.png" style="border-radius: 20px;">



Project website: [{{ page.title }}]({{ page.website }})


[Download paper here]({{page.paperurl}})
