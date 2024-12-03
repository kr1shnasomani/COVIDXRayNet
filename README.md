# COVID-19 Chest X-Ray Detection

The model uses the Xception architecture to classify chest X-ray images into "COVID" and "non-COVID" categories, achieving an accuracy of 87.53%. Incorporated effective preprocessing techniques, including image resizing and normalization, to enhance input quality.

## Execution Guide:

1. Run the following command lines in the terminal:
   ```
   pip install pandas numpy opencv-python seaborn matplotlib tqdm scikit-learn keras tensorflow
   ```
  
2. Download the dataset folder

3. Copy the path of the dataset folder and paste it into the code

4. After running all the cells, it will create an additional file called `Xception_Model.keras`

5. Enter the path of the image you want in the last cell to check if it has the presence of COVID-19 or not

6. This is how the final output will look like:

   ![image](https://github.com/user-attachments/assets/f5ef3561-cc00-44de-bc37-a8cc42a76994)

   ![image](https://github.com/user-attachments/assets/791ad909-ae92-41b3-b59a-14506a8fe7d1)


## Overview:
The Xception architecture is a deep learning model tailored for image classification tasks. Using depthwise separable convolutions, it efficiently reduces computational complexity while maintaining high accuracy. This makes it well-suited for applications like COVID-19 detection from chest X-rays, where distinguishing subtle differences between "COVID" and "non-COVID" images is critical. Xception's ability to capture intricate features ensures high performance, achieving an impressive accuracy of in classification. The architecture's efficiency and precision make it an excellent choice for medical imaging tasks, supporting rapid and accurate diagnosis in clinical settings.
