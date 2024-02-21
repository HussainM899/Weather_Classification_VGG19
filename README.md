# Weather Classification using VGG19

## Introduction
This project aims to classify images of weather into distinct categories using the VGG19 deep learning model. Below are the key components and findings of the project:

## Dataset
The dataset used in this project consists of weather images classified into various weather conditions. This dataset includes common weather categories such as sunny, cloudy, rainy, etc.

## Project Dependencies

### Data Handling & Visualization:
- matplotlib
- numpy
- cv2

### Deep Learning:
- tensorflow.keras with specific use of VGG19 and Model

### Data Preprocessing:
- ImageDataGenerator
- LabelEncoder
- LabelBinarizer

### Model Evaluation:
- classification_report
- confusion_matrix
- plot_confusion_matrix

### Utilities:
- os
- tqdm
- shuffle
- train_test_split

## Methods and Approach

### Data Preprocessing:
Images are loaded and preprocessed to fit the input requirements of the VGG19 model. Label encoding and one-hot encoding are applied to convert category labels into a numerical format.

### Data Augmentation:
Implemented to improve model generalization and prevent overfitting.

### Model:
Utilized the pre-trained VGG19 model as a base, adding custom layers to tailor it for the weather classification task.

### Training:
The model is compiled and trained using the Adam optimizer and categorical crossentropy loss function, with accuracy as the metric.

## Training and Validation Results
- The model was trained for 15 epochs, achieving a final training accuracy of approximately 99%.
- Validation accuracy peaked at 94%, with the model demonstrating a high ability to generalize.
- Training and validation losses showed a steady decrease, indicating learning progress.

## Testing Results
- The model achieved a test accuracy of 93.67% with a loss of 21.31%.
- The high test accuracy closely aligns with the validation accuracy, further validating the model's generalization capability.

## Classification Report
- The classification report showed high precision and recall scores for each category, with an overall accuracy of 94%.
- The f1-score for each class was consistently high, demonstrating the model's balanced performance across different weather conditions.

## Insights
- The model's performance is robust, but there may be room for improvement in specific categories where precision or recall could be increased.
- The early stopping callback prevented overfitting, as indicated by the close performance metrics between training and validation.

## Conclusion
The VGG19 model has proven to be effective for weather image classification, showing promise for real-world applications. Future work could involve expanding the dataset, implementing further data augmentation techniques, or experimenting with different model architectures.
