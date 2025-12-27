# 🧠 HMS EEG Brain Activity Classification
## EEGNet vs KAN vs Pretrained Vision Models

Deep learning experiments for classifying harmful brain activity from EEG spectrograms, based on the HMS Kaggle dataset. For dataset please refer to this link https://github.com/aisyahkhns/HMS-Brain-Classification

## 📊 Dataset

**HMS – Harmful Brain Activity Classification (Kaggle)**

- 17,089 EEG samples
- 4-channel EEG spectrograms
- 6 highly imbalanced classes:
  - Seizure
  - LPD (Low Period Discharge)
  - GPD (Generalized Period Discharge)
  - LRDA (Lateralized Rhythmic Delta Activity)
  - GRDA (Generalized Rhythmic Delta Activity)
  - Other

---

## 🧠 Models Compared

### Pretrained Vision Models (ImageNet)
- ResNet
- DenseNet
- EfficientNet
- Vision Transformer (ViT)

### EEG-Specialized Models
- **EEGNet** – Lightweight, EEG-aware convolutional network
- **KAN** – Kolmogorov-Arnold Network with learnable activation functions

---

## 🔄 Training Strategies

### Strategy 1: Large Models + Augmentation
Best for: Pretrained vision models

- Data augmentation: MixUp
- Loss function: KL Divergence
- Class balancing: Simple weighting
- Why: Improves generalization on large pretrained models

### Strategy 2: EEG Models + Signal Preservation
Best for: EEG-specialized architectures

- Data augmentation: None
- Loss function: Soft Focal Loss
- Class balancing: Aggressive weighting
- Why: Preserves physiological patterns in EEG signals

## 📈 Results & Insights
<img width="3570" height="2677" alt="results_table_final" src="https://github.com/user-attachments/assets/5e7ea6cc-0bfe-41d5-8c91-824053b2f30b" />


## 📚 References

- HMS Kaggle Competition: [link]
