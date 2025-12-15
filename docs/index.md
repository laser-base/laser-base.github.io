# LASER model documentation

LASER (Light Agent Spatial modeling for ERadication) is a high-performance, agent-based simulation framework for modeling the spread of infectious diseases. It supports spatial structure, age demographics, and modular disease logic using Python-based components.

The philosophy driving the development of LASER was to create a framework that was flexible, powerful, and fast, able to tackle a variety of complex modeling scenarios without sacrificing performance. But complexity often slows performance, and not every modeling question requires a full suite of model features. To solve this problem, LASER was designed as a set of core components, each with fundamental features that could be added—or not—to build working models. Users can optimize performance by creating models tailored to their research needs, only using components necessary for their modeling question. This building-block framework enables parsimony in model design, but also facilitates the building of powerful models with bespoke, complex dynamics.

LASER's core principles can be summarized as follows:

- **Efficient computation**: preallocated memory, fixed-size arrays, sequential array access, and cache-friendly operations.
- **Modular design**: users define properties and add modular **components** (step functions) that run each timestep.
- **Fast**: models can be progressively optimized using **NumPy**, **Numba**, or even C/OpenMP for performance.
- **Spatial focus**: agents belong to patches (nodes), with migration modules (gravity, radiation, Stouffer’s rank, etc.) for multi-patch models.

## Available packages

LASER provides functionality for modeling different modes of transmission and disease dynamics in different Python
packages. The following packages are currently available:


<div class="grid cards" markdown>

-   :octicons-globe-16:{ .lg .middle } __laser-generic__

    ---

    The laser-generic framework is designed to be flexible and is composed of modular components that can be used to create custom epidemiological models. For those who want to explore disease dynamics without the need to code from scratch, the framework includes epidemiological components that are designed model diseases with non-vector transmission dynamics. These modules can be used to create anything from simple compartmental models to more complex agent-based models with spatial dynamics. This documentation also includes API reference for laser-core, the package that contains the engine and utilities used by all LASER packages.

    [:octicons-arrow-right-24: laser-generic](https://laser.idmod.org/laser-generic)
</div>



