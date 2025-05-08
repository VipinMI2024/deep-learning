Fashion-MNIST Classification Project
Overview
This project involves training a neural network to classify images from the Fashion-MNIST dataset into 10 categories of clothing items. The goal was to explore deep learning concepts and achieve a solid accuracy while setting the stage for future NLP-related extensions, such as generating fashion captions.
Dataset

Source: Fashion-MNIST dataset
Training Data: 60,000 grayscale images (28x28 pixels)
Test Data: 10,000 grayscale images (28x28 pixels)
Classes (10 categories):
0: T-shirt/top
1: Trouser
2: Pullover
3: Dress
4: Coat
5: Sandal
6: Shirt
7: Sneaker
8: Bag
9: Ankle boot



Model Architecture

Type: Sequential neural network
Layers:
Flatten: Converts 28x28 images to a 784-element vector
Dense (32 units, ReLU activation): 25,120 parameters
Dense (10 units, Softmax activation): 330 parameters


Total Parameters: 25,450 (94.41 KB)
Trainable Parameters: 25,450
Non-trainable Parameters: 0
Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy
Metrics: Accuracy

Training

Epochs: 10
Training Progress:
Epoch 1: Accuracy: 0.8023, Loss: 0.7316
Epoch 5: Accuracy: 0.8702, Loss: 0.3585
Epoch 10: Accuracy: 0.8845, Loss: 0.3221



Results

Test Accuracy: 87%
Classification Report:
Precision, Recall, F1-Score (Macro Avg): 0.87
Support: 10,000 images
Notable: Classes like T-shirt/top (0.83 F1-score) and Ankle boot (0.95 F1-score) performed well, while Shirt (0.65 F1-score) struggled.


Confusion Matrix:
Strong diagonal (correct predictions), but some confusion between similar classes (e.g., Pullover vs. Shirt, Sandal vs. Sneaker).


Sample Predictions:
Correct: Ankle boot predicted as Ankle boot, Trouser predicted as Trouser.
Incorrect: Sandal predicted as Sneaker, Pullover predicted as Shirt.



Visualizations

Confusion Matrix: Heatmap showing prediction distribution across classes.
Sample Predictions: Visualized 25 test images with actual vs. predicted labels.

Requirements

Python 3.x
Libraries:
TensorFlow/Keras
NumPy
Matplotlib
Seaborn
Scikit-learn



Future Improvements

Experiment with convolutional neural networks (CNNs) for better image classification.
Add data augmentation to improve model robustness.
Explore NLP extensions, such as using a pre-trained model like BERT to generate fashion captions based on predicted classes.

License
This project is licensed under the MIT License.
# deep-learning
