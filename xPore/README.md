## 🧬 xPore: An AI-Powered App for Bioinformaticians

> Software to compare the nucleotide positions on RNA sequences, such as comparing cancer patient RNA with normal human RNA to identify molecular differences. This utilizes electrical signal data from a Nanopore sequencer, the first and only tool capable of efficiently sequencing RNA directly.

### Project Structure

```plaintext
📂 xPore
├─ 📂 assignment                               # Folder containing assignments
│  ├─ 📂 src                                   # Source code directory
│  │  └─ 📄 gaussian-mixture-model.ipynb       # Submitted Assignment
├─ 📂 Lecture                                  # Folder containing lecture notes
│  ├─ 📄 slide.pdf                             # Lecture slide
│  └─ 📄 mynote.pdf                            # Personal notes
└─ 📄 README.md                                # This file
```

### Table of Contents

- [Notes](#notes)
  - [Problem Statement](#problem-statement)
  - [Data Collection and Preparation](#data-collection-and-preparation)
  - [Modeling](#modeling)
  - [Evaluation](#evaluation)
  - [Future Work](#future-work)
- [Assignment](#assignment)

### Notes

[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/xPore-An-AI-Powered-App-for-Bioinformaticians-12ee5e00bcf04e77b3a9c98d000b3f96?pvs=4)  
[<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)

### Problem Statement

- Nanopore sequencing is a novel technology that can directly sequence RNA molecules.
- It measures raw electrical signal data at each nucleotide position along the RNA strand.
- This signal data contains information about RNA modifications like m6A methylation.
- The goal is to develop a computational method to accurately locate modified positions and quantify modification rates from nanopore data.

### Data Collection and Preparation

- Nanopore sequencing produces raw signal data in **FAST5** format.
- Basecalled sequence data is output in **FASTQ** format.
- A reference genome is provided in **FASTA** format.
- The data is preprocessed by aligning to the reference and aggregating into event-level data.
- Each event represents the raw signal for a k-mer in the original RNA sequence.

### Modeling

- A **Bayesian multi-sample Gaussian mixture model (GMM)** is used.
- It models the distribution of electrical signal levels at each genomic position.
- The **Expectation Maximization** algorithm is used to fit parameters of the GMM.
- Each position is modeled as a mixture of 2 Gaussians, representing unmodified and modified states.
- The model is trained on multiple samples together to improve statistical power.

### Evaluation

- The model achieves **86% AUC** on a held-out test set for detecting known m6A modifications.
- It provides interpretable modification rate estimates that closely match expected levels.
- It performs well on a variety of tissue types and cell lines.
- The model enables the discovery of differentially modified positions between conditions.

### Future Work

- Potential improvements, like an end-to-end model directly from raw signal data.
- Investigation of different model architectures, such as **deep autoencoders**.
- Extending the model to detect additional RNA modification types beyond m6A.

### Assignment

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>](https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/xPore/assignment/src/gaussian-mixture-model.ipynb)
