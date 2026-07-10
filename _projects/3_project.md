---
layout: page
title: Cell-to-cell communication
description: Information propagation across immune cell populations
importance: 4
category: current
img: assets/img/immune/cell_communication_flow.png
related_publications: true
---

How does information encoded in primary responders propagate to their neighbors? We showed that secreted **IFN-β acts as a local paracrine amplifier**, priming nearby cells and shaping population-level immune memory. This project builds on that finding to ask a more general question: as an immune signal spreads through a population, is its information content **preserved, amplified, or degraded**?

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/immune/cell_communication.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    A primary responder secretes cytokines that propagate through the population; we track how the information carried by the original signal is transformed as it passes from cell to cell.
</div>

We combine **single-cell transcriptomics**, **live-cell imaging** of NF-κB dynamics, and **cytokine transport modeling** (diffusion, uptake, and degradation) to follow a signal from the primary responder through successive neighbors. The goal is to quantify the **fidelity and transformation of information** across a multicellular network — whether a message survives the trip, gets sharpened by positive feedback, or is washed out by noise.

This bridges single-cell information theory with multicellular communication networks, and connects naturally to questions in **statistical physics** about signal propagation in noisy, heterogeneous systems.

**Key publications:** {% cite wang2025encoding %}
