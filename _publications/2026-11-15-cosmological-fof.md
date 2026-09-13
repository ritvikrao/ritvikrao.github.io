---
title: "Efficient Cosmological Friends-of-Friends Computation with Fine-Grained Optimizations"
collection: publications
category: conferences
permalink: /publication/2026-11-15-cosmological-fof
excerpt: 'We present a series of fine-grained optimizations to a parallel friends-of-friends (FoF) cluster-finding implementation built on the ParaTreeT and Union-Find libraries, achieving significant performance gains on highly imbalanced cosmological datasets without compromising cluster accuracy.'
date: 2026-11-15
venue: '16th IEEE/ACM Workshop on Irregular Applications: Architectures and Algorithms (IA<sup>3</sup>), held in conjunction with SC26 — accepted, to appear'
paperurl: '/files/cosmological-fof.pdf'
citation: 'Ritvik Rao and Laxmikant Kalé. (2026). &quot;Efficient Cosmological Friends-of-Friends Computation with Fine-Grained Optimizations.&quot; <i>16th IEEE/ACM Workshop on Irregular Applications: Architectures and Algorithms (IA3), held in conjunction with SC26</i>. To appear.'
bibtex: |
  @inproceedings{rao2026fof,
    title={Efficient Cosmological Friends-of-Friends Computation with Fine-Grained Optimizations},
    author={Rao, Ritvik and Kal{\'e}, Laxmikant},
    booktitle={Proceedings of the 16th IEEE/ACM Workshop on Irregular Applications: Architectures and Algorithms (IA3), held in conjunction with SC26},
    year={2026},
    organization={IEEE},
    note={To appear}
  }
---
One computationally intensive part of post-processing cosmological simulations is identifying clusters. One method to do this is via the friends-of-friends (FoF) algorithm, which is functionally equivalent to finding incremental connected components. Optimizing FoF for large, imbalanced datasets requires high precision. In this paper, we present a parallel approach that integrates a tree traversal library with a union-find library. While this combination provided a foundational framework, we discovered that it fell short of meeting the rigorous performance demands of complex cosmological data. To overcome this, we designed and implemented a series of fine-grained optimizations tailored to the unique memory and processing patterns of the algorithm. We demonstrate that our refined approach achieves significant performance gains for highly imbalanced outputs without compromising cluster accuracy or quality. Finally, we analyze these results and identify remaining opportunities for further improvement in scalable cluster finding.
