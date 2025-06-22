# DeepFake-Detection-using-Deep-Learning

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body style="font-family: Arial, sans-serif; line-height: 1.6; margin: 20px;">

  <h1>🧠 Deepfake Detection Using EfficientNet-B0 and BiLSTM</h1>
  <p>
    A robust deepfake detection system combining <strong>EfficientNet-B0</strong> for spatial feature extraction and 
    <strong>BiLSTM</strong> for temporal modeling. Trained on the <strong>Celeb-DF v2</strong> dataset, this architecture accurately 
    distinguishes real videos from deepfakes by analyzing facial features across video frames.
  </p>

  <h2>📂 Dataset</h2>
  <p>
    <strong>Dataset:</strong> <a href="https://www.kaggle.com/datasets">Celeb-DF v2</a><br>
    - 5900+ high-quality real and deepfake videos (~10 seconds each)<br>
    - Includes facial images for in-depth analysis<br>
    - Publicly available via Kaggle API
  </p>

  <h2>⚙️ Preprocessing</h2>
  <ul>
    <li><strong>Frame Extraction:</strong> Extract individual frames from video.</li>
    <li><strong>Face Detection:</strong> Isolate faces using MTCNN/Haar Cascades.</li>
    <li><strong>Resizing & Normalization:</strong> Resize to 224x224 and scale to [0, 1].</li>
    <li><strong>Data Augmentation:</strong> Apply rotation, flipping, and color jitter.</li>
  </ul>

  <h2>🧠 Model Architecture</h2>
  <h4>1. EfficientNet-B0 (Feature Extraction)</h4>
  <p>
    Extracts deep spatial features from video frames using compound scaling for high performance and efficiency.
  </p>
  
  <h4>2. BiLSTM (Temporal Modeling)</h4>
  <p>
    Processes feature sequences in both directions to capture temporal inconsistencies that reveal deepfakes.
  </p>
  
  <h4>3. Classification Layer</h4>
  <p>
    Outputs a binary prediction (Real / Deepfake).
  </p>

  <h2>🔁 Workflow</h2>
  <ol>
    <li>Input video</li>
    <li>Extract frames</li>
    <li>Detect and crop face</li>
    <li>EfficientNet-B0 for each frame</li>
    <li>BiLSTM processes feature sequence</li>
    <li>Classification layer outputs result</li>
  </ol>

  <h2>🖥 Training Setup</h2>
  <ul>
    <li><strong>GPU:</strong> NVIDIA RTX 4050</li>
    <li><strong>Languages:</strong> Python</li>
    <li><strong>Frameworks:</strong> TensorFlow, Keras</li>
    <li><strong>Tools:</strong> OpenCV, Matplotlib, NumPy, Kaggle API</li>
  </ul>

 

  <h2>📈 Results</h2>
  <p>
    Achieved high accuracy and generalization on Celeb-DF v2. Capable of identifying subtle inconsistencies across video frames.
  </p>



  <h2>🤝 Acknowledgments</h2>
  <ul>
    <li> <a href="https://www.kaggle.com/datasets">Celeb-DF v2 Dataset</a></li>
    <li> TensorFlow / Keras communities</li>
    <li> OpenCV, MTCNN contributors</li>
  </ul>

  <h2>📬 Contact</h2>
  <p>For queries, feel free to reach out via GitHub or email.</p>

</body>
</html>

