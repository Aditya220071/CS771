# CS771  – Learning with Prototypes (LwP)

## 📌 Introduction
This project was implemented as part of **CS771: Intro to Machine Learning (Fall 2024)**.  
We explored **Learning with Prototypes (LwP)** classifiers for sequential learning across evolving datasets, focusing on adapting to distributional changes while preserving past knowledge.
## 🎯 Objectives
1. **Sequential Training (Task 1)**  
   - Train an LwP chain on dataset **D1** and iteratively update using datasets **D2–D10**.  
   - Ensure no performance degradation on earlier datasets.  

2. **Handling Distribution Shifts (Task 2)**  
   - Extend to datasets **D11–D20**, originating from different distributions.  
   - Account for domain shift while maintaining generalization.  

3. **Research Component (Problem 2)**  
   - Study and present the NeurIPS 2021 paper *Lifelong Domain Adaptation via Consolidated Internal Distribution*.  
   - [🎥 Presentation Link](https://youtu.be/v6pdn3nURQs?si=q8y_rCxa-MOfMjWe)

## 📂 Dataset
- Derived from **CIFAR-10** image classification dataset (10 classes, 32×32 RGB images).  
- **D1**: labeled, **D2–D20**: unlabeled.  
- **D1–D10** share the same distribution, **D11–D20** are from different distributions.  

## 🛠️ Methodology

### 🔹 Task 1: Sequential LwP Chain
- **ResNet-18 (Feature Extractor)**  
  - Pretrained on ImageNet, features used for LwP.  
  - Accuracy: ~54%.  

- **Vision Transformer (ViT – Best Approach)**  
  - Patch embeddings + multi-head self-attention.  
  - Captured global dependencies effectively.  
  - Accuracy: ~95% average.  

### 🔹 Task 2: Distribution Differences
- **Noise Augmentation** (inspired by *Deja Vu: Continual Model Generalization*)  
  - Reduced bias, but accuracy gain was limited.  

- **ViT Transformer**  
  - Achieved ~88% accuracy across **D1–D20**.  

## 📊 Results
- **Task 1 (D1–D10)**: ViT achieved **95% accuracy**.  
- **Task 2 (D1–D20)**: ViT achieved **88% accuracy** under distribution shifts.  

## 🚀 Conclusion
- **ViT outperformed ResNet-18** for LwP on CIFAR-10.  
- Demonstrated strong performance in **sequential learning** and **domain adaptation**.  
- Showcased the effectiveness of **transformer-based models** in continual learning tasks.  

## 📖 References
- CIFAR-10 Dataset  
- ResNet-18: *Deep Residual Learning for Image Recognition*  
- Vision Transformer (ViT): *An Image is Worth 16x16 Words*  
- NeurIPS 2021: *Lifelong Domain Adaptation via Consolidated Internal Distribution*  

---

📌 *This project was completed as part of the course CS771 at IIT Kanpur.*
