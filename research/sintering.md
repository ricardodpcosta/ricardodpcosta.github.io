---
layout: page
title: Research
---

---

### _Selective laser sintering_

<p style="margin-bottom:1cm;"></p>


**Selective laser sintering (SLS)** is a powder bed fusion (PBF) process and one of the most prominent **additive manufacturing (AM)** technologies. Its popularity has been steadily increasing across critical and demanding industries due to its ability to fabricate parts with highly complex geometries and desirable mechanical properties, often with the potential to replace more expensive conventional processes. In SLS, parts are produced **layer-by-layer**, which enables the manufacture of intricate geometries without the need for additional tooling, while also reducing material waste since only the consolidated material is consumed. Combined with the possibility of fast design iterations, these characteristics make SLS particularly **cost-effective**, especially for **prototyping** and **low-volume production**. The use of a high-energy laser as the heat source directed onto a powder bed of fine particles ensures higher resolution, accuracy, and surface quality compared to other AM techniques. Furthermore, SLS offers superior mechanical properties, faster printing speeds, and greater versatility in machine configurations and compatible materials, consolidating its position as the most widely adopted AM process in engineering applications.

The intrinsic complexity of the SLS process arises from the interaction of **multi-physics phenomena**, which often hampers its broader industrial implementation. Conventional experimental optimisation is not only costly and time-consuming, but it can also fail to identify optimal configurations, motivating researchers to turn to computational modelling as a means of achieving deeper process understanding.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:80%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/selective_laser_sintering.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    Sintering and temperature distribution.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

In \[[J. Castro et al., 2023](https://doi.org/10.1063/5.0159825)], we developed a computational framework to simulate the SLS process for polymeric applications at the **particle-length scale**, aiming to capture the influence of the most significant process parameters. Specifically, **LIGGGHTS** was employed to simulate powder bed deposition with a realistic particle size distribution, while **OpenFOAM** was used to model the heat and mass transfer phenomena as well as the laser-induced sintering between particles on a representative powder bed section. In a subsequent work, \[[J. Castro et al., 2024](https://doi.org/10.3390/ma17081845)], we extended the model to account for both virgin and reused polymer granules with different viscosities, providing a more faithful representation of the actual feedstock. The numerical predictions showed strong agreement with experimental observations, confirming the potential of the developed model as a powerful tool to analyse and optimise the SLS process.
