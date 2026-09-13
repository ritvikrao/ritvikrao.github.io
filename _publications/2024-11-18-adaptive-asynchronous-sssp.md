---
title: "An Adaptive Asynchronous Approach for the Single-Source Shortest Paths Problem"
collection: publications
category: conferences
permalink: /publication/2024-11-18-adaptive-asynchronous-sssp
excerpt: 'We introduce ACIC, a highly asynchronous approach to the single-source shortest paths problem that uses continuous concurrent introspection and adaptation to reduce speculative loss without constraining parallelism.'
date: 2024-11-18
venue: '14th IEEE/ACM Workshop on Irregular Applications: Architectures and Algorithms (IA<sup>3</sup>), held in conjunction with SC24'
paperurl: '/files/adaptive-asynchronous-sssp.pdf'
citation: 'Ritvik Rao, Kavitha Chandrasekar, and Laxmikant V. Kalé. (2024). &quot;An Adaptive Asynchronous Approach for the Single-Source Shortest Paths Problem.&quot; <i>SC24-W: Workshops of the International Conference for High Performance Computing, Networking, Storage and Analysis</i>. pp. 697&ndash;702.'
bibtex: |
  @inproceedings{rao2024adaptive,
    title={An Adaptive Asynchronous Approach for the Single-Source Shortest Paths Problem},
    author={Rao, Ritvik and Chandrasekar, Kavitha and Kal{\'e}, Laxmikant V.},
    booktitle={SC24-W: Workshops of the International Conference for High Performance Computing, Networking, Storage and Analysis},
    pages={697--702},
    year={2024},
    organization={IEEE}
  }
---
Large-scale graphs with billions and trillions of vertices and edges require efficient parallel algorithms for common graph problems, one of which is single-source shortest paths (SSSP). Bulk-synchronous parallel algorithms such as Δ-stepping perform well on moderately-sized workloads, but the synchronization costs at a multi-node scale are large, so asynchronous approaches are needed for very large-scale graphs. However, asynchronous approaches to date are likely to suffer from large amounts of wasted, speculative execution. We introduce ACIC, a highly asynchronous approach modulated by continuous concurrent introspection and adaptation. Using message-driven concurrent reductions and broadcasts, task-based scheduling, and an adaptive aggregation library, we explore techniques such as evolving windows and generation and prioritized flow of optimal updates, or edge relaxations, aimed at reducing speculative loss without constraining parallelism. Our results, while preliminary, demonstrate the promise of these ideas, with the potential to impact a wider class of graph algorithms.
