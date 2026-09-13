---
title: "A Survey of Distributed Asynchronous Many-Task Models and Their Applications"
collection: publications
category: manuscripts
permalink: /publication/2026-08-14-amt-survey
excerpt: 'A comprehensive survey of distributed asynchronous many-task (AMT) runtime systems — including Charm++, HPX, Legion, PaRSEC, Uintah, Chapel, and StarPU — covering their design principles, execution models, and the application domains where they provide tangible benefits over MPI+X.'
date: 2026-08-14
venue: 'ACM Computing Surveys'
paperurl: '/files/amt-survey.pdf'
citation: 'Joseph Schuchart, Patrick Diehl, Michael Bauer, Aurelien Bouteiller, Gregor Daiss, Engin Kayraklioglu, Shreyas Khandekar, Thomas Herault, John Holmen, Ritvik Rao, Alexander Strack, Elliott Slaughter, Jennifer Spinti, Jeremy Thornock, Alex Aiken, Olivier Aumage, Martin Berzins, George Bosilca, Bradford Chamberlain, Hartmut Kaiser, and Laxmikant Kale. (2026). &quot;A Survey of Distributed Asynchronous Many-Task Models and Their Applications.&quot; <i>ACM Computing Surveys</i>. https://doi.org/10.1145/3840389'
bibtex: |
  @article{schuchart2026survey,
    title={A Survey of Distributed Asynchronous Many-Task Models and Their Applications},
    author={Schuchart, Joseph and Diehl, Patrick and Bauer, Michael and Bouteiller, Aurelien and Daiss, Gregor and Kayraklioglu, Engin and Khandekar, Shreyas and Herault, Thomas and Holmen, John and Rao, Ritvik and Strack, Alexander and Slaughter, Elliott and Spinti, Jennifer and Thornock, Jeremy and Aiken, Alex and Aumage, Olivier and Berzins, Martin and Bosilca, George and Chamberlain, Bradford and Kaiser, Hartmut and Kale, Laxmikant},
    journal={ACM Computing Surveys},
    year={2026},
    publisher={ACM},
    doi={10.1145/3840389}
  }
---
Asynchronous many-task (AMT) runtime systems have become an important paradigm for expressing fine-grained parallelism and managing asynchrony in high-performance computing (HPC). Originating from early dataflow concepts, AMTs have evolved to enable dynamic task generation, explicit dependency management, and asynchronous execution, facilitating the overlap of computation and communication. These capabilities address the limitations of traditional bulk-synchronous models, such as those employed in MPI+X, which can struggle with irregular, adaptive, or data-driven workloads. This survey provides a comprehensive overview of representative distributed AMT systems—including Charm++, HPX, Legion, PaRSEC, Uintah, Chapel, and StarPU—focusing on their design principles, execution models, and runtime mechanisms for scheduling, communication, and synchronization. We examine how these systems tackle key challenges such as load imbalance, runtime overheads, programmability, and performance portability. In addition, the paper discusses application domains where AMTs have demonstrated tangible benefits and highlights the conditions under which their use is most advantageous. The goal of this survey is to equip researchers and practitioners with a clear understanding of distributed AMT models and to provide guidance for selecting and applying the most suitable runtime system for specific computational objectives.
