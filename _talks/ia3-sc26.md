---
title: "Efficient Cosmological Friends-of-Friends Computation with Fine-Grained Optimizations"
collection: talks
type: "Talk"
permalink: /talks/ia3-sc26
venue: "IA^3 at SC26"
date: 2026-11-15
location: "Chicago, IL, USA"
---

[Slides (PDF)](/files/cluster-finding-ia3-talk.pdf)

One computationally intensive part of cosmological
simulations is identifying clusters. One method to do this is via the
friends-of-friends (FoF) algorithm, which is functionally equiv-
alent to finding incremental connected components. Optimizing
FoF for large, imbalanced datasets is challenging due to load and
communication imbalance. In this paper, we present a parallel
approach that integrates a tree traversal library with a union-
find library. While this combination provided a foundational
framework, we discovered that it fell short of meeting the
rigorous performance demands of complex cosmological data.
To overcome this, we designed and implemented a series of
fine-grained optimizations tailored to the unique memory and
processing patterns of the algorithm. We demonstrate that
our approach achieves significant performance gains for highly
imbalanced outputs without compromising cluster accuracy or
quality. Finally, we analyze these results and identify remaining
opportunities for further improvement in scalable cluster finding.
