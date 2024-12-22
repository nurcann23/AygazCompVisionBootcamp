# AygazCompVisionBootcamp  
# Animal Classification CNN Project  

This project aimed to develop a Convolutional Neural Network (CNN) model capable of distinguishing different animal classes. The project included data preparation, data augmentation, and manipulation techniques to evaluate model performance under various test scenarios.

1. Dataset
- Source: [Animals with Attributes 2 Dataset](https://drive.google.com/drive/folders/1FYvR3c99nxf0qH235gpyJW0UGPWpmr5U?usp=sharing)  

2. Data Preparation 
- A balanced dataset was created by selecting 650 images from each class.  
- All images were resized to 128x128 and normalized between 0 and 1.  
- The data was split into training and testing sets with a 70%-30% ratio.  

3. Data Augmentation 
To enhance the diversity of the training set, salt and pepper noise was added:  
- Application: 15% of the pixels in the images were randomly converted to black or white.  
- Objective: This technique aimed to increase the model's robustness to different scenarios.  

4. Model Design 
- Model Architecture:  
  - Conv2D and MaxPooling2D Layers: The model started with 16 filters in the first Conv2D layer, followed by 64 and 128 filters in subsequent layers. MaxPooling2D layers were used to reduce the spatial dimensions of feature maps.  
  - Fully Connected Layers: The flattened feature maps were passed through Dense layers with 256 and 10 neurons, respectively.  
  - Dropout Layer: A 50% dropout was applied to prevent overfitting.  

- Model Performance:
  - Accuracy: 90.36%
  - Val_accuracy: 81.13%

5. Manipulation of Test Data
- Brightness Reduction: 
  - The brightness of the test images was reduced.  
  - The manipulated dataset was tested, and accuracy dropped to 63.16%.  

- Color Balancing Algorithm: 
  - The Gray World algorithm was applied to the manipulated test data.
  - After applying this algorithm, accuracy further dropped to 19.89%  

6. Conclusion:  
- Manipulations significantly impacted model performance.  
- The color balancing algorithm further worsened the results.  
- To improve performance, different CNN architectures or methods like transfer learning could be explored.  

This project aimed to classify 10 animal classes using a CNN model. Various test scenarios were conducted to evaluate the model's robustness, and the results were documented. The project provides insights and suggestions for potential improvements to enhance the performance of machine learning models.  
