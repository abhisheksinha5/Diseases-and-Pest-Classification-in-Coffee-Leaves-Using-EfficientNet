# Coffee Leaf Disease and Pest Classification Using EfficientNet (B0-B4)

## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Dataset](#dataset)
4. [Model Architecture](#model-architecture)
5. [Training and Results](#training-and-results)
6. [Installation and Usage](#installation-and-usage)
7. [Future Scope](#future-scope)
8. [Contributing](#contributing)
9. [License](#license)

---

## Introduction

This project focuses on the **classification of coffee leaf diseases and pests** using deep learning techniques. We use **EfficientNet** (versions B0-B4) for detecting two specific types of diseases: **Rust** and **Miner**. Our goal is to build a robust model to help farmers by providing early diagnosis of diseases, thus reducing crop losses and minimizing the use of fertilizers.

---

## Objectives

- To accurately classify pests and diseases in coffee leaves using EfficientNet (B0-B4).
- To evaluate and compare the accuracy of different versions of EfficientNet.
- To reduce crop losses and the need for harmful fertilizers, ensuring a pollution-free environment.

---

## Dataset

We utilized a publicly available dataset of coffee leaf images. The dataset consists of two main categories: **Rust** and **Miner**. The data has been preprocessed and augmented to improve model performance.

### Dataset Structure
- `miner/`: Contains images of coffee leaves infected with miners.
- `rust/`: Contains images of coffee leaves affected by rust.

**Dataset Link**: https://www.kaggle.com/datasets/alvarole/coffee-leaves-disease?select=miner_img_xml

---

## Model Architecture

The model uses different versions of **EfficientNet** (B0-B4) to classify coffee leaf diseases. EfficientNet is a convolutional neural network (CNN) that scales the model depth, width, and resolution using a compound scaling method. We also implement **BiFPN** to improve feature extraction.

### EfficientNet Versions
- **EfficientNet-B0**: Input size 224x224
- **EfficientNet-B1**: Input size 240x240
- **EfficientNet-B2**: Input size 260x260
- **EfficientNet-B3**: Input size 300x300
- **EfficientNet-B4**: Input size 380x380

### Model Workflow
1. **Input Preprocessing**: Resizing, rotation, and edge detection.
2. **Feature Extraction**: Using EfficientNet to extract features.
3. **Pooling and Activation**: Average pooling followed by ReLU activation.
4. **Classification**: Softmax activation to output class probabilities.

### Model Diagram
![ ](https://github.com/abhisheksinha5/Diseases-and-Pest-Classification-in-Coffee-Leaves-Using-EfficientNet/blob/main/Project%20Images/EfficientNet.png)


---

## Training and Results

We trained the model using **EfficientNet-B0 to B4** for 100 epochs each. Below is the accuracy and loss for each version:

| Model             | Training Accuracy | Validation Accuracy | Training Loss | Validation Loss |
|-------------------|-------------------|---------------------|---------------|-----------------|
| **EfficientNet-B0** | 99.8%             | 86.2%               | 0.011         | 0.308           |
| **EfficientNet-B1** | 98.1%             | 58.6%               | 0.040         | 3.82            |
| **EfficientNet-B2** | 100%              | 100%                | 0.004         | 0.017           |
| **EfficientNet-B3** | 99.2%             | 79.3%               | 0.992         | 0.580           |
| **EfficientNet-B4** | 99.4%             | 100%                | 0.013         | 0.002           |

### Training Accuracy Graph
![ ](https://github.com/abhisheksinha5/Diseases-and-Pest-Classification-in-Coffee-Leaves-Using-EfficientNet/blob/main/Project%20Images/Training%20Graphs.png)


### Sample Output
![ ](https://github.com/abhisheksinha5/Diseases-and-Pest-Classification-in-Coffee-Leaves-Using-EfficientNet/blob/main/Project%20Images/output.png)

## Conclusion

The project successfully demonstrates the use of EfficientNet (B0-B4) for the classification of diseases and pests affecting coffee leaves. The results show that the model achieves high accuracy, particularly with the EfficientNet B2 and B4 versions, which indicate the potential for reliable and efficient detection of common coffee plant ailments like rust and miners.

By leveraging deep learning techniques and advanced computer vision methodologies, this model can significantly streamline the process of disease identification, which is typically labor-intensive and time-consuming when performed manually. The ability to automatically classify coffee leaf diseases not only enhances efficiency but also empowers farmers with timely insights, allowing for proactive measures to mitigate crop losses.

Moreover, the model's architecture can be adapted to classify diseases and pests in various crops beyond coffee, making it a versatile tool for agricultural applications. With further refinement, such as training on larger datasets and optimization of hyperparameters, the model's performance can be improved even further.

In conclusion, this project has the potential to revolutionize agricultural practices by promoting sustainable farming techniques. By reducing reliance on harmful fertilizers and minimizing environmental impact, farmers can achieve higher yields while contributing to a healthier ecosystem. Overall, this model represents a significant step forward in utilizing technology to enhance food safety and agricultural productivity.


---

## Installation and Usage

### Prerequisites

Ensure you have the following installed:
- Python 3.8+
- TensorFlow
- Keras
- NumPy
- OpenCV
- Matplotlib


