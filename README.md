# Rice Image Classification Project

This project involves the development of a deep learning model for classifying rice images. The following steps have been undertaken as part of the project:

## 1. Data Loading and Preprocessing
- Images from the [`Rice_Image_Dataset`] directory were loaded and class labels were extracted.
- The images were resized to 64x64 dimensions and pixel values were normalized.

## 2. Data Preparation
- Image and label data were split into training and test sets using the [`train_test_split`] function.
- Labels were encoded using [`LabelEncoder`] and converted to categorical format using the [`to_categorical`] function.

## 3. Model Development
- A deep learning model was built using the [`Sequential`] API.
- The model included various layers such as [`Conv2D`], [`MaxPooling2D`], [`Flatten`], [`BatchNormalization`], [`Dropout`], and [`Dense`].
- The model was compiled with the [`adam`] optimization algorithm and [`categorical_crossentropy`] loss function.

## 4. Model Training and Hyperparameter Optimization
- The model was trained on the training data and evaluated with validation data.
- Hyperparameter optimization was performed using [`kerastuner`] to select the best model.
- Early stopping ([`EarlyStopping`]) was used to prevent overfitting of the model.

## 5. Model Evaluation and Saving
- The best model was evaluated on the test data and the accuracy value was calculated.
- The model was saved as `rice_model.h5`.

## 6. Making Predictions
- The saved model was loaded and predictions were made on a new image.
- The predicted class and the actual class were displayed on the image.

### **Model Performance**:
   - The best model achieved an accuracy of 99.65% on the training data.
   - The model's accuracy on the test data was measured at 99%.

### **Model Evaluation**:
   - The model's loss value was calculated as 0.02 on the training data and 0.20 on the test data.
   - The classification report and confusion matrix of the model are as follows:

   ```
   Classification Report:
              precision    recall  f1-score 

     Arborio       1.00      1.00      1.00      
     Basmati       1.00      1.00      1.00      
      Ipsala       1.00      1.00      1.00      
     Jasmine       1.00      0.99      1.00      
   Karacadag       1.00      1.00      1.00      

   Confusion Matrix:
       [2989,    0,    0,    2,    6]
       [   0, 2990,    0,    5,    0]
       [   0,    0, 3083,    0,    0]
       [   5,   11,    0, 2979,    1]
       [   9,    0,    0,    0, 2920]
   ```
### Model Saving and Prediction
- The best model was saved as `rice_model.h5`.
- The saved model can predict with 99% accuracy on new images.

## Conclusion
This project demonstrates the development of an effective deep learning model for classifying rice images with high accuracy and low loss values.

