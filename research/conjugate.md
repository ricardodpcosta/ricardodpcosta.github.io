---
layout: page
title: Research
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  Short description on the major research topics of interest that I have investigated. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

### _Conjugate heat transfer problems_

<p style="margin-bottom:1cm;"></p>

Many real engineering applications concern **non-isothermal physical systems** that involve thermodynamic processes between solids and fluids, consisting of materials with different thermal properties that are **thermally coupled** through non-adiabatic contacts. The **conjugate heat transfer** (CHT) problem consists in determining the temperature distribution in these **multi-material domains** with specific thermodynamic laws applied for the heat transfer on the contacts.

Many multi-physics problems in fluid mechanics, solid mechanics, and electromagnetics involve multi-material domains and physical quantities that depend on the temperature, such as **thermomechanics**, **thermoelasticity**, **electrothermomagnetics**, and **fluid-thermal-structure interaction**. Thus, the development of accurate and robust discretisation methods for elliptic and parabolic equations with discontinuous coefficients is an essential challenge in the numerical simulation of real engineering applications.

In CHT, specific **interface conditions** are prescribed on the interface depending on the nature of the contact, usually imposing a discontinuous normal derivative of temperature due to the thermal energy conservation that needs to be satisfied. Additionally, if a **perfect contact without friction** is assumed, a continuous temperature across the interface is imposed (**continuity interface condition**), whereas real scenarios might require to assume **imperfect contacts with friction** resulting in an implicit temperature jump cross the interface (**jump interface condition**).

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/continuity_interface_condition.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/jump_interface_condition.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Continuity interface condition.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Jump interface condition.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

Treating multi-domain problems with discontinuous coefficients requires a special interface treatment, particularly for achieving a high-order of convergence. In [[Costa et al., 2019](https://doi.org/10.1016/j.cma.2019.07.029); [Costa et al., 2021](https://doi.org/10.1016/j.jcp.2021.110604); [Costa et al., 2022](https://doi.org/10.1002/nme.6892)], a novel technique is proposed based on a **Dirichlet-Neumann** and **Neumann-Neumann decomposition** on the interface to transform the conjugate problem into separated partitioned subproblems. Each subproblem can then be discretised as a **conventional boundary-valued convection-diffusion problem**, and the thermal coupling between subdomains is recovered through specific constrained polynomial reconstructions on the interface. The method was developed in the FVM paradigm for the 2D and 3D CHT problem with general interface conditions and was equipped with the **ROD method** to handle **arbitrary curved interfaces**, effectively achieving the sixth-order of convergence on unstructured meshes.

---
