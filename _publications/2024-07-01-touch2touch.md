---
title: "Touch2Touch: Cross-Modal Tactile Generation for Object Manipulation"
collection: publications
permalink: /publication/2024-07-01-touch2touch
excerpt: 'The diversity of touch sensor designs complicates general-purpose tactile processing. We address this by training a diffusion model for cross-modal prediction, translating tactile signals between GelSlim and Soft Bubble sensors. This enables sensor-specific methods to be applied across sensor types.'
date: 2024-07-01
venue: 'Preprint'
image: "/images/projects/touch2touch.gif"
paperurl: 'https://www.arxiv.org/abs/2409.08269'
website: 'https://www.mmintlab.com/research/touch2touch/'
authors: '<b>Samanta Rodriguez*</b>, Yiming Do*u, Miquel Oller, Andrew Owens, Nima Fazeli'
citation: "{{ authors }} &quot;{{ title }}&quot;.<i> {{venue}} {{ date | date: '%Y' }}</i>."
videourl: 'https://www.mmintlab.com/wp-content/uploads/2024/07/Touch2Touch-CoRL_2024_video.mp4'
---


<img src="{{ page.image }}" alt="{{ page.title }}" style="border-radius: 20px;">

Today’s touch sensors come in many shapes and sizes. This has made it challenging to develop general-purpose touch processing methods since models are generally tied to one specific sensor design. We address this problem by performing cross-modal prediction between touch sensors: given the tactile signal from one sensor, we use a generative model to estimate how the same physical contact would be perceived by another sensor. This allows us to apply sensor-specific methods to the generated signal. We implement this idea by training a diffusion model to translate between the popular GelSlim and Soft Bubble sensors. As a downstream task, we perform in-hand object pose estimation using GelSlim sensors while using an algorithm that operates only on Soft Bubble signals.


{% if page.videourl %}
    {% include video.html videourl=page.videourl %}
{% endif %}
{% if page.videoid %}
    {% include youtube.html videoid=page.videoid %}
{% endif %}

Project website: [{{ page.title }}]({{ page.website }})


[Download paper here]({{page.paperurl}})
