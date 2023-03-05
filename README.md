# Breastcancer_oneDNN_Conv1D

![04-Blog-Tumor-Cell-S](https://user-images.githubusercontent.com/111365771/222963183-1b677b56-822a-4b05-8b73-3d48a0c13db3.jpg)

# Introduction:

Breast cancer is one of the most common cancers in women worldwide. Early detection and accurate diagnosis of breast cancer are crucial for improving patient outcomes. In recent years, machine learning models have shown promising results in breast cancer diagnosis. In this project, we explore the use of Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) models for breast cancer diagnosis using the Wisconsin Diagnostic Breast Cancer (WDBC) dataset.

# Models Used:

![conv1d](https://user-images.githubusercontent.com/111365771/222963105-33e1ebef-2f74-4688-91d5-651f6ce720a0.png)

We implemented three different models for breast cancer diagnosis: CNN, LSTM, and Conv1D. The CNN model was used to extract features from the image data, while the LSTM and Conv1D models were used to process the time series data. We used Keras, a popular deep learning library, to implement these models.

#OneAPI oneDNN:

![download](https://user-images.githubusercontent.com/111365771/222963211-f7f2d17c-14d2-49e4-b4fe-0fa2394af262.jpg)

OneAPI oneDNN is a deep learning library designed for high-performance machine learning applications. It provides optimized implementations of common deep learning algorithms and is compatible with various hardware platforms. In this project, we used the oneDNN library to optimize the performance of our models.

# EDA Explanation:

## 1)Correlation:

![corrr](https://user-images.githubusercontent.com/111365771/222963247-fa100fe4-a5ba-40e5-95f3-047dccc9b037.png)

One of the first things we checked during the exploratory data analysis was the correlation between the different features in the WDBC dataset. We used a heatmap to visualize the correlation matrix, which showed us the strength and direction of the relationships between each pair of features. By looking at the heatmap, we can identify which features are strongly correlated with each other and which ones are not. This information can be useful in feature selection and dimensionality reduction, as highly correlated features may not provide much additional information and can potentially lead to overfitting.

## 2)Distribution of the target variable:

![dist](https://user-images.githubusercontent.com/111365771/222963279-d1515466-9bc0-49d7-9f89-28ea7d7962b2.png)

After checking the correlation between the features, we also visualized the distribution of the target variable, which in this case was the diagnosis column. We used a countplot to show the number of benign and malignant diagnoses in the dataset. By looking at the countplot, we can see that there are more benign cases than malignant cases in the dataset. This information is important because it can affect the model's performance and the selection of evaluation metrics. For example, if a model predicts all cases as benign, it will still achieve a relatively high accuracy, but it will not be useful in a real-world scenario.

## 3)Relationship between the mean radius and the diagnosis:

![rel](https://user-images.githubusercontent.com/111365771/222963292-d3b2f855-acd7-4348-ac35-8991e892d387.png)

Finally, we also looked at the relationship between one of the features, mean radius, and the diagnosis target variable. We used a boxplot to visualize the distribution of mean radius for benign and malignant cases separately. By looking at the boxplot, we can see that the mean radius tends to be higher for malignant cases than benign cases. This information can be useful in feature engineering and model selection, as it suggests that mean radius may be a useful feature for distinguishing between benign and malignant cases.

Results:
![res](https://user-images.githubusercontent.com/111365771/222963317-04853de7-1ede-4aa5-8ec2-c934e9b8be4d.png)
We trained and evaluated our models using the WDBC dataset. The CNN model achieved an accuracy of 97.37%, the LSTM model achieved an accuracy of 96.49%, and the Conv1D model achieved an accuracy of 95.61%. These results demonstrate the potential of machine learning models for breast cancer diagnosis and the effectiveness of oneDNN in optimizing their performance.
