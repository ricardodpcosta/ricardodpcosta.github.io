---
layout: page
title: FVLib code
---

## <span style="color:lightgrey">The Great </span>F<span style="color:lightgrey">inite</span> V<span style="color:lightgrey">olume</span> Lib<span style="color:lightgrey">rary</span>

<p style="margin-bottom:1cm;"></p>

The FVLib code is a library of advanced computational algorithms and numerical methods to solve partial differential equations (PDEs) within the **finite volume philosophy**. The project aims to deliver **high-accurate**, **high-performance**, and **high-efficient** simulations of a wide range of physics and mechanics problems in relevant industrial, environmental, and biomedical applications.

The FVLib code is the result of years of dedication and passion for applied mathematics and scientific computing, and the ambition of **pushing the limits of numerical simulation even further** in serving the scientific knowledge and technological innovation.

---

### **Modern object-oriented Fortran (2003/2008 standards)**

<p style="margin-bottom:1cm;"></p>

The FVLib code is programmed in modern Fortran (2003/2008 standards) with an object-oriented paradigm for better <span style="color:blue">_code reuse, maintenance, and readability_</span>. Its architecture is organised in three levels:

- **Core level**: including linear algebra algorithms, input/output interfaces, mesh and field handlers, sparse matrix structures, etc.

- **Applications level**: including specific model solvers, specific boundary and interface conditions, and pre-processing and post-processing tools.

- **Cases level**: including geometry files, mesh generation scripts, models and schemes parameters files, and running and post-processing scripts.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:100%; display:block; margin-left:auto; margin-right:auto;" src="public/apps.png">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:100%; display:block; margin-left:auto; margin-right:auto;" src="public/case.png">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Applications level.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Cases setup.
  </div>
</div>

---

### **Highly accurate schemes in space and time**

<p style="margin-bottom:1cm;"></p>

The discretisation methods implemented in the FVLib code are highly accurate in space and time, effectively achieving up to the eighth-order of convergence. Comprehensive benchmarking proves that high-order accurate schemes benefit from a <span style="color:blue">_better trade-off between accuracy and efficiency_</span> than the counterpart lower-order accurate ones. This property can be exploited in different ways:

- **Improved accuracy**: for the same discrete geometrical representation level (number of degrees of freedom), high-order accurate schemes provide <span style="color:blue">_significantly more accurate solutions_</span> than those obtained with the traditional first- and second-order accurate schemes.

- **Enhanced performance**: for the same approximate solution accuracy level, high-order accurate schemes provide <span style="color:blue">_significantly more efficient computations_</span> (execution time) than those of the traditional first- and second-order accurate schemes.

- **Resource-use efficiency**: for the same approximate solution accuracy level, high-order accurate schemes consume <span style="color:blue">_significantly less resources_</span> (power and memory) than those of the traditional first- and second-order accurate schemes.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:80%; display:block; margin-left:auto; margin-right:auto;" src="public/error_vs_dof.png">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:80%; display:block; margin-left:auto; margin-right:auto;" src="public/error_vs_time.png">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Error <em>versus</em> number of unknowns.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Error <em>versus</em> execution time.
  </div>
</div>

---

### **Unstructured meshes for complex geometries**

<p style="margin-bottom:1cm;"></p>

Complex geometries arise in many real-world problems of physics and engineering applications, for which domain fitted unstructured meshes are still the preferred approach for its <span style="color:blue">_flexibility and robustness_</span>, especially in 3D.

- **General element shapes**: the high-order accurate discretisation methods implemented in the FVLib code can handle <span style="color:blue">_2D and 3D unstructured meshes with general element shapes_</span> for the most demanding problems in intricate geometries.

- **Linear piecewise meshes**: the high-order accurate discretisation methods implemented in the FVLib code preserve the optimal <span style="color:blue">_high-orders of convergence with the standard linear piecewise elements_</span>, on arbitrary curved geometries, overcoming the cumbersomeness of generating and dealing with curved meshes as the traditional approaches.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="public/geometry.png">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="public/unstructured_mesh.png">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Intricate curved geometry.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Unstructured linear piecewise mesh.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

- **Gmsh compatible interface**: the FVLib code provides a compatibility interface with [Gmsh](https://gmsh.info/), an open source <span style="color:blue">_3D mesh generator with built-in pre- and post-processing facilities_</span>, designed to provide a fast, light and user-friendly meshing tool with parametric input and flexible visualisation capabilities.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:100%; display:block; margin-left:auto; margin-right:auto;" src="public/gmsh1.png">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:100%; display:block; margin-left:auto; margin-right:auto;" src="public/gmsh2.png">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Gmsh snapshot with geometry.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Gmsh snapshot with mesh.
  </div>
</div>

---

### **Parallel computing for HPC environments**

<p style="margin-bottom:1cm;"></p>

The FVLib code multi-processing capabilities are implemented based on the <span style="color:blue">_shared-memory and message-passing parallel programming models_</span> through the OpenMP and OpenMPI application programming interfaces. It allows the development and deployment of portable and scalable large-scale parallel applications that take advantage of modern HPC systems.

---

### Contributing

<p style="margin-bottom:1cm;"></p>

The FVLib code is not currently an open-source project. However, anyone willing to contribute to the project and/or making use of its capabilities on a collaboration basis is welcome. If you are interested in using it or need further details, you can always [contact me](mailto:rcosta@dep.uminho.pt).
