# Optimized Efficient Attention-Based Network for Facial Expressions Analysis in Neurological Health Care

[![Journal](https://img.shields.io/badge/Journal-Computers%20in%20Biology%20and%20Medicine-blue)](https://www.elsevier.com/locate/compbiomed)
[![Status](https://img.shields.io/badge/Status-In%20Press-success)](https://doi.org/10.1016/j.compbiomed.2024.108822)

## 📌 Overview
[cite_start]Facial Expression Analysis (FEA) plays a vital role in diagnosing and treating early-stage neurological disorders (NDs) like Alzheimer's and Parkinson's[cite: 693]. [cite_start]However, manual analysis is hindered by expertise requirements, while existing automatic methods struggle with high computational costs and a lack of real patient data[cite: 694].

[cite_start]To address these challenges, this repository hosts the implementation of a **novel, efficient, lightweight Convolutional Block Attention Module (CBAM) based Deep Learning Network (DLN)**[cite: 695]. [cite_start]This framework is designed to aid doctors in diagnosing ND patients by extracting relevant facial features with high efficiency, making it suitable for resource-constrained mobile healthcare devices[cite: 698].

## 📊 Conference Poster
![CBIM 2024 Poster](Fig/CBIM_24_P.png)

## 🔑 Key Highlights
* [cite_start]**Lightweight Architecture:** The model is optimized for smart health applications, occupying only **3 MB** with 0.9 million parameters, making it deployable on smartphones and Raspberry Pi[cite: 668, 698, 1053].
* [cite_start]**High Performance:** Achieved **73.2% accuracy**, **73.4% precision**, and **73.5% recall** on real patient data, significantly outperforming state-of-the-art models like ResNet-101 and MobileNet[cite: 697, 1052, 1087].
* [cite_start]**Attention Mechanism:** Utilizes a custom CNN with **Convolutional Block Attention Module (CBAM)** to refine features via channel and spatial attention, focusing on relevant facial regions while suppressing irrelevant background noise[cite: 802, 803].
* [cite_start]**Real-World Validation:** Validated on a compiled dataset of real ND patients (Parkinson's, Alzheimer's, Stroke) collected from medical sources, in addition to standard datasets like KDEF and RAVDESS[cite: 697, 971].

## 🏗️ Methodology
The proposed framework operates in four stages:
1.  [cite_start]**Data Acquisition & Pre-processing:** Utilizes the Viola-Jones algorithm for face detection, cropping, and resizing images to $148 \times 148$ to reduce computational cost[cite: 787, 790].
2.  [cite_start]**Feature Extraction:** A custom 6-layer CNN extracts high-level features[cite: 801].
3.  [cite_start]**Feature Refinement (CBAM):** * **Channel Attention Module (CAM):** Focuses on "what" is meaningful in the image[cite: 833].
    * [cite_start]**Spatial Attention Module (SAM):** Focuses on "where" the informative part is located[cite: 882].
4.  [cite_start]**Classification:** A fully connected layer with Softmax classifies the emotional state (e.g., Happy, Sad, Neutral, Angry, Disgust)[cite: 915].


## 📈 Experimental Results
We conducted extensive ablation studies and comparisons with state-of-the-art (SOTA) models. [cite_start]Our CBAM-based model demonstrated superior diagnostic performance, particularly for Parkinson's and Alzheimer's diseases[cite: 669].

| Model | Attention | Accuracy (%) | Parameters (M) | Inference Time (s) |
| :--- | :--- | :--- | :--- | :--- |
| ResNet-101 | CBAM | 42.0 | 43.9 | - |
| MobileNet | CBAM | 44.5 | 4.1 | - |
| **Proposed** | **CBAM** | **73.2** | **0.9** | **0.7** |

[cite_start]*Table: Performance comparison on Real Patient Data[cite: 1057].*


[cite_start]Qualitative analysis using attention maps confirms the model focuses on relevant facial regions (eyes, mouth) even in patients with reduced facial expressivity due to NDs[cite: 1073].


## 💾 Data Access
The Neurological FER evaluation dataset is provided as a `FER_NDs_Test_Data.rar` file in this repository. 
* [cite_start]**Note:** This dataset includes real patient data collected for cross-validation[cite: 667].
* For further questions regarding data access, please contact Munsif at [munsif3797@gmail.com](mailto:munsif3797@gmail.com).

## 💻 Code Availability
The complete source code for the proposed framework will be made available shortly. [cite_start]Stay tuned for updates![cite: 702].

## 📚 Citation
If you use this work, please cite our paper:

```bibtex
@article{Munsif2024Optimized,
  title={Optimized efficient attention-based network for facial expressions analysis in neurological health care},
  author={Munsif, Muhammad and Sajjad, Muhammad and Ullah, Mohib and Tarekegn, Adane Nega and Cheikh, Faouzi Alaya and Tsakanikas, Panagiotis and Muhammad, Khan},
  journal={Computers in Biology and Medicine},
  pages={108822},
  year={2024},
  publisher={Elsevier},
  doi={10.1016/j.compbiomed.2024.108822}
}
