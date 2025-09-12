---
layout: page
title: Research
---

---

### _Plastic injection moulding_

<p style="margin-bottom:1cm;"></p>


The present PhD project concerns the application of computational tools in the study of injection molding processes, especially focused on the shoe soles for the footwear industry. Recently, this industrial sector has been seeking to adapt its fabrication processes to small production series and highly customizable parts, which demands for modular and adaptable molds. The fabrication of such complex tools, can be partially simplified by resorting to additive manufacturing/rapid prototyping techniques. However, mold inserts can contain mechanically weak components, especially when produced with such non-conventional techniques. Therefore, these tools must be carefully designed to ensure an adequate performance and to avoid problems during production, which would substantially increase their cost.
The proposed project aims the development of a computational model able to support the shoe soles industry, in the improvement of their shoe sole fabrication process, including mold design tasks and prediction/correction of manufactured part defects. In that regard, not only the flow behaviour in the mold cavities will be simulated, but also the tool deformation and the residual stresses induced in the manufactured parts. Therefore, the developed codes will be able to support mold design tasks, including molds with weak accessories produced through rapid prototyping techniques. For these purposes, solidification and shrinkage of the materials inside the mold, motivated by temperature gradients during the cooling stage, will be considered in the developed computational model.
The envisaged developments will be implemented in the open-source computational library OpenFOAM® [1], based on the available solids4Foam toolbox [2], a fluid-structure interaction module. This module will be adapted to model multi-phase flows of compressible fluids, where the polymer phase requires constitutive equations for generalized Newtonian fluids, to mimic the rheological behaviour of molten polymers. Additionally, the codes will be complemented with a solidification model to predict the dimensional variations of the manufactured parts and the induced residual stresses. The developed tool will be made available to the community to increase its potential impact and exploitation in academia and industry.


<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    <img style="width:80%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/shoe_sole_injection2.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:100%; text-align:center;">
    Polymer melt front and mold inserst deformation.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>
