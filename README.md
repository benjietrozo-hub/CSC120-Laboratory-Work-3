# CSC120-Laboratory-Work-3 

https://colab.research.google.com/drive/1VMMh-ikPc4IbW3xfUkNFhHAiOFicKPOm?usp=sharing

Guide Questions (Student Explanation & Reflection)

1. Dataset Preparation

• How did you organize your dataset in Google Drive?

I organized my dataset in Google Drive by creating a main folder named “image_dataset”, which contains 20 subfolders, each representing a different type of fig. Each subfolder contains images specific to its class, ensuring proper labeling and organization.

• Why is folder structure important for TensorFlow image loading?

The folder structure is important because TensorFlow automatically assigns labels based on the names of the subfolders inside “image_dataset.” This ensures that each image is correctly categorized into one of the 20 fig classes, which is essential for accurate training.

2. Model Training

• What is the role of convolutional layers in image classification?

Convolutional layers extract important visual features such as edges, textures, and shapes from the fig images. Since many fig types look similar, these layers help the model learn subtle differences between the 20 classes.

• Why do we split data into training and validation sets?

We split the data so the model can learn from the training set and be evaluated using the validation set. This helps check if the model performs well on unseen data and prevents overfitting.

3. Performance Analysis

• What accuracy did your model achieve?

The model achieved a final validation accuracy of 72.47% with a validation loss of 0.8769. This indicates that the model can correctly classify most images, but there is still room for improvement, especially since it handles 20 different classes.

• How did the number of images affect the model’s performance?

The number of images had a significant effect on performance. Classes with more images were classified more accurately, while classes with fewer images reduced overall accuracy. Increasing the dataset size would likely improve the model’s performance beyond 72.47%.

4. Critical Thinking

• What challenges did you encounter while using your own dataset?
Some challenges included:

Similar appearance between different fig types
Imbalanced number of images per class
Variations in lighting, angle, and image quality

These challenges contributed to the model achieving a moderate accuracy of 72.47%.

• How can data augmentation improve your model?

Data augmentation can improve the model by increasing dataset diversity through transformations such as rotation, flipping, zooming, and brightness adjustments. This helps the model generalize better and can increase accuracy.

5. Application

• Suggest a real-world application for your trained model.

A real-world application is an automated fig classification system that can be used in agriculture or markets to identify and sort different types of figs efficiently.

• How can this system be integrated into a mobile or web application?

The system can be integrated by deploying the trained model as an API. A mobile or web app can capture or upload images, send them to the API, and receive classification results in real time.



Visualization & Overfitting

1. What signs indicated overfitting in your first model?
   
In the first model, overfitting was indicated when the training accuracy continued to increase while validation accuracy stayed low or fluctuated. At the same time, the validation loss was higher compared to training loss, showing that the model was memorizing training images instead of learning general patterns.

3. How did data augmentation affect validation accuracy?
   
Data augmentation improved validation accuracy by making the dataset more diverse. After applying transformations like rotation, flipping, and zooming, the model became more robust, which helped it perform better on unseen fig images and reduced overfitting.

Model Improvement

3. What is the purpose of dropout layers?
   
Dropout layers are used to prevent overfitting by randomly disabling some neurons during training. This forces the model to learn more general features instead of relying too much on specific patterns, improving its ability to generalize to new data.

5. Why does data augmentation improve generalization?
   
Data augmentation improves generalization because it increases the variety of training data without collecting new images. By exposing the model to different variations of the same image, it learns to recognize figs under different angles, lighting, and conditions.

Performance Comparison

5. Compare accuracy before and after improvements.
   
Before improvements, the model had lower and less stable validation accuracy due to overfitting. After applying data augmentation and dropout, the model achieved a final validation accuracy of 72.47% with a validation loss of 0.8769, showing improved generalization and stability.

7. Which technique contributed most to improvement?
   
Data augmentation contributed the most to the improvement because it significantly increased dataset diversity. This helped the model learn more generalized features across the 20 fig classes, reducing overfitting more effectively than other techniques.

Deployment & Application

7. Why is saving the model important?
   
Saving the model is important because it preserves the trained weights and architecture. This allows the model to be reused later without retraining, making it efficient for deployment in real applications.

9. How can this model be deployed in a real-world system?
    
The model can be deployed by converting it into an API using a backend framework. A mobile or web application can send uploaded or captured images to the server, and the model will return the predicted fig class in real time. It can also be integrated into agricultural systems for automated fruit classification.

