# **PixelCNN-Based Image Generation**

## **Overview**
This project explores the implementation of **PixelCNN**, a generative model designed to create images pixel-by-pixel by modeling the dependencies between pixels. Several advanced versions of PixelCNN were also developed, including:
- **Conditional PixelCNN**: Generates images based on specific labels.
- **Self-Attention PixelCNN**: Incorporates attention mechanisms to capture long-range dependencies between pixels.
- **Dilated PixelCNN**: Uses dilated convolutions to increase the receptive field for each pixel.

The primary goal was to generate coherent grayscale images from the MNIST dataset of handwritten digits and evaluate model performance using Negative Log-Likelihood (NLL) and Perplexity.

---

## **Key Features**
1. **Pixel-by-Pixel Image Generation**: The models generate each pixel sequentially, conditioned on previously generated pixels.
2. **Conditioning Mechanism**: Conditional PixelCNN can generate class-specific images (e.g., digits from 0 to 9).
3. **Attention Integration**: The self-attention mechanism helps in modeling global dependencies in the image.
4. **Dilated Convolutions**: Expands the receptive field without increasing the computational burden significantly.

---

## **Findings**
1. **Base PixelCNN**:  
   - Successfully generates random images but lacks global structure, especially for complex patterns.  

2. **Conditional PixelCNN**:  
   - Produces label-specific outputs, showing an improved ability to reflect the structure of MNIST digits.  
   - Slightly higher NLL due to the added complexity.  

3. **Self-Attention PixelCNN**:  
   - Demonstrated improved consistency across the image, particularly in maintaining digit structure.  
   - Increased computation time due to the attention mechanism.  

4. **Dilated PixelCNN**:  
   - Expanded the effective receptive field, enhancing local details in the generated images.  
   - However, it sometimes resulted in a higher NLL due to overfitting or increased model capacity.

---

## **Challenges**
- Balancing model complexity with performance.
- Maintaining computational efficiency with advanced features like attention and dilations.
- Ensuring coherent outputs for larger datasets or higher-resolution images.

---

## **Future Work**
- **Diverse Datasets**: Extend the approach to datasets such as CIFAR-10 and CelebA to evaluate performance on color images and more complex structures.  
- **Improved Architectures**: Experiment with deeper networks, hybrid attention mechanisms, or alternative autoregressive models like PixelSNAIL.  
- **Training Optimization**: Focus on techniques to reduce training time and stabilize NLL and perplexity values.  

---

## **Conclusion**
This project highlights the strengths and limitations of PixelCNN and its variants. While the models effectively capture dependencies between pixels, advanced techniques like attention and dilations show promise for generating more realistic and structured images. 

