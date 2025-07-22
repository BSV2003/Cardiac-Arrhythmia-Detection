# Ensemble Deep Learning Framework for Robust Arrhythmia Detection

> 🏥 A comparative deep learning framework for cardiac arrhythmia classification using ECG signals  
> 🧠 Includes CNN, LSTM, and CNN-BiLSTM models tested on the MIT-BIH Arrhythmia Dataset  
> 📊 Achieved **98.71% accuracy** and **92.72% macro F1-score** with CNN-BiLSTM  

---

## 📌 Abstract

Cardiac arrhythmias are irregular heart rhythms that can lead to stroke, heart failure, or sudden cardiac arrest. This project presents a deep learning-based ECG classification system using three architectures — **CNN**, **LSTM**, and **CNN-Bidirectional LSTM (CNN-BiLSTM)** — trained on the **MIT-BIH Arrhythmia Dataset** following the **AAMI standard**.

After comparative analysis:
- **CNN-BiLSTM** outperformed all models with **98.71% accuracy**
- Showed significant improvement in detecting **minority classes** like Supraventricular (S) and Fusion (F) beats
- Trained using advanced techniques like **dropout**, **learning rate scheduling**, and **gradient clipping**

---

## 🗃️ Dataset

- **Source**: MIT-BIH Arrhythmia Dataset from PhysioNet
- **Sampling Rate**: 360 Hz
- **Heartbeat Classes**:  
  - N: Normal  
  - S: Supraventricular  
  - V: Ventricular  
  - F: Fusion  
  - Q: Unknown

---

## 🏗️ Architectures Used

### 🔹 CNN
- Captures spatial features of ECG
- ReLU activations, pooling, dropout

### 🔹 LSTM
- Models temporal dependencies
- Suited for sequence-based anomaly detection

### 🔹 CNN-BiLSTM
- Hybrid model combining CNN for spatial and BiLSTM for bidirectional temporal learning
- Best results across all metrics

---

## 📈 Performance Comparison

| Model        | Test Accuracy | Macro F1-Score |
|--------------|---------------|----------------|
| CNN          | 97.70%        | 87.31%         |
| LSTM         | 96.77%        | 82.37%         |
| **CNN-BiLSTM** | **98.71%**    | **92.72%**     |

> 🔬 CNN-BiLSTM showed superior generalization, especially for rare arrhythmias.

---

## ⚙️ Training Details

- Optimizer: Adam
- Loss: Sparse Categorical Crossentropy
- Regularization: Dropout (0.3–0.5), Gradient Clipping, Early Stopping
- Learning Rate Scheduler: ReduceLROnPlateau

---

## 🧪 Evaluation Metrics

- Accuracy
- Precision, Recall, F1-score (Macro & Weighted)
- Per-class Accuracy
- Confusion Matrix

---

## 🚀 Future Enhancements

- Deploy on wearable devices (IoMT/Edge)
- Add explainability with Grad-CAM
- Test on larger datasets like PTB-XL
