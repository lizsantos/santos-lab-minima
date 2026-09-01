---
layout: page
title: Publications
permalink: /publications/
---

<div style="display: flex; gap: 15px; margin-bottom: 30px;">
  <a href="https://doi.org/10.1038/s41559-024-02586-3" target="_blank">
    <img src="/assets/images/covers/NEE_2025_cover.jpg" style="height: 400px; width: auto;">
  </a>
  <a href="https://doi.org/10.1098/rsbl.2023.0049" target="_blank">
    <img src="/assets/images/covers/biollett_2023_cover.jpg" style="height: 400px; width: auto;">
  </a>
</div>

{% assign years = site.data.scholar | map: "year" %}

<style>
.bibliography li {
  margin-bottom: 20px;
}
</style>

*Note: publications prior to 2025 appear under Elizabeth Miller.*

{% bibliography --group_by year --group_order descending %}