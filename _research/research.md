---
title: "Research"
collection: research
permalink: /research/research
redirect_from: 
  - /research/
---

<style>
/* ===== Global Styles ===== */
.title-blue {
  color: #4169E1;
}

.justify {
  text-align: justify;
}
</style>

<hr style="
  border: none;
  border-top: 3px double #4169E1;
  height: 0;
  width: 100%;
  margin: 20px auto;
">

<span class="title-blue"> Topic 1: Early-Stage Power Modeling for Digital Circuits and Systems</span>
======
<p class="justify"> 
As the architecture complexity, integration density and chip size of modern integrated circuits (IC) continue to grow, the importance of power efficiency increases and ICs' power consumption is turning out to be one of the pivotal design objectives. In this project, we seek opportunities to model power consumption of digital circuits and systems. Specifically, we investigate the power modeling techniques from design time to run time. These techniques are compatible with each other, and putting it all together, they can jointly facilitate the advancements of power savings in both design-time hardware construction and real-time application execution. 
</p>

---------------------------------------------------------
<p class="justify"> 
<strong>1. HLS-Based Power Modeling of Digital Circuits</strong>. We propose PowerGear, a graph-learning-assisted power estimation approach for high-level synthesis (HLS), which features high accuracy, efficiency, scalability, transferability, and applicability. PowerGear comprises two main components: a graph construction flow and a customized graph neural network (GNN) model. In the graph construction flow, PowerGear introduces buffer insertion, datapath merging, graph trimming and feature annotation techniques to transform HLS designs into graph-structured data, which encode both intra-operation micro-architectures and inter-operation interconnects annotated with switching activities. Additionally, PowerGear incorporates cross-function graph integration, dataflow adaptation, and design scaling strategies that make it compatible with multi-kernel, computation-intensive and large-scale applications. Furthermore, we propose a novel power-aware heterogeneous edge-centric GNN model, which effectively learns heterogeneous edge semantics and structural properties of the constructed graphs via edge-centric neighborhood aggregation, and eventually fits the formulation of dynamic power. Compared with on-board measurement, PowerGear shows average errors of 3.60% and 8.81% in total and dynamic power estimation, respectively, while the evaluation efficiency is improved by 41.9x. Moreover, PowerGear supports large-scale and dataflow-optimized neural networks with an error of only 3.91%, demonstrating broad applicability. Finally, PowerGear facilitates design space exploration for FPGA HLS, leading to a performance gain of up to 11.2%, compared with methods using state-of-the-art predictive models.
</p> 

<div style="display: flex; justify-content: center; align-items: center; gap: 20px; max-width: 100%;"> 
  <img src="http://zlinaf.github.io/images/powergear-overall.png" style="max-width: 60%;"> 
  <img src="http://zlinaf.github.io/images/powergear-graphconstruction.png" style="max-width: 40%;"> 
</div>

---------------------------------------------------------
<p class="justify"> 
<strong>2. Pre-HLS Architectural Power Modeling</strong>. Power estimation for customized accelerators, especially those derived from high-level programming languages, entails the invocation of a long electronic design automation (EDA) tool chain, thus incurring large timing overhead that hinders early design optimization. To mitigate this problem, we propose HIPPO, an architecture-level power modeling framework for field-programmable gate arrays (FPGAs). HIPPO operates directly on C/C++ programs, whose execution is prior to and independent of any EDA tool including the very front-end, high-level synthesis (HLS). During power modeling, HIPPO exploits the intrinsic C/C++ code hierarchies, including nested loops and operations, and enables multi-level power estimation that aligns with different code hierarchies. Specifically, HIPPO can be decomposed into (1) a code transformation flow that directly converts a C/C++ program with HLS pragmas into hardware-oriented and power-aware control and dataflow graph, (2) a hierarchy-preserving power modeling methodology that combines analytical modeling and data-driven learning approaches to effectively orchestrate different code hierarchies, and (3) an adaptive dataflow coarsening strategy which ensures modeling accuracy, efficiency and robustness by suppressing noise of onboard measurement. Experimental results demonstrate that HIPPO effectively decomposes and accurately predicts both dynamic and total power consumption, achieving average errors of 8.89% (dynamic) and 6.31% (total) for nested loops, and 9.86% (dynamic) and 3.41% (total) for single loops, respectively. These results prove that HIPPO paves the way for power-efficient high-level architecture exploration.
</p> 

<div style="display: flex; justify-content: center; align-items: center; gap: 24px;"> 
  <img src="http://zlinaf.github.io/images/hippo-overall.png" style="max-width: 50%;"> 
  <div style="display: flex; flex-direction: column; gap: 16px;"> 
    <img src="http://zlinaf.github.io/images/hippo-hierarchy.png" style="max-width: 100%;"> 
    <img src="http://zlinaf.github.io/images/hippo-modeling.png" style="max-width: 100%;"> 
  </div> 
</div>

---------------------------------------------------------
<p class="justify"> 
<strong>3. Run-Time Power Monitoring and Management</strong>. We study in-situ monitoring of FPGA power consumption at run time. We propose and evaluate a power monitoring scheme capable of accurately estimating the dynamic power of FPGA designs in a fine-grained timescale during onboard execution. Customized computer-aided design (CAD) flows are devised for power modeling either offline or online. Traditional decision trees and customized model ensemble strategies are deployed for power model establishment with offline sampling, while online decision trees are used for simultaneous power inference and training with real-time sample collection. Following this, we introduce the light-weight and scalable realization of the developed models, which can be integrated into the target applications for FPGA dynamic power monitoring at run time. The novel power monitoring techniques open up new opportunities for real-time FPGA power management in both coarse-grained and fine-grained timescales.
</p>

<div style="display: flex; justify-content: center; align-items: center; gap: 20px; max-width: 100%;">
  <img src="http://zlinaf.github.io/images/insitu-overall.png" style="max-width: 80%;">
  <img src="http://zlinaf.github.io/images/insitu-modeling.png" style="max-width: 20%;">
</div>

<br>

<hr style="
  border: none;
  border-top: 3px double #4169E1;
  height: 0;
  width: 100%;
  margin: 20px auto;
">

<span class="title-blue"> Topic 2: Automated Power and Performance Co-Optimization of ICs</span>
======

High-level synthesis (HLS) streamlines accelerator customization by delivering a high-level hardware programming paradigm enriched with a variety of optimization directives. However, the quality of HLS designs is largely determined by the selection of directives in navigating trade-offs among multiple design metrics, a non-trivial process that can significantly prolong design turnaround time. Moreover, the inability of power gating makes it even more difficult to optimize power from the perspective of HLS. We seek to co-optimize power and performance of ICs from high-level architectural abstractions.

---------------------------------------------------------
<p class="justify"> 
<strong>1. Large-Scale Design Space Exploration</strong>. Design space exploration (DSE) serves as a promising solution to HLS optimization, but existing studies on DSE suffer from a lack of efficiency or generalization capability in large-scale application scenarios. To address this problem, we propose AutoShrink, a DSE engine that automatically and adaptively shrinks the large search space of an HLS design to gradually retain only high-quality solutions. AutoShrink incorporates: (1) a comprehensive design space pruning strategy that integrates domain knowledge and consolidates the joint effect of directives; and (2) an importance-guided Pareto optimization algorithm that dynamically tracks the importance ranking of the applied directives and leverages this ranking to effectively steer the search toward Pareto-optimal solutions. Experimental results demonstrate that AutoShrink efficiently achieves a close approximation of the Pareto frontier across diverse benchmarks with design spaces scaling up to 10^16, which attains an average deviation of only 8.1%, outperforming three generic optimization methods and three state-of-the-art customized approaches by 5.73x and 4.47x, respectively.
</p>

<div style="display: flex; justify-content: space-between; gap: 10px; max-width: 100%;">
    <img src="http://zlinaf.github.io/images/autoshrink-overall.png" style="max-width: 40%;" alt="图1">
    <img src="http://zlinaf.github.io/images/autoshrink-pruning.png" style="max-width: 60%;"  alt="图2">
</div>





