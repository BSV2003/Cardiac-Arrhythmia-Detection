# Ensemble Deep Learning Framework for Robust Arrhythmia Detection

> 🏆 **Conference Accepted Work**  
> This project was presented and accepted at the **3rd International Conference on Industry 4.0 Technology (I4Tech2025), IEEE Conference #64670**  
> 📄 Paper Title: *Ensemble Deep Learning Framework for Robust Arrhythmia Detection*

📌 Abstract

Cardiac arrhythmias, characterized by irregular heart rhythms, are a leading cause of morbidity and mortality worldwide, often leading to stroke, heart failure, or sudden cardiac arrest. Accurate and early detection plays a vital role in patient safety and treatment.

This work introduces a comparative deep learning framework for ECG-based arrhythmia detection using three architectures — Convolutional Neural Networks (CNN), Long Short-Term Memory Networks (LSTM), and a hybrid CNN-Bidirectional LSTM (CNN-BiLSTM). The models were trained and evaluated on the MIT-BIH Arrhythmia Dataset, adhering to the AAMI EC57 standard for heartbeat classification.

Experimental results highlight that the CNN-BiLSTM model achieved superior performance with 98.71% accuracy and a 92.72% macro F1-score, outperforming both standalone CNN and LSTM. The hybrid model demonstrated significant improvements in identifying minority heartbeat classes such as Supraventricular (S) and Fusion (F) beats, which are critical for real-world clinical deployment.

The study concludes that ensemble and hybrid deep learning architectures provide a more robust solution for automated arrhythmia detection, with strong potential for integration into wearable IoMT (Internet of Medical Things) devices and real-time healthcare monitoring systems.

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
