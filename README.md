# Fashion-MNIST Classification Project

## 🧾 Overview

This deep learning project uses the Fashion-MNIST dataset to train a neural network that classifies grayscale images of clothing into one of ten categories. The aim is to build a solid baseline model, explore model performance, and eventually extend the project to include natural language tasks such as fashion captioning.

---

## 📂 Dataset

* **Source**: Fashion-MNIST (by Zalando, available in TensorFlow/Keras)
* **Train Set**: 60,000 images
* **Test Set**: 10,000 images
* **Image Size**: 28x28 pixels (grayscale)
* **Classes**:

  ```
  0: T-shirt/top    5: Sandal
  1: Trouser        6: Shirt
  2: Pullover       7: Sneaker
  3: Dress          8: Bag
  4: Coat           9: Ankle boot
  ```

---

## 🧠 Model Architecture

* **Type**: Sequential neural network
* **Layers**:

  * `Flatten`: Converts 28x28 image to 784-dim vector
  * `Dense(32, activation='relu')`: Fully connected layer (25,120 parameters)
  * `Dense(10, activation='softmax')`: Output layer (10 classes)
* **Total Parameters**: 25,450
* **Optimizer**: Adam
* **Loss Function**: Sparse Categorical Crossentropy
* **Metric**: Accuracy

---

## 📈 Training Summary

* **Epochs**: 10

| Epoch | Accuracy | Loss   |
| ----- | -------- | ------ |
| 1     | 0.8023   | 0.7316 |
| 5     | 0.8702   | 0.3585 |
| 10    | 0.8845   | 0.3221 |

---

## ✅ Results

* **Test Accuracy**: **87%**
* **Classification Metrics (Macro Avg)**:

  * Precision: \~0.87
  * Recall: \~0.87
  * F1-Score: \~0.87
  * Support: 10,000 images
* **Per-Class Observations**:

  * High F1-Score: Ankle boot (0.95), Trouser (0.93)
  * Lower F1-Score: Shirt (0.65), Pullover (0.72)

---

## 🔍 Confusion Matrix Insights

* Strong diagonal (many correct predictions)
* Common misclassifications:

  * Pullover ↔ Shirt
  * Sandal ↔ Sneaker

---

## 🖼 Visualizations

* **Confusion Matrix**: Heatmap of predicted vs. true labels
* **Sample Predictions**:

  * ✅ Correct: Ankle boot → Ankle boot, Trouser → Trouser
  * ❌ Incorrect: Sandal → Sneaker, Pullover → Shirt

---

## ⚙️ Requirements

* **Python** 3.x
* **Libraries**:

  ```bash
  pip install tensorflow numpy matplotlib seaborn scikit-learn
  ```

---

## 🚀 Future Improvements

* Upgrade to a Convolutional Neural Network (CNN) for better accuracy
* Introduce data augmentation to increase generalization
* Extend to NLP: generate fashion-related captions using models like BERT or GPT

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributions

Contributions are welcome! Open an issue or submit a pull request.

---

## 📬 Contact

For any questions, feel free to reach out via [GitHub](https://github.com/VipinMI2024).

---

**Built by Vipin Mishra - [GitHub](https://github.com/VipinMI2024)**
