---
title: "Runtime Adaptivity for CSE and Machine Learning with Charm4Py, CharmTyles, and CharmNumerics"
collection: talks
type: "Talk"
permalink: /talks/jlesc-talk-2
venue: "JLESC 2026"
date: 2026-05-20
location: "Julich, DE"
---

While high-performance computing traditionally consisted of CSE and large scientific applications, modern applications like data analytics and machine learning have now become more prominent. These new applications contain some of the same challenges as previous HPC workloads, including a need to deal with runtime variability and adaptation. As the focus in ML shifts from model-building via massive training to inference and large-scale serving, and as issues such as energy consumption and resource utilization gain importance, runtime adaptivity will become important for these domains as well. The increasing use of cloud infrastructure also emphasizes resource elasticity as well as resource heterogeneity, along with multi-tenancy. To solve these issues, we propose the use of Charm4Py, CharmTyles, and CharmNumerics, which build off the proven capabilities of the Charm++ parallel runtime system, but target data science and machine learning, along with Python-based CSE applications.

Charm4Py is a Python-based runtime system based on overdecomposition, which builds on top of Charm++. Charm4Py, like Charm++, is targeted towards traditional HPC applications, but combines the use of popular Python libraries with dynamic load balancing and computation-communication overlap. Charm4Py can also be used as an alternative to existing Python runtimes. In particular, we have developed an implementation of the Ray core API on top of Charm4Py, which allows existing Ray programs to use dynamic load balancing by representing Ray actors as Charm4Py chares, all without requiring any modification to existing Ray programs.

CharmTyles also builds upon Charm++, but in the direction of domain-specific abstractions. CharmTyles consists of a Python frontend and a Charm++/C++ backend. Operations from the Python frontend are represented by the backend as an abstract syntax tree, allowing for lazy evaluation and low-latency execution of operations. The Charm++ backend provides a set of libraries that are targeted towards data science applications, including CharmStencil (a library for stencil computations) and CharmPandas (an implementation of the Pandas library in Charm++).

Additionally, we propose CharmNumerics, a NumPy alternative built on top of the CharmTyles framework. CharmNumerics supports the same wide variety of matrix operations as NumPy, but with overdecomposition and load balancing that will particularly benefit sparse matrix operations.

Along with supporting Charm++ features, Charm4Py, CharmTyles, and CharmNumerics also support the use of heterogeneous computing resources. Our libraries support execution on NVIDIA, AMD, and Intel GPUs, enabling device scaling that is necessary on modern supercomputers. Additionally, we have added new communication abilities to the Charm runtime that allow for direct device-to-device communication on GPUs. On top of this, we also now allow for Charm++ and Charm4Py programs to be run on cloud providers and orchestrators such as AWS and Kubernetes, and we also support resource elasticity by allowing the number of nodes to be changed during execution.
