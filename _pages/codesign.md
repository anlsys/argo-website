---
title: Hardware Co-Design
permalink: /overview/codesign/
---

FPGAs
-----

![TRIP architecture]({{ site.baseurl }}/assets/images/trip-arch.png){: .align-right .shadow .responsive-width-40}
TRIP (An Ultra-Low Latency, **T**eraOps/s **R**econfigurable **I**nference
**P**rocessor for Multi-Layer Perceptrons) is a "soft" deep neural network
for MLPs.  It features a hybrid OpenCL-Verilog design, where the MLP engine
is written in Verilog and OpenCL is used for data exchange between the CPU
and the FPGA.  It runs on the Nallatech 385A platform (Arria10).

![TRIP performance with CANDLE]({{ site.baseurl }}/assets/images/trip-candle.png){: .align-left .shadow .responsive-width-40}
The table shows how such a targeted, custom design can outperform more
general-purpose vendor offerings.  We continue improving the design with
features such as mixed precision, more efficient data movement, and a
scalable OS/runtime.  This project is a collaboration with Boston
University.

Thermal-Aware Computing
-----------------------

![Thermal effects]({{ site.baseurl }}/assets/images/thermal-apps.png){: .align-right .shadow .responsive-width-50}
Cooling power is a non-negligible issue in HPC systems, and thermal
variations at every level (environment, hardware from transistors to
clusters) make it worse.  The figure shows how running the same code on
four nodes of the same cluster can result in significantly different
temperatures of the compute elements.  We are studying CPUs, GPUs, and
FPGAs and are using machine-learning prediction models for better task
scheduling on the system.  This project is a collaboration with
Northwestern University.
<br clear="both" />

_Kazutomo Yoshii (ANL)_
{: .smaller}
