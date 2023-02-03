# Classification of Ship and IceBerg
### Introduction
The Statoil Iceberg Classifier Challenge is a dataset available on Kaggle that provides a unique opportunity to apply deep learning techniques to a real-world problem. The dataset includes images of ships and icebergs, taken from a satellite, and the goal is to classify these images as either a ship or an iceberg.

## Road Map
### Part 1: Band1 or Band2, scaled or orginal data
In part 1, we use DNN for Band1 and 2 on the scaled and original datasets to find which set of data works better.
-Implementing DNN for Band1 on the original dataset

-Implementing DNN for Band1 on the scaled dataset

-Implementing DNN for Band2 on the original dataset

-Implementing DNN for Band2 on the scaled dataset

### Part 2: Rotate the Images based on the inc_angle
In part 2, we rotate all images based on the inc_angle to remove the impact of the inc_angle.

Please note that there are 133 missing data for the inc_angle. We fill these values with the mean of the inc_angle.

### Part 3: Instead of filling the missing data, we drop them.

### Part 4: we combine band1 and band2 to generate new band which contains the information from both bands.

### Part 5: we compare the results

### Data Visualization: 
Let's Visualize the data

![myimage](data_vis.png)

## Part 1: 
Let's compare the results for band1 and 2 on the original and scaled dataset.

Band1 Original Dataset: 

Loss : 0.6           
Accuracy: 80%

Band2 Original Dataset: 

Loss : 0.5        
Accuracy: 77%

Band1 Scaled Dataset: 

Loss : 0.38         
Accuracy: 86%

Band2 Scaled Dataset: 

Loss : 0.39         
Accuracy: 82%

Let's visualize the results by the confusion matrix

Band1 Original Dataset: 

![myimage](band_1_org.png)
-------------------------------------------
Band2 Original Dataset: 

![myimage](band_2_org.png)
-------------------------------------------
Band1 Scaled Dataset: 

![myimage](band_1_scaled.png)
-------------------------------------------
Band2 Scaled Dataset: 

![myimage](band_2_scaled.png)
-------------------------------------------
## Part 1 Conclusion:
According to the results from part 1, Band1 with the scaled dataset has the best performance on the DNN model.

Confusion Matrix Analsys:

The DNN model correctly identified 141 out of 164 Icebergs and misclassified 23 as ships. It also accurately predicted 135 out of 157 ships, but wrongly identified 22 as Icebergs.

## Part 2: Rotation on the Filled dataset
As The Band1 and the scaled dataset had the highest accuracy, we use them to apply rotation. We fill the missing data on the inc_angle with mean of inc_angle.

Results: 

Loss : 0.43         
Accuracy: 86%

Confusion Matrix:

![myimage](rot_scaled_band1.png)

## Part 3 : Rotation on the dropped dataset.
Let's drop the missing values instead of filling them with mean, and after that apply the rotation.

Results

Loss : 0.31        
Accuracy: 87%

Confusion Matrix:

![myimage](band1_drop_rotate.png)

## Part 2 and 3 Conclusion:

In parts 3 and 4, it was observed that the accuracy of the model can be improved by rotating the images by the specific inc_angle for each image and removing the missing values and their corresponding images.

## Part 4: Combining Band1 and Band2

In this section, we merge two bands to create a new band that contains information from both bands.

Results
Loss : 0.28        
Accuracy: 91%

Confusion Matrix:

![myimage](band_combined.png)

### Part 5 Conclusion:

The results of the combination of both bands are evident in the decreased loss function and increased accuracy, as well as in the improved confusion matrix.
