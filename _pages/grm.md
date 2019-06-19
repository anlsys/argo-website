---
title: GRM
permalink: /overview/grm/
---

![PowerSlurm architecture]({{ site.baseurl }}/assets/images/slurm.png){: .align-right .shadow .responsive-width-40}
Global management of power in Argo is handled by the Global Resource
Manager (GRM).  As part of this effort we added dynamic power awareness to
the popular batch scheduler SLURM, as shown in the first figure.  Our
collaborators from the University of Tokyo tested it on 960 nodes of the
HA8K system, analyzing idle power and throughput.  The results in the
second figure show the benefits of hardware overprovisioning at scale as
well as sensitivity to the degree of overprovisioning.

![Overprovisioning]({{ site.baseurl }}/assets/images/power-mgmt.png){: .shadow .responsive-width-40}

We also extended the Flux scheduler with power awareness addressing static
manufacturing variation; in an experiment on a 1,200-node system at LLNL
this resulted in a 2.3x reduction in rank-to-rank performance
variation under a power cap.

![Overprovisioning]({{ site.baseurl }}/assets/images/powerstack.png){: .align-right .shadow .responsive-width-60}
Recently, _PowerStack_ has emerged as a new community-wide effort for power
management in HPC systems.  We---together with our partners from industry,
academia, and other research labs across the United States, Europe, and
Asia---are the founding members of this initiative.  PowerStack is expected
to leverage some of the tools we have developed; parts of the Argo power
management infrastructure will also serve as first prototypes.
<br clear="both" />

---

For a complete list of GRM-related resources, check the [For Developers]({{
site.baseurl }}/devel/#powerstack) page.


_Stephanie Brink, Aniruddha Marathe, Tapasya Patki, Barry Rountree (LLNL);
David Lowenthal (U&nbsp;Arizona)_
{: .smaller}
