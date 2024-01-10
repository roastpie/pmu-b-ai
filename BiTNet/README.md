<h2 id="bitnet">
    🩺 BiTNet: AI for diagnosing ultrasound image
</h2>

> ระบบ AI สำหรับช่วยคัดกรองความผิดปกติในช่องท้องส่วนบน ด้วยภาพถ่ายอัลตราซาวน์ถูกพัฒนาขึ้นมาเพื่อ       1. ช่วยลดงานของรังสีแพทย์ในการวินิจฉัยภาพถ่ายอัลตราซาวน์ที่ถูกส่งมาสอบถามจากแพทย์เวชปฏิบัติที่ทำหน้าที่คัดกรองผู้ป่วยมะเร๋งท่อน้ำดีที่หน้างาน       2. ช่วยเพิ่มความมั่นใจในการวินิจฉัยของแพทย์เวชปฏิบัติในการวินิจฉัยความผิดปกติอีกด้วย

### Project structure

```plaintext
📂 BiTNet
├─ 📂 assignment                              # Folder containing assignments
│  ├─ 📂 src                                  # Source code directory
│  │  └─ 📄 image_classificaiton.ipynb        # Submitted Assignment
├─ 📂 Lecture                                 # Folder containing lecture notes
│  ├─ 📄 slide.pdf                            # Lecture slide
│  └─ 📄 mynote.pdf                           # My personal note
└─ 📄 README.md                               # This file
```

### Table of Contents

<ul>
  <li>
  <details>
    <summary>Notes</summary>
   <ul>
      <li><a href="#data-aquisition">Data Aquisition</a></li>
      <li><a href="#data-preparation">Data Preparation</a></li>
      <li><a href="#model-development">Model Development</a></li>
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

### Notes
[<img src="https://img.shields.io/badge/view%20in%20notion-grey?style=for-the-badge&logo=notion" />](https://xinnypie.notion.site/BiTNet-AI-for-diagnosing-ultrasound-image-3a11b5b76d7846c7baa456101bc33585?pvs=4) [<img src="https://img.shields.io/badge/view%20in%20pdf-grey?style=for-the-badge&logo=github" />](./lecture/file/mynote.pdf)



### Data Aquisition

- **Surveys:** Surveys were conducted with youth in the region to assess their interest in coding and AI education, their skills and knowledge in these areas, and their career goals.
- **Focus groups:** Focus groups were conducted with youth, educators, and industry professionals to gather feedback on the project and its goals.
- **Data from ultrasound screenings:** Ultrasound screenings are conducted every six months for a cohort of youth in the region. The data from these screenings is used to identify youth who are at risk for certain health conditions.

### Data Preparation

- **Data collection:** The ultrasound images are collected using a variety of methods, including portable ultrasound machines and tele-radio consultation. The images are stored in a secure database.
- **Data cleaning:** The images are cleaned using a variety of techniques, including image segmentation and noise removal. This helps to ensure that the images are clear and easy to interpret.
- **Data labeling:** The images are labeled by a team of expert radiologists. The radiologists use a standardized classification scheme to identify the images as normal or abnormal.
- **Data augmentation:** The data is augmented using a variety of techniques, including horizontal and vertical shifts, rotations, brightness adjustments, shearing, and zooming. This helps to increase the size and diversity of the dataset, which can improve the performance of the machine learning models.

### Model Development

- **Model selection:** The researchers selected the **EfficientNetB5** model because it has been shown to achieve state-of-the-art performance on a variety of tasks, including image classification. The researchers also selected the **BiTNet** model because it is specifically designed for medical image classification.
- **Data preparation:** The researchers prepared the data using the following steps:
    - **Data collection:** Ultrasound images were collected from a cohort of youth in the northeastern region of Thailand. The images were collected every six months, and they were used to identify youth who are at risk for certain health conditions.
    - **Data cleaning:** The images were cleaned to remove any background information that is not relevant to the task of identifying health conditions. This was done using a variety of techniques, including image segmentation and noise removal.
    - **Data labeling:** The images were labeled as either normal or abnormal, based on the diagnosis of a radiologist. The labeling was done by a team of expert radiologists.
    - **Data augmentation:** The data was augmented using a variety of techniques, including horizontal and vertical shifts, rotations, brightness adjustments, shearing, and zooming. This was done to increase the size and diversity of the dataset, which can improve the performance of the machine learning models.
- **Model training:** The researchers trained the **EfficientNetB5** model using the following steps:
    - **Pre-training:** The model was pre-trained on the ImageNet dataset, which contains over 14 million images of 1,000 different classes. This was done using the Adam optimizer and a learning rate of 0.0001.
    - **Fine-tuning:** The model was fine-tuned on the dataset of ultrasound images. This was done using the Adam optimizer and a learning rate of 0.0001. The model was trained for 100 epochs.

### Future Work

- **The first AI system in the world that screens CCA via ultrasound image:** This is a significant achievement that could have a major impact on the early detection and treatment of cholangiocarcinoma (CCA), a type of liver cancer.
- **Diagnose 25 abnormalities in the human upper abdominal:** This shows that the AI models developed by the project have the potential to be used for a wide range of diagnostic tasks.
- **Currently used in Srinagarind Hospital and 205 Affiliated hospitals:** This shows that the project is already having a real-world impact on the lives of people in Thailand.
- **Cloud-based AI Services:** This makes the AI models developed by the project more accessible to a wider range of users.

### Assignment

<a target="_blank" href="https://colab.research.google.com/github/xinnypie/pmb-u-ai/blob/master/BiTNet/assignment/src/image_classificaiton.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
