# **Final Report - Breast Cancer Tumor Classification**
**OBJECTIVE:** To build a convnet to accuratly predict if a breast tumor is malignant (i.e. cancerous) or benign.

## *Contents*

* Introduction
* Data
    - Image Downloading and formatting
* Building the Baseline Neural Network (i.e. Traditional Method)
* Building the Convolutional Neural Network
    - Data preprocessing 
* Data Preprocessing
* Non-Convolutional Neural Network
* Convolutional Neural Network
* Modifying our ConvNet
* Pre-Trained Convnets
* Accuracy Measurements
* Conclusion
* Appendix


## *Introduction*

Although the screening of breast cancer has been found to greatly reducing mortality among breast cancer patients, there has been high rates of false positives and negatives documented in the U.S and Canada. More specifically the average sensitivity of digital mammography has been on average around 86.7% while the average specificity around 88.9%. 

With these numbers, it is safe to state that breast cancer detection has proved to be been a major issue for the pathologists and medical practitioners in diagnosis and treatment planning of the second leading cause of cancer deaths in the world. 

The manual identification of cancer from microscopic biopsy images is to some degree subjective in nature and may vary from expert to expert depending on their expertise and other factors including lack of specific and accurate quantitative measures to classify the biopsy images as harmless (benign) or cancerous (malignant) one. 

For this project, we aim to use Deep Learning to classify microscopic images of breast tumor tissue into benign or malignant categories to facilitate a speedy and accurate workflow to be used as an additional tool in tackling the challenges stated above. 

Traditionally, we know that the distinction between the two have been at times a daunting task for pathologists, resulting in the conservative approach of going the treatment route for a patient that may not have otherwise needed treatment. We aim to use Convolutional Neural Networks to create a higher level of confidence in both the diagnosis as well as the treatment of these varying cases, as well as to reduce both the emotional trauma as well as the costs associated with undergoing unnecessary treatments.

We will be demonstrating our efforts to increase the accuracy of Neural Nets and for our final metrics, we aim to look at not only the prediction accuracy on our testing data, but also pay particular attention to the precision of true positives (TP), true negatives (TN), false positive (FP) and false negative (FN). 

Lastly, throughout this report, we have included additional information either above or inside each block code for enhanced readability. 

##  *Data*

Our dataset is obtained from The Breast Cancer Histopathological Image Classification (BreakHis). It is composed of 9,109 microscopic images of breast tumor tissue collected from 82 patients using different magnifying factors (40X, 100X, 200X, and 400X). It contains 2,480 benign and 5,420 malignant samples (700X460 pixels, 3-channel RGB, 8-bit depth in each channel, PNG format). This database has been built in collaboration with the P&D Laboratory – Pathological Anatomy and Cytopathology, Parana, Brazil. 

What we really liked about this dataset compared to others was that it provided microscopic images at different levels of magnification compared to most datasets in this category which usually only provide one. This characteristic of the data paired with the limited number of images available will most likely affect the overall accuracy compared to models that are trained on only one magnification. However, this will *allow for the development of a more flexible/universal model* which can process several different magnifications of images while still being accurate enough to assist the pathologist in making a final decision.

We have included the direct link to this data set here:

https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/
