🧠 ** HMS EEG Brain Activity Classification **

EEGNet vs KAN vs Pretrained Vision Models

Deep learning experiments for classifying harmful brain activity from EEG spectrograms, based on the HMS Kaggle dataset.

🧪 Do EEG-specific models beat large ImageNet-pretrained networks?
This repository explores the answer.

⸻

📊 Dataset
	•	HMS – Harmful Brain Activity Classification (Kaggle)
	•	17,089 EEG samples
	•	4-channel EEG spectrograms
	•	6 highly imbalanced classes
	•	Seizure
	•	LPD
	•	GPD
	•	LRDA
	•	GRDA
	•	Other

⸻

🧠 Models

🔹 Pretrained Baselines
	•	ResNet
	•	DenseNet
	•	EfficientNet
	•	Vision Transformer (ViT)

🔹 EEG-Specialized Models
	•	EEGNet – lightweight, EEG-aware convolutional network
	•	KAN – Kolmogorov-Arnold Network with learnable activation functions

⸻

🔄 Two Training Philosophies

🧩 1. Large Models → Use Augmentation
	•	MixUp data augmentation
	•	KL Divergence loss
	•	Simple class weighting

✔ Improves generalization for large pretrained vision models

⸻

🧠 2. EEG Models → Preserve Signal
	•	No data augmentation
	•	Soft Focal Loss
	•	Aggressive class balancing

✔ Preserves EEG temporal and frequency structure

⚠️ Mixing EEG signals can destroy meaningful physiological patterns.
