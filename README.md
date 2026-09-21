# CDSAB: A Multi-Granularity Chinese Text Similarity Benchmark for Alignment-Guided Evaluation

CDSAB is a multi-granularity Chinese text similarity benchmark designed for the systematic evaluation of **lexical, semantic, and alignment-guided text similarity methods**.

The benchmark supports controlled experiments across different text lengths, structural granularities, and domains. It is intended to study not only which similarity methods perform well, but also **when global representations are sufficient and when local alignment provides additional useful information**.

CDSAB accompanies our research on alignment-guided Chinese text similarity and is released to support reproducibility and further research in Chinese NLP, document similarity, long-text representation, semantic alignment, and information retrieval.

---

## Dataset Overview

CDSAB contains three complementary evaluation components:

1. **Length-controlled literary text similarity**
2. **Chapter-level structural similarity**
3. **Legal semantic similarity**

These components allow similarity methods to be evaluated across different:

- text lengths;
- document granularities;
- structural relationships;
- domains;
- representation strategies;
- aggregation strategies.

---

## 1. Length-Controlled Literary Text Similarity

This component provides a controlled benchmark for studying the effect of text length on similarity measurement.

### Statistics

- **405 documents**
- **135 source texts**
- **3 length levels**
  - long
  - medium
  - short
- **3 source sets**
- **8,910 within-set, within-length document pairs**

Each source text is represented at multiple length levels, enabling controlled comparison of similarity methods under different amounts of textual context.

The texts cover several categories of Chinese literature, including:

- modern literature;
- Ming-Qing fiction;
- modern prose;
- classical prose.

This component is particularly useful for comparing lexical and semantic methods as text length increases.

---

## 2. Chapter-Level Structural Similarity

This component contains selected chapters from six Chinese novels and is designed for evaluating long-text representation and local structural alignment.

The selected chapter ranges are:

| Work | Selected Chapters |
|---|---|
| She Diao Ying Xiong Zhuan | 1-5, 12-16, 24-28, 36-40 |
| Shen Diao Xia Lv | 1-5, 12-16, 24-28, 36-40 |
| Xiao Ao Jiang Hu | 1-5, 12-16, 24-28, 36-40 |
| Tian Long Ba Bu | 1-5, 16-20, 31-35, 46-50 |
| Shu Jian En Chou Lu | 1-5, 6-10, 11-15, 16-20 |
| Bi Xue Jian | 1-5, 6-10, 11-15, 16-20 |

This component supports experiments involving:

- global document embeddings;
- chunk-based representations;
- segment-to-segment similarity;
- local alignment;
- top-k alignment;
- alignment-aware aggregation;
- global-versus-local similarity comparison.

---

## 3. Legal Semantic Similarity

The legal-domain component is derived from the **CAIL2019-SCM** semantic similarity task.

It provides an additional domain for examining whether observations obtained from literary and narrative text generalize to legal text.

Where original third-party data cannot be redistributed directly, this repository provides only redistributable materials such as:

- identifiers;
- metadata;
- pair definitions;
- split information;
- preprocessing instructions;
- reconstruction information.

Users should obtain restricted source material from the original authorized source and comply with its applicable license or terms of use.

---

## Research Questions

CDSAB was designed to support questions such as:

1. How does text length affect Chinese text similarity measurement?
2. When do lexical approaches remain competitive with neural semantic representations?
3. How much information is lost when a long document is represented by a single embedding?
4. When does chunk-level representation improve similarity estimation?
5. When does local alignment outperform direct global comparison?
6. How should local similarity scores be aggregated?
7. Do conclusions remain consistent across literary, narrative, and legal domains?
8. Which combinations of representation and aggregation are appropriate for different similarity tasks?

---

## Supported Method Families

The benchmark can be used to evaluate methods including:

### Lexical Methods

- TF-IDF
- character n-grams
- BM25
- Jaccard similarity
- MinHash

### Semantic Methods

- sentence embeddings
- document embeddings
- SBERT-style encoders
- SimCSE-style encoders
- Chinese pretrained embedding models
- M3E-based representations

### Long-Text and Alignment Methods

- global document encoding
- chunk-level encoding
- segment-level comparison
- local alignment
- top-k segment matching
- weighted aggregation
- alignment-guided similarity
- lexical-semantic hybrid similarity

---

## Repository Structure

The public release is organized approximately as follows:

```text
CDSAB-Chinese-Text-Similarity-Benchmark/
├── README.md
├── LICENSE
├── metadata/
├── literary_length/
├── chapter_alignment/
├── legal_scm/
├── splits/
├── pair_lists/
└── documentation/
