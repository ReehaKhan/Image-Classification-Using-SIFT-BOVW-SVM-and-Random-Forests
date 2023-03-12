# Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests

In this task, Image Classification is performed using the concept of Bag of Visual Words as the feature extractor followed by 2 different classifiers i.e., Support Vector Machines and Random Forests. The feature descriptor used is Scale-Invariant Feature Transform (SIFT). The algorithm is evaluated on 2 different data sets. The performance is quantified using metrics like Accuracy Score, F-1 Score, True Positive Rates, and True Negative Rates.

## Introduction
Image Classification is a computer vision problem that involves assigning label(s) to an image based on its features. Bag of Visual Words is an image classification technique that represents an image as a histogram of the local features of the image. The feature descriptors are extracted using different feature extractors like SIFT, SURF, BRISK, etc. Once the features descriptors are extracted, clustering Algorithm is then applied to the feature descriptors to define the vocabulary. The centers of these clusters are the visual words in the vocabulary or the codebook. 
Each image can be represented as the frequency of the visual words present in the image. This frequency is found by creating histograms for each image. This histogram representation of each image is then normalised. The histograms are then fed into the classifiers along with their true labels to train the classifier. When any new image is being tested, the image is first converted into the histogram representation which is then fed into the classifier to make a prediction. 

## Methodology
In this task, 2 different data sets are used and for each the same pipeline is followed.
![Methodology Diagram](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/flowchart.jpg)

## Data Sets
Two Data Sets have been used in this task. 
1. The first dataset contains object images with 4 classes: Soccer Ball, Accordion, Dollar Bill, and MotorBike. The train set and test set has already been split. The train set contains 14 images per class making a total of 56 images, and the test set contains 2 images per class making a total of 8 images.
2. The second dataset contains a total of 3670 flowers images with 5 classes: daisy (633 images), dandelion (898 images), roses (641 images), sunflowers (699 images), and tulips (799 images). The train set and test set is split by using the train_test_split function from sklearn.  

[Data Link](https://drive.google.com/drive/folders/1pashiwjX_g6bPr9OAZQnOFK6CljP8ElX?usp=sharing)

## Requirements
- python version 3.8
- opencv-python 4.6.0
- scikit-learn 1.2.1

## Steps to run the Notebook
1. Download the Notebook (a preview of the file is not available on Github due to the file being heavy).
2. Open the Notebook using Google Colab or Jupyter Notebook.
3. Use the link of the data set shared to replace the paths of the dataset in the notebook.
4. Run the Notebook to first train the model and then test on the given data set.
5. The trained model can be used on other images as well.

## Results
The evaluation metrics used are Accuracy score, F1 score, true positive rate (TPR), and false positive rate (FPR). The classifiers are Support Vector Machines (SVM) and Random Forests (RF).
1. Objects Data Set

![Evaluation Metric Scores on Objects DataSet](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/objects_metrics.jpg)

2. Flowers Data Set

![Evaluation Metric Scores on Flowers DataSet](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/flowers_metrics.jpg)


### Few Correct and Incorrect Predictions
1. Objects Data Set

    - SVM
   
        - Correctly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/objects_svm_correct_pred.jpg)
        - Incorrectly Classified   
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/objects_svm_wrong_pred.jpg)
    
    
    - Random Forests
    
        - Correctly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/objects_rf_correct_pred.jpg)
        - Incorrectly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/objects_rf_wrong_pred.jpg)
    
    
    
2. Flowers Data Set

    - SVM
    
        - Correctly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/flowers_svm_correct_pred.jpg)
        - Incorrectly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/flowers_svm_wrong_pred.jpg)
    
    - Random Forests
    
        - Correctly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/flowers_rf_correct_pred.jpg)
        - Incorrectly Classified
    ![alt text](https://github.com/ReehaKhan/Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests/blob/main/images/flowers_rf_wrong_pred.jpg)
    
