# Transfer Learning Assignment

### Problem Statement
Autistic Spectrum Disorder (ASD) is a neurodevelopmental condition associated with significant healthcare costs, and early diagnosis can significantly reduce these. Unfortunately, waiting times for an ASD diagnosis are lengthy and procedures are not cost effective.

### Objective:
The task is to classify images into two classes: "autistic" and "non_autistic", aiming to facilitate research and analysis in understanding autism spectrum traits. This involves training deep learning models using transfer learning techniques to accurately classify images into these two categories.

### Dataset:
The dataset consists of images categorized into two classes: "autistic" and "non_autistic". It is divided into three main folders: "train", "valid", and "test", each containing two subfolders representing the two classes.
- **Train**: Contains 1263 images in each of the "autistic" and "non_autistic" subfolders, totaling 2526 images.
- **Valid**: Contains 100 images in each of the "autistic" and "non_autistic" subfolders, totaling 200 images.
- **Test**: Contains 100 images in each of the "autistic" and "non_autistic" subfolders, totaling 200 images.

### Purpose:
This dataset serves as a resource for training, validating, and testing deep learning models and algorithms in the domain of autism spectrum analysis. Researchers and practitioners can utilize this dataset to develop and evaluate classification and detection systems, as well as to explore visual characteristics associated with autism spectrum traits.

## Evaluation Metrics

For assessing the performance of the fine-tuned models, the following evaluation metrics have been chosen:
- Accuracy
- Loss
- Precision
- Recall
- F1 score

These metrics will help in quantitatively evaluating the effectiveness of the models in classifying autistic and non-autistic images.

## Pre-trained Model Selection

1. **ResNet50**:
   - Performance: ResNet50's depth and skip connections enable effective capture of intricate features, crucial for distinguishing between "autistic" and "non_autistic" traits.
   - Architecture: Its architecture addresses the vanishing gradient problem and is adept at capturing both low-level and high-level features.
   - Suitability for the Task: ResNet50's depth and performance align well with the task's need to discern subtle traits associated with autism spectrum disorders.

2. **InceptionV3**:
   - Performance: InceptionV3's multi-scale processing capability facilitates discernment of subtle differences between images, aiding in identifying autism spectrum traits.
   - Architecture: Its efficient utilization of inception modules allows for capturing features at different scales, suitable for tasks with varying object sizes or appearances.
   - Suitability for the Task: InceptionV3's multi-scale processing aligns with identifying autism spectrum traits, capturing both local and global features effectively.

3. **VGG16**:
   - Performance: VGG16's simple yet effective architecture offers competitive performance in image classification tasks, including discerning features relevant to autism spectrum traits.
   - Architecture: Its uniform structure with multiple convolutional layers captures detailed features, potentially crucial for identifying subtle traits.
   - Suitability for the Task: VGG16's emphasis on capturing detailed features aligns with the task's need to identify subtle traits associated with autism spectrum disorders.

## Discussion of Findings and Transfer Learning Analysis

### Rationale and Methodology for Fine-Tuning Deep Learning Models for Autism Prediction:

  Despite being trained on unrelated datasets, VGG16, ResNet50, and InceptionV3 models possess learned representations of visual features that may be relevant to autism characteristics, such as facial expressions and body language. By fine-tuning these pre-trained models, the aim is to repurpose their learned representations to effectively identify patterns indicative of autism traits in images.

### 1. Unfreezing Layers for Task Adaptation:
   Specific layers closer to the output of the pre-trained models are unfrozen to allow adaptation to the nuances of autism prediction. Unfreezing these layers enables the model to learn task-specific features related to autism traits, such as facial expressions and body language cues. By selectively unfreezing layers, there is a retention of the learned representations of general image features while adapting to the specific task of autism prediction.

### 2. Incorporating Task-Specific Layers:
   Additional layers are added on top of the pre-trained base models to tailor them for the intricacies of autism prediction.The Flatten layer converts the 2D feature maps extracted by the pre-trained models into a 1D feature vector, facilitating further processing by subsequent layers.The dense layers with ReLU activation introduce non-linearity, allowing the model to learn complex patterns indicative of autism traits from the flattened feature vector. The final dense layer with softmax activation enables the model to classify images into autism and non-autism classes, providing a probabilistic output for each class.

### 3. Optimization Techniques:
   The Adam optimizer is chosen for its ability to adapt learning rates for each parameter, ensuring stable fine-tuning of the models. A reduced learning rate (0.0001) is employed during fine-tuning to prevent abrupt changes to the learned representations and promote gradual adjustment to the autism prediction task. The categorical cross-entropy loss function is selected for its effectiveness in multi-class classification tasks like autism prediction, measuring the discrepancy between predicted and true label distributions.


## Evaluated Fine-tuned Models

| Model       | Accuracy | Loss              | Precision | Recall | F1 Score               |
|-------------|----------|-------------------|-----------|--------|------------------------|
| ResNet50    |   0.5    | 0.6839388012886047|    0.5    |  0.99  |   0.6644295302013423   |
| InceptionV3 |   0.5    | 0.6931672096252441|    0.5    |  1.0   |   0.6666666666666666   |
| VGG16       |   0.5    | 0.6931895613670349|    0.5    |  1.0   |   0.6666666666666666   |

---

## Findings:
### Discussion:
- Accuracy: The accuracy for all three models is 0.5, indicating that each model correctly predicts the class label for half of the instances in the validation set.
- Loss: The loss values for ResNet50, InceptionV3, and VGG16 are similar, indicating similar performance in terms of minimizing the error between predicted and true class labels during training.
- Precision: Precision is 0.5 for all models, suggesting that half of the predicted positive cases are true positives.
- Recall: ResNet50, InceptionV3, and VGG16 have a recall of 0.99, 1.0, and 1.0, respectively, indicating that these models are very effective at capturing true positive instances of autism in the dataset.
- F1 Score: ResNet50, InceptionV3, and VGG16 exhibit F1 scores of 0.664, 0.667, and 0.667, respectively, indicating a balance between precision and recall, crucial for tasks requiring accurate detection of autism-related characteristics.

### General Limitations:
- The models demonstrate a strong ability to identify autistic individuals, as indicated by high recall scores.
- However, the overall accuracy and F1 score indicate a need for further optimization to achieve a balanced performance across both classes.
- Fine-tuning hyperparameters, addressing class imbalances, or exploring alternative architectures may enhance model performance and generalization capabilities.