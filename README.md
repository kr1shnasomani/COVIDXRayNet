# COVID-19 Chest X-Ray Detection

The model uses the Xception architecture to classify chest X-ray images into "COVID" and "non-COVID" categories, achieving an accuracy of 87.53%. Incorporated effective preprocessing techniques, including image resizing and normalization, to enhance input quality.

## Execution Guide:

1. Run the following command line in the terminal:
   ```
   pip install pandas numpy opencv-python seaborn matplotlib tqdm scikit-learn keras tensorflow
   ```
  
2. Download the dataset (link to the dataset: **https://www.kaggle.com/datasets/plameneduardo/sarscov2-ctscan-dataset**)

3. Copy the path of the dataset folder and paste it into the code

4. After running all the cells, it will create an additional file called `Xception_Model.keras` (this file stores the model)

6. Enter the path of the image you want in the last cell to check if it has the presence of COVID-19 or not

7. This is how the final output will look like:

   ![image](https://github.com/user-attachments/assets/f5ef3561-cc00-44de-bc37-a8cc42a76994)

   ![image](https://github.com/user-attachments/assets/791ad909-ae92-41b3-b59a-14506a8fe7d1)


## Overview:
The provided code implements a deep learning pipeline for detecting COVID-19 from medical images using the Xception model, a powerful Convolutional Neural Network (CNN) architecture. Below is an overview of the code's key components and their functionality:

1. **Imports:** The code imports essential libraries like `os`, `pandas`, `numpy`, `cv2`, `keras`, and `tensorflow`, among others. These libraries provide the necessary tools for handling data, image processing, model creation, training, and evaluation.

2. **Loading the Dataset:**
   - The dataset consists of two categories: `COVID` and `non-COVID`. These images are located in a specified directory (`data_dir`). The code reads the filenames and assigns each image to its corresponding class (`COVID` or `non-COVID`) in a pandas DataFrame.
   - It processes the images by resizing them to 64x64 pixels and normalizing them (dividing pixel values by 255) to scale the input images.

3. **Splitting the Data:** The dataset is split into training and testing datasets using `train_test_split`, with 80% for training and 20% for testing.

4. **Model Architecture (Xception):**
   - A custom Xception-based CNN model is built using Keras. Xception is a pre-trained model, which is fine-tuned for this specific task. The architecture involves:
     - **Conv2D** layer to introduce convolutional processing.
     - **Xception** as the base model (excluding the top classification layers).
     - **GlobalAveragePooling2D** to reduce the feature map size.
     - **BatchNormalization** and **Dropout** layers to stabilize training and prevent overfitting.
     - **Dense** layers for classification.
   - The model uses the Adam optimizer and categorical cross-entropy as the loss function for classification.

5. **Model Training:**
   - The model is trained using an image data generator (`ImageDataGenerator`) to augment the dataset with transformations like rotation, shifting, and zooming to improve model generalization.
   - Two callbacks are used during training:
     - `ReduceLROnPlateau`: Reduces the learning rate if the validation accuracy plateaus.
     - `ModelCheckpoint`: Saves the model with the best performance on the validation set.

6. **Training Accuracy & Loss Visualization:** The training and validation accuracy/loss are visualized over epochs using `matplotlib` to track the model's progress.

7. **Model Evaluation:** After training, the model is evaluated on the test set, and the loss and accuracy are printed. Additionally, the code calculates precision, recall, F1-score, and other metrics using the `classification_report` from `sklearn`.

8. **Confusion Matrix:** The confusion matrix is computed to evaluate how well the model is classifying the test set images into `COVID` and `non-COVID`. The confusion matrix is displayed using a heatmap, which shows the true positives, true negatives, false positives, and false negatives.

9. **Image Prediction Function:** A function `predict_image` is defined to make predictions on individual images. It takes an image path, loads and preprocesses the image, and then predicts whether the image belongs to the `COVID` or `non-COVID` category. The predicted class and confidence score are displayed along with the resized image.

10. **Test Prediction:** The function is then used to predict the disease type for specific images from both the `COVID` and `non-COVID` categories.

11. **Key Results:**
   - The model achieves an accuracy of around 87.53% on the test set, which indicates reasonable performance in distinguishing between COVID and non-COVID cases.
   - The classification report shows good precision, recall, and F1-scores for both classes (`COVID` and `non-COVID`), with the COVID class having slightly better performance.

### Summary:
This code represents a complete workflow for training a deep learning model to detect COVID-19 in medical images, evaluate its performance, and make predictions. The use of the Xception model allows leveraging a powerful pre-trained model, which helps in better accuracy and faster convergence for image classification tasks. The code also includes data preprocessing, model evaluation, and visualization of key metrics.
