# Machine-Learning-class-project-Vid-games-
🎮 Video Game Hit vs. Non-Hit Prediction
Machine Learning Classification Project
<p align="center"> <img src="https://img.shields.io/badge/Python-3.10-blue"/> <img src="https://img.shields.io/badge/Machine%20Learning-Classification-orange"/> <img src="https://img.shields.io/badge/Status-Completed-success"/> </p>
🔍 Project Overview
<!-- ===================== HERO ===================== -->
<div align="center">

# 🎮 What Makes a Video Game a “Hit”?
### A Machine Learning Classification Project (Hit vs. Non-Hit)

<a href="https://www.kaggle.com/datasets/thedevastator/discovering-hidden-trends-in-global-video-games">
  <img alt="Dataset" src="https://img.shields.io/badge/Dataset-Kaggle-blue">
</a>
<img alt="Python" src="https://img.shields.io/badge/Language-Python-informational">
<img alt="ML" src="https://img.shields.io/badge/ML-Classification-orange">
<img alt="Best Model" src="https://img.shields.io/badge/Best%20Model-Random%20Forest-success">

<br/>

<p>
Predict whether a game is a <b>Hit</b> (Review ≥ 75) using platform, genre, publisher, year, and global/regional sales.
</p>

</div>

---

## 🔥 TL;DR Results (from our final model evaluation)
<div align="center">

<!-- KPI CARDS -->
<table>
  <tr>
    <td align="center" style="padding:12px 18px; border:1px solid #ddd; border-radius:14px;">
      <div style="font-size:13px; color:#666;">Best Model</div>
      <div style="font-size:22px;"><b>Random Forest</b></div>
    </td>
    <td align="center" style="padding:12px 18px; border:1px solid #ddd; border-radius:14px;">
      <div style="font-size:13px; color:#666;">Accuracy</div>
      <div style="font-size:22px;"><b>80%</b></div>
    </td>
    <td align="center" style="padding:12px 18px; border:1px solid #ddd; border-radius:14px;">
      <div style="font-size:13px; color:#666;">ROC-AUC</div>
      <div style="font-size:22px;"><b>0.81</b></div>
    </td>
    <td align="center" style="padding:12px 18px; border:1px solid #ddd; border-radius:14px;">
      <div style="font-size:13px; color:#666;">Hit Recall (Class 1)</div>
      <div style="font-size:22px;"><b>0.94</b></div>
    </td>
  </tr>
</table>

</div>

> **Key takeaway:** Models were generally better at identifying **hits** than **non-hits**, even after using class weights.

---

## 🎯 Problem Statement
Can video games be classified as a **“hit”** or **“non-hit”** using attributes such as **platform, genre, publisher, and global sales**?

### Hit Definition (Metacritic-style threshold)
- **Hit (1):** Review score ≥ **75**
- **Non-Hit (0):** Review score < **75**

---

## 📊 Dataset
**Discovering Hidden Trends in Global Video Games** (Kaggle)  
- **Original rows:** 1,907  
- **After cleaning:** **1,878** (dropped 31 missing values)  
- **Variables:** 13 total (categorical + numerical)

🔗 Kaggle: https://www.kaggle.com/datasets/thedevastator/discovering-hidden-trends-in-global-video-games

---

## 🧹 Data Preparation
- Dropped missing values (31 rows) → **1,878** rows remaining
- Created target variable: `is_hit = 1 if review >= 75 else 0`
- **Train/Test split:** 80/20 (consistent across all models)
- Used **class weights** to address imbalance (hit vs non-hit)
- Dropped leakage/ID columns: **Index**, **Rank** (Rank lets the model “cheat”)

---

## 🧠 Models Tested
- Logistic Regression
- Naive Bayes
- Decision Tree
- Random Forest (best overall)

---

## 🧪 Performance Summary (Test Set)

### Overall (Accuracy + ROC-AUC)
| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | **73%** | **0.780** |
| Decision Tree | **~70%** | **0.756** |
| Random Forest | **80%** ✅ | **0.81** |
| Naive Bayes | **~67%** | **0.843** |

> Note: Naive Bayes had the **highest AUC (0.843)** but lower overall accuracy and different error tradeoffs.

---

### Class-Level Metrics (Precision / Recall / F1)
**Logistic Regression**
| Class | Precision | Recall | F1 |
|---|---:|---:|---:|
| Non-Hit (0) | 0.48 | 0.68 | 0.56 |
| Hit (1) | 0.87 | 0.74 | 0.80 |

**Decision Tree**
| Class | Precision | Recall | F1 |
|---|---:|---:|---:|
| Non-Hit (0) | 0.45 | 0.71 | 0.55 |
| Hit (1) | 0.87 | 0.69 | 0.77 |

**Random Forest (Best Accuracy)**
| Class | Precision | Recall | F1 |
|---|---:|---:|---:|
| Non-Hit (0) | 0.71 | 0.40 | 0.51 |
| Hit (1) | 0.82 | 0.94 | 0.88 |

**Naive Bayes**
| Class | Precision | Recall | F1 |
|---|---:|---:|---:|
| Non-Hit (0) | 0.91 | 0.38 | 0.53 |
| Hit (1) | 0.61 | 0.96 | 0.74 |

---


### 📊 Accuracy by Model

**Logistic Regression — 0.73**  
<img src="https://progress-bar.xyz/73/?scale=100&title=&width=400" />

**Decision Tree — 0.70**  
<img src="https://progress-bar.xyz/70/?scale=100&title=&width=400" />

**Random Forest ⭐ — 0.80**  
<img src="https://progress-bar.xyz/80/?scale=100&title=&width=400" />

**Naive Bayes — 0.67**  
<img src="https://progress-bar.xyz/67/?scale=100&title=&width=400" />



---

### 👥 Team
Edward Dai · Meghna Prakash · Alex Huang · Srinidhi Chevvuri · Preme Chinpattanakul
