---
title: "Research"
collection: research
permalink: /research/research
redirect_from: 
  - /research/
---

<br>

<div style="text-align: justify;">


<span style="color: #4169E1">Early-Stage Power Modeling for Digital Circuits and Systems</span>
======

<p style="text-align: justify;">
As the architecture complexity, integration density and chip size of modern integrated circuits (IC) continue to grow, the importance of power efficiency increases and ICs' power consumption is turning out to be one of the pivotal design objectives. In this project, we seek opportunities to model power consumption of digital circuits and systems. Specifically, we investigate the power modeling techniques from design time to run time. These techniques are compatible with each other, and putting it all together, they can jointly facilitate the advancements of power savings in both design-time hardware construction and real-time application execution.
</p>

---------------------------------------------------------
**1. HLS-Based Power Modeling of Digital Circuits**. We propose PowerGear, a graph-learning-assisted power estimation approach for high-level synthesis (HLS), which features high accuracy, efficiency, scalability, transferability, and applicability. PowerGear comprises two main components: a graph construction flow and a customized graph neural network (GNN) model. In the graph construction flow, PowerGear introduces buffer insertion, datapath merging, graph trimming and feature annotation techniques to transform HLS designs into graph-structured data, which encode both intra-operation micro-architectures and inter-operation interconnects annotated with switching activities. Additionally, PowerGear incorporates cross-function graph integration, dataflow adaptation, and design scaling strategies that make it compatible with multi-kernel, computation-intensive and large-scale applications. Furthermore, we propose a novel power-aware heterogeneous edge-centric GNN model, which effectively learns heterogeneous edge semantics and structural properties of the constructed graphs via edge-centric neighborhood aggregation, and eventually fits the formulation of dynamic power. Compared with on-board measurement, PowerGear shows average errors of 3.60% and 8.81% in total and dynamic power estimation, respectively, while the evaluation efficiency is improved by 41.9x. Moreover, PowerGear supports large-scale and dataflow-optimized neural networks with an error of only 3.91%, demonstrating broad applicability. Finally, PowerGear facilitates design space exploration for FPGA HLS, leading to a performance gain of up to 11.2%, compared with methods using state-of-the-art predictive models.

<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
  <img src="http://zlinaf.github.io/images/powergear-overall.png" width="50%">
  <img src="http://zlinaf.github.io/images/powergear-graphconstruction.png" width="50%">
</div>

---------------------------------------------------------
**2. Pre-HLS Architectural Power Modeling**. Power estimation for customized accelerators, especially those derived from high-level programming languages, entails the invocation of a long electronic design automation (EDA) tool chain, thus incurring large timing overhead that hinders early design optimization. To mitigate this problem, we propose HIPPO, an architecture-level power modeling framework for field-programmable gate arrays (FPGAs). HIPPO operates directly on C/C++ programs, whose execution is prior to and independent of any EDA tool including the very front-end, high-level synthesis (HLS). During power modeling, HIPPO exploits the intrinsic C/C++ code hierarchies, including nested loops and operations, and enables multi-level power estimation that aligns with different code hierarchies. Specifically, HIPPO can be decomposed into (1) a code transformation flow that directly converts a C/C++ program with HLS pragmas into hardware-oriented and power-aware control and dataflow graph, (2) a hierarchy-preserving power modeling methodology that combines analytical modeling and data-driven learning approaches to effectively orchestrate different code hierarchies, and (3) an adaptive dataflow coarsening strategy which ensures modeling accuracy, efficiency and robustness by suppressing noise of onboard measurement. Experimental results demonstrate that HIPPO effectively decomposes and accurately predicts both dynamic and total power consumption, achieving average errors of 8.89% (dynamic) and 6.31% (total) for nested loops, and 9.86% (dynamic) and 3.41% (total) for single loops, respectively. These results prove that HIPPO paves the way for power-efficient high-level architecture exploration.

<div style="display: flex; justify-content: center; align-items: center; gap: 24px;">
  <img src="http://zlinaf.github.io/images/hippo-overall.png" style="max-width: 50%;">
  <div style="display: flex; flex-direction: column; gap: 16px;">
    <img src="http://zlinaf.github.io/images/hippo-hierarchy.png" style="max-width: 100%;">
    <img src="http://zlinaf.github.io/images/hippo-modeling.png" style="max-width: 100%;">
  </div>
</div>

---------------------------------------------------------
**3. Run-Time Power Monitoring and Management**. We study in-situ monitoring of FPGA power consumption at run time. We propose and evaluate a power monitoring scheme capable of accurately estimating the dynamic power of FPGA designs in a fine-grained timescale during onboard execution. Customized computer-aided design (CAD) flows are devised for power modeling either offline or online. Traditional decision trees and customized model ensemble strategies are deployed for power model establishment with offline sampling, while online decision trees are used for simultaneous power inference and training with real-time sample collection. Following this, we introduce the light-weight and scalable realization of the developed models, which can be integrated into the target applications for FPGA dynamic power monitoring at run time. The novel power monitoring techniques open up new opportunities for real-time FPGA power management in both coarse-grained and fine-grained timescales.


FPGA Acceleration of AI Algorithms
======

<p align="center">
  <img src="https://zlinaf.github.io/images/dt-acc2.png">
</p>

Decision trees are machine learning models commonly used in various application scenarios. In the era of big data, traditional decision tree induction algorithms are not suitable for learning large-scale datasets due to their stringent data storage requirement. Online decision tree learning algorithms have been devised to tackle this problem by concurrently training with incoming samples and providing inference results. However, even the most up-to-date online tree learning algorithms still suffer from either high memory usage or high computational intensity with dependency and long latency, making them challenging to implement in hardware. To overcome these challenges, we introduce a new quantile-based algorithm to improve the induction of the Hoeffding tree, one of the state-of-the-art online learning models. The proposed algorithm is light-weight in terms of both memory and computational demand, while still maintaining high generalization ability. A series of optimization techniques dedicated to the proposed algorithm have been investigated from the hardware perspective, including coarse-grained and fine-grained parallelism, dynamic and memory-based resource sharing, pipelining with data forwarding. We further present a high-performance, hardware-efficient and scalable online decision tree learning system on a field-programmable gate array (FPGA) with system-level optimization techniques. 

CPU+FPGA Heterogeneous System Prototyping
======

<p align="center">
  <img src="http://zlinaf.github.io/images/cpu-fpga.png"  height="500">
</p>

Modern multicore systems are migrating from homogeneous systems to heterogeneous systems with accelerator-based computing in order to overcome the barriers of performance and power walls. In this trend, FPGA-based accelerators are becoming increasingly attractive, due to their excellent flexibility and low design cost. In this project, we propose the architectural support for efficient interfacing between FPGA-based multi-accelerators and chip-multiprocessors (CMPs) connected through the network-on-chip (NoC). Distributed packet receivers and hierarchical packet senders are designed to maintain scalability and reduce the critical path delay under a heavy task load. A dedicated accelerator chaining mechanism is also proposed to facilitate intra-FPGA data reuse among accelerators to circumvent prohibitive communication overhead between the FPGA and processors. In order to evaluate the proposed architecture, a complete system emulation with programmability support is performed using FPGA prototyping. Experimental results demonstrate that the proposed architecture has high-performance, and is light-weight and scalable in characteristics. 

<\div>
