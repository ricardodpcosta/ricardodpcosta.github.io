---
layout: page
title: Research
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  Short description on the major research topics of interest that I have investigated. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

### _High-order accurate discretisation_

<p style="margin-bottom:1cm;"></p>

Treating complex geometries is critical in developing high-order accurate discretisation methods (above the second-order) for the numerical simulation of real engineering applications. However, most works published in that context only consider simple domains with straight/polygonal boundaries, substantially limiting their practical applicability. In particular, the treatment of curved domains requires sophisticated techniques to overcome the geometrical mismatch between the **physical boundary** (where the boundary conditions are prescribed) and the **mesh boundary** (where the equations are discretised).

In the finite element paradigm, the **isoparametric elements method** has become the conventional approach for treating curved boundaries and recovering the optimal high-order of convergence. The technique employs **curved meshes** to geometrically fit the physical boundary, and similar techniques have been proposed for the finite volume (FVM) and discontinuous Galerkin (DGM) methods. Although effective, these techniques suffer from significant drawbacks, such as:

- **Sophisticated meshing algorithms** for generating meshes with curved elements.
- **Cumbersome quadrature rules** for integration on the curved elements.
- **Complex nonlinear transformations** for the mapping between curved and standard elements.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:50%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/curved_mesh.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:50%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/polygonal_mesh.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Curved mesh element.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Linear piecewise mesh element.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

In [[Costa et al., 2018](https://doi.org/10.1016/j.apm.2017.10.016); [Costa et al., 2019](https://doi.org/10.1002/nme.5953)], a novel approach is proposed, the **reconstruction for off-site data (ROD) method**, to recover the high-order of convergence for arbitrary curved boundaries while overcoming such limitations. The ROD method transfers the prescribed boundary conditions from the physical boundary to the mesh boundary through specific constrained polynomial reconstructions, while the problem unknowns are defined on the mesh and the discretisation is performed on linear piecewise elements solely, thus requiring:

- **Conventional meshing algorithms** for generating meshes with linear piecewise elements.
- **Simple quadrature rules** for integration on the linear piecewise elements.

The technique was developed in the FVM paradigm for the 2D convection-diffusion problem with **general boundary conditions**, effectively achieving the sixth-order of convergence on unstructured meshes. The proposed approach has received significant attention from the scientific community for its **simplicity**, **efficiency**, and **generality** in handling any boundary condition, and the extension to the FDM and DGM has already been successfully accomplished [[Fernández-Fidalgo et al., 2020](https://doi.org/10.1016/j.cma.2019.112782); [Clain et al., 2021](https://doi.org/10.1016/j.jcp.2021.110217); [Santos et al., 2024](https://doi.org/10.1007/s10915-024-02613-2)].

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/curved_domain.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/unstructured_mesh.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Curved domain.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Unstructured mesh.
  </div>
</div>
