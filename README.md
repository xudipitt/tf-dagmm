# tf-dagmm
A tensorflow Implementation of [dagmm](https://openreview.net/pdf?id=BJJLHbb0-): Deep Autoencoding Gaussian Mixture Model for Unsupervised Anomaly Detection, Zong et al, 2018

## Requirement
I've trained the model successfully on the below packages:
* Python 3.6.4
* Tensorflow 1.5.0(GPU version)

## Note
* This tf model is used to perform a real case of anomaly detection for my job. 
I cannot provide the dataset I used due to the commercial security.
* I've done some experiments on using several autoencoders(compressions namely in the paper) to analyze the important regions as experts suggested in each image.
The results didn't perform well however.
* In my case the required training time is short. The results seem good about 2000 ~ 3000 epochs

## Issue
* When the dimension of encoded vector grows large(larger than 4 for example), The issue of "Matrix is uninvertible" will occur during the training. 
I think it is the singularity issue of GMM(just my guess). Currently I cannot solve this bug. Any suggestion is welcome.