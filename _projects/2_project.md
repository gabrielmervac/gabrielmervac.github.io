---
layout: page
title: Immune memory and response prediction
description: Predicting future cellular responses from transcription-factor dynamics
importance: 2
category: current
img: assets/img/immune/response_prediction.png
related_publications: true
---

Do the dynamics of a transcription factor carry enough information to **predict a cell's future response**? Innate immune memory — the tolerance or priming a cell shows on a second encounter — is usually measured in bulk. By tracking individual macrophages across **two sequential stimulations** with a live NF-κB reporter, we asked whether memory is stochastic noise or a deterministic property written into each cell's initial state.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/immune/response_prediction.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    From an immune cell's first response, an LSTM neural network learns to predict its future NF-κB dynamics — reading memory directly off the single-cell time course.
</div>

**Memory is predictable from the first response.** We trained **LSTM recurrent neural networks** to predict a cell's second-stimulus response group directly from its first-stimulus NF-κB trace. Tolerance is genuinely predictable — the strength of a cell's initial response forecasts how strongly it will be tolerized — and the *time-dependent* dynamics carry information that static summaries and simpler classifiers miss. Mutual-information analysis shows memory is encoded continuously across the entire response, not in a single feature.

**Deterministic memory from initial cell state.** Modeling shows that much of this apparent randomness is deterministic: simulating a population that differs only in **gamma-distributed receptor abundance** reproduces both the heterogeneous first responses and the downstream memory. So-called "naïve" macrophages are functionally heterogeneous, and their memory can, in principle, be read from their starting protein levels.

**IFN-β as a paracrine memory amplifier.** Distinct molecular circuits underlie the two memory types: a **cell-intrinsic negative feedback loop** produces tolerance, while **secreted IFN-β positive feedback** produces priming — blocking IFN-β abolishes it. IFN-β acts as a local *quorum amplifier*: together with paracrine TNF-α it sustains signaling and buffers cell-to-cell variability, boosting responses in low-receptor cells while barely affecting high-receptor ones. This couples a cell-intrinsic memory to a cell-extrinsic, population-level circuit that can be read out and predicted from single-cell traces.

**Key publications:** {% cite wang2025encoding %}
