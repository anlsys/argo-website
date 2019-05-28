---
title: AML
permalink: /overview/aml/
---

AML provides explicit, application-aware memory management for deep memory
systems.  It offers a collection of building blocks that are _generic_,
_customizable_, and _composable_.  Applications can specialize the
implementation of each offered abstraction and can mix and match the
components as needed.  AML can be used to create, for example, a
software-managed scratchpad for multilevel DRAM hierarchy such as HBM and
DDR.  Such a scratchpad provides applications with a memory region with a
predictable high performance for critical data structures.

We provide applications and runtimes with a descriptive API for data
access, where all data placement decisions are explicit, and so is the
movement of data between different memory types.  At the same time, the API
does abstract the memory topology and other device complexities.  We focus
on optimizing data locality for current and future hardware generations;
applications provide insights for static allocations, and we can also
dynamically and asynchronously remap to optimize for a particular data
layout or to best take advantage of the memory hierarchy.

![AML components]({{ site.baseurl }}/assets/images/aml.png){: .align-right .responsive-width-20}
The first figure depicts the major components of AML, which include the
following:
* Topology & hardware management (dependent on NUMA, hwloc, and SICM)
* Data layout descriptions (application-specific)
* Tiling schemes (including ghost areas)
* Data movement facilities (currently primarily `memcpy` or `move_pages`)
* Pipelining helpers (scratchpad, asynchronous requests)

![AML application]({{ site.baseurl }}/assets/images/memory-mgmt.png){: .align-left .shadow .responsive-width-40}
We conducted an experiment on an Intel Knights Landing system running in
flat/quad mode to verify the effectiveness of the AML prefetching using a
custom DGEMM implementation, which uses pipelining to move data between DDR
and MCDRAM, OpenMP tasks, and an inner kernel autotuned for AVX2.  We
compared prefetching against two static allocation approaches: one where
all the data is in the regular DDR memory and one where it is optimally
distributed between DDR and MCDRAM.  As shown in the second figure, the
prefetcher achieves performance equal to or better than that of the optimal
static allocation on inputs that exceed the capacity of MCDRAM.
<br clear="both" />

_Nicolas Denoyelle, Swann Perarnau, Brice Videau (ANL)_
{: .smaller}
