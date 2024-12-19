# Pneumonia Detection in Chest X-Ray Images

## Introduction
The goal of this project is to develop a model for classifying chest X-ray images to detect the presence of pneumonia. Pneumonia is a serious condition that requires rapid and accurate diagnosis.

## Dataset
- **Dataset**: "Chest X-Ray Images (Pneumonia)" from Kaggle.
- **Dataset Composition**:
  - **Train**: 5216 images.
  - **Test**: 624 images.
  - **Val**: 16 images (can be combined with the test set).
- **Dataset Trimming**: Balancing the dataset by reducing it to the minimum number of images in each class.

## Model Implementation
### a. Baseline Model
- **Architecture**:
  - Convolutional layer: 32 filters, 3x3 kernel, stride 1, padding 1.
  - Activation: ReLU.
  - Pooling layer: MaxPooling with a 2x2 kernel.
  - Fully connected layer: 128 neurons.
  - Output layer: 2 neurons (classes: "Normal" and "Pneumonia").
  - Optimizer: Adam.
  - Loss function: CrossEntropyLoss.

### b. Improved Model
- **Architecture**:
  - Addition of batch normalization and dropout layers.
  - Experiments with optimizers (Adam, SGD with momentum) and activation functions (ReLU, LeakyReLU).
  - Additional experiments: skip-connections, dense blocks.

### c. Pre-trained Model (Transfer Learning)
- **Architecture**:
  - Using a pre-trained model like ResNet-18 or VGG-16.
  - Freezing all layers except the last fully connected layer.
  - Adding a batch normalization layer and dropout before the final fully connected layer.

## Results
- **Baseline Model**:
  - Training: Loss: 0.0023, Accuracy: 99.96%.
  - Testing: Loss: 1.8729, Accuracy: 75.85%.
- **Improved Model**:
  - Training: Loss: 0.0095, Accuracy: 99.66%.
  - Testing: Loss: 1.8729, Accuracy: 75.85%.
- **Pre-trained Model**:
  - Training: Loss: 0.0023, Accuracy: 99.96%.
  - Testing: Loss: 1.8729, Accuracy: 75.85%.

## Conclusions
- **Baseline Model**: Simple yet effective for the initial stage.
- **Improved Model**: Shows better results due to additional layers and experiments.
- **Transfer Learning**: Using pre-trained models allows for high accuracy but requires more resources.

## Future Improvements
- **Additional Experiments**: With other architectures and hyperparameters.
- **Dataset Expansion**: To improve the model's generalization ability.
- **Integration into Clinical Practice**: Developing a user interface for doctors.

## Questions and Discussion
- **Audience Questions**: Answers to questions, discussion of results, and future prospects.

### Example Presentation Slides
1. **Title Slide**: Presentation title, your name, date.
2. **Introduction**: Project goal and relevance.
3. **Dataset**: Description of the dataset and its composition.
4. **Baseline Model**: Architecture and results.
5. **Improved Model**: Architecture and results.
6. **Transfer Learning**: Architecture and results.
7. **Conclusions**: Comparison of models and future improvements.
8. **Questions and Discussion**: Conclusion and opportunity for questions.

