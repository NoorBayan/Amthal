# Amthāl: A Dataset and Computational Model of the Qur’an’s Conceptual Universe

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
[![License: MIT](https://img.shields.io/badge/Code%20License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![License: CC BY 4.0](https://img.shields.io/badge/Data%20License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Status](https://img.shields.io/badge/Status-Under%20Peer%20Review-blue.svg)]() <!-- شارة اختيارية للإشارة إلى أن العمل قيد المراجعة -->

---

## About The Project

The **Amthal Project** provides the data and code for a large-scale computational analysis of the Qur'an's conceptual universe. This repository contains a new, richly annotated corpus of **4,078 figurative instances**, validated through a rigorous inter-coder reliability protocol, alongside a fully reproducible workflow for modeling the text's ideological architecture as a network. The provided scripts allow for the replication of our core finding: the structural centrality of the **PATH, POWER, and COGNITION** triad.

Grounded in the ethos of Open Science, this project makes all its scholarly products transparently available to facilitate verification and extension. A manuscript detailing the full theoretical and analytical findings is currently under peer review; a citation will be added upon its publication.

## Ethical Considerations & Usage Notice

The data and models in this repository engage with the Qur'an, a text of profound religious and cultural significance to communities worldwide. We have developed these resources with a commitment to scholarly accountability and methodological transparency. We ask that all users engage with them in a similar spirit.

We encourage responsible use aligned with ethical, respectful, and culturally sensitive research practices. We propose the following principles, drawn from critical data studies and digital humanities, as a guide for users:

-   **Data as Representation, Not Reality:** This dataset is a *model* of the Qur'an's figurative language, not the text itself. It is a form of *capta* (data actively constructed through scholarly judgment), not objective *data*. We urge users to avoid computational reductionism and to remember that any analysis of this data is an analysis of one specific, theoretically-grounded representation.

-   **Contextual and Cultural Sensitivity:** The meanings encoded in this dataset are deeply embedded in historical, theological, and linguistic contexts. We caution against making decontextualized or universalist claims. Any interpretation should acknowledge the rich exegetical traditions and interpretive communities that surround the Qur'an.

-   **Reflexivity and Positionality:** As researchers, our own backgrounds and theoretical commitments shape our work. We encourage users to reflect on their own positionality and how it influences their analysis and interpretation of these resources.

The computational models presented here are intended as **analytical tools, not as theological claims**. They are designed to reveal structural patterns to facilitate new scholarly questions, not to provide definitive answers or replace traditional hermeneutics. We invite users to engage with these resources in a spirit of critical inquiry and intellectual humility.


## Dataset & Documentation

At the core of this project is the **Amthal Corpus**, a new, richly annotated dataset of figurative language in the Qur'an. It serves as the empirical foundation for our computational analysis.

### Dataset Overview

-   **Content:** 4,078 manually annotated figurative instances.
-   **Annotation Depth:** 25+ fields covering conceptual, rhetorical, and affective dimensions.
-   **Validation:** Annotation quality was ensured via a formal Inter-Coder Reliability (ICR) protocol.
-   **Location:** The primary data files (`instances.csv`, `relations.csv`) are located in the `/data/processed/` directory.

### Comprehensive Documentation

For a complete understanding of the dataset and our methodological commitments, please refer to the following documents:

1.  **Datasheet:** Provides a high-level overview of the project's motivation, composition, ethical considerations, and recommended use cases. It is essential reading for anyone intending to use these resources.

    ➡️ **[Read the Full Datasheet for the Amthal Corpus](./data/datasheet.md)**

2.  **Codebook (Data Dictionary):** Offers a detailed, field-by-field description of the dataset, including all annotation categories, decision rules, and examples.

    ➡️ **[View the Full Codebook in `/data/README.md`](./data/README.md)**


## Reproducibility Summary

This project adheres to best practices for scientific reproducibility. We have taken the following steps to ensure our analysis is transparent and verifiable:

-   ✅ **All analysis scripts are provided** in the `/code/` directory.
-   ✅ **Random seeds are fixed** in stochastic processes (e.g., sampling) to ensure identical results.
-   ✅ **A complete environment file (`requirements.txt`) is included** for dependency management.
-   ✅ **A detailed codebook is provided** in `/data/README.md` to explain the dataset.
-   ✅ **The full analysis pipeline is documented**, with direct links to interactive notebooks.



## Reproducing the Analysis

Our entire analytical workflow is documented and executable across a series of focused, self-contained notebooks. Each notebook allows for the full replication of a specific analysis or visualization from our study.

You can run these notebooks locally after setting up the environment, or explore them interactively online using Google Colab. Below, we have organized the notebooks thematically to guide you through the different components of our research.

---

### 1. Core Network Construction & Structural Analysis

This set of notebooks focuses on building the Qur'an's conceptual network and analyzing its fundamental topological properties.

#### 1.1. Network Building & Visualization
| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Global Conceptual Network**          | Constructs and visualizes the main weighted co-occurrence network.                                | <a href="https://colab.research.google.com/drive/18e7N4VWuzkfjqKjO1gGyMKkg9NYQK_mc?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Network Adjacency Matrix Heatmap**   | Provides an alternative view of the network's structure by visualizing its adjacency matrix.        | <a href="https://colab.research.google.com/drive/1Ur2rGKgAYbWwAr2UUpPVJXrkasO8CTxt?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Top 15 Strongest Conceptual Pairings** | Creates a focused subgraph visualizing only the 15 most frequent co-occurrence links.             | <a href="https://colab.research.google.com/drive/1k9u9Ddkedisc0upYwu1El5zT7S_Ox3iM?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

#### 1.2. Centrality & Prominence
| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Top 10 Central Conceptual Domains**  | Calculates and tabulates the top 10 most influential concepts based on centrality scores.         | <a href="https://colab.research.google.com/drive/1SjOmwBSnV90Cbril4jPxpxU-gFzD8_IG?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Weighted Degree Centrality Distribution**| Plots the distribution of weighted degree scores to show the network's hierarchical structure.  | <a href="https://colab.research.google.com/drive/1OoXjektz4F9t_8tp4lano0eVwgz7EuAw?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Centrality vs. Textual Prominence**  | Creates a scatter plot comparing a concept's network role against its textual frequency.         | <a href="https://colab.research.google.com/drive/1FI2__lgj6CINr2dSw7eYAbighd_rnYX4?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

---

### 2. Community Structure & Thematic Analysis

These notebooks explore the network's thematic clusters, both algorithmically detected and predefined.

#### 2.1. Algorithmic Community Detection
| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Leiden Community Stability Analysis**| Runs the Leiden algorithm 100 times to find the most stable community partition.                  | <a href="https://colab.research.google.com/drive/1MAQF6EZPYRUuBgHjPIuTaLJNsV59otW9?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Leiden vs. Louvain Robustness Check**| Compares the stable Leiden partition against the Louvain algorithm to validate the structure.       | <a href="https://colab.research.google.com/drive/1Qcx_wyURaR5MGzcHz0fqp359vBg1ILb4?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Network Viz (Leiden Communities)**   | Visualizes the global network with nodes colored according to the stable Leiden partition.        | <a href="https://colab.research.google.com/drive/1FimBd_yUA0O8ver1DqXXUcoY__CEE6ih?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Network Viz (Louvain Communities)**  | Provides an alternative network visualization using the classic Louvain algorithm for comparison.   | <a href="https://colab.research.google.com/drive/1hqCniVSIwLr5fPV-GVoZakKX8gXKhzZY?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Sankey Diagram (Leiden)**            | Visualizes the flow of instances from concepts into the stable Leiden communities.                | <a href="https://colab.research.google.com/drive/19QqFNmU-5W--XD39zZrsSDXIE18s9zKD?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Sankey Diagram (Louvain)**           | Generates an alternative Sankey diagram based on the Louvain partition for comparative analysis.  | <a href="https://colab.research.google.com/drive/11JpMYz3Vo8sYmOJj23Xzr8tfKE2zQbix?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

#### 2.2. Predefined Thematic Analysis
| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Profiles of Predefined Communities** | Generates a detailed analytical table profiling a set of expert-defined thematic communities.     | <a href="https://colab.research.google.com/drive/1uAwbicpKNHp5JjJc8tZtkT_NuzGFrH7m?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Summary of Community Profiles**      | Creates a multi-panel figure summarizing the quantitative profiles of predefined communities.       | <a href="https://colab.research.google.com/drive/11LJfqwMCa5UFYxHPWihYLkm14Hdwvllu?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

---

### 3. Diachronic Analysis (Meccan vs. Medinan)

This series of notebooks conducts a comparative statistical analysis of conceptual distributions between the two revelation periods.

| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Conceptual Density Comparison**      | Visualizes diachronic shifts in the prominence of the top 12 conceptual domains.                  | <a href="https://colab.research.google.com/drive/1JQroowzd6VrlsM1dZskyHBMzskfhYsuN?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Rhetorical Function Comparison**     | Creates a heatmap showing the shifting distribution of rhetorical functions over time.              | <a href="https://colab.research.google.com/drive/1dA9tz3dX6UqYr_rXDLbLw95KxXWZQX46?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Abstraction Level Comparison**       | Compares the proportion of Concrete vs. Abstract metaphors between periods.                       | <a href="https://colab.research.google.com/drive/1sAW5ltlPx6e9EHt6XehUmhoDNczpHF1Z?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Affective Valence Comparison**       | Visualizes the shift in the text's overall affective tone between periods.                        | <a href="https://colab.research.google.com/drive/1OM8glIzf9roDtK9xOUo3lwutHJVsRHS8?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Standardized Residuals Analysis**    | Plots residuals from a Chi-squared test to identify significantly over/under-represented concepts.  | <a href="https://colab.research.google.com/drive/1KzA_1JDmu0ZPWTzKkOIWL2NmACPow_EN?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Qualitative Profiles of Shifting Concepts**| Provides a deep, qualitative analysis of the concepts that shift most significantly.            | <a href="https://colab.research.google.com/drive/1tb_Ll2GzbVx4bIHeuQ4_EtPvniifpG0S?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Summary Table of Shifting Concepts** | Generates a table detailing the concepts with statistically significant distributional shifts.      | <a href="https://colab.research.google.com/drive/1tfLzepOTp7lPEdwWpJ7-pbIqAlQ7oayN?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

---

### 4. Affective & Functional Analysis

These notebooks investigate the relationship between affective charge (valence) and rhetorical intent.

| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Valence-Function Association Heatmap**| Visualizes the statistical association between valence and function using standardized residuals.   | <a href="https://colab.research.google.com/drive/1PbHB6yiMmwpWChIMG48RO6RMKAz13L2J?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Valence-Function Bipartite Network** | Provides a network-based alternative to the heatmap for visualizing significant associations.       | <a href="https://colab.research.google.com/drive/1-XMqLwuaokf_n2PUCW-IrY26qZHP7K0j?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Top Valence-Function Associations Table**| Summarizes the strongest statistical pairings between affective valence and rhetorical function. | <a href="https://colab.research.google.com/drive/1k6h-XwNqksJsJ9tSlz6wkDslDoQBH1RO?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Valence Distribution by Function**   | Illustrates the affective profile of each rhetorical function using a stacked bar chart.        | <a href="https://colab.research.google.com/drive/1tTd0QufZZCASAjbNTrcM36E1HNVJ5ni1?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Valence Profile of Top Concepts**    | Creates a heatmap showing the distinct emotional signature of the most prominent concepts.        | <a href="https://colab.research.google.com/drive/16kecPstSvvI8fbmtAHzGREtF03RzGU3H?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

---

### 5. Supplementary & Foundational Analyses

This section contains notebooks for foundational analyses and the sensitivity checks discussed in the supplementary materials.

| Analysis / Visualization               | Description                                                                                       | Explore in Colab                                                                    |
| :------------------------------------- | :------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Conceptual Domain Frequency**        | Generates a bar chart showing the overall frequency distribution of all annotated concepts.       | <a href="https://colab.research.google.com/drive/1xr04aoh_J9cab2AVB7J_zyajgfg9mW6E?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Network Weighting Sensitivity Analysis**| Validates the robustness of centrality measures against different edge weighting schemes.       | <a href="https://colab.research.google.com/drive/1KvBk2ShdXqcbwbF_ltFooMuxw0Eng6ul?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |


### Local Execution

For users who prefer to run the analysis locally, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/NoorBayan/Amthal.git
    cd Amthal
    ```
2.  **Set up the environment:**
    Install the required packages using pip:
    ```bash
    pip install -r code/requirements.txt
    ```
3.  **Run the notebooks:**
    The Jupyter notebooks are located in the `/code/analysis/` directory.


## License

The entire content of this repository, including all data and source code, is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.

This means you are free to share, use, and adapt the materials for any purpose, provided you give appropriate credit to the original authors. For full details, please see the [LICENSE](LICENSE) file.


## Feedback, Contributions, and Contact

We welcome community feedback and contributions to this project.

The preferred method for all communication—including bug reports, questions, and suggestions—is to **[open an issue](https://github.com/NoorBayan/Amthal/issues)** on this GitHub repository. Using GitHub issues ensures that all discussions are transparent, tracked, and accessible to the entire community.

If you would like to contribute directly, please feel free to fork the repository and submit a pull request. We appreciate your engagement.


