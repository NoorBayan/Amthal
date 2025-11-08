# 📘 Qur’anic Figurative Language Codebook
*Version 1.0 — 2025*

> This Codebook provides a comprehensive, field-by-field documentation of the dataset  
> **“Qur’anic Figurative Language Instances”**, a manually annotated corpus of 4,000+ figurative expressions  
> classified by rhetorical, conceptual, and interpretive dimensions.

---

## 🧭 Overview

Each row in the dataset (`instances.csv`) represents one figurative instance drawn from the Qur’an.  
The fields are grouped into **five thematic categories** and cross-referenced through bilingual (Arabic–English) dictionaries stored in `/data/dictionaries/`.

---

## 1. 🆔 Identification & Location Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Instance_ID` | Unique integer serving as primary key. | `1023` | Unique integer |
| `Sura_No` | Chapter number in the Qur’an. | `2` | `1–114` |
| `Aya_No` | Verse number within the sura. | `255` | Integer |
| `vers_text` | Full Arabic text of the verse. | `اللَّهُ لَا إِلَٰهَ إِلَّا هُوَ الْحَيُّ الْقَيُّومُ...` | Arabic string |
| `Revelation_Phase` | Historical phase of revelation. | `Meccan` | `Meccan`, `Medinan` |

---

## 2. ✂️ Extraction & Classification Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Snippet` | Arabic phrase forming the figurative expression. | `وَسِعَ كُرْسِيُّهُ السَّمَاوَاتِ وَالْأَرْضَ` | Arabic string |
| `Keywords` | Comma-separated Arabic terms from context. | `كرسي، السماوات، الأرض` | List of Arabic words |
| `Figure_Type` | Classical rhetorical figure type. | `Metaphor` | `Metaphor`, `Simile`, `Metonymy`, `Figurative Expression` (`|` for multiple) |

---

## 3. 🧩 Conceptual Abstraction Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Dominant_Concept` | Parent conceptual domain. | `Light` | 21 controlled domains (e.g., Light, Darkness, Path, Power) |
| `Child_Concept` | Sub-domain linked to the parent concept. | `Guidance` | Domain-specific subcategory |
| `Core_Concept_Pair` | Source-to-target mapping of the metaphor. | `LIGHT→GUIDANCE` | `SOURCE→TARGET` |

---

## 4. 🧠 Analytical & Interpretive Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Rhetorical_Function` | Pragmatic or persuasive purpose of the image. | `Promise` | `Promise`, `Warning`, `Argumentation`, `Illustration`, `Glorification`, `Gratitude` |
| `Valence` | Affective or evaluative polarity. | `Positive` | `Positive`, `Negative`, `Neutral` |
| `Dominance_Score` | Centrality of instance to verse meaning (1–5). | `4` | `1–5` |
| `Abstraction_Level` | Perceptual vs conceptual nature of imagery. | `Concrete` | `Concrete`, `Abstract` |
| `Target_Audience` | Primary intended audience in discourse. | `Believers` | `Believers`, `Disbelievers`, `Hypocrites`, `People of the Book`, `General` |
| `Image_Source_Type` | Domain from which the image originates. | `Natural` | 15 domains (Natural, Artifactual, Somatic, Auditory, Spatial, Temporal, Quantitative, Mathematical, Social, Cognitive, Mental, Conceptual, Abstract, Existential, Supernatural) |
| `Semantic_Implication` | Cognitive or emotional impact intended. | `Awe\|Certainty` | Controlled list, multi-valued (`|`-separated) |

---

## 5. 🧾 Annotation Metadata Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Hierarchy` | Indicates primary or secondary figure in verse. | `Primary` | `Primary`, `Secondary` |
| `Ambiguity_Flag` | Confidence level of the annotator. | `Clear` | `Clear`, `Ambiguous` |

---

## 6. 📚 Controlled Dictionaries

| **Dictionary** | **File Path** | **Description** | **Entries** |
|----------------|---------------|----------------|-------------|
| Concept Domains | `Dominant_Concept_dic.json` | 21 conceptual domains | 21 |
| Rhetorical Functions | `Rhetorical_Function_dic.json` | 9 rhetorical categories | 9 |
| Image Sources | `Image_Source_Type_dic.json` | Domains of figurative imagery | 15 |
| Valence | `Valence_dic.json` | Polarity encoding | 3 |
| Revelation Phase | `Revelation_Phase_dic.json` | Meccan / Medinan | 2 |
| Hierarchy | `Hierarchy_dic.json` | Primary / Secondary | 2 |
| Ambiguity Flag | `Ambiguity_Flag_dic.json` | Confidence flag | 2 |

---

## 7. 🧩 Example Entry

| **Field** | **Value** |
|------------|-----------|
| `Instance_ID` | 3738 |
| `Sura_No` | 66 |
| `Aya_No` | 12 |
| `vers_text` | وَمَرْيَمَ ٱبْنَتَ عِمْرَانَ ٱلَّتِىٓ أَحْصَنَتْ فَرْجَهَا... |
| `Snippet` | ٱلَّتِىٓ أَحْصَنَتْ فَرْجَهَا *(She who guarded her chastity)* |
| `Dominant_Concept` | Power |
| `Figure_Type` | Metaphor |
| `Rhetorical_Function` | Glorification |
| `Valence` | Positive |
| `Abstraction_Level` | Concrete |
| `Target_Audience` | Believers |
| `Image_Source_Type` | Somatic |
| `Semantic_Implication` | Purity\|Divine Agency |
| `Revelation_Phase` | Medinan |

---

## 8. 🔍 Interpretive Framework

- The schema integrates **classical Arabic rhetoric (balāghah)** with **Conceptual Metaphor Theory (CMT)**.  
- Annotation emphasizes **methodological reflexivity**, ensuring interpretive transparency.  
- The merged *Glorification* category subsumes rare *Praise* cases (e.g., Mary), aligning with the Qur’an’s **theocentric logic**—all exaltation ultimately magnifies the Divine.  
- `Ambiguity_Flag` retains interpretive uncertainty without data loss.

---

## 9. 🔗 Relations Table — Modeling Inter-instance Dynamics

The **Relations Table** captures how figurative instances interact *within the same verse* to form composite rhetorical or conceptual structures.  
Each row represents a **directed edge** between two figurative instances (`Instance_ID_1 → Instance_ID_2`).

---

### 9.1 Identification Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Instance_ID_1` | Foreign key referencing the first figurative instance in the pair. | `1` | Integer (exists in Instances Table) |
| `Instance_ID_2` | Foreign key referencing the second figurative instance in the pair. | `2` | Integer (exists in Instances Table) |

---

### 9.2 Analytical Fields

| **Field** | **Description** | **Example** | **Allowed Values** |
|------------|----------------|--------------|--------------------|
| `Relation_Type` | Logical or structural function linking the two instances. Answers *“How does instance 2 connect to instance 1?”* | `Causality` | `Contrast`, `Reinforcement`, `Causality`, `Progression`, `Explication` |
| `Relation_Nature` | Qualitative texture or semantic tone of the relation. Answers *“What is the feel or conceptual nature of this link?”* | `Complementary` | `Antithetical`, `Synonymous`, `Complementary`, `Sequential`, `Explicative` |
| `Governing_Rhetorical_Purpose` | High-level rhetorical function achieved through the synergy of both instances. | `تَأْسِيسُ رَابِطَةٍ سَبَبِيَّةٍ قَاطِعَةٍ بَيْنَ الْوَسِيلَةِ وَالْغَايَةِ` | Analytical Arabic text string |
| `Semantic_Bridge` | Conceptual link or shared metaphorical core connecting the two instances. | `مِحْوَرُ رِحْلَةِ الْمُؤْمِنِ وَنَتِيجَتِهَا الْمَضْمُونَةِ` | Analytical Arabic text string |
| `Detailed_Analysis` | Full interpretive commentary describing how both images co-produce meaning. | See example below | Extended Arabic analytical text |

---

### 9.3 Example Rows

| **Instance_ID_1** | **Instance_ID_2** | **Relation_Type** | **Relation_Nature** | **Governing_Rhetorical_Purpose** | **Semantic_Bridge** |
|--------------------|--------------------|--------------------|----------------------|----------------------------------|----------------------|
| `1` | `2` | `Contrast` | `Antithetical` | تَحْدِيدُ مَاهِيَّةِ "الصِّرَاطِ" مِنْ خِلَالِ التَّقَابُلِ بَيْنَ الْمُنْعَمِ عَلَيْهِمْ وَالضَّالِّينَ. | مَفْهُومُ "الصِّرَاطِ" كَمِحْوَرٍ بَيْنَ الْهِدَايَةِ وَالضَّلَالِ. |
| `4` | `5` | `Causality` | `Complementary` | تَأْسِيسُ رَابِطَةٍ سَبَبِيَّةٍ بَيْنَ الْهِدَايَةِ وَالْفَلَاحِ. | مِحْوَرُ رِحْلَةِ الْمُؤْمِنِ وَنَتِيجَتِهَا الْمَضْمُونَةِ. |
| `6` | `7` | `Reinforcement` | `Complementary` | تَصْوِيرُ الشُّمُولِ التَّامِّ لِعُزْلَةِ الْكَافِرِينَ الرُّوحِيَّةِ وَالْمَعْرِفِيَّةِ. | الْعَائِقُ الْإِدْرَاكِيُّ كَمِفْتَاحٍ لِفَهْمِ انْقِطَاعِ الْهُدَى. |

---

### 9.4 Interpretive Framework

- The **Relations Table** transforms the dataset from a collection of isolated metaphors into a **network of relational meanings**.  
- Each edge encodes how two figures cooperate (or conflict) to generate layered rhetorical force — e.g., contrast, causation, reinforcement.  
- By combining `Relation_Type` and `Relation_Nature`, the model distinguishes *logical* from *affective* relations, enabling **multilevel discourse analysis**.  
- All relations are **directed**, reflecting interpretive asymmetry (Instance 1 → Instance 2).  

---


### 9.5 Cross-Linking with Instances Table

The `Relations Table` is **fully relational**:
- Both `Instance_ID_1` and `Instance_ID_2` reference the `Instance_ID` field in `/data/instances.csv`.  
- This relational design allows network reconstruction (e.g., graph-based analysis using NetworkX or Gephi).  
- A combined schema supports both **quantitative topological metrics** and **qualitative interpretive mappings**.

---



---
