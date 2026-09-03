---
title: "An Adaptive Asynchronous Approach for the Single-Source Shortest Paths Problem"
collection: talks
type: "Talk"
permalink: /talks/ia3-sc24
venue: "IA^3 at SC24"
date: 2024-11-17
location: "Atlanta, GA, USA"
---

Large-scale graphs with billions and trillions of ver-
tices and edges require efficient parallel algorithms for common
graph problems, one of which is single-source shortest paths
(SSSP). Bulk-synchronous parallel algorithms such as ∆-stepping
experience large synchronization costs at the scale of many nodes,
so asynchronous approaches are needed for scalability. However,
asynchronous approaches are susceptible to wasteful, speculative
execution. We introduce ACIC, a highly asynchronous approach
modulated by continuous concurrent introspection and adapta-
tion. Using message-driven concurrent reductions and broadcasts,
task-based scheduling, and an adaptive aggregation library, we
explore techniques such as evolving windows and generation and
prioritized flow of optimal updates, or edge relaxations, aimed at
reducing speculative loss without constraining parallelism. Our
results, while preliminary, demonstrate the promise of these ideas,
with the potential to impact a wider class of graph algorithms.
