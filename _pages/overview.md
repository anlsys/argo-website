---
title: Overview
permalink: /overview/
feature_row_umap:
  - image_path: /assets/images/umap-pic.png
    alt: "UMap"
    title: "UMap"
    excerpt: "User Level Memory Map (UMap) is a memory map approach to
    incorporating NVRAM into complex memory hierarchy.  It replaces `mmap`
    for out-of-core data.  By exploiting large virtual address spaces, data
    sets can be accessed directly as if in memory; this is particularly
    well suited to analyzing large observational and simulation data.
    Thanks to its user-space design, UMap is flexible and easy to use."
    url: "/overview/umap/"
    btn_label: "Read More"
    btn_class: "btn--info"
feature_row_aml:
  - image_path: /assets/images/memory-mgmt.png
    alt: "AML"
    title: "AML"
    excerpt: "AML provides explicit, application-aware memory management
    for deep memory systems.  It can be used to create, for example, a
    software-managed scratchpad for multilevel DRAM hierarchy such as HBM
    and DDR.  Such a scratchpad provides applications with a memory region
    with a predictable high performance for critical data structures."
    url: "/overview/aml/"
    btn_label: "Read More"
    btn_class: "btn--info"
feature_row_grm:
  - image_path: /assets/images/slurm.png
    alt: "GRM"
    title: "GRM"
    excerpt: "Global management of power in Argo is handled by the Global
    Resource Manager (GRM).  As part of this effort we added dynamic power
    awareness to the popular batch scheduler SLURM.  We also extended the
    Flux scheduler with power awareness, addressing static manufacturing
    variation.  This work is part of the community-wide _PowerStack_
    effort."
    url: "/overview/grm/"
    btn_label: "Read More"
    btn_class: "btn--info"
feature_row_nrm:
  - image_path: /assets/images/nrm-landscape.png
    alt: "NRM"
    title: "NRM"
    excerpt: "Power management at the node level is built into the Argo
    Node Resource Manager (NRM).  It works in a closed control loop,
    obtaining goals from the GRM, acting on application workloads launched
    within slices, and getting feedback through the monitoring of hardware
    sensors measuring, for example, power draw or temperature."
    url: "/overview/nrm/"
    btn_label: "Read More"
    btn_class: "btn--info"
feature_row_slices:
  - image_path: /assets/images/resource-mgmt.png
    alt: "Slices"
    title: "Slices"
    excerpt: "The management of slices is another responsibility of the
    NRM, which maps them to the node's hardware topology, arbitrating
    resources between applications and runtime services, and providing
    integration with the power management.  Resources can be dynamically
    reconfigured at run time; interfaces are provided for use from
    applications and from global services."
    url: "/overview/nrm/"
    btn_label: "Read More"
    btn_class: "btn--info"
feature_row_codesign:
  - image_path: /assets/images/trip-arch.png
    alt: "TRIP"
    excerpt: "A significant portion of this work is covered by NDAs so it
    cannot be included here.  Instead, we provide an overview of related
    open research carried out in collaboration with universities."
    url: "/overview/codesign/"
    btn_label: "Read More"
    btn_class: "btn--info"
---

<div class="noborder" markdown="1">

We are building a portable, open source, integrated, validated, and
scalability tested software stack that improves the performance and
scalability and provides increased functionality to exascale applications
and runtime systems.

System resources should be managed in cooperation with applications and
runtime systems to provide improved performance and resilience.  This is
motivated by the increasing complexity of HPC hardware and application
software, which needs to be matched by corresponding increases in the
capabilities of system management solutions.

Our approach is to augment and optimize for HPC the existing open source
offerings used by the vendors.  The Argo software is developed as a toolbox
-- a collection of autonomous components that can be freely mixed and
matched to best meet the user's needs.

The project currently has four focus areas:
* [Memory management](#memory-management)
* [Power management](#power-management)
* [Resource management](#resource-management)
* [Hardware co-design](#hardware-co-design)

---

Memory Management
-----------------

We are developing software techniques to enable applications and runtime
systems to make the best use of the capabilities of complex new memory
types being incorporated into exascale node designs.

Due to a large variety of emerging technologies, we are pursuing two
complementary strategies aimed at different memory types.

{% include feature_row_custom id="feature_row_umap" type="left" %}
{% include feature_row_custom id="feature_row_aml" type="right" %}

---

Power Management
----------------

Dynamic power management is expected to be critical in the exascale era,
both in terms of not exceeding the overall available power budget and in
terms of utilizing the available power to make the most application
progress.  In the Argo project, we employ hierarchical power management
that includes both system-global and node-local mechanisms and policies.

{% include feature_row_custom id="feature_row_grm" type="left" %}
{% include feature_row_custom id="feature_row_nrm" type="right" %}

---

Resource Management
-------------------

We use resource partitioning to divide physical resources on the compute
nodes into separate partitions which we call _slices_.  Slices can be used
to separate individual components of parallel workloads, in addition to
cordoning off system services; this physical separation ensures an improved
performance isolation between components.

{% include feature_row_custom id="feature_row_slices" type="left" %}

---

Hardware Co-Design
------------------

We are continuously exploring emerging new hardware trends and devices,
looking for how best to exploit the new capabilities in both traditional
HPC workloads and emerging ones such as machine learning.  We try to
identify how the new features should be integrated into existing runtime
systems and operating systems and in what way such features should be
exposed to applications.

{% include feature_row_custom id="feature_row_codesign" type="left" %}

</div>
