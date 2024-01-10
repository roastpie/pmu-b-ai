<h2 id="xpore">
    🧬 xPore: An AI-Powered App for Bioinformaticians
</h2>

> ซอฟท์แวร์ที่ช่วยเปรียบเทียบตำแหน่งของลำดับเบสบนสาย RNA ของเซลล์ใด ๆ เช่น เปรียบเทียบระหว่าง RNA ของผู้ป่วยมะเร็งกับคนปกติ ว่าตำแหน่งใดบนสาย RNA ที่มีลักษณะโมเลกุลไม่เหมือนกัน โดยการใช้ข้อมูลสัญญาณไฟฟ้าที่มาจาก Nanopore sequencer ซึ่งเป็นเครื่องมือแรกและเครื่องมือชนิดเดียวในตอนนี้สามารถ sequence ลำดับเบสของสาย RNA ได้โดยตรงอย่างมีประสิทธิภาพ

## Project structure

```plaintext
📂 xPore
├─ 📂 assignment                               # Folder containing assignments
│  ├─ 📂 src                                   # Source code directory
│  │  └─ 📄 gaussian-mixture-model.ipynb       # Submitted Assignment
├─ 📂 Lecture                                  # Folder containing lecture notes
│  ├─ 📄 slide.pdf                             # Lecture slide
│  └─ 📄 mynote.pdf                            # My personal note
└─ 📄 README.md                                # This file
```

## Table of Contents

<ul>
  <li>
  <details>
    <summary>Notes</summary>
    <ul>
      <li>
       <a href="#problem-statement">Problem Statement</a>
      </li>
      <li><a href="#data-collection-and-preparation">Data Collection and Preparation</a></li>
      <li><a href="#modeling">Modeling</a></li>
      <li><a href="#evaluation">evaluation</a></li>
      <li><a href="#future-work">Future Work</a></li>
    </ul>
  </details>
  </li>
  <li>
   <a href="#assignment">
    Assignment
    </a>
  </li>
</ul>

## Notes
[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/xPore-An-AI-Powered-App-for-Bioinformaticians-12ee5e00bcf04e77b3a9c98d000b3f96?pvs=4) [<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)

### Problem Statement

- Nanopore sequencing is a novel technology that can directly sequence RNA molecules
- It measures raw electrical signal data at each nucleotide position along the RNA strand
- This signal data contains information about RNA modifications like m6A methylation
- Goal is to develop a computational method to accurately locate modified positions and quantify modification rates from nanopore data

### Data Collection and Preparation

- Nanopore sequencing produces raw signal data in FAST5 format
- Basecalled sequence data is output in FASTQ format
- A reference genome is provided in FASTA format
- These data are preprocessed by aligning to the reference and aggregating into event-level data
- Each event represents the raw signal for a k-mer in the original RNA sequence

### Modeling

- A Bayesian multi-sample Gaussian mixture model (GMM) is used
- It models the distribution of electrical signal levels at each genomic position
- Expectation Maximization algorithm used to fit parameters of the GMM
- Each position is modeled as a mixture of 2 Gaussians representing unmodified and modified states
- The model is trained on multiple samples together to improve statistical power

### Evaluation

- Model achieves 86% AUC on held-out test set for detecting known m6A modifications
- Provides interpretable modification rate estimates that closely match expected levels
- Performs well on variety of tissue types and cell lines
- Enables discovery of differentially modified positions between conditions

### Future Work

- Potential improvements like end-to-end model directly from raw signal data
- Investigate different model architectures like deep autoencoders
- Extend model to detect additional RNA modification types beyond m6A

### Assignment

<a target="_blank" href="https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/xPore/assignment/src/gaussian-mixture-model.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
