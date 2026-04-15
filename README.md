# Medical Abstract Classification using Bio_ClinicalBERT

This repository contains a deep learning project focused on classifying medical abstracts into multiple clinical categories. By leveraging **Bio_ClinicalBERT** and advanced handling of imbalanced datasets, this implementation achieved a significant performance improvement over existing benchmarks.

## Overview
Automating the classification of medical literature is crucial for clinical decision support and efficient information retrieval. This project utilizes a specialized transformer-based model to categorize complex medical abstracts into five distinct pathological conditions.

### Dataset Specifications
* Source: [TimSchopf/medical_abstracts](https://huggingface.co/datasets/TimSchopf/medical_abstracts)
* Format: Large-scale medical text corpus.
* Target Classes:
  1. *Neoplasms*
  2. *Digestive System Diseases*
  3. *Nervous System Diseases*
  4. *Cardiovascular Diseases*
  5. *General Pathological Conditions*

### Project Taxonomy
* Learning Paradigm: Supervised Learning
* Task: Multilabel / Multiclass Classification
* Domain: Natural Language Processing (NLP), Clinical Text Mining

## Technical Methodology
The project implements a sophisticated pipeline tailored for clinical domain language:

1.  Model Architecture: Bio_ClinicalBERT, a BERT model pre-trained on clinical notes and biomedical literature, ensuring the model understands specialized medical terminology.
2.  Imbalance Mitigation: 
Implementation of `pos_weight` in the loss function to penalize misclassifications of minority classes effectively.

## Performance Benchmark
This implementation demonstrates a state-of-the-art improvement in classification accuracy:

* Current Implementation: **69% Macro F1-Score**
* Reference Benchmark: Achieved ~66% (based on [FIT2024 Research](https://www.ieice.org/publications/conference-FIT-DVDs/FIT2024/data/html/program/pdf/E-044.pdf))
* Delta: **+3% improvement** in generalization, largely attributed to the effective use of class weighting and domain-specific fine-tuning.

## Requirements & Prerequisites
* Python 3.9+
* PyTorch
* HuggingFace Transformers & Datasets
* Scikit-learn
* Matplotlib / Seaborn (for EDA & Evaluation)

## Installation & Usage
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/username/your-repo-name.git](https://github.com/username/your-repo-name.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Model Configuration:**
    Ensure you have access to `emilyalsentzer/Bio_ClinicalBERT` on HuggingFace.

## References & Credits
* Model: [Bio_ClinicalBERT on HuggingFace](https://huggingface.co/emilyalsentzer/Bio_ClinicalBERT)
* Author: Achmad Baihaqie Wibowo - S1 Informatics, Telkom University
* Further Reading: 
    * [Natural Language Processing is Fun](https://medium.com/@ageitgey/natural-language-processing-is-fun-9a0bff37854e)
    * [WeightedRandomSampler Guide](https://medium.com/data-science/demystifying-pytorchs-weightedrandomsampler-by-example-a68aceccb452)