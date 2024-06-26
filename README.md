# Gesture-Recognition-Project

# Problem Statement:

Develop a deep learning model for video action recognition capable of accurately classifying human actions or activities in video sequences. The model should be able to differentiate between various actions such as walking, running, jumping, etc., and achieve high accuracy in classifying these actions.

Recognising 5 different hand gestures to control a smart TV. We need to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

- Thumbs up: Increase the volume
- Thumbs down: Decrease the volume
- Left swipe: 'Jump' backwards
- Right swipe: 'Jump' forward
- Stop: Pause the movie

The training data consists of a few `hundred videos categorised into one of the five classes`. Each video (typically 2-3 seconds long) is divided into a sequence of `30 frames(images)`. These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

# Overview:
The objective of this project is to create a robust deep learning model that can effectively identify and classify human actions or activities in video clips.

The proposed model architecture will leverage convolutional neural networks (CNNs) for spatial feature extraction and recurrent neural networks (RNNs) for capturing temporal dependencies. CNNs will extract spatial features from individual frames, while RNNs will analyze sequences of features to understand the temporal relationships between frames.

The dataset will consist of video clips annotated with corresponding action labels. The dataset will be divided into training, validation, and test sets for model training, validation, and evaluation.

# Expected Outcome:

The expected outcome is a deep learning model that can accurately classify human actions in video sequences, achieving high classification accuracy on the test set. This model will have practical applications in various domains, including surveillance systems, human-computer interaction interfaces, and sports analytics.

# Model Architecture:

- The model architecture consists of a combination of convolutional neural networks (CNNs) and recurrent neural networks (RNNs).
- ResNet50, a pre-trained CNN, is used as the backbone for feature extraction from individual frames.
- A CNN layer with a 2x2 kernel and 64 filters is added after ResNet50 for additional spatial feature extraction.
- The CNN output is then fed into a stack of two SimpleRNN layers, which capture temporal dependencies in the video sequences.
- Finally, a Dense layer with a softmax activation function is used for multi-class classification.

# Training Configuration:

- Stochastic Gradient Descent (SGD) optimizer is used for model optimization.
- Categorical cross-entropy loss function is used as the optimization objective.
- Learning rate reduction on plateau is implemented using the ReduceLROnPlateau callback.
- The model is trained for 20 epochs with a batch size of 10.

# Model Evaluation:

- Training and validation data are generated using a custom data generator.
- Model performance metrics include categorical cross-entropy loss and categorical accuracy.
- Training progress and performance are visualized using loss curves.

# Performance:

- The model achieves high training accuracy, with categorical accuracy reaching 100%.
- Validation accuracy is also high, reaching up to 97% on some epochs.

# Contributers:
- Zeba Firdouse
-  Rajesh
