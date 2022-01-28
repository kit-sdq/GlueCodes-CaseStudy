## GlueCodes - Analyzing the Confidentiality of BWUniCluster 2.0

This repository contains all files to analyze the confidentiality of the [BWUniCluster](https://www.bwhpc.de/) based on architectural modeling.
In non-trivial software systems, multiple components are often glued together using small code snippets: *Glue Code*.
To analyze the confidentiality of such architectures with [Palladio](https://www.palladio-simulator.com/), we applied a [data flow-based analysis](https://publikationen.bibliothek.kit.edu/1000139064).

### Getting started

This repository contains all model files to run the analysis. For getting started, follow these steps:

1. Download and install [Eclipse Modeling Tools 2021-12](https://www.eclipse.org/downloads/packages/release/2021-12/r/eclipse-modeling-tools).
2. Use the included `install.p2f` to install all required software in Eclipse
3. Clone or download this repository, e.g., by using the git CLI: `git clone https://github.com/kit-sdq/GlueCodes-CaseStudy.git`
4. Import the downloaded folder as existing project in Eclipse
5. To run the analysis, create a new `PCM Confidentiality (DSL)` run configuration and select the included files

### Model summary

The modeling is based on Palladio with data flow-specific annotations, e.g., data operations and characteristics.
The model is based on publicly available information, e.g., the [architecture description](https://wiki.bwhpc.de/e/BwUniCluster_2.0_Hardware_and_Architecture).
We modeled the different types of nodes (login nodes, admin nodes, file server nodes) as resources and allocated multiple components that provide user and admin services.
We analyzed several documented data flow constraints such as user authentication and access restriction to internal nodes.
See `query.DCPDSL` for details.