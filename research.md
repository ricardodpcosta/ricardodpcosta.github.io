---
layout: page
title: Research
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  Short description on the major research topics of interest that I have investigated. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

<style>

      boxes-image:after {
        content: "";
        position: absolute;
        z-index: 1;
        bottom: 0;
        left: 0;
        pointer-events: none;
        background-image: linear-gradient(to bottom, rgba(255,255,255,0), rgba(255,255,255, 1) 90%);
        width: 100%;
        height: 4em;
      }

</style>

<div class="boxes-section">
  <div class="boxes-container">
    <div class="boxes-box">
      <a class="boxes-link" href="{{ 'research/incompressible_flows.html' | relative_url }}">
        <div class="boxes-image">
          <img src="{{ 'public/pressure.png' | relative_url }}" alt="">
        </div>
        <div class="boxes-title">
          <h3>Incompressible fluid flow problems</h3>
        </div>
      </a>
    </div>
    <div class="boxes-box">
      <a class="boxes-link" href="{{ 'research/slip_conditions.html' | relative_url }}">
        <div class="boxes-image">
          <img src="{{ 'public/streamlines.png' | relative_url }}" alt="">
        </div>
        <div class="boxes-title">
          <h3>General slip boundary conditions</h3>
        </div>
      </a>
    </div>
    <div class="boxes-box">
      <a class="boxes-link" href="{{ 'research/curved_boundaries.html' | relative_url }}">
        <div class="boxes-image">
          <img src="{{ 'public/unstructured_mesh.png' | relative_url }}" alt="">
        </div>
        <div class="boxes-title">
          <h3>Arbitrary curved boundaries</h3>
        </div>
      </a>
    </div>
    <div class="boxes-box">
      <a class="boxes-link" href="{{ 'research/heat_transfer.html' | relative_url }}">
        <div class="boxes-image">
          <img src="{{ 'public/continuity_interface_condition.png' | relative_url }}" alt="">
        </div>
        <div class="boxes-title">
          <h3>Conjugate heat transfer problems</h3>
        </div>
      </a>
    </div>
    <div class="boxes-box">
      <a class="boxes-link" href="{{ 'research/vorticity_formulations.html' | relative_url }}">
        <div class="boxes-image">
          <img src="{{ 'public/omega.png' | relative_url }}" alt="">
        </div>
        <div class="boxes-title">
          <h3>Navier-Stokes equations in vorticity formulations</h3>
        </div>
      </a>
    </div>
</div>
