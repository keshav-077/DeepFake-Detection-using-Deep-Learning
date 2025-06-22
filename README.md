<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <h1>🎭 Deepfake Detection Using EfficientNet-B0 & BiLSTM</h1>
  <p>
    This project showcases an advanced deepfake detection pipeline that combines the strengths of Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs). It leverages <strong>EfficientNet-B0</strong> for spatial feature extraction and <strong>BiLSTM</strong> for capturing temporal dependencies across video frames.
  </p>

  <div class="section">
    <h2>📦 Dataset</h2>
    <p>
      We use the <strong><a href="https://www.kaggle.com/datasets">Celeb-DF v2</a></strong> dataset, which contains over 5,900 high-resolution videos of both real and deepfake celebrities.
    </p>
    <ul>
      <li>10-second long video clips with frame-level detail</li>
      <li>Rich facial expressions and diverse manipulations</li>
      <li>Perfect for benchmarking deepfake detection algorithms</li>
    </ul>
  </div>

  <div class="section">
    <h2>⚙️ Preprocessing Pipeline</h2>
    <ol>
      <li><strong>Frame Extraction:</strong> Convert each video into image sequences</li>
      <li><strong>Face Detection:</strong> Crop facial regions using Haar Cascades or MTCNN</li>
      <li><strong>Resizing & Normalization:</strong> Resize to 224×224 and scale pixel values to [0, 1]</li>
      <li><strong>Augmentation:</strong> Apply random flips, rotations, and color jittering</li>
    </ol>
  </div>

  <div class="section">
    <h2>🧠 Model Architecture</h2>
    <h3>1. EfficientNet-B0</h3>
    <p>
      A scalable CNN architecture used for extracting spatial features from each video frame. It uses compound scaling to optimize depth, width, and resolution.
    </p>

    <h3>2. BiLSTM</h3>
    <p>
      A bidirectional LSTM captures forward and backward temporal dependencies across the frame sequence, allowing the model to detect subtle inconsistencies indicative of deepfakes.
    </p>

    <h3>3. Classification</h3>
    <p>
      Final output is passed through a dense layer to predict whether the input video is <strong>Real</strong> or <strong>Fake</strong>.
    </p>
  </div>

  <div class="section">
    <h2>🚀 How It Works</h2>
    <pre>
🎥 Input Video
   └──> 🎞 Frame Extraction
            └──> 🧍 Face Detection
                     └──> 🧠 EfficientNet-B0 (per frame)
                              └──> 🔁 BiLSTM (sequence analysis)
                                       └──> 🟢 Classification: Real / Fake
    </pre>
  </div>

  <div class="section">
    <h2>🧪 Experimental Setup</h2>
    <ul>
      <li><strong>Processor:</strong> Intel Core i7-13900H</li>
      <li><strong>GPU:</strong> NVIDIA RTX 4060 (8GB VRAM)</li>
      <li><strong>RAM:</strong> 16 GB</li>
      <li><strong>OS:</strong> Windows 11</li>
      <li><strong>Frameworks:</strong> Python, TensorFlow, Keras</li>
    </ul>
  </div>

  <div class="section">
    <h2>📊 Performance Metrics</h2>
    <ul>
      <li><strong>Accuracy:</strong> Overall correctness of predictions</li>
      <li><strong>Precision:</strong> Correctly identified deepfakes out of all predicted deepfakes</li>
      <li><strong>Recall:</strong> Correctly identified deepfakes out of all actual deepfakes</li>
      <li><strong>F1 Score:</strong> Balance between precision and recall</li>
    </ul>
  </div>

  <div class="section">
    <h2>✅ Key Features</h2>
    <ul>
      <li>Combines CNN and RNN for spatio-temporal deepfake detection</li>
      <li>Real-time capable with high generalization on unseen data</li>
      <li>Efficient, lightweight design using pretrained components</li>
    </ul>
  </div>

  <div class="section">
    <h2>📌 Future Scope</h2>
    <ul>
      <li>Integrate audio-based deepfake detection</li>
      <li>Deploy model on mobile or edge devices</li>
      <li>Extend to additional datasets like FaceForensics++</li>
    </ul>
  </div>

  <div class="section">
    <h2>📬 Contact</h2>
    <p>
      For collaboration or inquiries, feel free to connect via <a href="https://github.com/your-profile">GitHub</a> or email.
    </p>
  </div>

</body>
</html>
