---
layout: page
title: Research
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  Short description on the major research topics of interest that I have investigated. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

### _General slip boundary conditions_

<p style="margin-bottom:1cm;"></p>

The conventional **no-slip boundary condition** does not hold in several fluid flow problems and must be replaced with appropriate **slip boundary conditions** according to the wall and fluid properties. From **inviscid** to **viscoelastic fluid flows**, imposing appropriate slip boundary conditions is an essential problem in many real engineering applications. However, not only they are still a subject of discussion among fluid dynamicists, but also these conditions are particularly challenging to impose and their numerical treatment is a delicate issue far from being well-developed, particularly in the context of very high-order accurate methods.

The literature on general slip boundary conditions is limited, and the existing methods can only achieve the first- and second-orders of convergence. On the other hand, the complexity of these conditions significantly increases on **curved boundaries**, since the tangential component of the fluid traction vector on the boundary depends on the **boundary line curvature**. In 3D, these conditions become especially challenging since both principal **surface curvatures** are necessary.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:40%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/boundary_minimum_curvature.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:40%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/boundary_maximum_curvature.png' | relative_url }}">
  </div>
</div>
 <div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Boundary minimum curvature.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Boundary maximum curvature.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

In [[Costa et al., 2023](https://doi.org/10.1016/j.cma.2023.116274)], a simple, efficient, and very high-order accurate method is proposed in the FVM paradigm to impose **general slip boundary conditions** prescribed on **arbitrary curved boundaries** for 3D fluid flow problems governed by the **incompressible Navier–Stokes equations**. Following previous works, the pressure-velocity coupling is realised with staggered mesh discretisation approach is employed to handle the **div-grad duality**. On curved boundaries, the slip boundary conditions are reformulated on a local reference system, allowing a direct application of the **ROD method** to achieve the eighth-order of convergence on unstructured meshes.
