# ChestXrayDiagnosis
This program was created as a part of an AI for Medical Diagnosis course on Coursera. 
It takes chest x-ray images as inputs and outputs probability of diagnosis for a 
variety of conditions. 

First, it is ensured there is no data leakage between training, validation, and test
datasets. The x-ray images are prepared by standardizing the mean to 0 and the 
standard deviation to 1. The images are also converted to a three-channel format.
To address class imbalance a weighted loss function is used. A pre-trained 
DenseNet121 model loaded directely from Keras is utilized with two additional layers
added. After training, the predictions are generated and evaluated using ROC curves
and AUROC values. 

Finally, the use of GradCAM is explored to evaluate the important regions in the  
images for predicting pathological condition. 

