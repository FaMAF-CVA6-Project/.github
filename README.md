# FaMAF CVA6 Project

Tools for looking inside a RISC-V processor, one cycle at a time.

![A CVA6 pipeline rendered by CVA6Flow](https://raw.githubusercontent.com/FaMAF-CVA6-Project/CVA6Flow/main/docs/CVA6Flow_intro.png)

This organisation collects the work of an undergraduate thesis at [FaMAF](https://www.famaf.unc.edu.ar/), Universidad Nacional de Córdoba. The central question: how closely can a fast, tractable simulator (gem5's MinorCPU) be configured to behave like a real RISC-V core (the CORE-V CVA6), and can we see the difference cycle by cycle?

Answering it takes two pipeline visualisers, one for each side, built to look and behave the same way so the two pipelines can be placed side by side.

## Repositories

- **[MinorFlow](https://github.com/FaMAF-CVA6-Project/MinorFlow)** — a browser-based pipeline visualiser for gem5's MinorCPU, reconstructing the pipeline from gem5 debug traces.
- **[CVA6Flow](https://github.com/FaMAF-CVA6-Project/CVA6Flow)** — the RTL sibling, a visualiser for the CORE-V CVA6 core simulated in Verilator, reconstructed from raw VCD signals. Every metric traces back to an actual RTL signal.
- **[CVA6](https://github.com/FaMAF-CVA6-Project/CVA6)** — the fork of [openhwgroup/cva6](https://github.com/openhwgroup/cva6) used as the reference core for this work.

Both visualisers are single, dependency-free HTML files with a streaming Python tracer. There is nothing to install.

## Context

MinorFlow is the subject of a paper accepted to a workshop at CARLA 2026, the Latin America High Performance Computing Conference, held in Córdoba, Argentina.

## Authors

Manuel Nieto, Francisco Cortez Casini, María Delfina Vélez Ibarra and Gonzalo Tomás Vodanovich, at FaMAF, Universidad Nacional de Córdoba.
