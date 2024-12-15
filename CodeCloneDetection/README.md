## 🕵🏼 AI for Detecting Code Plagiarism

> An AI system for detecting code similarity and plagiarism has been developed to assist software developers in identifying similar code. This system aims to reduce the workload of software developers and educators, allowing them to quickly and accurately detect code plagiarism in student submissions.

### Project Structure

```plaintext
📂 CodeCloneDetection
├─ 📂 assignment                                      # Folder containing assignments
│  ├─ 📂 src                                          # Source code directory
│  │  └─ 📄 code2vec-to-detect-code-clone.ipynb       # Submitted Assignment
├─ 📂 Lecture                                         # Folder containing lecture notes
│  ├─ 📄 slide.pdf                                    # Lecture slide
│  └─ 📄 mynote.pdf                                   # Personal notes
└─ 📄 README.md                                       # This file
```

### Table of Contents

- [Notes](#notes)
  - [Problem Statement](#problem-statement)
  - [What are Code Clones?](#what-are-code-clones)
  - [Modeling](#modeling)
  - [Evaluation](#evaluation)
  - [Conclusions](#conclusions)
  - [Future Work](#future-work)
- [Assignment](#assignment)

### Notes

[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/AI-for-detecting-code-plagiarism-d6da4d5671f84e08b1595cb7d32da919?pvs=4)  
[<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)

### Problem Statement

- Existing techniques and tools face challenges when detecting clones with multiple modifications (e.g., added, deleted, or modified statements).
- Many tools are difficult to use because they are command-line based.

### What are Code Clones?

**Code Clones** are two or more code fragments that are similar enough to be considered duplicates. They can be classified into two main types:

- **Syntactic Clones :** Identical or nearly identical code fragments, except for layout differences, white space, and comments.
- **Functional Clones :** Code fragments that perform the same functionality, even if the syntax or algorithms differ.

**Causes of Code Clones**
- Copy-paste errors
- Reusing code from other projects
- Using code templates
- Automated code generation

### Modeling

**1. Data Collection and Preparation**

- **Data Source :** BigCloneBench, a large and reliable dataset of code clones.
- **Data Splitting :** Stratified sampling to create balanced training and testing sets.

**2. Code Metrics Extraction**

- **Syntactic Metrics :** 11 metrics focusing on structural characteristics (e.g., number of tokens, identifiers, operators).
- **Semantic Metrics :** 12 features extracted using **code2vec**, a neural model that represents code as vectors capturing semantic meaning.

**3. Machine Learning Models**

- **Models Considered :** Decision Tree, Random Forest, and Support Vector Machine (SVM) with Sequential Minimal Optimization (SMO).

**Key Points**
- **Data Quality :** Reliable dataset for training and evaluation.
- **Feature Engineering :** Combining syntactic and semantic metrics to capture code similarity.
- **Model Exploration :** Testing different machine learning models to find the best fit.

### Evaluation

**Accuracy Evaluation**

- **BigCloneBench (BCB) Dataset**
  - Precision, Recall, and F1-scores were calculated for different clone types.
  - F1-scores ranged from 0.65 to 0.86.
- **Real Software Projects**
  - Evaluated on three real-world projects (JUnit4, Natty, Merry).
  - Precision scores ranged from 0.41 to 0.77.

**Tool Adoption Evaluation:**

- **Target Users :** Computer Science students, programmers, and developers.
- **User Study Methodology**
  - Between-Subjects design comparing a command-line tool (Simian) to a web-based tool (Merry).
  - Metrics included tool usability, ease of understanding, and likeliness to use.

### Conclusions

**Key Points**
- **Merry** is a web-based tool using machine learning to detect code clones.
- **Goals:** Improve accuracy and user experience compared to existing tools.
- **Merry Engine:** Uses 4 machine learning models with good performance on the BigCloneBench dataset but varied results on real projects.
- **Merry Web Application:** Integrates with GitHub and offers a user-friendly interface.

**Challenges and Limitations**
- Supports only Java.
- Performance issues with code2vec.
- Evaluation performance may not reflect real-world projects.
- Scalability concerns with MongoDB.
- Small sample size in user study.

### Future Work

- Expand tool support to other languages.
- Improve code2vec performance.
- Create dedicated models for each clone type.
- Solve MongoDB limitations by querying parts of documents at a time.
- Increase the number of participants in user studies.

### Assignment

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>](https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/CodeCloneDetection/assignment/src/code2vec-to-detect-code-clone.ipynb)
