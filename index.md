---
title: Argo
layout: splash
header:
  overlay_image: /assets/images/argo-spacecloud.jpg
excerpt: Low-Level Resource Management for the OS and Runtime
feature_row:
  - image_path: /assets/images/memory-mgmt.png
    alt: "Argo Memory Management"
    title: "Memory Management"
    excerpt: "We are developing software techniques to enable applications
    and runtime systems to make the best use of the capabilities of complex
    new memory types being incorporated into exascale node designs."
    url: /overview/#memory-management
    btn_label: "Read More"
    btn_class: "btn--info"
  - image_path: /assets/images/power-mgmt.png
    alt: "Argo Power Management"
    title: "Power Management"
    excerpt: "Dynamic power management is expected to be critical in the
    exascale era.  We employ hierarchical power management that includes
    both system-global and node-local mechanisms and policies."
    url: /overview/#power-management
    btn_label: "Read More"
    btn_class: "btn--info"
  - image_path: /assets/images/resource-mgmt.png
    alt: "Argo Resource Management"
    title: "Resource Management"
    excerpt: "We divide physical resources on compute nodes into
    separate partitions called slices, separating individual
    components of parallel workloads, in addition to cordoning off system
    services."
    url: /overview/#resource-management
    btn_label: "Read More"
    btn_class: "btn--info"
---

The goal of the Argo project is to augment and optimize existing OS/R
components for use in production HPC systems, providing portable, open
source, integrated software that improves the performance and scalability
of and that offers increased functionality to exascale applications and
runtime systems.

---

{% include feature_row %}

### News:

<ul>
  {% for post in site.posts limit:3 %}
    <li>
	  <b>{{ post.date | date_to_string: "ordinal", "US" }}</b>&nbsp;&nbsp;&nbsp;{{ post.title }}
	  <div class="smaller">
      {{ post.excerpt | markdownify | strip_html }} <a class="btn-dots" href="{{ site.baseurl }}{{ post.url }}">...</a>
	  </div>
    </li>
  {% endfor %}
</ul>
[More News]({{ site.baseurl }}/news/){: .btn .btn--info }

---

Argo is a collaborative project between [Argonne National
Laboratory](https://www.anl.gov/) and [Lawrence Livermore National
Laboratory](https://www.llnl.gov/).  It is funded by the [U.S.  Department
of Energy](https://www.energy.gov/) as part of the [Exascale Computing
Project (ECP)](https://www.exascaleproject.org/).
{: .smaller}
