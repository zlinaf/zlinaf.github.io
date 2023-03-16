---
title: "Research"
redirect_from: 
  - /research/
---

Learning-Based Power Modeling for FPGA
======

![Power Modeing for FPGA](http://zlinaf.github.io/images/power-modeling.png)

Field-programmable gate arrays (FPGAs) are gaining popularity in wide-ranging domains including data centers and embedded systems, where they serve as reconfigurable hardware accelerators for speeding up computation-centric tasks. As the architecture complexity, integration density and chip size of modern FPGAs continue to grow, the importance of power efficiency increases and FPGA power consumption is turning out to be a key design constraint. In this project, we seek opportunities to exploit the use of machine learning techniques to model FPGA power consumption, and conduct power-oriented optimizations based on the power models. Specifically, we investigate the FPGA power modeling techniques from design time to run time. These techniques are compatible with each other, and putting it all together, they can jointly facilitate FPGA power savings in both design-time hardware construction and real-time application execution.

**Power Modeling and DSE**. We investigate power modeling for design-time power analysis and power-oriented design space exploration (DSE) for FPGA designs. We propose PowerGear and HL-Pow, an accurate, fast and early-stage power modeling methodology for high-level synthesis (HLS). In these works, we incorporate an automated feature construction flow to efficiently identify and extract features that exert a major influence on power consumption, simply based upon HLS results, and a modeling flow that can build an accurate and generic learning-based power model applicable to a variety of designs with HLS. By using our design flow, the power evaluation process for FPGA designs can be significantly expedited because the power inference is established on HLS instead of the time-consuming register-transfer level (RTL) implementation flow. To further facilitate design-time power minimization, we describe a novel and fast DSE algorithm built on top of modeling frameworks to reach a close approximation of the Pareto frontier between latency and power consumption.

**Run-Time Power Monitoring and Management**. We study in-situ monitoring of FPGA power consumption at run time. We propose and evaluate a power monitoring scheme capable of accurately estimating the dynamic power of FPGA designs in a fine-grained timescale during onboard execution. Customized computer-aided design (CAD) flows are devised for power modeling either offline or online. Traditional decision trees and customized model ensemble strategies are deployed for power model establishment with offline sampling, while online decision trees are used for simultaneous power inference and training with real-time sample collection. Following this, we introduce the light-weight and scalable realization of the developed models, which can be integrated into the target applications for FPGA dynamic power monitoring at run time. The novel power monitoring techniques open up new opportunities for real-time FPGA power management in both coarse-grained and fine-grained timescales.
