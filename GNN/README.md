
# Real-world Applications of GNN 

## Introduction
This project explores the use of **Graph Neural Networks (GNNs)** for node classification on the **Cora dataset**, which consists of research papers and their citation relationships. The goal is to predict the topic of each paper based on its citation network.

## Dataset
- **2708 nodes** (research papers)
- **10556 edges** (citations)
- **1433 features** per paper (bag-of-words)
- **7 classes** representing different research topics
- The dataset is split into **training**, **validation**, and **test** sets.

## Model
The model uses a **Graph Convolutional Network (GCN)** with **Batch Normalization** and **Dropout** to improve stability and prevent overfitting. The architecture includes:
1. Input layer (1433 features) -> 64-dimensional hidden layer
2. 64-dimensional intermediate layers
3. Output layer (7 classes)

## Results
- **Training Accuracy:** Close to 100% after 25 epochs
- **Validation Accuracy:** 70-75%, indicating some overfitting.
- **Ablation Studies:** Removing BatchNorm or Dropout worsened performance, suggesting these components help with generalization.

## Conclusion
The model demonstrated good performance on the Cora dataset, with Batch Normalization and Dropout proving essential for preventing overfitting and improving accuracy.
