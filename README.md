# DeepFake-Detection-using-Deep-Learning

🔍 Deepfake Detection Using EfficientNet-B0 and BiLSTM
A robust deepfake detection system that leverages EfficientNet-B0 for spatial feature extraction and Bidirectional LSTM (BiLSTM) for capturing temporal dependencies across video frames. Built and trained using the Celeb-DF v2 dataset, this project targets the identification of manipulated facial videos with high precision.

#📌 Project Highlights

Dataset: Celeb-DF v2 (5,900+ high-quality real and fake celebrity videos)

Model Architecture: EfficientNet-B0 + BiLSTM + Dense Classification Layer

Preprocessing: Frame extraction, face detection, resizing, normalization, and data augmentation

Training Hardware: NVIDIA RTX 4050 GPU

Frameworks & Tools: Python, TensorFlow, Keras, NumPy, OpenCV, Matplotlib, Kaggle API

#🧠 Methodology
1. Preprocessing
Frame Extraction: Videos split into individual frames.

Face Detection: Facial regions isolated using MTCNN/Haar Cascades.

Resizing & Normalization: Standardized to 224×224 and scaled to [0, 1].

Data Augmentation: Random flips, rotations, and color jitter to prevent overfitting.

2. Architecture
📸 EfficientNet-B0
Used as the feature extractor to process each frame.

Outputs deep visual embeddings that capture spatial inconsistencies common in deepfakes.

⏱ BiLSTM
Processes sequences of embeddings (frames) in both forward and backward directions.

Captures temporal inconsistencies between frames that reveal manipulations.

🧾 Classifier
Final dense layer outputs binary classification: Real or Fake.
