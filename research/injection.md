---
layout: page
title: Research
---

---

### _Injection moulding_

<p style="margin-bottom:1cm;"></p>

**Injection moulding (IM)** is the most widely used polymer processing technique for mass production, capable of handling a broad range of plastic parts, from simple to highly complex geometries. It is a cyclic process that encompasses several stages, from melting polymer pellets to cooling the final product inside the mould. IM industries require substantial investments in machinery and moulds. The production of different parts demands the use of different moulds—even when product variations are minimal—which increases the time required for **design and tool manufacturing** as well as the final product cost. Moreover, for small production batches, the fabrication of conventional steel moulds often results in disproportionately high costs.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/shoe_sole_injection2.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    Polymer melt front in a shoe sole injection.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

To address these challenges, IM industries have been adapting their manufacturing processes to **small series production** and highly **customisable parts**, notably through the use of modular and adaptable moulds. The fabrication of such versatile tools can be partially streamlined with **additive manufacturing/rapid prototyping techniques**, which enable the production of mould inserts that allow rapid modification of mould geometries. However, mould inserts produced with non-conventional techniques can contain mechanically weak components. As a result, these tools must be carefully designed to ensure adequate performance and avoid failures during production, which would otherwise substantially increase overall costs.

Computational modelling tools hold significant potential for supporting **mould design** by predicting the **polymer melt flow**, **mould insert deformation**, and **residual stresses** in parts during material solidification and shrinkage. These capabilities are motivating the IM industry to increasingly adopt computational modelling, moving away from traditional, costly, and time-consuming trial-and-error design methods. However, to simultaneously predict polymer melt flow, mould insert deformation, and residual stresses in produced parts, advanced multi-physics approaches are required, involving **fluid-structure interaction (FSI)** problems.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/shoe_sole_injection3.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    Polymer melt front in a shoe sole injection and mould inserts deformation.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

This investigation forms part of the doctoral thesis project of \[[R. Ribeiro, 2025](https://ricardodpcosta.github.io/activities.html#supervised-theses)] (Doctoral Program in Science and Engineering of Polymers and Composites, University of Minho, Portugal). The envisaged developments will be implemented in the open-source computational library **OpenFOAM**, building on the existing **solids4Foam** toolbox for fluid–structure interaction. This module will be extended to model multi-phase compressible fluid flows, where the polymer phase is described through constitutive equations for **generalised Newtonian fluids**, capturing the rheological behaviour of molten polymers. Furthermore, a **solidification model** will be incorporated to predict dimensional variations of manufactured parts and the resulting **thermal residual stresses**. The developed tool will be released as open-source to maximise its impact and uptake in both academia and industry.
