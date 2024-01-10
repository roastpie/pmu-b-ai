<h2 id="mental-disorder-detection">
    📊 Mental disorder detection from social media data
</h2>

> Predicting mental health disorders from social media data เป็นการทำนายโรคซึมเศร้าจากข้อมูลการโพสบนสื่อสังคมออนไลน์ถูกพัฒนาขึ้นเพื่อ        1.เพื่อทำนายโรคซึมเศร้าจากข้อมูลสื่อสังคมออนไลน์ ซึ่งเริ่มต้นด้วยการรวบรวมข้อมูลจากแพลตฟอร์มสื่อสังคมออนไลน์ เช่น เฟสบุ๊ค, ทวิตเตอร์, อินสตาแกรม หรือเว็บไซต์อื่น ๆ ที่ผู้คนใช้ในการแสดงความรู้สึกและความคิดเห็นของพวกเขาเกี่ยวกับสถานะจิตใจของตนเอง        2.หลังจากที่เราสามารถทำนายโรคซึมเศร้าได้ด้วยความแม่นยำ เราสามารถใช้ข้อมูลนี้เพื่อรวบรวมกลุ่มผู้ที่เสี่ยงต่อโรคซึมเศร้าและให้การสนับสนุนที่เหมาะสมได้

### Project structure

```plaintext
📂 Mental-disorder-detection
├─ 📂 assignment                           # Folder containing assignments
│  ├─ 📂 src                               # Source code directory
│  │  └─ 📄 nlp-classification.ipynb       # Submitted Assignment
├─ 📂 Lecture                              # Folder containing lecture notes
│  ├─ 📄 slide.pdf                         # Lecture slide
│  └─ 📄 mynote.pdf                        # My personal note
└─ 📄 README.md                            # This file
```

### Table of Contents

<ul>
  <li>
  <details>
    <summary>Notes</summary>
    <ul>
      <li><a href="data-collection">Data Collection</a></li>
      <li><a href="#data-exploration-preprocessing">Data Exploration & Preprocessing</a></li>
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
[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/Mental-disorder-detection-from-social-media-data-25897b7a6407476aadd2dc25835beee1?pvs=4) [<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)


### Data Collection

**Direct Participant Data Collection**

- **Questionnaires:** Surveys delivered to participants to gather specific information about their experiences, conditions, or opinions.
- **Electronic Health Records (EHR):** Extracting relevant data from participants' medical records with their consent.

**Social Media Data Aggregation**

- **Keyword Search:** Identifying relevant data by searching public social media posts for specific keywords or phrases like "I was diagnosed with [condition name]".
- **Annotation:** Manually tagging or classifying extracted data to categorize and analyze it effectively.

**Benefits and Considerations**

- **Direct Participant Data**

**Pros:** Controlled data quality, targeted information gathering, participant consent and ethical considerations.

**Cons:** Potential for response bias, time and cost required to recruit and survey participants.

- **Social Media Data**

**Pros:** Large volume of data available, insights into real-world language and behavior, potential for cost-effectiveness.

**Cons:** Privacy concerns, data quality challenges due to ambiguity and misinformation, ethical considerations regarding non-consensual data collection.

### Data Exploration & Preprocessing

**Feature Extraction:**

- This involves transforming raw text data into numerical representations that computers can understand.
- Techniques like **bag-of-words** (as shown in the example) analyze word frequency and create vectors for each document.
- Other tools like **LIWC** analyze linguistic features like pronouns and emotional tones.

### Assignment

<a target="_blank" href="https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/Mental-disorder-detection/assignment/src/nlp-classification.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
