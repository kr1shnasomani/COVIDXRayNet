<h1 align="center">COVIDXRayNet</h1> 
This project leverages CNN models (Xception, VGG16, ResNet50) to detect COVID-19 from chest X-ray images. It compares model performance based on accuracy, precision, recall, and F1-score, offering insights into the best architecture for reliable medical image classification.

## Accuracy & Loss Over Epochs:

| Model Name | Accuracy                                                                                  | Loss                                                                                      |
|------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Xception   | ![image](https://github.com/user-attachments/assets/7dec0a90-01ef-4e9a-846d-b5988bab9dcf) | ![image](https://github.com/user-attachments/assets/43a15ff8-bc06-447a-9dd6-f3ed3d3b5c96) |
| ResNet50   | ![image](https://github.com/user-attachments/assets/3abdd91b-f597-487a-b93b-ac4cd2e4f4d3) | ![image](https://github.com/user-attachments/assets/5597a454-ca09-450d-840e-d2a9d3ea8e44) |
| VGG16      | ![image](https://github.com/user-attachments/assets/8088e746-a2f0-46bf-bc05-6770546e746f) | ![image](https://github.com/user-attachments/assets/d4079cd1-cb92-40f1-9e56-4a4a2e92cf8d) |

## Confusion Matrix:

| Model Name | Plot                                                                                      |
|------------|-------------------------------------------------------------------------------------------|
| Xception   | ![image](https://github.com/user-attachments/assets/15161ad2-409f-4343-8255-e5c0e55ce730) |
| ResNet50   | ![image](https://github.com/user-attachments/assets/1f6bd203-b734-4ef0-a0da-6bcd4bf66d3f) |
| VGG16      | ![image](https://github.com/user-attachments/assets/8935cfec-957b-4e86-a10d-8b76eb6eb026) |

## Model Prediction:

| Model Name | COVID                                                                                     | non-COVID                                                                                 |
|------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Xception   | ![image](https://github.com/user-attachments/assets/6c9f547c-19e4-43fb-b689-21462acd0296) | ![image](https://github.com/user-attachments/assets/49fdc908-ad2b-4292-9fdf-86b02d6e58c8) |
| ResNet50   | ![image](https://github.com/user-attachments/assets/e2ee79af-4b61-4bc6-b2d5-0e2f73ddfb3f) | ![image](https://github.com/user-attachments/assets/9be8d9b8-2bf0-4573-a88e-5b4d7b273c03) |
| VGG16      | ![image](https://github.com/user-attachments/assets/055eb479-2370-4873-b20c-3651b2fb69e9) | ![image](https://github.com/user-attachments/assets/935e999a-f937-46e9-b940-ee5358fc2692) |

## Model Comparison:

| Model Name | Accuracy | Loss | Recall (COVID) | Recall (non-COVID) | Precision (COVID) | Precision (non-COVID) | F1-Score (COVID) | F1-Score (non-COVID) | Overall Accuracy | Model Size (MB) |
|------------|----------|------|----------------|--------------------|-------------------|-----------------------|------------------|----------------------|------------------|-----------------|
| Xception   | 0.81     | 0.39 | 0.72           | 0.91               | 0.89              | 0.78                  | 0.79             | 0.84                 | 0.82             | 86.4            |
| ResNet50   | 0.84     | 0.41 | 0.82           | 0.87               | 0.86              | 0.84                  | 0.84             | 0.85                 | 0.85             | 214             |
| VGG16      | 0.81     | 0.39 | 0.97           | 0.96               | 0.96              | 0.97                  | 0.96             | 0.96                 | 0.96             | 204             |
