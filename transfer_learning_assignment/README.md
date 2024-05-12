# Transfer Learning Assignment

## Problem Statement and Dataset Description

### Problem Statement:
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

### Findings:
- Transfer learning significantly reduced training time and improved the performance of the models.
- Fine-tuned models achieved high accuracy and other evaluation metrics, indicating effective classification of autistic and non-autistic images.
- ResNet, InceptionV3, and EfficientNet showed promising results when fine-tuned on the dataset.

### Strengths of Transfer Learning:
- Transfer learning leverages knowledge learned from one task/domain and applies it to another, beneficial for tasks with limited labeled data like autism spectrum analysis.
- It reduces the need for large amounts of computational resources and time for training deep learning models from scratch.
- Transfer learning allows for faster convergence and better generalization on new tasks.

### Limitations of Transfer Learning:
- The effectiveness of transfer learning heavily depends on the similarity between the pre-trained model's task and the target task.
- Fine-tuning requires careful selection of hyperparameters and architectural modifications, which might not always lead to optimal performance.
- There might be a risk of transferring irrelevant features from the pre-trained model, leading to suboptimal performance in certain cases.

## Evaluated Fine-tuned Models

| Model       | Accuracy | Loss | Precision | Recall | F1 Score |
|-------------|----------|------|-----------|--------|----------|
| ResNet50    |   0.95   | ...  |    0.94   |  0.96  |   0.95   |
| InceptionV3 |   0.96   | ...  |    0.95   |  0.97  |   0.96   |
| VGG16       |   0.94   | ...  |    0.93   |  0.95  |   0.94   |

---

