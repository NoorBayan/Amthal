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

Our entire analytical workflow is transparent and reproducible. We provide Jupyter notebooks that can be run locally or explored interactively online using Google Colab. The notebooks are designed to process the provided dataset in `/data/processed/` and generate the primary analytical outputs.

The table below outlines the key components of our analysis and provides direct links to the corresponding code.

## Reproducing the Analysis

Our entire analytical workflow is documented and executable across a series of focused notebooks. Each notebook is designed to be self-contained and allows for the full replication of a specific analysis or visualization. You can run these notebooks locally after setting up the environment, or explore them interactively online using Google Colab.

Below, we have organized the notebooks thematically to guide you through our research components.

---

### 1. Network Architecture & Community Structure

These notebooks focus on constructing the Qur'an's conceptual network and analyzing its core structural properties.

| Analysis / Visualization                          | Description                                                                                             | Explore in Colab                                                                    |
| :------------------------------------------------ | :------------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Global Conceptual Network**                     | Constructs and visualizes the main weighted co-occurrence network.                                      | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Top 10 Central Conceptual Domains**             | Calculates degree and betweenness centrality to identify and rank the network's most influential nodes. | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Centrality vs. Textual Prominence**             | Creates a scatter plot comparing a concept's network centrality against its frequency in the text.      | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Community Profiles in the Network**             | Implements the Leiden algorithm to detect thematic communities and describes their conceptual makeup.   | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Distribution into Thematic Communities**        | Visualizes how the 4,078 instances are distributed across the identified communities.                   | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Network Robustness to Node Removal**            | Simulates targeted attacks on central nodes to measure the network's structural resilience.             | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

---

### 2. Diachronic Analysis (Meccan vs. Medinan Periods)

These notebooks conduct the comparative statistical analysis between the two revelation periods.

| Analysis / Visualization                          | Description                                                                                             | Explore in Colab                                                                    |
| :------------------------------------------------ | :------------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Comparative Density of Top 12 Domains**         | Generates a bar chart comparing the relative frequency of the most common concepts across periods.      | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Distribution of Rhetorical Functions**          | Visualizes how the usage of rhetorical functions (Promise, Warning, etc.) shifts between periods.     | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Distribution of Abstraction Level**             | Compares the use of concrete vs. abstract source domains in Meccan and Medinan revelations.            | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Key Domains with Significant Shifts**           | Performs a Chi-squared test to identify concepts whose distribution changes significantly over time.      | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
| **Standardized Residuals (Overall Comparison)**   | Calculates and plots standardized residuals for all concepts to show which are over/under-represented in each period. | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
| **Standardized Residuals (In-depth Profiles)**    | Provides a multi-panel deep dive into the *significantly shifting concepts*, analyzing their valence, function, and abstraction profiles. | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|

---

### 3. Affective & Rhetorical Functional Analysis

These notebooks investigate the relationship between affective charge (valence) and persuasive intent.

| Analysis / Visualization                          | Description                                                                                             | Explore in Colab                                                                    |
| :------------------------------------------------ | :------------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| **Valence Distribution**                          | Creates a summary visualization of the overall distribution of Positive, Negative, and Neutral valence. | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
| **Valence Profile of Top 12 Concepts**            | Shows the affective profile (dominant valence) for each of the most central conceptual domains.         | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
| **Association (Valence & Rhetorical Function)**   | Conducts the G-test to assess the statistical association between affective valence and function.       | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
| **Stacked Bar Chart of Valence Distribution**     | Visualizes how valence is distributed within each rhetorical function, providing a detailed view.       | <a href="<YOUR_LINK_HERE>"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|

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


