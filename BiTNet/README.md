## 🩺 BiTNet: AI for Diagnosing Ultrasound Images

> The AI system for screening upper abdominal abnormalities using ultrasound images has been developed to:
> 1. Assist radiologists in diagnosing ultrasound images sent by general practitioners for screening cholangiocarcinoma (CCA) patients.
> 2. Boost the confidence of general practitioners in diagnosing abnormalities.

### Project Structure

```plaintext
📂 BiTNet
├─ 📂 assignment                              # Folder containing assignments
│  ├─ 📂 src                                  # Source code directory
│  │  └─ 📄 image_classificaiton.ipynb        # Submitted Assignment
├─ 📂 Lecture                                 # Folder containing lecture notes
│  ├─ 📄 slide.pdf                            # Lecture slide
│  └─ 📄 mynote.pdf                           # Personal notes
└─ 📄 README.md                               # This file
```

### Table of Contents

- [Notes](#notes)
  - [Data Acquisition](#data-aquisition)
  - [Data Preparation](#data-preparation)
  - [Model Development](#model-development)
  - [Future Work](#future-work)
- [Assignment](#assignment)

### Notes

[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/BiTNet-AI-for-diagnosing-ultrasound-image-3a11b5b76d7846c7baa456101bc33585?pvs=4)  
[<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)

### Data Acquisition

- **Surveys:** Conducted to assess youth interest in coding, AI education, and their career goals.
- **Focus Groups:** Gathered feedback from youth, educators, and professionals about the project.
- **Ultrasound Screenings:** Conducted every six months for youth in the region, identifying those at risk for specific health conditions.

### Data Preparation

- **Data Collection:** Ultrasound images are collected through portable machines and tele-radio consultations, stored in a secure database.
- **Data Cleaning:** Images undergo segmentation and noise removal to ensure clarity.
- **Data Labeling:** Expert radiologists label the images as normal or abnormal using a standardized classification scheme.
- **Data Augmentation:** Techniques like horizontal and vertical shifts, rotations, brightness adjustments, shearing, and zooming are used to enhance dataset size and diversity.

### Model Development

- **Model Selection:** **EfficientNetB5** is chosen for its state-of-the-art performance in image classification, while **BiTNet** is used for medical image classification tasks.
- **Training Steps:**
  - **Pre-training:** EfficientNetB5 is pre-trained on ImageNet with over 14 million images.
  - **Fine-tuning:** The model is fine-tuned on the ultrasound dataset using the Adam optimizer for 100 epochs.

### Future Work

- **AI for CCA Screening:** The system can detect cholangiocarcinoma (CCA) from ultrasound images, potentially improving early detection and treatment.
- **Diagnose 25 Abnormalities:** AI models could expand to diagnose a broader range of conditions in the upper abdomen.
- **Current Usage:** The system is in use at Srinagarind Hospital and 205 affiliated hospitals, impacting real-world healthcare.
- **Cloud-based AI Services:** Expanding access to AI tools for wider use.

### Assignment

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>](https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/BiTNet/assignment/src/image_classificaiton.ipynb)
