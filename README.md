🧠 HMS EEG Brain Activity Classification

EEGNet vs KAN vs Pretrained Vision Models

Deep learning experiments for classifying harmful brain activity from EEG spectrograms, based on the HMS Kaggle dataset.

🧪 Do EEG-specific models beat large ImageNet-pretrained networks?
This repo explores the answer.

⸻

📊 Dataset
	•	HMS – Harmful Brain Activity Classification (Kaggle)
	•	17,089 EEG samples
	•	4-channel EEG spectrograms
	•	6 highly imbalanced classes (Seizure, LPD, GPD, LRDA, GRDA, Other)

⸻

🧠 Models

🔹 Pretrained Baselines

ResNet · DenseNet · EfficientNet · Vision Transformer

🔹 EEG-Specialized
	•	EEGNet – lightweight, EEG-aware CNN
	•	KAN – Kolmogorov-Arnold Network with learnable activations

⸻

🔄 Two Training Philosophies

🧩 1. Large Models → Use Augmentation
	•	MixUp augmentation
	•	KL Divergence loss
	•	Simple class weighting
✔ Helps generalization of large pretrained models

⸻

🧠 2. EEG Models → Preserve Signal
	•	NO data augmentation
	•	Soft Focal Loss
	•	Aggressive class balancing
✔ Keeps EEG temporal & frequency structure intact

⚠️ Mixing EEG signals can destroy meaningful physiological patterns.
