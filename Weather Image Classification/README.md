

# **Weather Classification Using Deep Learning Models**

## **Introduction**
This project focuses on developing and evaluating various machine learning models for weather classification using image data. Models range from simple neural networks to advanced architectures like convolutional neural networks (ConvNets) and pre-trained MobileNet.

The goal is to compare their performance and identify the most effective model for accurate weather prediction.

---

## **Project Structure**
- **Notebook**: Contains all the code, visualizations, and explanations.
- **Saved Model**: The best-performing ConvNet model is saved for reproducibility.
- **Validation Dataset**: Used for evaluating and comparing model predictions.

---

## **Tasks Overview**
### **Task 1: Simple Neural Network**
- Implemented a basic neural network for baseline performance.
- **Accuracy**: ~71.95%
- Observations: Minimal overfitting but limited capacity to capture complexity.

### **Task 2: Enhanced Neural Network**
- Added layers to improve performance.
- **Accuracy**: ~76.05%
- Observations: Higher performance but more prone to overfitting.

### **Task 3: Advanced Deep Learning Models**
#### **3.1 ConvNet**
- A custom convolutional neural network designed for this task.
- **Test Accuracy**: 88.62%
- Observations: Best overall performance, effective for all weather categories.

#### **3.2 MobileNet**
- Used MobileNet pre-trained on ImageNet with frozen weights.
- **Test Accuracy**: 85.63%
- Observations: Performed well, but not as accurate as the custom ConvNet.

---

## **Performance Summary**
| **Model**    | **Test Accuracy** | **Overfitting** | **Notes**                          |
|--------------|-------------------|-----------------|------------------------------------|
| Simple NN    | 71.95%            | Low             | Baseline model.                   |
| Complex NN   | 76.05%            | Moderate        | Improved but prone to overfitting.|
| ConvNet      | 88.62%            | Minimal         | Best-performing model.            |
| MobileNet    | 85.63%            | Moderate        | Competitive but slightly weaker.  |

---

## **Evaluation Highlights**
1. **Best Model**: ConvNet with 88.62% test accuracy.
2. **Category-wise Performance**:
   - **Easiest Weather to Detect**: Shine, due to high precision and recall.
   - **Most Difficult Weather to Detect**: Sunrise, with lower precision and recall.

---

## **Conclusion**
The ConvNet model proved to be the most effective for weather classification, outperforming both simple neural networks and pre-trained MobileNet. Its architecture efficiently balanced accuracy and generalization.

---