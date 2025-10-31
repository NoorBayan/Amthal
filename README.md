# Amthāl: A Dataset and Computational Model of the Qur’an’s Conceptual Universe

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
[![License: MIT](https://img.shields.io/badge/Code%20License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![License: CC BY 4.0](https://img.shields.io/badge/Data%20License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Status](https://img.shields.io/badge/Status-Under%20Peer%20Review-blue.svg)]() <!-- شارة اختيارية للإشارة إلى أن العمل قيد المراجعة -->

---

## About The Project

The **Amthal Project** provides the data and code for a large-scale computational analysis of the Qur'an's conceptual universe. This repository contains a new, richly annotated corpus of **4,078 figurative instances**, validated through a rigorous inter-coder reliability protocol, alongside a fully reproducible workflow for modeling the text's ideological architecture as a network. The provided scripts allow for the replication of our core finding: the structural centrality of the **PATH, POWER, and COGNITION** triad.

Grounded in the ethos of Open Science, this project makes all its scholarly products transparently available to facilitate verification and extension. A manuscript detailing the full theoretical and analytical findings is currently under peer review; a citation will be added upon its publication.


## Dataset Overview: The Amthal Corpus

At the core of this project is the **Amthal Corpus**, a new, richly annotated dataset of figurative language in the Qur'an. It was developed to serve as a high-quality empirical foundation for computational and humanistic research.

### Key Features

-   **Comprehensive Scope:** Contains **4,078 manually annotated figurative instances** (metaphors, similes, metonymy, etc.) covering the entire Qur'anic text.
-   **Multi-Dimensional Annotation:** Each instance is described across **25+ analytical fields**, capturing its conceptual source domain, rhetorical function, affective valence, and contextual properties.
-   **Rigorous Validation:** The dataset's annotation schema was developed and refined through a collaborative, multi-annotator process and validated with a formal Inter-Coder Reliability (ICR) protocol to ensure high consistency.

### Data Files

The dataset is provided in two primary CSV files (UTF-8 encoded) located in the `/data/processed/` directory:

-   `instances.csv`: The main table where each row represents a single figurative instance.
-   `relations.csv`: A supplementary table modeling the relationships between instances that co-occur within the same verse.

### Full Documentation (Codebook)

A complete data dictionary, including detailed descriptions of all fields, decision rules, and illustrative examples, is available in the dedicated README file within the data directory.

➡️ **[View the Full Codebook in `/data/README.md`](./data/README.md)**


## Reproducing the Analysis

Our entire analytical workflow is transparent and reproducible. We provide Jupyter notebooks that can be run locally or explored interactively online using Google Colab. The notebooks are designed to process the provided dataset in `/data/processed/` and generate the primary analytical outputs.

The table below outlines the key components of our analysis and provides direct links to the corresponding code.

<table>
  <thead>
    <tr>
      <th align="left"><b>Analytical Component</b></th>
      <th align="left"><b>Description</b></th>
      <th align="left"><b>Explore in Colab</b></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top"><strong>1. Network Construction & Centrality Analysis</strong></td>
      <td valign="top">This notebook builds the conceptual co-occurrence network from the Amthal Corpus. It applies the edge weighting scheme, calculates key centrality metrics (Degree, Betweenness), and performs the sensitivity analysis across different weighting models.</td>
      <td valign="top">
        <a href="<YOUR_COLAB_LINK_FOR_NETWORK_ANALYSIS>">
          <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
        </a>
      </td>
    </tr>
    <tr>
      <td valign="top"><strong>2. Community Detection & Thematic Clustering</strong></td>
      <td valign="top">Implements the Leiden algorithm to partition the network into thematic communities ("metaphorical ecologies"). This notebook also visualizes the final network structure, highlighting the identified clusters and their relationships.</td>
      <td valign="top">
        <a href="<YOUR_COLAB_LINK_FOR_COMMUNITY_DETECTION>">
          <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
        </a>
      </td>
    </tr>
    <tr>
      <td valign="top"><strong>3. Diachronic & Functional Statistical Analysis</strong></td>
      <td valign="top">Contains the code for the statistical tests. This includes the Chi-squared analysis for comparing conceptual distributions across revelation periods (Meccan/Medinan) and the G-test for assessing the association between affective valence and rhetorical function.</td>
      <td valign="top">
        <a href="<YOUR_COLAB_LINK_FOR_STATS_TESTS>">
          <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
        </a>
      </td>
    </tr>
  </tbody>
</table>

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


