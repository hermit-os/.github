<img width="100" align="right" src="https://raw.githubusercontent.com/hermit-os/.github/main/logo/hermit-logo.svg" />

# Hermit

[![Zulip Badge](https://img.shields.io/badge/chat-hermit-57A37C?logo=zulip)](https://hermit.zulipchat.com/)

This is the organization of the Hermit unikernel project from RWTH Aachen University.
These are the main components of the project:

- [hermit-os/kernel](https://github.com/hermit-os/kernel) is the Hermit kernel.
- [hermit-os/hermit-rs](https://github.com/hermit-os/hermit-rs) provides Rust application support.
- [hermit-os/uhyve](https://github.com/hermit-os/uhyve) is a specialized hypervisor for Hermit.
- [hermit-os/loader](https://github.com/hermit-os/loader) is a bootloader for other platforms, such as QEMU.

## Quick Start

- [hermit-os/hermit-rs-template](https://github.com/hermit-os/hermit-rs-template) is a starting point for your Rust application.
- An introductory presentation is available at [hermit-os.github.io/tutorial](https://hermit-os.github.io/tutorial).

## Publications

Several scientific publications have been made based on the Hermit project:

- Jonathan Klimt, Martin Kröning, Stefan Lankes, and Antonello Monti. 2023. On the Challenge of Sound Code for Operating Systems. In *Proceedings of the 12th Workshop on Programming Languages and Operating Systems* (Koblenz, Germany) *(PLOS ’23)*. Association for Computing Machinery, New York, NY, USA, 83–90. <https://doi.org/10.1145/3623759.3624554>
- Stefan Lankes, Jonathan Klimt, Jens Breitbart, and Simon Pickartz. 2020. RustyHermit: A Scalable, Rust-Based Virtual Execution Environment. In *High Performance Computing*, Heike Jagode, Hartwig Anzt, Guido Juckeland, and Hatem Ltaief (Eds.). Springer International Publishing, Cham, 331–342. <https://doi.org/10.1007/978-3-030-59851-8_22>
- Mincheol Sung, Pierre Olivier, Stefan Lankes, and Binoy Ravindran. 2020. Intra-Unikernel Isolation with Intel Memory Protection Keys. In *Proceedings of the 16th ACM SIGPLAN/SIGOPS International Conference on Virtual Execution Environments* (Lausanne, Switzerland) *(VEE ’20)*. Association for Computing Machinery, New York, NY, USA, 143–156. <https://doi.org/10.1145/3381052.3381326>
- Stefan Lankes, Jens Breitbart, and Simon Pickartz. 2019. Exploring Rust for Unikernel Development. In *Proceedings of the 10th Workshop on Programming Languages and Operating Systems* (Huntsville, ON, Canada) *(PLOS’19)*. Association for Computing Machinery, New York, NY, USA, 8–15. <https://doi.org/10.1145/3365137.3365395>
- Pierre Olivier, Daniel Chiba, Stefan Lankes, Changwoo Min, and Binoy Ravindran. 2019. A Binary-Compatible Unikernel. In *Proceedings of the 15th ACM SIGPLAN/SIGOPS International Conference on Virtual Execution Environments* (Providence, RI, USA) *(VEE 2019)*. Association for Computing Machinery, New York, NY, USA, 59–73. <https://doi.org/10.1145/3313808.3313817>
- Stefan Lankes, Simon Pickartz, and Jens Breitbart. 2017. A Low Noise Unikernel for Extrem-Scale Systems. In *Architecture of Computing Systems - ARCS 2017*, Jens Knoop, Wolfgang Karl, Martin Schulz, Koji Inoue, and Thilo Pionteck (Eds.). Springer International Publishing, Cham, 73–84. <https://doi.org/10.1007/978-3-319-54999-6_6>
- Stefan Lankes, Simon Pickartz, and Jens Breitbart. 2016. HermitCore: A Unikernel for Extreme Scale Computing. In *Proceedings of the 6th International Workshop on Runtime and Operating Systems for Supercomputers* (Kyoto, Japan) *(ROSS ’16)*. Association for Computing Machinery, New York, NY, USA, Article 4, 8 pages. <https://doi.org/10.1145/2931088.2931093>

<details>
    <summary>BibTeX</summary>

```bibtex
@inproceedings{klimt2023,
    author    = {Klimt, Jonathan and Kr\"{o}ning, Martin and Lankes, Stefan and Monti, Antonello},
    title     = {On the Challenge of Sound Code for Operating Systems},
    year      = {2023},
    isbn      = {9798400704048},
    publisher = {Association for Computing Machinery},
    address   = {New York, NY, USA},
    url       = {https://doi.org/10.1145/3623759.3624554},
    doi       = {10.1145/3623759.3624554},
    abstract  = {The memory-safe systems programming language Rust is gaining more and more attention in the operating system development communities, as it provides memory safety without sacrificing performance or control. However, these safety guarantees only apply to the safe subset of Rust, while bare-metal programming requires some parts of the program to be written in unsafe Rust. Writing abstractions for these parts of the software that are sound, meaning that they guarantee the absence of undefined behavior and thus uphold the invariants of safe Rust, can be challenging. Producing sound code, however, is essential to avoid breakage when the code is used in new ways or the compiler behavior changes. In this paper, we present common patterns of unsound abstractions derived from the experience of reworking soundness in our kernel. During this process, we were able to remove over 400 unsafe expressions while discovering and fixing several hard-to-spot concurrency bugs along the way.},
    booktitle = {Proceedings of the 12th Workshop on Programming Languages and Operating Systems},
    pages     = {83–90},
    numpages  = {8},
    keywords  = {operating system, systems programming, safe, soundness, unsafe, memory safety, Rust},
    location  = {Koblenz, Germany},
    series    = {PLOS '23}
}

@inproceedings{lankes2020,
    author    = {Lankes, Stefan and Klimt, Jonathan and Breitbart, Jens and Pickartz, Simon},
    editor    = {Jagode, Heike and Anzt, Hartwig and Juckeland, Guido and Ltaief, Hatem},
    title     = {RustyHermit: A Scalable, Rust-Based Virtual Execution Environment},
    booktitle = {High Performance Computing},
    year      = {2020},
    publisher = {Springer International Publishing},
    address   = {Cham},
    pages     = {331--342},
    abstract  = {System-level development has been dominated by programming languages such as C/C++ for decades. These languages are inherently unsafe, error-prone, and a major reason for vulnerabilities. High-level programming languages with a secure memory model and strong type system are able to improve the quality of the system software. This paper explores the programming language Rust for development of a scalable, virtual execution environment and presents the integration of a Rust-based IP stack into RustyHermit. RustyHermit is part of the standard Rust toolchain and common Rust applications are able to build on top of RustyHermit.},
    isbn      = {978-3-030-59851-8}
}

@inproceedings{sung2020,
    author    = {Sung, Mincheol and Olivier, Pierre and Lankes, Stefan and Ravindran, Binoy},
    title     = {Intra-Unikernel Isolation with Intel Memory Protection Keys},
    year      = {2020},
    isbn      = {9781450375542},
    publisher = {Association for Computing Machinery},
    address   = {New York, NY, USA},
    url       = {https://doi.org/10.1145/3381052.3381326},
    doi       = {10.1145/3381052.3381326},
    abstract  = {Unikernels are minimal, single-purpose virtual machines. This new operating system model promises numerous benefits within many application domains in terms of lightweightness, performance, and security. Although the isolation between unikernels is generally recognized as strong, there is no isolation within a unikernel itself. This is due to the use of a single, unprotected address space, a basic principle of unikernels that provide their lightweightness and performance benefits. In this paper, we propose a new design that brings memory isolation inside a unikernel instance while keeping a single address space. We leverage Intel's Memory Protection Key to do so without impacting the lightweightness and performance benefits of unikernels. We implement our isolation scheme within an existing unikernel written in Rust and use it to provide isolation between trusted and untrusted components: we isolate (1) safe kernel code from unsafe kernel code and (2) kernel code from user code. Evaluation shows that our system provides such isolation with very low performance overhead. Notably, the unikernel with our isolation exhibits only 0.6\% slowdown on a set of macro-benchmarks.},
    booktitle = {Proceedings of the 16th ACM SIGPLAN/SIGOPS International Conference on Virtual Execution Environments},
    pages     = {143–156},
    numpages  = {14},
    keywords  = {unikernels, memory safety, memory protection keys},
    location  = {Lausanne, Switzerland},
    series    = {VEE '20}
}

@inproceedings{lankes2019,
    author    = {Lankes, Stefan and Breitbart, Jens and Pickartz, Simon},
    title     = {Exploring Rust for Unikernel Development},
    year      = {2019},
    isbn      = {9781450370172},
    publisher = {Association for Computing Machinery},
    address   = {New York, NY, USA},
    url       = {https://doi.org/10.1145/3365137.3365395},
    doi       = {10.1145/3365137.3365395},
    abstract  = {System-level development has been dominated by programming languages like C/C++ for decades. These languages are inherently unsafe, error-prone, and a major reason for vulnerabilities. High-level programming languages with a secure memory model and strong type system are able to improve the quality of the system software. In this paper, we explore the programming language Rust for kernel development and present RustyHermit, which is a unikernel completely written in Rust without any C/C++. We show that the support for RustyHermit can be transparently integratable in the Rust toolchain and common Rust applications are build-able on top of RustyHermit. Previously, we developed the C-based unikernel HermitCore with a similar design to RustyHermit and we are able to compare both kernels. We show that the performance of both kernels is similar and only ~3.27 \% of RustyHermit relies on unsafe code, that cannot be checked by the compiler in detail.},
    booktitle = {Proceedings of the 10th Workshop on Programming Languages and Operating Systems},
    pages     = {8–15},
    numpages  = {8},
    location  = {Huntsville, ON, Canada},
    series    = {PLOS'19}
}

@inproceedings{olivier2019,
    author    = {Olivier, Pierre and Chiba, Daniel and Lankes, Stefan and Min, Changwoo and Ravindran, Binoy},
    title     = {A Binary-Compatible Unikernel},
    year      = {2019},
    isbn      = {9781450360203},
    publisher = {Association for Computing Machinery},
    address   = {New York, NY, USA},
    url       = {https://doi.org/10.1145/3313808.3313817},
    doi       = {10.1145/3313808.3313817},
    abstract  = {Unikernels are minimal single-purpose virtual machines. They are highly popular in the research domain due to the benefits they provide. A barrier to their widespread adoption is the difficulty/impossibility to port existing applications to current unikernels. HermiTux is the first unikernel providing binary-compatibility with Linux applications. It is composed of a hypervisor and lightweight kernel layer emulating OS interfaces at load- and runtime in accordance with the Linux ABI. HermiTux relieves application developers from the burden of porting software, while providing unikernel benefits such as security through hardware-assisted virtualized isolation, swift boot time, and low disk/memory footprint. Fast system calls and kernel modularity are enabled through binary rewriting and analysis techniques, as well as shared library substitution. Compared to other unikernels, HermiTux boots faster and has a lower memory/disk footprint. We demonstrate that over a range of native C/C++/Fortran/Python Linux applications, HermiTux performs similarly to Linux in most cases: its performance overhead averages 3\% in memory- and compute-bound scenarios.},
    booktitle = {Proceedings of the 15th ACM SIGPLAN/SIGOPS International Conference on Virtual Execution Environments},
    pages     = {59–73},
    numpages  = {15},
    keywords  = {Unikernels, Binary Compatibility. Virtualization, Operating Systems, Linux Kernel},
    location  = {Providence, RI, USA},
    series    = {VEE 2019}
}

@inproceedings{lankes2017,
    author    = {Lankes, Stefan and Pickartz, Simon and Breitbart, Jens},
    editor    = {Knoop, Jens and Karl, Wolfgang and Schulz, Martin and Inoue, Koji and Pionteck, Thilo},
    title     = {A Low Noise Unikernel for Extrem-Scale Systems},
    booktitle = {Architecture of Computing Systems - ARCS 2017},
    year      = {2017},
    publisher = {Springer International Publishing},
    address   = {Cham},
    pages     = {73--84},
    abstract  = {We expect that the size and the complexity of future supercomputers will increase on their path to exascale systems and beyond. Therefore, system software has to adapt to the complexity of these systems to simplify the development of scalable applications. In cloud environments, the activity of a virtual machine on a neighboring core may decrease performance due to issues such as cache contamination (noise neighbor problem). In this paper, we present the unikernel operating system HermitCore coming up with predictable runtimes, which improves the scalability. It extends the multi-kernel approach with unikernel features while providing better programmability and scalability for hierarchical systems. In addition, the same binary can be used to run as unikernel within virtual machines. By using a unikernel, the memory footprint of Virtual Machines (VMs) is decreased, which reduces the pressure on the cache system and improves the overall performance. We prove the predictable runtime of the design via micro benchmarks by taking the example of HermitCore on the upcoming manycore architecture Knights Landing.},
    isbn      = {978-3-319-54999-6}
}

@inproceedings{lankes2016,
    author    = {Lankes, Stefan and Pickartz, Simon and Breitbart, Jens},
    title     = {HermitCore: A Unikernel for Extreme Scale Computing},
    year      = {2016},
    isbn      = {9781450343879},
    publisher = {Association for Computing Machinery},
    address   = {New York, NY, USA},
    url       = {https://doi.org/10.1145/2931088.2931093},
    doi       = {10.1145/2931088.2931093},
    abstract  = {We expect that the size and the complexity of future supercomputers will increase on their path to exascale systems and beyond. Therefore, system software has to adapt to the complexity of these systems for a simplification of the development of scalable applications. In this paper, we present a unikernel operating system design for HPC. It extends the multi-kernel approach while providing better programmability and scalability for hierarchical systems, such as HLRS' Hazel Hen, which base on multiple cluster-on-a-chip processors. We prove the scalability of the design via micro benchmarks by taking the example of HermitCore---our prototype implementation of the new design.},
    booktitle = {Proceedings of the 6th International Workshop on Runtime and Operating Systems for Supercomputers},
    articleno = {4},
    numpages  = {8},
    location  = {Kyoto, Japan},
    series    = {ROSS '16}
}
```

</details>

## Contribution

Hermit is being developed here, on [github.com/hermit-os](https://github.com/hermit-os).
Create your own fork, send us a pull request, and chat with us on [Zulip](https://hermit.zulipchat.com/).

## Acknowledgments

<p>
    <img src="https://media.githubusercontent.com/media/hermit-os/.github/main/profile/EN_fundedbyEU_VERTICAL_RGB_POS.png#gh-light-mode-only" height="250" alt="Funded by the European Union" />
    <img src="https://media.githubusercontent.com/media/hermit-os/.github/main/profile/EN_fundedbyEU_VERTICAL_RGB_NEG.png#gh-dark-mode-only" height="250" alt="Funded by the European Union" />
    <img src="https://media.githubusercontent.com/media/hermit-os/.github/main/profile/bmbf_internet_in_farbe_en.jpg" height="250" alt="Sponsored by the Federal Ministry of Education and Research" />
</p>
