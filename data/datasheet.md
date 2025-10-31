# Datasheet for the Amthal Corpus

This document provides a detailed overview of the Amthal Corpus, a dataset of conceptual metaphors in the Qur'an. It follows the principles of Datasheets for Datasets [1] to ensure transparency and accountability.

**Version:** 1.0  
**Last Updated:** [Date of last update]

---

## 1. Motivation

**For what purpose was the dataset created?**

The Amthal Corpus was created to address a significant gap in the computational study of sacred texts: the lack of large-scale, empirically grounded resources for analyzing figurative language. The primary motivations were:

*   To provide the first comprehensive, machine-readable map of the Qur'an's conceptual metaphor system.
*   To enable systematic, reproducible research into the ideological and rhetorical structures of a foundational cultural text.
*   To create a high-quality benchmark dataset for developing and evaluating Natural Language Processing (NLP) tools for classical Arabic, particularly in the area of metaphor detection and interpretation.
*   To serve as a case study for accountable and reflexive data creation practices in the digital humanities.

**Who created the dataset and on behalf of which entity?**

The dataset was created by the authors of the associated research paper: Badriyya B. Al-onazi, Wadee A. Nashir, Anoud A. Alhamad, and Reema G. Al-anazi, affiliated with Princess Nourah bint Abdulrahman University and Digital Dhad Experts.

---

## 2. Composition

**What do the instances that comprise the dataset represent?**

Each instance in the primary table (`instances.csv`) represents a single figurative expression (metaphor, simile, metonymy, etc.) identified within the Qur'anic text. The dataset is designed to capture not only the textual snippet but also its deeper conceptual, functional, and affective layers.

**How many instances are there in the dataset?**

The corpus contains **4,078** unique instances.

**What data does each instance consist of?**

Each instance is described by **27 fields**, organized into five thematic groups:
1.  **Identification & Location:** `Instance_ID`, `Sura_No`, `Aya_No`, etc.
2.  **Extraction & Classification:** `Snippet`, `Keywords`, `Figure_Type`.
3.  **Conceptual Abstraction:** `Dominant_Concept`, `Child_Concept`, `Core_Concept_Pair`.
4.  **Analytical & Interpretive:** `Rhetorical_Function`, `Valence`, `Dominance_Score`.
5.  **Annotation Metadata:** `Hierarchy`, `Ambiguity_Flag`.

A complete description of each field is available in the **[Codebook](./data/README.md)**.

**What is the source of the data?**

The textual basis is the Uthmanic standard text from the Tanzil Project (version 1.0.2), which is widely recognized for its orthographic accuracy in computational Qur'anic studies.

---

## 3. Collection & Annotation Process

**How was the data collected?**

The data was collected through a manual, expert-driven annotation process. The entire Qur'anic text was systematically read by a team of researchers to identify and extract all instances of the targeted figurative language types.

**Who annotated the data?**

The annotation was performed by a team of trained researchers with expertise in Arabic linguistics, classical rhetoric, and Qur'anic studies.

**What was the annotation process?**

The annotation followed a multi-stage protocol:
1.  **Codebook Development:** An initial annotation schema was developed based on Conceptual Metaphor Theory and classical Arabic rhetorical theory. This schema was iteratively refined through pilot annotation rounds.
2.  **Independent Annotation:** A stratified random sample of the corpus (≈15%, 612 instances) was independently annotated by two core team members.
3.  **Inter-Coder Reliability (ICR) Testing:** The consistency of annotations was measured using Cohen’s Kappa. The high agreement score confirmed the robustness of the annotation schema.
4.  **Adjudication:** All disagreements were resolved through a documented, multi-stage adjudication protocol. These discussions were used to refine the codebook and establish clear precedents for ambiguous "boundary cases." Anonymized examples are available in the `adjudication_logs/` directory.

---

## 4. Biases, Risks, and Limitations

This dataset is a scholarly product and, like all data, contains inherent biases and limitations. Users should be aware of the following:

*   **Interpretive Bias:** The annotations represent one systematic, theoretically-grounded interpretation of the Qur'an's figurative language. They are a form of scholarly *capta* and should not be treated as an objective or final "ground truth." Other valid interpretations are possible.
*   **Textual Bias:** The corpus is based exclusively on the standard Uthmanic *rasm* (Hafs an Asim recitation). It does not account for the textual variations present in other canonical Qur'anic readings (*qira'at*), which could influence the interpretation of certain passages.
*   **Granularity Limitation:** The primary unit of analysis for relationships is the verse (*aya*). This co-occurrence model may not capture longer-range narrative or rhetorical connections that span multiple verses.
*   **Categorical Abstraction:** The `Dominant_Concept` field simplifies complex imagery into one of 21 predefined categories. This act of reductionism, while necessary for computational analysis, inevitably loses some of the original nuance.

---

## 5. Recommended Usage

**What are the recommended use cases for this dataset?**

*   **Academic Research:** For computational linguistics, digital humanities, and Islamic studies research, particularly in areas of computational rhetoric, semantic network analysis, and Conceptual Metaphor Theory.
*   **NLP Model Training & Evaluation:** As a benchmark dataset for training and evaluating NLP models for tasks such as metaphor detection, classification, and sentiment analysis in classical Arabic.
*   **Educational Purposes:** As a resource for teaching advanced concepts in Arabic linguistics, rhetoric, and digital text analysis.

**What are the uses that are NOT recommended?**

This dataset is **NOT intended for**:

*   **Theological or Juridical Rulings:** The annotations are for linguistic and rhetorical analysis only and should not be used as a basis for deriving religious doctrine, law (*fiqh*), or theological claims.
*   **Automated Generation of Sacred Text:** Training generative AI models to produce text that mimics the style of the Qur'an is a misuse of this data and is strongly discouraged due to profound ethical and religious sensitivities.
*   **Decontextualized Analysis:** Drawing conclusions from the data without reference to the broader Qur'anic context and the rich tradition of Islamic exegesis (*tafsir*) can lead to misleading or inaccurate interpretations.
*   **Promoting Hate Speech or Misinformation:** Using the data to support Islamophobic narratives, sectarian arguments, or any form of hate speech is a direct violation of the intended scholarly purpose of this work.

---
**[1]** Gebru, T., Morgenstern, J., Vecchione, B., Vaughan, J. W., Wallach, H., Daumé III, H., & Crawford, K. (2021). Datasheets for datasets. *Communications of the ACM, 64*(12), 86-92.
