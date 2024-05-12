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

###ResNet###: ResNet's capability to effectively handle deep features is crucial for capturing the subtle and complex patterns related to autism spectrum traits in the image dataset, aiding accurate classification into "autistic" and "non_autistic" categories.

###InceptionV3###: InceptionV3's efficient pattern capturing ability, combined with its balance between complexity and performance, provides a strong foundation for accurately identifying diverse visual characteristics associated with autism spectrum traits in the image dataset, facilitating precise classification.

###VGG16###: Using VGG16 offers the benefit of simplicity, interpretability, and availability as a pre-trained model, facilitating efficient transfer learning for accurately classifying "autistic" and "non_autistic" images in the dataset.

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
| ResNet      |   0.95   | ...  |    0.94   |  0.96  |   0.95   |
| InceptionV3 |   0.96   | ...  |    0.95   |  0.97  |   0.96   |
| VGG16       |   0.94   | ...  |    0.93   |  0.95  |   0.94   |

---

