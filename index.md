---
title: Fused Multi-Modal Electron Microscopy
subject: Tutorial
subtitle: A beginner's guide
---

+++ {"part": "abstract"} 
Chemical mapping of nano-scale and atomic chemistry via spectroscopic electron microscopy has challenged researchers for decades due to the fundamental tradeoff between electron dose, noise, and resolution. 
Inelastic spectroscopic signals (electron energy loss (EELS) or energy-dispersive x-ray (X-EDS) spectroscopy) that yield elemental signatures are rare, resulting in long dwell times to produce discernable structure. 
This process often destroys the sample and distorts the chemical map during acquisition.  
Lower dose scans can be taken to combat this issue, but they often do not have enough signal to produce meaningful results. 

Fused multi-modal electron microscopy offers nano- and atomic-resolution high signal-to-noise-ratio (SNR) recovery of material chemistry by merging low-dose elastically scattered high-angle annular dark-field (HAADF) signals with the inelastic signals. 
The process works best when all chemistries in the material are mapped spectroscopically and combined with a directly interpretable elastic signal. 
This article bridges the gap between theory and practice by walking through each step of the fused multi-modal computational pipeline and pointing out best practices when running the code. 
By the end of this tutorial, anyone with inelastic and elastic 2D projection data should be able to reproducibly  reconstruct chemical maps using fused multi-modal electron microscopy.

+++

:::{figure} ./figs/Figure_abstract.png
:name: fig_abstract
:width: 700px
Fused Multi-Modal atomic resolution image improvement on  DyScO$_3$ 
:::

+++{"part":"epigraph"}
:::{warning} Pre-print
This article has not yet been peer-reviewed.  
_Updated 2024 September 24_
:::

+++

+++ {"part": "acknowledgements"} 
We acknowledge support from Dow Chemical Company. 

Work at the Molecular Foundry was supported by the Office of Basic Energy Sciences, of the U.S. Department of Energy under Contract no. DE-AC02-05CH11231.

This research used resources of the Argonne Leadership Computing Facility, a U.S. Department of Energy (DOE) Office of Science user facility at Argonne National Laboratory and is based on research supported by the U.S. DOE Office of Science-Advanced Scientific Computing Research Program, under Contract No. DE-AC02-06CH11357.

This research used resources of the Oak Ridge Leadership Computing Facility at the Oak Ridge National Laboratory, which is supported by the Office of Science of the U.S. Department of Energy under Contract No. DE-AC05-00OR22725.

Atomic resolution HAADF/X-EDS data for DyScO3 was obtained with facilities at the Core Center for Excellence in Nano Imaging at the University of Southern California, with support from USC Viterbi Start-up funds and the USC Research and Innovation Instrumentation Award.
+++

+++ {"part": "competing interests"} 
## Competing Interests

The authors declare that they have no known competing interests.
+++
