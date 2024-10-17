# plant_disease_detection_using_CNN
This repository contains a Convolutional Neural Network (CNN) model to detect and classify plant diseases from leaf images. This project was developed as part of CSC 542 - Neural Networks for the Spring 2024 semester, under the guidance of Dr. Edgar Lobaton at North Carolina State University (NCSU).

Our project aims to automate plant disease detection and classification using CNNs, offering a faster and more accurate alternative to traditional methods that are labor-intensive and time-consuming. 

##Motivation
The motivation stems from the substantial challenges posed by plant diseases to agriculture, such as crop loss and compromised food security. 
By providing farmers with a CNN-based tool for early disease detection, we aim to facilitate timely interventions and improve crop management practices.

**Dataset**

We have worked with the PlantVillage dataset. This dataset contains 38 classes of plants with over 50,000 expertly curated images on healthy and infected leaves of crops plants through the existing online platform PlantVillage. You can find the dataset [here](https://github.com/spMohanty/PlantVillage-Dataset)

**Baseline Model**

  We chose Random Forest as our baseline model for plant disease detection based on several factors:
  
1. Random Forest is ideal for the diverse and complex Plantvillage dataset. Its strength lies in handling high-dimensional data and nonlinear relationships between features, making it effective for both classification and regression tasks.
2. Random Forest's ensemble of decision trees prevents overfitting, making it ideal for datasets like Plant Village, characterized by noise and variability from factors such as image quality differences and plant variations.
3. Random Forest offers feature importance scores, aiding in understanding which image characteristics are most influential in disease classification. This interpretability assists in discerning underlying data patterns.

**Baseline Results**

![image](https://github.com/user-attachments/assets/1995075a-1440-4742-b2c3-17cd82b66ce0)

![image](https://github.com/user-attachments/assets/d3eeb17b-7fed-4fc8-91f9-0c29cdff2c5c)


**Improvised Model**

1. CNNs excel in processing visual data by automatically learning hierarchical representations from raw pixel values, eliminating the need for handcrafted features. This is ideal for our dataset, as CNNs adeptly capture intricate patterns and textures in leaf images, crucial for distinguishing healthy from diseased plants.
2. CNN architectures exploit spatial locality and translational invariance in images, benefiting plant disease detection. They use shared weights and local receptive fields to detect symptoms irrespective of their location, enhancing model robustness and generalization.
3. The hierarchical nature of CNNs enables them to learn increasingly abstract representations of features as information flows through successive layers. This hierarchical feature learning is particularly beneficial for plant disease detection, where diseases may manifest in subtle variations across different plant species and environmental conditions.

**CNN Architecture**

![image](https://github.com/user-attachments/assets/1b2b4b6e-4984-4477-a36d-b47cea326477)

**Improvised Results**

![image](https://github.com/user-attachments/assets/0ea317a1-4986-485e-a79d-19377f446823)

![image](https://github.com/user-attachments/assets/1e33e0bb-7f02-41b7-9487-9b858959981e)

**Comparative Results**

![image](https://github.com/user-attachments/assets/ec13efd8-7532-40d5-9b85-4cb16f157893)

### Challenges
1. **Data Imbalance:** Some diseases were underrepresented in the dataset. We applied oversampling techniques and used a weighted loss function to handle class imbalance.
2. **Overfitting:** We included dropout layers and early stopping to mitigate overfitting.

**Conclusion**

1. The CNN model, with its hierarchical feature learning and image-specific architecture, outperforms the Random Forest model in terms of accuracy and generalization for image classification tasks.
2. CNN model appears to be more suitable for image classification tasks due to its ability to learn complex features directly from raw pixel values and achieve higher accuracy.

## Future Work

- **Ensemble Methods:** Combining CNN with other machine learning models (like Random Forest or SVM) could further enhance accuracy.
- **Transfer Learning:** Using pre-trained models like VGG16 or ResNet could improve the results by leveraging networks trained on large image datasets.
- **Real-Time Application:** Deploying the model in a mobile app for real-time disease detection in the field.
  
## Model Deployment
To make the model usable in real-world scenarios, it can be deployed using cloud services (AWS, Google Cloud) or embedded in mobile applications for on-site disease diagnosis. An API can also be developed for image-based disease classification.

## Acknowledgements
We would like to thank:
- Dr. Edgar Lobaton for his guidance.
- NCSU for providing the infrastructure for the project.
- The [PlantVillage](https://github.com/spMohanty/PlantVillage-Dataset) team for the dataset.

---

**Contributors**  
- Neha Jagtap
- Pranjali Jadhav
- Swaranjali Jadhav

