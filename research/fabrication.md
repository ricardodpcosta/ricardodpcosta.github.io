---
layout: page
title: Research
---

---

### _Fused filament fabrication_

<p style="margin-bottom:1cm;"></p>

**Fused Filament Fabrication (FFF)** is a subset of material extrusion additive manufacturing that involves the **layer-by-layer deposition** of thermoplastic materials. The process comprises multiple stages, from **feeding** the solid filament into a heated nozzle, to **deposition** onto the build platform or previously deposited layers, followed by **cooling** and **solidification**. Its cost-effectiveness, ease of use, and ability to fabricate geometrically complex components make FFF an attractive manufacturing technology for industrial applications. However, the process often struggles to meet the stringent mechanical, dimensional, and surface quality requirements demanded by industry. While experimental approaches remain the standard for process optimisation, they are typically resource-intensive, time-consuming, and may not yield globally optimal process parameters. Consequently, there is growing interest in **computational modelling** to gain deeper insight into the underlying physical phenomena and to overcome the performance limitations of FFF.

Numerical simulation of the FFF process presents significant challenges due to its inherently **multi-physical** and **multi-scale** nature. Each stage involves complex physical phenomena, including **heat transfer**, **phase change**, **non-Newtonian** polymer behaviour, **interfacial adhesion**, and **interactions** with the surrounding environment and the moving extruder, all occurring over disparate spatial and temporal scales. As a result, simulations often decompose the full process into separate stages, each modelled using specialised numerical tools. In particular, the extrusion and deposition of the molten polymer remains the least understood stage due to its complexity, with many simplifications commonly adopted, which can compromise the representativeness of numerical results.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:80%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/fused_filament_fabrication1.png' | relative_url }}">
  </div>
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:80%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/fused_filament_fabrication2.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    Deposition along a straight path.
  </div>
  <div class="column" style="width:100%; text-align:center;">
    Deposition along a curved path.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

This investigation forms part of the doctoral thesis project of \[[J. Castro, 2025](https://ricardodpcosta.github.io/activities.html#supervised-theses)] (Doctoral Program in Science and Engineering of Polymers and Composites, University of Minho, Portugal). The envisaged developments will be implemented in the open-source computational library **OpenFOAM** to establish a comprehensive computational framework for simulating the FFF process, using a scalable and practical approach to overcome current limitations. The proposed methodology leverages the **oversetMesh** functionality, which enables dynamic mesh handling with overlapping regions, to implement a **dynamic patch** acting as a localised mass source within an incompressible, non-isothermal two-phase flow formulation for immiscible fluids, thereby replicating the deposition of molten polymer. The developed framework will be capable of simulating the deposition of multiple filaments across successive layers, while capturing their temperature profiles and interactions with one another and with machine components. Based on the resulting **temperature distribution** and **filament adhesion**, the tool will allow prediction of mechanical properties, including **dimensional variations** and **residual thermal stresses**. The developed tool will be released as open-source to maximise its impact and uptake in both academia and industry.
