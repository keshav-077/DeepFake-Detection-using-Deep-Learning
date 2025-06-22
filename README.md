<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Deepfake Detection using EfficientNet-B0 & BiLSTM</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 40px;
      background-color: #f8f9fa;
      color: #212529;
    }
    h1, h2, h3, h4 {
      color: #0d6efd;
    }
    code {
      background-color: #e9ecef;
      padding: 2px 4px;
      border-radius: 4px;
    }
    pre {
      background: #e9ecef;
      padding: 10px;
      border-radius: 5px;
      overflow-x: auto;
    }
  </style>
</head>
<body>

  <h1>🎭 Deepfake Detection using EfficientNet-B0 and BiLSTM</h1>

  <p>
    This project presents a deepfake detection system that integrates <strong>EfficientNet-B0</strong> for extracting spatial features and 
    <strong>BiLSTM</strong> for modeling temporal dependencies across video frames. The model is trained and evaluated on the 
    <strong>Celeb-DF v2</strong> dataset.
  </p>

  <h2>📁 3. Methodology</h2>

  <h3>3.1 Dataset</h3>
  <p>
    The Celeb-DF v2 dataset, known for evaluating deepfake detection models, includes over 5,900 high-quality videos (10s each) 
    of real and fake celebrities. It contains corresponding facial images for each video and is publicly available on Kaggle. 
    The dataset features deepfakes generated using state-of-the-art techniques, making it ideal for robust evaluation.
  </p>

  <h3>3.2 Preprocessing</h3>
  <ol>
    <li><strong>Video Frame Extraction:</strong> Converted videos to individual frames to enable frame-by-frame analysis.</li>
    <li><strong>Resizing & Normalization:</strong> Frames resized to 224x224 and normalized to [0, 1].</li>
    <li><strong>Data Augmentation:</strong> Applied flipping, rotation, and color jittering to prevent overfitting.</li>
    <li><strong>Face Detection:</strong> Used Haar Cascades or MTCNN to extract and isolate facial regions in each frame.</li>
  </ol>

  <h3>3.3 Algorithm</h3>
  <p>
    The system uses <strong>EfficientNet-B0</strong> (CNN) to extract spatial features and <strong>BiLSTM</strong> (RNN) to capture forward and backward temporal 
    dependencies across frames.
  </p>

  <h4>EfficientNet-B0</h4>
  <p>
    EfficientNet-B0 balances model depth, width, and resolution using compound scaling. It efficiently extracts visual cues such 
    as texture and motion inconsistencies commonly present in deepfakes.
  </p>

  <h4>BiLSTM</h4>
  <p>
    A bidirectional RNN that analyzes sequences in both forward and backward directions to learn fine-grained temporal changes 
    between video frames.
  </p>

  <h4>Mathematical Formulation:</h4>
  <pre>
  Forget Gate: Ft = σ(Wf * [ht-1 , xt] + bf)
  Input Gate: It = σ(Wi * [ht-1 , xt] + bi)
  Cell State Update: Ct = ft * Ct-1 + it * Ct
  Output Gate: Ot = σ(Wo * [ht-1, xt] + bo)
  Hidden State Update: ht = ot * tanh(Ct)
  </pre>

  <h3>3.4 Architecture and Working</h3>
  <ul>
    <li><strong>EfficientNet-B0:</strong> Extracts features from each frame.</li>
    <li><strong>BiLSTM:</strong> Processes the temporal sequence of frame features.</li>
    <li><strong>Classifier:</strong> Final output layer predicts Real or Fake.</li>
  </ul>

  <h4>Working Steps:</h4>
  <ol>
    <li>Extract frames from video</li>
    <li>Detect and crop face</li>
    <li>Pass each frame through EfficientNet-B0</li>
    <li>Feed sequence to BiLSTM</li>
    <li>Output final prediction: Real or Deepfake</li>
  </ol>

  <h3>3.5 Flow Chart</h3>
  <ul>
    <li>📈 Data Flow Diagram (DFD)</li>
    <li>🧠 Architecture of EfficientNet-B0</li>
    <li>🔁 Architecture of BiLSTM</li>
  </ul>

  <h2>🔬 4. Experimentation and Results</h2>

  <h3>4.1 Experimental Setup</h3>
  <ul>
    <li><strong>Processor:</strong> Intel Core i7-13900H</li>
    <li><strong>GPU:</strong> NVIDIA RTX 4060 (8GB VRAM)</li>
    <li><strong>RAM:</strong> 16 GB</li>
    <li><strong>Storage:</strong> 1TB SSD</li>
    <li><strong>OS:</strong> Windows 11</li>
    <li><strong>Frameworks:</strong> Python, TensorFlow, Keras</li>
  </ul>

  <h3>4.2 Performance Metrics</h3>
  <ul>
    <li><strong>Precision:</strong> Correct positive predictions out of all predicted positives.</li>
    <li><strong>Recall:</strong> Correct positive predictions out of all actual positives.</li>
    <li><strong>F1-Score:</strong> Harmonic mean of Precision and Recall.</li>
    <li><strong>Accuracy:</strong> Overall correctness of the model.</li>
  </ul>

  <h3>4.3 Results</h3>
  <p>
    The model demonstrates high accuracy and strong performance across all metrics on the Celeb-DF v2 dataset, 
    especially in detecting manipulated (deepfake) content, validating the effectiveness of the combined 
    EfficientNet-B0 + BiLSTM architecture.
  </p>

  <h2>📬 Contact</h2>
  <p>
    For inquiries, collaborations, or feedback, feel free to reach out via GitHub or email.
  </p>

</body>
</html>
