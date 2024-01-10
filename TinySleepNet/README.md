<h2 id="tinysleepnet">
    🧠 TinySleepNet: Learning from Biosignal
</h2>

> แบบจำลองการเรียนรู้เชิงลึก (Deep Learning Model) สำหรับวิเคราะห์การนอน (Sleep Stage Scoring) ด้วยคลื่นสัญญาณสมอง ภายใต้โครงการ Learning from Biosignals

### Project structure

```plaintext
📂 TinySleepNet
├─ 📂 assignment                  # Folder containing assignments
│  ├─ 📂 src                      # Source code directory
│  │  └─ 📄 brain-signal.py       # Submitted Assignment
├─ 📂 Lecture                     # Folder containing lecture notes
│  ├─ 📄 slide.pdf                # Lecture slide
│  └─ 📄 mynote.pdf               # My personal note
└─ 📄 README.md                   # This file
```

### Table of Contents

<ul>
  <li>
  <details>
    <summary>Notes</summary>
    <ul>
      <li>
       <a href="#problem-statement">Problem Statement</a>
      </li>
      <li><a href="#biosignal-analysis">Biosignal analysis</a></li>
      <li><a href="#sleep-stage-scoring">Sleep stage scoring</a></li>
      <li><a href="#model">Model</a></li>
      <li><a href="#evaluation">Evaluation</a></li>
      <li><a href="#conclusions">Conclusions</a></li>
    </ul>
  </details>
  </li>
  <li>
   <a href="#assignment">
    Assignment
    </a>
  </li>
</ul>

### Notes
[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/TinySleepNet-Learning-from-Biosignal-b27307b831fb480585483e5bf8cdb741?pvs=4) [<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)
### Problem Statement

- Labor-intensive and time-consuming
- Too many signals to collect at home à not portable and troublesome device setup

### Biosignal analysis

1. **Data preparation:** Before analyzing the biosignals, we need to clean them up. This involves removing noise and artifacts that can disrupt the analysis.
2. **Feature extraction:** Once the data is clean, we identify meaningful characteristics, or "features," from the signals. These features are chosen by experts who understand what's important for sleep stage scoring.
3. **Model building:** Using the extracted features, we train machine learning models. These models learn to recognize patterns in the features and associate them with different sleep stages (e.g., REM, NREM).

> Deep Learning Utilize multiple layers of non-linear transformation
to convert from inputs into representations that are
useful for subsequent tasks such as classification
> 

### Sleep stage scoring

**NREM sleep** is further divided into three stages:

- **N1** is the lightest stage of sleep, and it is characterized by slow, rolling eye movements and reduced muscle activity.
- **N2** is a deeper stage of sleep, and it is characterized by more regular brain waves and decreased muscle activity.
- **N3** is the deepest stage of sleep, and it is characterized by very slow, delta waves and the absence of muscle activity.

**REM sleep** is characterized by rapid eye movements, increased brain activity, and muscle paralysis. It is thought to be important for memory consolidation and dreaming.

**The normal sleep pattern** involves cycling through all stages of NREM and REM sleep several times during a night. The first sleep cycle is typically shorter and lighter than later cycles. REM sleep periods become longer and deeper as the night progresses.

**Awake** is a fifth stage of sleep that is characterized by the absence of sleep stages N1-REM. It is typically brief and occurs between sleep cycles.

**Sleep stage scoring is a multi-class classification problem in machine learning.** This means that there are five classes to classify: N1, N2, N3, REM, and Awake.

**To assess the quality of sleep,** researchers use a variety of metrics, including:

- **Total sleep time (TST)**: The total number of minutes spent asleep.
- **Time in bed (TIB)**: The total time spent in bed, including time spent awake.
- **Sleep efficiency (%):** The percentage of time spent in bed that is spent asleep.

### Model

| Feature | DeepSleepNet | TinySleepNet |
| --- | --- | --- |
| Representation learning | Two branches of CNNs | Single branch of CNNs with hierarchical structure |
| Sequence learning | Bidirectional RNNs | Unidirectional RNNs |
| Data augmentation | Signal augmentation | Signal augmentation and sequence augmentation |
| Computational resources | More | Less |
| Parameters | More | Less |
| Performance | Similar | Similar |
| Deployment | More challenging | Easier |

### Evaluation

- **Experimental Setup**
• k-fold cross-validation (non-overlapping patient split)
- **Performance Metrics**
• Overall: accuracy (ACC), macro-averaged F1-Score (MF1), Cohen’s Kappa ( )
• Per-class: precision (PR), recall (RE), F1-Score (F1)
- **Visualization**
• Hypnogram

### Conclusions

- **Deep learning is mostly used for supervised learning with biosignals.** This means it relies on labeled data to learn and predict outcomes.
- **Transforming raw signals into spectrogram or image representations can be an alternative.** This allows using CNNs, which are good at processing images. However, this is not always ideal for end-to-end training.
- **Directly applying deep learning on raw signals is challenging.** This is mainly successful when the signals have clear patterns for each class and enough training data.
- **Remote monitoring is a promising area for deep learning in biosignals.** This involves adapting models from clinical settings to work with wearable devices.

### Assignment

<a target="_blank" href="https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/1d-cnn-for-brain-signal/assignment/src/gaussian-mixture-model.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
