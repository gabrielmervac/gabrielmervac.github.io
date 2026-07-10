---
layout: page
title: Information encoding in immune cells
description: How single macrophages detect and classify inflammatory signals
importance: 2
category: current
img: assets/img/immune/info_encoding.png
related_publications: true
---

How do macrophages detect and classify inflammatory signals, and what are the physical limits of that sensing? Using **primary macrophages expressing a fluorescent NF-κB reporter** (RelA/p65), automated microfluidics for precisely timed stimulation, and live-cell imaging, we tracked the single-cell signaling response to pathogen- and cytokine-derived cues delivered as pulses lasting anywhere from **one second to a thousand seconds**.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/immune/info_encoding.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Macrophages encode signal identity through distinct dynamic features: pathogen signals are read out by amplitude/dose, cytokine signals by duration — and single cells reliably detect stimuli lasting as little as one second.
</div>

**Cells detect signals lasting as little as one second.** Even a one-second pulse of a pathogen or cytokine ligand is enough to fully activate NF-κB in a single macrophage — remarkable given that the downstream transcription and translation it drives unfold over minutes to hours. Applying **information theory** to the measured single-cell dynamics, we find that cells discriminate between stimuli with near-optimal fidelity: the information carried by these ultra-short signals approaches that of stimulation lasting hours.

**Two modes of encoding.** The response separates signals along two axes: **amplitude/dose-based encoding for pathogens** and **duration-based encoding for cytokines**. This lets a cell respond to the *dose* of a pathogen encountered even briefly, while filtering out transient cytokine fluctuations unless they persist — a signal-processing strategy tuned to the statistics of real infections.

**Structured single-cell heterogeneity.** Rather than responding uniformly, cells fall into early responders, late responders, and non-responders, in ligand-dependent proportions. A mathematical model combining ligand–receptor kinetics with a minimal NF-κB feedback core reproduces this heterogeneity, showing it arises from cell-to-cell variability in receptor abundance and signaling kinetics — and predicts general regimes of activation for any receptor pathway that converges on NF-κB.

This work combines custom microfluidic platforms for precise stimulus delivery with live-cell fluorescence microscopy and information-theoretic analysis, revealing highly optimized signal-processing machinery at the single-cell level.

**Key publications:** {% cite mercado2025ultrashort %}
