# LASER

LASER (Light Agent Spatial modeling for ERadication) is a high-performance, agent-based simulation framework for modeling the spread of infectious diseases to better inform policy decisions. It supports spatial structure, age demographics, and modular disease logic using Python-based components. LASER can also be configured to run as a compartmental model. LASER is freely available for use under the MIT license and community contributions are welcome.

## Design principles

The philosophy driving the development of LASER was to create a framework that was flexible, powerful, and fast, able to tackle a variety of complex modeling scenarios. But complexity often slows performance, and not every modeling question requires a full suite of model features.

To solve this, we designed LASER as a set of core components with fundamental features that could be added—or not—to build working models. You can optimize performance using only the components necessary for your modeling questions. This building-block framework enables parsimony in model design, but also facilitates the building of powerful models with bespoke, complex dynamics.

LASER's core principles are as follows:

<div class="grid cards" markdown>

-   :octicons-cpu-16:{ .lg .middle } __Efficient computation__

    ---

    Preallocated memory, fixed-size arrays, sequential array access, and cache-friendly operations enable the simulation of millions of agents.

-   :material-vector-square-plus:{ .lg .middle } __Modular design__

    ---

    Define properties and add modular components (step functions) that run each timestep. Use only the components needed to answer your specific questions.

-   :material-map:{ .lg .middle } __Spatial focus__

    ---

    Simulate spatial dynamics using agents that belong to patches (nodes), with migration modules (gravity, radiation, Stouffer’s rank, etc.) for multi-patch models.

-   :material-rocket-launch:{ .lg .middle } __Fast and flexible__

    ---

    Models can be progressively optimized using NumPy, Numba, or even C/OpenMP for fast performance.

</div>

## Available packages

LASER provides functionality for modeling different modes of transmission and disease dynamics in different Python
packages. The following packages are currently available:


<div class="grid cards" markdown>

-   :material-web:{ .lg .middle } __laser-generic__

    ---

    laser-generic is a flexible, modular framework designed to simulate non-vector disease transmission. You can use laser-generic modules to create anything from simple compartmental models to more complex agent-based models with spatial dynamics. The laser-generic docs includes API reference for laser-core, the package that contains the engine and utilities used by all LASER packages.

    [:octicons-arrow-right-24: laser-generic](https://laser.idmod.org/laser-generic)

-   :material-emoticon-sick-outline:{ .lg .middle } __laser-measles__

    ---

    laser-measles is a spatial epidemiological modeling toolkit that helps researchers and public health teams simulate measles transmission, evaluate vaccination strategies, and plan outbreak responses. It translates surveillance data and demographic information into projections that inform immunization planning and resource allocation—with a focus on settings where measles remains a leading cause of vaccine-preventable death.

    [:octicons-arrow-right-24: laser-measles](https://laser.idmod.org/laser-measles)

</div>

## Get started

If you build, calibrate, or extend LASER models, these are the entry points:

<div class="grid cards" markdown>

-   :material-book-open-variant:{ .lg .middle } __Documentation__

    ---

    The documentation for laser-generic, including API reference for both laser-generic and laser-core.

    [:octicons-arrow-right-24: Docs](https://laser.idmod.org/laser-generic/get-started/)

-   :material-school:{ .lg .middle } __Tutorials__

    ---

    Step-by-step tutorials for getting started with LASER.

    [:octicons-arrow-right-24: Tutorials](https://laser.idmod.org/laser-generic/tutorials/)

-   :material-github:{ .lg .middle } __Source code__

    ---

    The LASER organization on GitHub, with source code for all models.

    [:octicons-arrow-right-24: Code](https://github.com/laser-base)

-   :material-source-merge:{ .lg .middle } __Contributing__

    ---

    Guidelines for those who want to contribute to LASER development.

    [:octicons-arrow-right-24: Contributing](https://laser.idmod.org/laser-generic/contribute/)

</div>

## Upcoming features

Following the initial 1.0 release of LASER in late 2025, we are focused on developing the following features:

- Improvements to speed and user experience
- Technical foundations to accelerate high-fidelity epidemiological modeling
- Advanced demographics and spatial support
- Utility functions for LaserFrames
- Broader AI support
- Documentation and tutorial updates
- Analysis and calibration functions
- Reference models and metapopulation modeling (MPM) support
- Models for polio and cholera simulation

See what's new for [laser-generic](https://laser.idmod.org/laser-generic/whatsnew/) and [laser-measles](https://laser.idmod.org/laser-measles/whatsnew/).
