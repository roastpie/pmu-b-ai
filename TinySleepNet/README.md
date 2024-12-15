## 🧠 TinySleepNet: Learning from Biosignal

> An efficient deep learning model for sleep stage scoring based on raw, single-channel EEG.

### Project Structure

```plaintext
📂 TinySleepNet
├─ 📂 assignment                  # Folder containing assignments
│  ├─ 📂 src                      # Source code directory
│  │  └─ 📄 brain-signal.py       # Submitted Assignment
├─ 📂 Lecture                     # Folder containing lecture notes
│  ├─ 📄 slide.pdf                # Lecture slide
│  └─ 📄 mynote.pdf               # Personal notes
└─ 📄 README.md                   # This file
```

### Table of Contents

- [Notes](#notes)
  - [Problem Statement](#problem-statement)
  - [Biosignal Analysis](#biosignal-analysis)
  - [Sleep Stage Scoring](#sleep-stage-scoring)
  - [Model](#model)
  - [Evaluation](#evaluation)
  - [Conclusions](#conclusions)
- [Assignment](#assignment)

### Notes

[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/TinySleepNet-Learning-from-Biosignal-b27307b831fb480585483e5bf8cdb741?pvs=4)  
[<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)

### Problem Statement

- Labor-intensive and time-consuming process.
- Many signals need to be collected at home, making it non-portable and requiring complicated device setups.

### Biosignal Analysis

1. **Data Preparation**: Clean up biosignals by removing noise and artifacts to ensure accurate analysis.
2. **Feature Extraction**: Identify meaningful features from the signals, selected by experts for their relevance to sleep stage scoring.
3. **Model Building**: Train machine learning models on the extracted features to recognize patterns and associate them with different sleep stages (e.g., REM, NREM).

> Deep learning uses multiple layers of non-linear transformations to convert inputs into representations useful for subsequent tasks like classification.

### Sleep Stage Scoring

**NREM Sleep** is divided into three stages:
- **N1**: Lightest stage, characterized by slow eye movements and reduced muscle activity.
- **N2**: Deeper sleep with regular brain waves and decreased muscle activity.
- **N3**: Deepest stage, marked by very slow delta waves and absence of muscle activity.

**REM Sleep**: Characterized by rapid eye movements, increased brain activity, and muscle paralysis. Essential for memory consolidation and dreaming.

**Awake**: A fifth stage, characterized by the absence of sleep stages N1-REM, typically brief and occurring between sleep cycles.

**Sleep Stage Scoring** is a multi-class classification problem in machine learning with five classes: N1, N2, N3, REM, and Awake.

**Sleep Quality Metrics**:
- **Total Sleep Time (TST)**: Total minutes spent asleep.
- **Time in Bed (TIB)**: Total time spent in bed, including awake time.
- **Sleep Efficiency (%)**: Percentage of time spent in bed that is spent asleep.

### Model Comparison

| Feature               | DeepSleepNet       | TinySleepNet     |
|-----------------------|--------------------|------------------|
| Representation Learning| Two branches of CNNs | Single branch of CNNs with hierarchical structure |
| Sequence Learning      | Bidirectional RNNs  | Unidirectional RNNs |
| Data Augmentation      | Signal augmentation | Signal & sequence augmentation |
| Computational Resources | More               | Less             |
| Parameters             | More               | Fewer            |
| Performance            | Similar            | Similar          |
| Deployment             | More challenging   | Easier           |

### Evaluation

- **Experimental Setup**: k-fold cross-validation with non-overlapping patient split.
- **Performance Metrics**:
  - Overall: Accuracy (ACC), Macro-averaged F1-Score (MF1), Cohen’s Kappa (κ)
  - Per-class: Precision (PR), Recall (RE), F1-Score (F1)
- **Visualization**: Hypnogram for sleep stage progression.

### Conclusions

- Deep learning is mostly applied for supervised learning with biosignals, relying on labeled data to predict outcomes.
- Transforming raw signals into spectrograms or image representations allows using CNNs, though not always ideal for end-to-end training.
- Direct application of deep learning to raw signals is challenging but can work with sufficient data and clear patterns.
- Remote monitoring through wearable devices is a promising direction, adapting clinical models for real-world applications.

### Assignment

[<img src="https://img.shields.io/badge/view%20in%20github-grey?style=for-the-badge&logo=github" />](./assignment/src/brain-signal.py)
