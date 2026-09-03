---
title: "Charm4Py: A Programming Model for Distributed Adaptive Python"
collection: talks
type: "Tutorial"
permalink: /talks/charm4py-tutorial-ipdps
venue: "IPDPS 2026"
date: 2026-05-25
location: "New Orleans, LA, USA"
---

[More information here](https://github.com/charmplusplus/charm4py-tutorial2026)

Many programming models have been developed to implement scalable parallel programs. Charm++ is built around the concept of distributed migratable objects, called chares. This empowers an introspective and adaptive runtime system (aRTS) to support automatic overlap of communication and computation, dynamic load balancing, energy optimization, fault tolerance, and resource elasticity. These signature adaptive capabilities distinguish Charm++ from MPI, the predominant parallel programming model.

Charm4Py is an implementation of the Charm++ programming model that makes these adaptive capabilities available to parallel Python programmers. Charm4Py programs use Python classes to implement chare objects; Charm++ features such as dynamic load balancing and asynchronous communication are made available to Charm4Py programs by linking it with the Charm++ aRTS under the hood. Charm4Py can thus be thought of as Distributed Adaptive Python, a parallel programming model with distributed adaptivity features that is compatible with existing Python conventions, and allows the use of existing popular Python libraries.

This tutorial aims to teach effective parallel programming using Charm4Py. Attendees will start with basic knowledge of Python, and by the end of the tutorial are expected to be able to code sophisticated parallel applications that can run on clusters, supercomputers, and cloud-based resources scalably and adaptively.
