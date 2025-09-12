---
layout: page
title: Research
---

---

### _Fused filament fabrication_

<p style="margin-bottom:1cm;"></p>


Fused Filament Fabrication (FFF) is a subset of material extrusion additive manufacturing which involves the deposition of thermoplastic materials in a layer-by-layer fashion. The process operates by forcing a solid filament through a heated nozzle, where it melts and is extruded. It is the pressure exerted by the continuous feeding of the unmelted filament that forces the molten polymer through the nozzle, enabling its deposition onto the build platform or previously deposited layers. FFF is extensively utilized, particularly among hobbyists and small-scale manufacturers, owing to its cost-effectiveness, ease of use, and capability to fabricate geometrically complex components. However, the process often fails to meet the strict mechanical, dimensional, and surface quality requirements demanded by industrial applications. These limitations have prompted significant research efforts focused on process optimization to bridge the gap between FFF and conventional manufacturing techniques. Despite experimental approaches remaining as the standard, they are typically resource-intensive, time-consuming, and may not yield globally optimal process parameters. As a result, there is growing interest in computational modeling to gain deeper insight into the underlying physical phenomena and to address performance limitations of the FFF process.
The numerical simulation of the FFF process presents significant challenges due to its inherently multi-physical and multi-scale nature. The process encompasses several stages from the solid filament feeding to its extrusion and subsequent cooling and solidification. Each phase involves complex physical phenomena, including heat transfer, phase change, non-Newtonian polymer behavior, interfacial adhesion and interactions with the surrounding media and moving extruder, all of which occur over disparate spatial and temporal scales. Consequently, simulations often decompose the full process into separate stages, each modeled using specialized numerical tools. The first phase involves thermal analysis of the solid filament's transition to a molten state within the extruder. Simulations at this stage primarily focus on solving the temperature distribution and identifying the location and dynamics of the melting interface. The second phase includes the molten polymer extrusion through the nozzle and its deposition and interaction with the surrounding media. This stage is particularly complex and remains the least understood, as it involves dynamic free-surface flows, inter-layer bonding mechanisms and interactions with ambient conditions. Simulations of this phase are critical for predicting the filament’s morphology, dimensional accuracy and interfacial adhesion. The final phase is focused on the post-deposition behavior of the material, emphasizing thermal evolution and eventual solidification coupled with the cooling-induced consequent residual stress development, which are responsible for significant defects, such as warping, delamination and dimensional inaccuracies. Given the less understood complexity of the second phase, recent research of the FFF process has focused on its characterization. These approaches are often under isothermal conditions to isolate deposition behavior and investigate the shape of individual or very limited numbers of filaments as functions of deposition and extrusion parameters. Additionally, to simplify the kinematics of the moving extruder, many models adopt an inverted reference frame [1,2], where the substrate moves relative to the stationary nozzle. While this may facilitate computational implementation, it requires doubling the computational domain and interrupting the simulation to accommodate multi-layer deposition. Despite their utility, such simplifications prove to be impractical and prone to limited conclusions, highlighting the need for more advanced integrations.
The present study aims to establish a comprehensive computational framework for simulating the FFF process using a scalable and practical approach to surpass the current limitations. The developed method should be capable of simulating the deposition of several filaments in multiple successive layers while determining their temperature profiles and considering interactions with each other and the machine components. Based on the temperature data and filament adhesion, the tool should determine mechanical properties based on residual thermal stresses and contractions estimations. This presentation covers the current state of development as an initial step toward the overarching objective. The framework is built upon the open-source computational library OpenFOAM, from which a selection of solvers was evaluated, and the overInterDyMFoam solver was ultimately chosen due to its suitability. It extends the capabilities of the widely adopted interFoam solver, sharing its incompressible and isothermal formulation for two-phase flow of immiscible fluids, by incorporating the oversetMesh feature, which enables dynamic mesh handling with overlapping regions, making it well-suited for simulating moving elements. The proposed approach employs the oversetMesh functionality to implement a dynamic patch that acts as a localized mass source, replicating the deposition of molten material. This patch is surrounded by moving boundaries, representing the terminal section of the extruder nozzle, whose geometry is being modeled to improve the accuracy of the velocity profile and capture its interactions with the extrudate. Currently, the most prominent process parameters, such as extruder velocity, extrusion rate, layer height and gap, are adjustable and able to reflect state-of-the-art conditions and their influence on the deposited filament’s shape, modeled considering typical polymeric behavior, can be observed. Despite the lack of sufficient experimental validation at the present stage, the simulations yield expected results in a physical consistent behavior, with accurate conservation of mass and realistic velocity fields. These developments underscore the potential of the proposed approach and motivate further developments. The next stages will involve implementing a thermal transport model and extending the formulation to accommodate multiphase flows, both of which are essential for a high-fidelity FFF simulation.

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

This investigation forms part of the doctoral thesis project of \[[J. Castro, 2025](https://ricardodpcosta.github.io/activities.html#supervised-theses)] (Doctoral Program in Science and Engineering of Polymers and Composites, University of Minho, Portugal).
