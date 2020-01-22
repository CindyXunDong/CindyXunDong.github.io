---
layout: post
title: Final Project
---
This project aims to develop an algorithm that takes in images of different kinds of garbage as input data, and classify them into the right category. Dataset used in my algorithm is downloaded from Kaggle (https://www.kaggle.com/asdasdasasdas/garbage-classification/kernels). And references come from (https://towardsdatascience.com/how-to-build-an-image-classifier-for-waste-sorting-6d11d3c9c478). 

**Introduction**
As the problem of pollution is getting worse on the planet, the concept of waste management gains its attention from people. Many countries start to sort garbage according to their categories in order to reuse some of them and correctly dispose them. For example, some places in China exerts garbage management as a law and people will be charged if they failed to classify garbage correctly. Jobs similar to helping sorting garbage become more and more popular. However, sorting garbage with pure human effort is tiring and time-wasting. Therefore, garbage classification algorithm can effectively reduce the amount of time people have to spend on sorting garbage, and hopefully improve the accuracy of sorting garbage. 

**Procedure**
Firstly, import fastai and other packages that are necessary in this project.

<img src="/images/importfinal.png" width="600"/>

Before importing images, put them into a zip file on local computer, and extract them with codes. Print names of the categories to see if lost any data.

<img src="/images/extract.png" width="600"/>

Rename some of the images so that they have the same names.

<img src="/images/renamefinal.png" width="600"/>

Split images into train, valid and test sets, and organize them into another file that is named "data".

<img src="/images/split.png" width="600"/>
<img src="/images/move.png" width="600"/>

Reshape all the images so that they are of the same size, and print some data to check if they are all recallable.

<img src="/images/reshape.png" width="600"/>
<img src="/images/showdata.png" width="600"/>

Fit the model on training data.

<img src="/images/model.png" width="600"/>

Find a good learning rate, which can be obtained by plotting loss versus learning rate and find the middle point on the downward slope.

<img src="/images/learningrate.png" width="600"/>

Print training data with the designated learning rate. This may take a long time :)

<img src="/images/trainingdata.png" width="600"/>

After training, if curious of the most confused categories, print a confusion matrix or the most confused categories with their counts.

<img src="/images/trainingconfusion.png" width="600"/>
<img src="/images/mostconfused.png" width="600"/>

Fit the model on testing data.

<img src="/images/testingmodel.png" width="600"/>

Get testing data by print the predicted categories or the first image to see if it matches with the first predicted item.

<img src="/images/testingdata.png" width="600"/>
<img src="/images/check.png" width="600"/>

If curious of the most confused categories, print a confusion matrix.

<img src="/images/testingconfusion.png" width="600"/>

Print testing accuracy.

<img src="/images/testingaccuracy.png" width="600"/>

Finally, perform data analysis and find a general trend for printed data such as training loss, valid loss, error rate etc.. Find statistical values such as accuracy, predict, TPR etc.. through google spreadsheet.

A GitHub repo can be seen with this link (https://github.com/CindyXunDong/Final_Project_Codes)