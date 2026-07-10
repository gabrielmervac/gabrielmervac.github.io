---
layout: page
title: Self-driving microfluidic lab for cell dynamics
description: An autonomous closed-loop platform that runs its own live-cell experiments
importance: 3
category: current
img: assets/img/autonomous_chip/closed_loop.png
related_publications: false
---

I am leading the platform engineering for an **autonomous, closed-loop system** that runs its own live-cell experiments with no human in the inner loop. The platform continuously cycles through four stages — **acquire → analyze → decide → act → repeat** — imaging living cells, quantifying their state, deciding what to deliver next, and acting on the chip, continuously, for days.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autonomous_chip/closed_loop.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The closed loop: fluorescence and phase-contrast imaging feed cell segmentation and intensity analysis, a local decision agent selects the next intervention, and a microfluidic chip delivers signals, drugs, and media on demand.
</div>

**Why this matters.** Biology is still largely run one experiment at a time, by hand. The space of possible stimuli, doses, and sequences is far too large to explore serially or without feedback. By closing the loop, the stimulation trajectory that drives a cell from one state to another stops being just an output — it becomes a new kind of scientific data, and the controller itself becomes an instrument.

The platform couples **massively parallel microfluidics** (dozens to hundreds of independent chambers) with **live-cell fluorescence microscopy**. Images are segmented with **CellPose** and analyzed with a computer-vision pipeline; a decision layer built on **ODE models of the underlying biology** and a local reasoning agent chooses each next intervention, progressing from classical **PID control** to **model-predictive control** and adaptive, learning controllers. All inference runs **locally, on-prem** — no data leaves the lab.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autonomous_chip/platform_architecture.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    System architecture: a hardware station (microscope + microfluidics) and an analysis machine (segmentation + decision agent) connected by a REST layer, designed to scale horizontally to hundreds of chambers.
</div>

**The biology.** We are using this platform to tackle a ladder of control problems of increasing complexity:

- **NF-κB signaling dynamics** — steering the transcription-factor activity of single cells between oscillatory and sustained regimes.
- **Downstream gene and protein expression** — using those dynamics as a handle to dial target genes up or down.
- **Tumor-microenvironment population dynamics** — steering the composition of a living co-culture of cancer, stromal, and immune cells.
- **Stem-cell differentiation** — driving cells along defined lineage trajectories via **Wnt/β-catenin** dynamics.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autonomous_chip/coculture_micrograph.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autonomous_chip/dual_reporter_imaging.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Left: multiplexed co-culture of cancer cells, fibroblasts, and macrophages. Right: a dual-reporter iPSC line reading out live β-catenin localization and Wnt transcriptional output simultaneously.
</div>

My role spans the full engineering stack — the microfluidic control, the imaging and analysis pipeline, the decision/control layer, and the NF-κB biology that anchors the first closed-loop demonstrations.
