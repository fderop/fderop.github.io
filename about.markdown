---
layout: page
title: About
permalink: /about/
---

## Florian De Rop

<style>
  .lightbox-bg {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 1000;
    justify-content: center;
    align-items: center;
    cursor: pointer;
  }
  
  .lightbox-img {
    max-width: 90%;
    max-height: 90%;
    object-fit: contain;
  }
  
  body.lightbox-open {
    overflow: hidden;
  }
</style>

<img src="/assets/images/myself.jpeg" alt="Florian De Rop" style="width: 225px; margin-bottom: 1rem; cursor: pointer;" onclick="openLightbox('/assets/images/myself.jpeg')">

<div class="social-links">
    <a href="https://x.com/fvderop" title="X"><i class="fa-brands fa-x-twitter"></i></a>
    <a href="https://github.com/fderop" title="GitHub"><i class="fab fa-github"></i></a>
</div>

<script>
  // Create lightbox elements programmatically to ensure they're added to the body
  document.addEventListener('DOMContentLoaded', function() {
    // Create the lightbox container
    const lightbox = document.createElement('div');
    lightbox.id = 'lightbox';
    lightbox.className = 'lightbox-bg';
    lightbox.onclick = closeLightbox;
    
    // Create the image element
    const img = document.createElement('img');
    img.id = 'lightbox-image';
    img.className = 'lightbox-img';
    
    // Add image to lightbox
    lightbox.appendChild(img);
    
    // Add lightbox to document body (not inside the about section)
    document.body.appendChild(lightbox);
  });
  
  function openLightbox(src) {
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-image');
    lightboxImg.src = src;
    lightbox.style.display = 'flex';
    document.body.classList.add('lightbox-open');
  }
  
  function closeLightbox() {
    const lightbox = document.getElementById('lightbox');
    lightbox.style.display = 'none';
    document.body.classList.remove('lightbox-open');
  }
</script>

Technical staff @ [Retro.bio](https://www.retro.bio)  
Previously researcher @ [Aerts lab](https://aertslab.org)  

[HyDrop](https://elifesciences.org/articles/73971)  
[scATAC-seq Benchmark](https://www.nature.com/articles/s41587-023-01881-x)
[scForest](https://github.com/aertslab/scforest/blob/master/scforest.pdf)


