---
layout: splash
title: "Welcome to pyOpenSci"
author_profile: false
published: true
site-map: true
permalink: /
header:
    overlay_image: images/header.jpg
    overlay_filter: 0.6
    actions:
        - label: "Submit a Package"
          url: "https://github.com/pyOpenSci/software-review/issues"
        - label: "Read our Peer Review Guide"
          url: "https://www.pyopensci.org/software-peer-review/"
mission:
  - excerpt: 'We build diverse community that supports free and open Python tools for processing scientific data. We also build technical skills needed to contribute to open source and that support open science. Join our global community.'
programs:
  - image_path: images/brooke-cagle-group-unsplash.png
    image_caption: "Brooke Cagle, Unsplash"
    alt: "placeholder image 1"
    title: "Diverse Community"
    excerpt: "We are building a diverse and supportive community with skills that support open source and open science. Join the discussion on [twitter](https://www.twitter.com/pyopensci) or follow along on [discourse](https://pyopensci.discourse.group/)."
  - image_path: images/desola-lanre-ologun-unsplash.png
    image_caption: "Desola Lanre Ologun, Unsplash"
    alt: "placeholder image 2"
    title: "Open Peer Review"
    excerpt: "Our open peer review process of Python tools supports standardized software quality and usability. It also provides needed credit and visibility to tool maintainers. Finally it removes redundancy of packages with similar functionaly across the scientific Python ecosystem."
    url: /about-peer-review/
    btn_label: "Learn More About Package Peer Review"
    btn_class: "btn--primary"
  - image_path: images/brooke-cagle-unsplash.png
    title: "Skills for Open Source and Open Science"
    image_caption: "Brooke Cagle, Unsplash"
    excerpt: "We will develop a mentorship and training program over the next year to support those who are new to open science and code review. Stay tuned for more."
---

{% include feature_row id="mission" type="center" %}
{% include feature_row id="programs"%}

<div class="notice--info" markdown="1">
## Recent Blog Posts & Updates

<div class="feature__wrapper">
   {% for post in site.categories['highlight'] limit:3 %}
   <div class="feature__item">
      <div class="archive__item">
         <div class="archive__item-body">
            <h3 class="archive__item-title"><a href="{{ site.baseurl }}{{ post.url}}" rel="permalink">{{ post.title }}</a></h3>
            <div class="archive__item-excerpt">
               <p>{{ post.excerpt | markdownify }}</p>
            </div>
         </div>
      </div>
   </div>
   {% endfor %}
</div>

<p><a href="/blog/" class="btn btn--info btn--large">View All Posts <i class="fa fa-4 fa-arrow-circle-right" aria-hidden="true"></i></a></p>
</div>


<!-- packages reviewed -->


## Recently Accepted Python Packages

<div class="grid">
    {% for apackage in site.data.packages %}
    {% if apackage.highlight %}
{% include package-grid.html  %}
    {% endif %}
    {% endfor %}
</div>

<br clear="both">

   <a href="/python-packages/" class="btn btn--info">View All Accepted Packages <i class="fa fa-4 fa-arrow-circle-right" aria-hidden="true"></i></a>

