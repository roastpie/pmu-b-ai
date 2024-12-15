## 📊 Mental Disorder Detection from Social Media Data

> Predicting mental health disorders from social media data is aimed at identifying depression through posts on platforms such as Facebook, Twitter, Instagram, and other websites. The project focuses on:
> 1. Predicting depression from social media data by collecting information from platforms where people express their feelings and mental state.
> 2. Once accurate predictions are made, this data can be used to identify individuals at risk and provide appropriate support.

### Project Structure

```plaintext
📂 Mental-disorder-detection
├─ 📂 assignment                           # Folder containing assignments
│  ├─ 📂 src                               # Source code directory
│  │  └─ 📄 nlp-classification.ipynb       # Submitted Assignment
├─ 📂 Lecture                              # Folder containing lecture notes
│  ├─ 📄 slide.pdf                         # Lecture slide
│  └─ 📄 mynote.pdf                        # Personal notes
└─ 📄 README.md                            # This file
```

### Table of Contents

- [Notes](#notes)
  - [Data Collection](#data-collection)
  - [Data Exploration & Preprocessing](#data-exploration-preprocessing)
- [Assignment](#assignment)

### Notes

[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/Mental-disorder-detection-from-social-media-data-25897b7a6407476aadd2dc25835beee1?pvs=4)  
[<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)

### Data Collection

#### Direct Participant Data Collection

- **Questionnaires:** Surveys delivered to participants to gather specific information about their experiences, conditions, or opinions.
- **Electronic Health Records (EHR):** Extracting relevant data from participants' medical records with their consent.

#### Social Media Data Aggregation

- **Keyword Search:** Identifying relevant data by searching public social media posts for specific keywords or phrases like "I was diagnosed with [condition name]".
- **Annotation:** Manually tagging or classifying extracted data to categorize and analyze it effectively.

#### Benefits and Considerations

- **Direct Participant Data**
  - **Pros:** Controlled data quality, targeted information gathering, participant consent, and ethical considerations.
  - **Cons:** Potential for response bias, time, and cost required to recruit and survey participants.

- **Social Media Data**
  - **Pros:** Large volume of data available, insights into real-world language and behavior, potential for cost-effectiveness.
  - **Cons:** Privacy concerns, data quality challenges due to ambiguity and misinformation, ethical considerations regarding non-consensual data collection.

### Data Exploration & Preprocessing

#### Feature Extraction

- This involves transforming raw text data into numerical representations that computers can understand.
- Techniques like **bag-of-words** (as shown in the example) analyze word frequency and create vectors for each document.
- Other tools like **LIWC** analyze linguistic features such as pronouns and emotional tones.

### Assignment

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>](https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/Mental-disorder-detection/assignment/src/nlp-classification.ipynb)
