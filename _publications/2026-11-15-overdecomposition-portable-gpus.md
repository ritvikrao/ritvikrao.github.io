---
title: "Efficient and Portable Support for Overdecomposition on Distributed GPU Platforms"
collection: publications
category: conferences
permalink: /publication/2026-11-15-overdecomposition-portable-gpus
excerpt: 'We show that overdecomposition can be sustained efficiently and portably on GPUs across vendors, by mitigating host-side serialization costs transparently at the runtime layer in a single-source Charm++/Kokkos environment running unchanged on NVIDIA and AMD systems.'
date: 2026-11-15
venue: '9th Annual Parallel Applications Workshop, Alternatives To MPI+X (PAW-ATM), held in conjunction with SC26 — accepted, to appear'
paperurl: '/files/overdecomposition-portable-gpus.pdf'
citation: 'Aditya Bhosale, Anant Jain, Shourya Goel, Ritvik Rao, Peddoju Sateesh Kumar, and Laxmikant Kalé. (2026). &quot;Efficient and Portable Support for Overdecomposition on Distributed GPU Platforms.&quot; <i>9th Annual Parallel Applications Workshop, Alternatives To MPI+X (PAW-ATM), held in conjunction with SC26</i>. To appear.'
bibtex: |
  @inproceedings{bhosale2026overdecomposition,
    title={Efficient and Portable Support for Overdecomposition on Distributed GPU Platforms},
    author={Bhosale, Aditya and Jain, Anant and Goel, Shourya and Rao, Ritvik and Kumar, Peddoju Sateesh and Kal{\'e}, Laxmikant},
    booktitle={Proceedings of the 9th Annual Parallel Applications Workshop, Alternatives To MPI+X (PAW-ATM), held in conjunction with SC26},
    year={2026},
    note={To appear}
  }
---
Overdecomposition enables asynchronous many-task runtimes such as Charm++ to overlap communication with computation and to balance load dynamically. Its benefits are well established on CPUs, but GPUs achieve peak efficiency with large kernels and bulk transfers, raising the concern that fine-grained execution will incur prohibitive launch, synchronization, and communication overheads. This paper investigates whether overdecomposition can be sustained efficiently on GPUs, and portably across vendors. We find that at fine granularity, the dominant costs arise not on the device but from serialization on the host, in vendor-specific ways, and that they can be mitigated transparently by the runtime: by parallelizing kernel submission and completion detection across a hierarchy of processes and threads sharing each GPU, and by routing every message through device-to-device paths suited to its destination. We evaluate these techniques in a single-source Charm++/Kokkos environment that runs unchanged on NVIDIA and AMD systems. On Task Bench, they reduce the minimum effective task granularity from 26–37µs to 4µs, and in weak and strong scaling studies of three mini-applications, Jacobi2D, MiniMD, and LULESH, on up to 64 A40 and 32 MI250X GPUs, overdecomposed execution matches MPI performance across a range of overdecomposition factors.
