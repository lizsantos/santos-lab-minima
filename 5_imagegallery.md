---
layout: page
title: Image Gallery
permalink: /imagegallery/
---

<style>
.gallery-container {
  text-align: center;
  padding: 20px 0;
}

.gallery-image {
  max-height: 500px;
  max-width: 100%;
  width: auto;
}

.gallery-caption {
  margin-top: 15px;
  font-size: 1em;
}

.gallery-caption .common {
  font-size: 1.2em;
  font-weight: bold;
}

.gallery-caption .species {
  font-style: italic;
}

.gallery-caption .museum {
  font-size: 0.9em;
  color: #aaa;
}

.gallery-nav {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 30px;
  font-size: 1em;
}

.gallery-nav button {
  background: none;
  border: 1px solid #aaa;
  color: #aaa;
  padding: 8px 20px;
  cursor: pointer;
  font-size: 1em;
  border-radius: 4px;
}

.gallery-nav button:hover {
  border-color: white;
  color: white;
}

.gallery-counter {
  color: #aaa;
}
</style>

<div class="gallery-container">
  <img class="gallery-image" id="gallery-img" src="" alt="">
  <div class="gallery-caption">
    <div class="common" id="gallery-common"></div>
    <div class="species" id="gallery-species"></div>
    <div class="museum" id="gallery-museum"></div>
  </div>
  <div class="gallery-nav">
    <button onclick="changeImage(-1)">← Previous</button>
    <span class="gallery-counter"><span id="gallery-current">1</span> / <span id="gallery-total"></span></span>
    <button onclick="changeImage(1)">Next →</button>
  </div>
</div>

<script>
const images = [
  {% for item in site.data.gallery %}
  { file: "{{ item.file }}", species: "{{ item.species }}", common: "{{ item.common }}", museum: "{{ item.museum }}" },
  {% endfor %}
];

let current = 0;

function showImage(index) {
  const item = images[index];
  document.getElementById("gallery-img").src = "/assets/images/gallery/" + item.file;
  document.getElementById("gallery-img").alt = item.species;
  document.getElementById("gallery-species").textContent = item.species;
  document.getElementById("gallery-common").textContent = item.common;
  document.getElementById("gallery-museum").textContent = item.museum;
  document.getElementById("gallery-current").textContent = index + 1;
}

function changeImage(dir) {
  current = (current + dir + images.length) % images.length;
  showImage(current);
}

document.getElementById("gallery-total").textContent = images.length;
showImage(0);
</script>

---

All specimens are from the Scripps Institution of Oceanography Marine Vertebrate Collection, San Diego, CA.