
# Stroke Detection from Brain CT Scans

## Project Overview
This project aims to develop a binary classifier using a pre-trained VGG16 model to identify the presence of stroke in brain CT scan images. The dataset consists of brain CT scan images, categorized into two groups: normal and with stroke signs. Images are pre-processed and resized to 224x224 pixels before being fed into the model.

## Model Training
The model is trained on a balanced dataset of brain CT scan images for 15 epochs, achieving a test accuracy of 91.91%. This high accuracy indicates that the model is effectively distinguishing between normal brain images and those showing signs of stroke.

## How to Reproduce This Project
To reproduce this project, follow the steps below:

1. **Clone the Repository**
    ```
    git clone https://github.com/clintonasoh/stroke-detection-in-CT-scans.git
    ```

2. **Install Dependencies**
    Navigate to the project directory and install the required Python packages:
    ```
    pip install -r requirements.txt
    ```

3. **Load the Dataset**
    Replace the image folder paths `normal_dir` and `stroke_dir` in the jupyter notebook with your local dataset path. 

4. **Run the Training Script**
    Execute the Python script that trains the model.

5. **Evaluate the Model**
    After training, use the evaluation part of the script to test the model's performance on unseen data.

## Critical Analysis

### Results
- The test accuracy of 91.91% is promising, suggesting that transfer learning with VGG16 is suitable for medical image analysis tasks like stroke detection.
- Given the balanced dataset, the achieved accuracy reflects the model's capability in handling both classes (normal and stroke) effectively.

### Discussion
- **Generalization Ability**: The high accuracy on the test set suggests good generalization. However, further validation with external datasets is crucial to ensure the model's robustness across different imaging devices and conditions.
- **Class Distribution**: The balanced nature of the dataset aids in avoiding bias towards a particular class, contributing to the model's performance.

### Bugs and Limitations
- **Overfitting**: Despite achieving high accuracy, there's a potential risk of overfitting, especially if the model is exposed to highly diverse external datasets. Regularization techniques and data augmentation were employed to mitigate this.
- **Data Diversity**: The dataset's scope, while balanced, might not cover all possible variations in stroke appearances. Increasing data diversity could further improve model robustness.

### Confusion
- **Misclassifications**: There might be instances where the model misclassifies images, especially in cases where stroke signs are subtle or overlap with artifacts. Analyzing the confusion matrix can help identify such cases and guide further improvements.

## Future Directions
- **Dataset Expansion**: Including more diverse examples from different demographics and imaging equipment could enhance model performance.
- **Model Experimentation**: Exploring other pre-trained models or custom architectures might yield better results or efficiency.
- **Clinical Validation**: Collaborating with medical professionals to validate model predictions against clinical outcomes would be essential for real-world applications.

## Conclusion
The project demonstrates the potential of using deep learning and transfer learning for medical image analysis, specifically stroke detection in brain CT scans. While the results are promising, continuous efforts in model improvement, dataset expansion, and clinical validation are necessary to fully realize its application in healthcare settings.
