---
layout: page
title: Research
---

---

### _Plastic injection moulding_

<p style="margin-bottom:1cm;"></p>

**Injection moulding (IM)** is the most widely used polymer processing technique for mass production, capable of handling a broad range of plastic parts, from simple to highly complex geometries. It is a cyclic process that encompasses several stages, from melting polymer pellets to cooling the final product inside the mould. IM industries require substantial investments in machinery and moulds. The production of different parts demands the use of different moulds—even when product variations are minimal—which increases the time required for **design and tool manufacturing** as well as the final product cost. Moreover, for small production batches, the fabrication of conventional steel moulds often results in disproportionately high costs.

To address these challenges, IM industries have been adapting their manufacturing processes to **small series production** and highly **customisable parts**, notably through the use of modular and adaptable moulds. The fabrication of such versatile tools can be partially streamlined with **additive manufacturing/rapid prototyping techniques**, which enable the production of mould inserts that allow rapid modification of mould geometries. However, mould inserts produced with non-conventional techniques can contain mechanically weak components. As a result, these tools must be carefully designed to ensure adequate performance and avoid failures during production, which would otherwise substantially increase overall costs.

Computational modelling tools hold significant potential for supporting **mould design** by predicting both the **polymer melt flow** and the **mould inserts mechanical behaviour**. These capabilities are motivating the IM industry to increasingly adopt computational modelling, moving away from traditional, costly, and time-consuming trial-and-error design methods. However, to simultaneously predict polymer melt flow and mould insert mechanical behaviour, advanced multi-physics approaches are required, involving **fluid-structure interaction (FSI)** between the polymer melt and the mould inserts.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/shoe_sole_injection2.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    Polymer melt front and mould inserts deformation.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

<!--
The proposed project aims the development of a computational model able to support the shoe soles industry, in the improvement of their shoe sole fabrication process, including mold design tasks and prediction/correction of manufactured part defects. In that regard, not only the flow behaviour in the mold cavities will be simulated, but also the tool deformation and the residual stresses induced in the manufactured parts. Therefore, the developed codes will be able to support mold design tasks, including molds with weak accessories produced through rapid prototyping techniques. For these purposes, solidification and shrinkage of the materials inside the mold, motivated by temperature gradients during the cooling stage, will be considered in the developed computational model.

The envisaged developments will be implemented in the open-source computational library OpenFOAM® [1], based on the available solids4Foam toolbox [2], a fluid-structure interaction module. This module will be adapted to model multi-phase flows of compressible fluids, where the polymer phase requires constitutive equations for generalized Newtonian fluids, to mimic the rheological behaviour of molten polymers. Additionally, the codes will be complemented with a solidification model to predict the dimensional variations of the manufactured parts and the induced residual stresses. The developed tool will be made available to the community to increase its potential impact and exploitation in academia and industry.
-->
