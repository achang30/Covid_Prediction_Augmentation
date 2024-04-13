# Data Augmentation for Covid-19 Classification

### Note: A comprehensive analysis can be found in the pdf file. 

Allen Chang


29 March 2024

## Abstract

In early 2019, the novel coronavirus began rapidly spreading around the globe. At the 
time, there was little known about the virus and no known treatment and vaccines. At present, 
much more research has been conducted, and there is much more abundant data for disease 
analysis. Here, I create deep learning models to classify whether a patient has coronavirus based 
on chest x-ray scans. I also experiment with various data augmentation methods to identify 
which one results in best performance. 

## Introduction

According to the WHO, as of July 2021, there have been approximately 190,833,853 
confirmed Covid-19 cases and 4,100,087 confirmed Covid-19 related deaths [1]. Thus, this is a 
severe worldwide pandemic. With Covid-19 being incredibly widespread, having a quick, 
efficient, and accurate method to determine whether a patient is infected is crucial. Typically,
deep learning models benefit from increased training data. Thus, I will experiment with various 
augmentation methods to increase training data and examine whether they present better model 
performance. 

## Methodology


In this study, I will utilize a CNN model architecture to identify individuals infected with 
COVID-19. One model will be trained on duplicated normal training data, one model will be 
trained on Gaussian blurred data concatenated with normal training data, and one model will be 
trained on scaled data. I will compare the models using various metrics including F1-score, 
accuracy, AUROC, precision, and recall. 
The data can be found here: https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database/data

(Covid-1 to Covid-500 used for Train; Normal-1 to Normal-1500 used for Train)
(Covid-2941 to Covid-3440 used for Val; Normal-7869 to Normal-8868 used for Val)

## Expected Results

I expect the models trained on augmented data to see a statistically significant 
improvement from the model trained on normal training data due to the model being able to 
adapt to natural variation in scans. Nevertheless, I am eager to see which augmentation method
performs better. 
A relatively small sample size may be one limitation. Furthermore, more architectures 
can be tested. More trials can also be done to better assess if there is truly a significant difference 
between augmentation methods. 

## References


[1]	S. U. Rehman, S. U. Rehman, and H. H. Yoo, “COVID-19 challenges and its therapeutics,” Biomed. Pharmacother., vol. 142, p. 112015, Oct. 2021, doi: 10.1016/j.biopha.2021.112015.


## Extra References


The authors of the dataset have asked the following two sources to be cited:
-M.E.H. Chowdhury, T. Rahman, A. Khandakar, R. Mazhar, M.A. Kadir, Z.B. Mahbub, K.R. Islam, M.S. Khan, A. Iqbal, N. Al-Emadi, M.B.I. Reaz, M. T. Islam, “Can AI help in screening Viral and COVID-19 pneumonia?” IEEE Access, Vol. 8, 2020, pp. 132665 - 132676.
-Rahman, T., Khandakar, A., Qiblawey, Y., Tahir, A., Kiranyaz, S., Kashem, S.B.A., Islam, M.T., Maadeed, S.A., Zughaier, S.M., Khan, M.S. and Chowdhury, M.E., 2020. Exploring the Effect of Image Enhancement Techniques on COVID-19 Detection using Chest X-ray Images. arXiv preprint arXiv:2012.02238.



