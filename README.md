🐶🐱 Cat vs Dog Image Classification

This project implements a Convolutional Neural Network (CNN) model to classify images of cats and dogs using TensorFlow and Keras.
📁 Dataset

The dataset used contains:

    19,910 training images

    5,090 validation images

    2 classes: Cats and Dogs

Images were preprocessed and split into train/, validation/, and test/ folders accordingly.
🧠 Model Architecture

The architecture includes the following layers:

    Input Layer: Conv2D with 32 filters and ReLU activation

    Three Convolutional Blocks:

        Each block includes Conv2D layers with increasing filters (64, 128, 256), followed by Batch Normalization, MaxPooling2D, and Dropout (rate=0.2)

    Fully Connected Layers:

        Flatten, Dense(512, activation='relu'), BatchNormalization, Dropout

    Output Layer:

        Dense(2, activation='softmax')

Alternative architectures like ResNet50 and DenseNet121 were also tested.
🏋️‍♀️ Training

    Epochs: 5

    Optimizer: Adam

    Loss: Categorical Crossentropy

    Learning Rate: 0.001

Training Accuracy Progress:

    Epoch 1: 76.96%

    Epoch 3: 84.48%

    Epoch 5: 86.33%

📊 Evaluation
Classification Report (on test set of 2,500 images):
Class	Precision	Recall	F1-Score
Cat	0.84	0.92	0.87
Dog	0.91	0.82	0.86

    Overall Accuracy: 87%

    Macro Average F1-Score: 87%

Confusion Matrix

The confusion matrix shows a balanced performance across both classes with slight misclassifications.
📈 Visualizations

    Loss and Accuracy Curves: Plotted for both training and validation sets across epochs

    Confusion Matrix: Visualized using a heatmap

✅ Conclusion

The CNN model achieved a strong performance on the binary classification task. Further improvements could involve:

    Data augmentation

    Hyperparameter tuning

    Transfer learning with deeper pretrained models
