---
layout: page
title: Research
permalink: /research/
description: Research activities in robotic additive manufacturing, artificial intelligence, process monitoring and digital twins.
nav: true
nav_order: 2
---

<style>
.research-intro {
  max-width: 950px;
  margin-bottom: 3rem;
}

.research-axis {
  margin: 3.5rem 0 4.5rem 0;
  padding-bottom: 3rem;
  border-bottom: 1px solid #d9e2ec;
}

.axis-number {
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  color: #00a1b2;
  text-transform: uppercase;
  margin-bottom: 0.4rem;
}

.research-axis h2 {
  color: #003b71;
  font-weight: 600;
  margin-bottom: 1.2rem;
}

.research-image {
  width: 100%;
  max-width: 900px;
  display: block;
  margin: 1.8rem auto;
  border-radius: 6px;
}

.research-image-small {
  width: 48%;
  display: inline-block;
  vertical-align: top;
  margin: 1%;
  border-radius: 6px;
}

.research-equation {
  background: #f7f9fb;
  border-left: 4px solid #00a1b2;
  padding: 1.2rem 1.5rem;
  margin: 1.8rem 0;
}

.variable-list {
  font-size: 0.94rem;
  line-height: 1.7;
}

.research-chain {
  text-align: center;
  font-weight: 600;
  color: #003b71;
  margin: 1.8rem 0;
  padding: 1rem;
  background: #f7f9fb;
}

.project-tag {
  display: inline-block;
  border: 1px solid #00a1b2;
  border-radius: 20px;
  padding: 0.25rem 0.8rem;
  margin: 0.2rem;
  font-size: 0.85rem;
  color: #003b71;
}

.phd-card {
  padding: 1.1rem 1.3rem;
  margin: 1rem 0;
  border-left: 3px solid #00a1b2;
  background: #f8fafc;
}

@media (max-width: 700px) {
  .research-image-small {
    width: 100%;
    margin: 0.5rem 0;
  }
}
</style>

<div class="research-intro">

My research focuses on the development of **intelligent, adaptive and data-driven manufacturing systems**, with a particular emphasis on robotic additive manufacturing.

My work combines **robotics, process modelling, multi-physics sensing, computer vision, artificial intelligence and digital twins**, from material deposition to large-scale manufacturing and construction.

The research is structured around four complementary scientific axes.

</div>

---

<div class="research-axis">

<div class="axis-number">Research Axis 01</div>

## Robotic & Large-Scale Additive Manufacturing

<img src="/assets/img/research_robotic_am.jpg"
     class="research-image"
     alt="Robotic large-scale additive manufacturing">

My research investigates **robot-based material deposition** and the development of manufacturing strategies for large-scale additive manufacturing.

The work covers paste-based materials, construction materials, polymers, composites and metallic additive manufacturing, with a particular interest in the coupling between **robot kinematics, deposition parameters, material behaviour and final geometry**.

The robotic trajectory can be represented by the Tool Centre Point state:

<div class="research-equation">

$$
\mathbf{p}(t)
=
[x(t),y(t),z(t),\phi(t),\theta(t),\psi(t)]^T
$$

<div class="variable-list">

**Variables and metrics**

- $x,y,z$ — Cartesian TCP position [mm]
- $\phi,\theta,\psi$ — TCP orientation [rad or °]
- $t$ — process time [s]

</div>
</div>

For extrusion-based additive manufacturing, the relationship between material flow and robot velocity provides a first-order estimate of the deposited cross-section:

<div class="research-equation">

$$
A_d(t) \simeq \frac{Q(t)}{v(t)}
$$

<div class="variable-list">

**Variables and metrics**

- $A_d$ — deposited cross-sectional area [mm²]
- $Q$ — volumetric material flow rate [mm³·s⁻¹]
- $v$ — printing velocity [mm·s⁻¹]

</div>
</div>

The scientific challenge is to understand how these process variables interact with material rheology and robotic motion to control **dimensional accuracy, deposition stability and manufacturing repeatability**.

<div class="research-chain">
Robot trajectory → Material deposition → Process/material interaction → Geometry → Performance
</div>

</div>

<div class="research-axis">

<div class="axis-number">Research Axis 02</div>

## In-situ Monitoring, Computer Vision & Artificial Intelligence

<img src="/assets/img/research_smartamp.jpg"
     class="research-image"
     alt="SmartAMP AI-driven monitoring">

<span class="project-tag">ANR JCJC SmartAMP</span>
<span class="project-tag">Computer Vision</span>
<span class="project-tag">Multi-Physics Monitoring</span>
<span class="project-tag">Artificial Intelligence</span>

A central part of my research concerns the development of **in-situ monitoring strategies for additive manufacturing**.

The ANR JCJC **SmartAMP** project investigates the combination of multi-physics sensing, computer vision and artificial intelligence to characterize the manufacturing state during paste-based additive manufacturing.

A multi-modal observation vector can be written as:

<div class="research-equation">

$$
\mathbf{x}(t)
=
[T(t),F(t),Q(t),v(t),\mathbf{I}(t)]^T
$$

<div class="variable-list">

**Variables and metrics**

- $T$ — process/material temperature [°C]
- $F$ — interaction or extrusion force [N]
- $Q$ — material flow rate [kg·s⁻¹ or mm³·s⁻¹]
- $v$ — printing velocity [mm·s⁻¹]
- $\mathbf{I}$ — image data or extracted vision descriptors [px, intensity or dimensionless features]
- $t$ — acquisition time [s]

</div>
</div>

The objective is to estimate the process state from heterogeneous and temporally evolving observations:

<div class="research-equation">

$$
\hat{\mathbf{s}}(t)
=
f_{\boldsymbol{\theta}}
\left(
\mathbf{x}_{t-k:t}
\right)
$$

<div class="variable-list">

**Variables and metrics**

- $\hat{\mathbf{s}}(t)$ — estimated manufacturing/process state
- $f_{\boldsymbol{\theta}}$ — data-driven or AI model
- $\boldsymbol{\theta}$ — trainable model parameters
- $\mathbf{x}_{t-k:t}$ — sequence of multi-modal observations
- $k$ — temporal observation window [samples or s]
- $t$ — current acquisition time [s]

</div>
</div>

Computer vision is investigated for **interlayer detection, texture characterization, geometrical distortion measurement and defect identification**, while AI models are used for classification, state estimation and decision support.

<div class="research-chain">
Sensing → Data → Features → State estimation → Decision → Feedback
</div>

</div>

<div class="research-axis">

<div class="axis-number">Research Axis 03</div>

## Process Modelling & Digital Twins

<img src="/assets/img/research_digital_twin.png"
     class="research-image"
     alt="Digital twins and robotic additive manufacturing">

My research on digital twins aims at establishing a continuous link between the **physical manufacturing process, experimental observations and numerical models**.

Current applications include:

- **metallic repair and WAAM** — ANR SAMSARA,
- **polymer and composite additive manufacturing**,
- **paste-based materials for construction**,
- process monitoring and model updating.

Model calibration can be formulated as an inverse problem:

<div class="research-equation">

$$
\boldsymbol{\theta}^{*}
=
\underset{\boldsymbol{\theta}}{\operatorname{argmin}}
\left\|
\mathbf{y}_{\mathrm{exp}}
-
\mathbf{y}_{\mathrm{model}}(\boldsymbol{\theta})
\right\|_2^2
$$

<div class="variable-list">

**Variables and metrics**

- $\boldsymbol{\theta}$ — vector of model parameters
- $\boldsymbol{\theta}^{*}$ — identified/calibrated parameter vector
- $\mathbf{y}_{\mathrm{exp}}$ — experimental observations
- $\mathbf{y}_{\mathrm{model}}$ — numerical-model predictions
- $\|\cdot\|_2^2$ — squared Euclidean discrepancy

Depending on the process, $\mathbf{y}$ can contain temperature [°C], geometrical dimensions [mm], displacement [mm], force [N] or other experimentally measured quantities.

</div>
</div>

The objective is to progressively update numerical representations using manufacturing data in order to improve **prediction, process understanding and ultimately adaptive control**.

<div class="research-chain">
Physical process → Sensors → Experimental data → Model calibration → Digital twin → Prediction & control
</div>

</div>

<div class="research-axis">

<div class="axis-number">Research Axis 04</div>

## Sustainable & Robotic Construction

<img src="/assets/img/research_ecobrick.jpg"
     class="research-image-small"
     alt="Ecobrick robotic construction">

<img src="/assets/img/research_earth_dome.jpg"
     class="research-image-small"
     alt="Additive manufacturing of earth-based construction">

My research also investigates how robotic manufacturing can contribute to more **resource-efficient and locally adapted construction processes**.

### Ecobrick 4.0

**Ecobrick 4.0** investigates the robotisation and improvement of raw-earth brick placement using both **Cable-Driven Parallel Robots (CDPR)** and serial robotic systems, including sensor-based feedback and control strategies.

### ITA — Inclusivité en Terre Additive

The **ITA** project focuses on additive manufacturing using **locally sourced earth materials**, connecting material characterization, extrusion behaviour, robotic deposition and construction-scale applications.

### SmartAMP

The **ANR JCJC SmartAMP** project complements this work through intelligent monitoring of paste-based additive manufacturing processes.

A multi-criteria representation of manufacturing performance can be written as:

<div class="research-equation">

$$
\mathbf{P}
=
[G,M,E,R]^T
$$

<div class="variable-list">

**Performance indicators**

- $G$ — geometrical performance [mm or % depending on indicator]
- $M$ — mechanical performance [MPa]
- $E$ — environmental impact [kg CO₂-eq]
- $R$ — material/resource consumption [kg or kg·m⁻²]

$\mathbf{P}$ represents a **multi-criteria performance vector** rather than a universal scalar performance indicator.

</div>
</div>

<div class="research-chain">
Local material → Characterization → Robotic fabrication → Monitoring → Structure → Performance
</div>

</div>

---

# PhD Supervision

My research activities are closely connected to doctoral training at the interface between **robotics, additive manufacturing, materials, monitoring and digital modelling**.

## Current PhD candidates

<div class="phd-card">

### Yunfan Li

**Research topic:** Computer vision and intelligent monitoring for additive manufacturing.

**Laboratory:** LS2N — Nantes Université

**Supervision:** Mathieu Ritou · Sébastien Levilly · Elodie Paquet

</div>

<div class="phd-card">

### Lucile Sauvestre

**Research topic:** Development of robotized construction principles based on earth materials.

**Projects:** ANR JCJC SmartAMP · AMI Bâtisseur 2030

**Laboratories:** IRDL · LS2N

**Supervision:** Sébastien Garnier · Arnaud Perrot · Elodie Paquet

</div>

<div class="phd-card">

### Brendan Chalvet

**Research topic:** Robotic additive manufacturing, composite tooling and digital twins.

**Funding:** CIFRE — 5heol

**Laboratories:** GeM · LS2N

**Supervision:** Pascal Casari · Sébastien Le Loch · Elodie Paquet

</div>

<div class="phd-card">

### Shaoxuan Liang

**Research topic:** Digital twins and modelling for additive manufacturing.

**Laboratories:** LS2N · GeM

**Supervision:** Mathieu Ritou · Matthieu Rauch · Elodie Paquet

</div>

## Completed PhDs

<div class="phd-card">

### Ali El Hage

**CIFRE PhD — SEGULA Technologies**

Research on digital manufacturing chains and robotic additive manufacturing for construction.

**Laboratories:** GeM · LS2N

**Supervision:** Nordine Leklou · Philippe Poullain · Elodie Paquet

</div>

<div class="phd-card">

### Sarra Oueslati

**IRT PERFORM PhD**

Research on monitoring and characterization of Wire Arc Additive Manufacturing (WAAM).

**Supervision:** Mathieu Ritou · Farouk Belkadi · Elodie Paquet

</div>

---

# Open Science & Research Data

Open and reproducible research is an important component of these activities.

Research datasets, experimental data and associated scientific resources are progressively made available through **Zenodo**, in connection with publications and research projects.

→ **Research data on Zenodo**
