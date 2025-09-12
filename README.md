# Amthāl Corpus

## 📖 Codebook: The Qur'anic Rhetorical Imagery Corpus

### Introduction
This document serves as the official **codebook** for the *Amthāl* corpus project, which focuses on analyzing the **conceptual network of rhetorical imagery in the Qur’an**.  

Each row in the dataset represents one **rhetorical instance** (مثيل بلاغي) extracted and annotated from the Qur’anic text.  
The purpose of this codebook is to:
- Provide a clear explanation of every field (column).
- Define its purpose and possible values.
- Ensure full **transparency**, **consistency**, and **reproducibility** for future research.

---

## 📂 Field Descriptions

### 1️⃣ Identification & Localization Fields
| Field Name        | Description | Possible Values |
|-------------------|-------------|-----------------|
| **Sura_No**       | Numerical identifier of the Surah (chapter). Essential for locating the imagery. | Integer, 1–114 |
| **Aya_No**        | Numerical identifier of the verse within the Surah. Combined with *Sura_No* provides a unique reference. | Integer |
| **Revelation_Phase** | Classifies the verse based on historical context. | Makki, Madani |

---

### 2️⃣ Extraction & Rhetorical Classification
| Field Name        | Description | Possible Values |
|-------------------|-------------|-----------------|
| **Snippet**       | Direct textual evidence (verbatim phrase) containing the imagery. Ensures transparency and quick review. | Arabic text from the verse, or NA |
| **Keywords**      | List of key words from the snippet and its context, useful for computational analysis. | Comma-separated list, or NA |
| **Figure_Type**   | Rhetorical category of the instance. | تشبيه (Simile), استعارة (Metaphor), كناية (Metonymy), مجاز لغوي (Figurative Expression) |

---

### 3️⃣ Conceptual Abstraction
| Field Name        | Description | Possible Values |
|-------------------|-------------|-----------------|
| **Dominant_Concept** | Core concept serving as a *node* in the conceptual network. Provides a unified abstract category. | Controlled Arabic vocabulary (e.g., نور “light”, ظلام “darkness”, طريق “path”), or NA |
| **Core_Concept_Pair** | Source–Target conceptual mapping that specifies the cognitive projection. | Arabic phrase in `source/target` form (e.g., النور/الهداية “light/guidance”), or NA |

---

### 4️⃣ Analytical & Contextual Fields
| Field Name        | Description | Possible Values |
|-------------------|-------------|-----------------|
| **Rhetorical_Function** | Pragmatic function of the image in context (i.e., what it aims to achieve). | وعد (Promise), وعيد (Threat), حجاج (Argument), تقريب (Illustration), تعظيم (Glorification), امتنان (Gratitude) |
| **Valence**       | Emotional or semantic polarity of the imagery. | Positive, Negative, Neutral |
| **Dominance_Score** | Quantitative scale (1–5) measuring the centrality of the imagery within the verse. | Integer, 1 (marginal) – 5 (central) |
| **Abstraction_Level** | Nature of the source domain of the image. | Tangible, Abstract |
| **Intra_Verse_Relation** | Relationship of this image to other images in the same verse (if any). | Contrast, Complement, Sequence, None |

---

### 5️⃣ Metadata & Annotation Quality
| Field Name        | Description | Possible Values |
|-------------------|-------------|-----------------|
| **Hierarchy**     | Distinguishes between the primary and secondary images within a verse. | Primary, Secondary, NA |
| **Ambiguity_Flag** | Marks the annotator’s confidence level in interpreting the imagery. | Clear, Ambiguous, NA |

---

## 📌 Notes
- Each row corresponds to **one rhetorical instance**.  
- Certain fields may take the value **NA** when not applicable.  
- This codebook is intended to guide researchers in **using, analyzing, and extending** the Amthāl corpus.  

---

## 🚀 Usage Example
You can load the dataset in Python with `pandas`:

```python
import pandas as pd

df = pd.read_csv("Amthal_Corpus.tsv", sep="\t", encoding="utf-8")
print(df.head())
