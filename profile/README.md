![FaMAF CVA6 Project](https://raw.githubusercontent.com/FaMAF-CVA6-Project/CVA6/master/assets/FaMAF_CVA6_header.svg)

Tools for looking inside a RISC-V processor, one cycle at a time.

![A CVA6 pipeline rendered by CVA6Flow](https://raw.githubusercontent.com/FaMAF-CVA6-Project/CVA6Flow/main/docs/CVA6Flow_intro.png)

This organisation collects the work of an undergraduate thesis at [FaMAF](https://www.famaf.unc.edu.ar/), Universidad Nacional de Córdoba. The central question: how closely can a fast, tractable simulator (gem5's MinorCPU) be configured to behave like a real RISC-V core (the CORE-V CVA6), and can we see the difference cycle by cycle?

Answering it takes a gem5 configuration matched to the CVA6 RTL, and three pipeline viewers built to look and behave the same way: one for each side, and one that places the two pipelines side by side.

## New here?

Start with the [CVA6 repository](https://github.com/FaMAF-CVA6-Project/CVA6#readme) for setup and how to run everything, or try a viewer in the browser with its sample runs: [MinorFlow](https://famaf-cva6-project.github.io/MinorFlow/) and [CVA6Flow](https://famaf-cva6-project.github.io/CVA6Flow/).

## Repositories

- **[MinorFlow](https://github.com/FaMAF-CVA6-Project/MinorFlow)**: a browser-based pipeline visualiser for gem5's MinorCPU, reconstructing the pipeline from gem5 debug traces.
- **[CVA6Flow](https://github.com/FaMAF-CVA6-Project/CVA6Flow)**: the RTL sibling, a visualiser for the CORE-V CVA6 core simulated in Verilator, reconstructed from raw VCD signals. Every metric traces back to an actual RTL signal.
- **[CVA6](https://github.com/FaMAF-CVA6-Project/CVA6)**: the fork of [openhwgroup/cva6](https://github.com/openhwgroup/cva6) used as the reference core. It also holds the gem5 configuration matched to it, the benchmarks both sides run, FlowCompare, which shows the two pipelines side by side, and the recipes for the two Docker images.

Both viewers are single, dependency-free HTML files with a streaming Python tracer, so there is nothing to install to read a run. To produce your own, the two images carry the whole toolchain, ready built: [manuel313/famaf_cva6](https://hub.docker.com/r/manuel313/famaf_cva6) and [manuel313/famaf_gem5](https://hub.docker.com/r/manuel313/famaf_gem5).

## Context

MinorFlow is the subject of a paper accepted and presented at CARLA 2026, the Latin America High Performance Computing Conference, held in Córdoba, Argentina. It is awaiting publication in the conference proceedings, in Springer's _Communications in Computer and Information Science_ series.

## Authors

Manuel Nieto, Francisco Cortez Casini, María Delfina Vélez Ibarra and Gonzalo Tomás Vodanovic, at FaMAF, Universidad Nacional de Córdoba.
