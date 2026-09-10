---
layout: home
nav_exclude: true
---

# Welcome!

<div style="text-align: center; margin: 30px 0;">
  <img id="random-fish" src="" alt="" style="max-height: 300px; max-width: 100%; width: auto;">
  <div id="random-caption" style="margin-top: 10px;">
    <div id="fish-common" style="font-weight: bold; font-size: 1.1em;"></div>
    <div id="fish-species" style="font-style: italic;"></div>
    <div id="fish-museum" style="font-size: 0.85em; color: #aaa;"></div>
  </div>
</div>

<script>
const fish = [
  {% for item in site.data.gallery %}
  { file: "{{ item.file }}", species: "{{ item.species }}", common: "{{ item.common }}", museum: "{{ item.museum }}" },
  {% endfor %}
];

const pick = fish[Math.floor(Math.random() * fish.length)];
document.getElementById("random-fish").src = "/assets/images/gallery/" + pick.file;
document.getElementById("random-fish").alt = pick.species;
document.getElementById("fish-common").textContent = pick.common;
document.getElementById("fish-species").textContent = pick.species;
document.getElementById("fish-museum").textContent = pick.museum;
</script>

**Our Mission:** To make conceptual advances in understanding the diversification of life, inspired by the natural history of fishes.

Our research interests include **macroevolution**, **diversification**, **biogeography**, **phylogenomics**, **ichthyology** and **deep-sea biology**.

**Interested in joining?** Visit the [**Join the Lab**](/join/) page for more information.

---

## Principal Investigator

<div style="display: flex; gap: 30px; align-items: flex-start; margin-bottom: 20px;">
  <div style="flex: 1;">
    <p><strong>Elizabeth Santos</strong> (she/her)<br>
    Assistant Professor & Director of Fishes<br>
    <a href="https://eeob.osu.edu">Department of Evolution, Ecology and Organismal Biology</a><br>
    <a href="https://www.biosci.ohio-state.edu/musbiodiv/">Museum of Biological Diversity</a><br>
    The Ohio State University<br>
    <strong>Contact:</strong> santos.323 'at' osu.edu</p>
  </div>
  <img src="/assets/images/lab_headshots/santos_frontpage.jpg" style="width: 420px; flex-shrink: 0; margin-top: -30px;">
</div>

---

# News


### *August 2026*

New paper in *Evolution*! [Integration promotes morphological innovation in deep-sea anglerfishes](https://doi.org/10.1093/evolut/qpag139) 


### *June 2026*

Two new preprints! 

- [Macroevolution of deep-sea fishes with necks!](https://www.biorxiv.org/content/10.64898/2026.06.21.733442v1.abstract) 

- [Ecomorphological diversification inferred from 571 micro-CT scans of fish skulls](https://www.biorxiv.org/content/10.64898/2026.06.19.733456v1.abstract) 


### *May 2026*

- **Abi Huber** joined as a MS student, and **Shannon Kuznar** joined as a postdoc. Welcome!


### *January 2026*

- Liz was interviewed about deep-sea fishes by Bob McDonald for Quirks and Quarks! [Listen here](https://www.cbc.ca/radio/quirks/jan-17-pumas-penguins-9.7047780)


### *November 2025*

- Our new paper on [deep-sea fish body shapes](https://doi.org/10.1093/evolut/qpaf207) was covered by [OSU News!](https://news.osu.edu/how-fishes-of-the-deep-sea-have-evolved-into-different-shapes/) 


### *August 2025*

- The Santos Lab opens at Ohio State! [See new faculty spotlight](https://eeob.osu.edu/newsletter/2025-2026-edition/new-faculty-spotlights)