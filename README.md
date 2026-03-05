# Gene Regulatory Network Inference Evaluation – DREAM5 Network 3

This repository contains the **R and Python scripts used in the evaluation of gene regulatory network (GRN) inference methods** presented in our study. The analysis focuses on comparing individual methods and consensus strategies using the benchmark dataset from the **DREAM5 Challenge**, specifically **Network 3 (E. coli)**.

The repository aims to support **reproducibility of the experiments** described in the manuscript by providing scripts used for data preprocessing, network inference aggregation, and performance evaluation.

---

## Overview

Gene regulatory network inference aims to reconstruct regulatory interactions between genes from gene expression data. Several computational methods have been proposed for this task, each relying on different statistical or information-theoretic approaches.

In this study we evaluate:

* **Individual inference methods**
* **Consensus networks** derived from multiple methods
* Performance against the **reference network provided in the DREAM5 challenge**

The evaluation investigates how combining predictions from different algorithms may improve the identification of true regulatory interactions.

---

## Dataset

The analyses use the benchmark dataset from the **DREAM5 Network Inference Challenge**.

* **Network:** Network 3
* **Organism:** *Escherichia coli*
* **Data type:** Gene expression data
* **Reference network:** Gold standard regulatory interactions provided by the challenge

More information about the challenge can be found here:

[https://dreamchallenges.org/dream5-network-inference-challenge/](https://dreamchallenges.org/dream5-network-inference-challenge/)

---

## Repository Structure

```
.
├── data/              # Input datasets and reference networks
├── scripts/           # R and Python scripts used in the analysis
├── results/           # Generated outputs and evaluation results
├── figures/           # Plots and visualizations produced in the study
└── README.md          # Repository documentation
```

Typical tasks implemented in the scripts include:

* Loading and preprocessing expression datasets
* Integrating results from multiple inference methods
* Generating consensus networks
* Comparing predicted edges with the DREAM5 gold standard
* Computing evaluation metrics

---

## Methods Evaluated

The repository includes scripts used to analyze results produced by multiple GRN inference methods. These methods are evaluated:

1. **Individually**, considering the network inferred by each method
2. **Collectively**, through consensus approaches that combine predictions from several methods

Consensus strategies consider the frequency with which regulatory interactions are predicted across methods.

---

## Evaluation Strategy

Predicted regulatory interactions were compared against the DREAM5 gold standard network.

Edges were categorized according to their occurrence across inference methods:

* **Found edges**
  Regulatory interactions identified by one or more inference methods.

* **Low prediction edges**
  Interactions predicted by very few methods.

* **Not found edges**
  Interactions present in the reference network but not predicted by any evaluated method.

These categories were used to further analyze functional enrichment and biological relevance.

---

## Requirements

The scripts were developed using **R** and **Python**.

### R dependencies

Typical packages used in the analysis include:

* `tidyverse`
* `data.table`
* `igraph`
* `ggplot2`
* `UpSetR`

### Python dependencies

Typical libraries include:

* `pandas`
* `numpy`
* `networkx`
* `matplotlib`

---

## Citation

```
Costa-Silva J., Barbosa M., Paschoal A. R., et al.
[[Inference of gene regulatory networks: a study for the identification and characterisation of gene relationships]
[BMC Bioinformatics], [2026].
```

---

## License

This repository is provided for **academic and research purposes**.
Please refer to the LICENSE file for details.

---

## Contact

For questions regarding the scripts or the analyses:

**Juliana Costa-Silva**
Email: [julianacostasilvati@gmail.com](mailto:julianacostasilvati@gmail.com)
