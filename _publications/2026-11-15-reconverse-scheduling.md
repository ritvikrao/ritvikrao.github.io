---
title: "Reconverse: A New Scheduling Library for Multithreaded Task-Based Runtime Systems"
collection: publications
category: conferences
permalink: /publication/2026-11-15-reconverse-scheduling
excerpt: 'We present Reconverse, a new scheduling library for task-based runtime systems that replaces Charm++''s aging Converse layer, showing improved performance and speedups of up to 2x on large-scale applications.'
date: 2026-11-15
venue: '9th Annual Parallel Applications Workshop, Alternatives To MPI+X (PAW-ATM), held in conjunction with SC26 — accepted, to appear'
paperurl: '/files/reconverse-scheduling.pdf'
citation: 'Ritvik Rao, Jiakun Yan, Aditya Bhosale, and Laxmikant Kalé. (2026). &quot;Reconverse: A New Scheduling Library for Multithreaded Task-Based Runtime Systems.&quot; <i>9th Annual Parallel Applications Workshop, Alternatives To MPI+X (PAW-ATM), held in conjunction with SC26</i>. To appear.'
bibtex: |
  @inproceedings{rao2026reconverse,
    title={Reconverse: A New Scheduling Library for Multithreaded Task-Based Runtime Systems},
    author={Rao, Ritvik and Yan, Jiakun and Bhosale, Aditya and Kal{\'e}, Laxmikant},
    booktitle={Proceedings of the 9th Annual Parallel Applications Workshop, Alternatives To MPI+X (PAW-ATM), held in conjunction with SC26},
    year={2026},
    note={To appear}
  }
---
Task-based runtime systems, including Charm++, provide benefits not available with MPI, such as dynamic load balancing and automatic computation-communication overlap. Charm++ is currently built on top of an old scheduling layer called Converse. However, Converse lacks many features that are essential for distributed multithreaded performance, and other programming models cannot directly use the Converse scheduler. To solve these problems, we present Reconverse, a new scheduling layer for task-based runtime systems. Reconverse is a separately compiled library that can be linked to Charm++ or other runtime systems. Compared to Converse, Reconverse contains experimental features for optimizing fine-grained applications such as lottery queue scheduling. Reconverse also supports new machine layers such as LCI, a new communication layer for multithreaded runtime systems. We show that Reconverse improves performance compared to Converse on multiple benchmarks and also demonstrates speedups of up to 2x on large-scale applications, showing the benefits of Reconverse for multithreaded distributed workloads.
