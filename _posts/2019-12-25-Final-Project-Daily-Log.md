---
layout: post
Title: Final Project Daily Log
---

Below is a log of my daily progress, including:

1.) What I worked on today

2.) What I learned

3.) Any road blocks or questions that I need to get answered

4.) What my goals are for tomorrow

**January 7th**
I worked on reading concepts of image classification as well as sample codes that Lauren shared with me (https://www.analyticsvidhya.com/blog/2019/01/build-image-classification-model-10-minutes/). I also found my dataset on Kaggle (https://www.kaggle.com/asdasdasasdas/garbage-classification/kernels) and added another folder of data for food waste images. 
I learned to organize images into different folders. In addition, I learned three different ways to import my data into my program. Firstly, I can type in the path of my image files just like what I will have to do for creating a GitHub repo. Moreover, I can upload my images onto my Google drive and write codes to get my programs access to my drive. Lastly, I can extract a zip file of all of my images from my computer. I decide to use the third method so far, but will try the other ones if I get stuck.
Since I don't need the recycle garbage category to be so detailed, I want to group the cardboard, glass, metal and paper folders into one big recycle folder. However, this folder will contain significantly more images than other folders and it may be hard for the computer to classify. 
I will read my images into my computer and organize my data into different folders using codes for tomorrow. If I have extra time, I will start training my model.

<img src="/images/Cardboard.png" width="600"/>
<img src="/images/Glass.png" width="600"/>
<img src="/images/Trash.png" width="600"/>

**January 8th**
As planned yesterday, I worked on uploading my images to my Jupiter notebook, importing packages, extracting zip files, and almost finished organizing my data into different folders. 
During my working process, I've encountered some issues. When I was importing packages, it was shown that fastai couldn't be installed because the system couldn't find the module. At first, I followed a Github post (https://forums.fast.ai/t/modulenotfounderror-no-module-named-fastai/10663/16) by adding a path for the fastai package. However, since I was in a different folder than the path that I installed, my computer still couldn't find the package. After consulting with Lauren, I installed pytorch and fastai to my computer from my terminal, and thus made my importation successful. Another issue came up when I was trying to read my data files to my codes. It turned out that the name I entered to my code didn't match with the name of the file, and I didn't upload the file to my Jupiter notebook. From the two issues, I learned to install packages using my terminal, and to check my files more carefully before I work on my codes.
When I was organizing my images, there was an issue that I couldn't solve. Because one folder of my data came from another dataset, although the files are of the same type, the names of the images within the folder didn't match with the other ones. Therefore, I couldn't refer to them as the other ones. In order to solve the issue, I intended to use the os.rename() method (https://www.geeksforgeeks.org/rename-multiple-files-using-python/), but the renaming process wasn't successful, so I will need more help on that.
For tomorrow, I will solve the issue of renaming and thus be able to organize my data. Then I will be able to train my algorithm and hopefully get a prediction. 

<img src="/images/import.png" width="600"/>
<img src="/images/zipfile.png" width="600"/>
<img src="/images/organize.png" width="600"/>

**January 9th**
I worked on solving the problems I encountered yesterday. Since the filenames of the food folder which is newly downloaded didn't match with the other folders, I used the os.rename() method (https://www.tutorialspoint.com/rename-multiple-files-using-python) to rename all of the files in the food folder so that they match with the other folders. After fixing the problem, I was able to organize my data into different classes corresponding to their garbage types. I also began some of the training process. I let the computer learn the model that I will use for image classification, which is the resent34 model. //
At first, I was struggled with renaming the files, because the codes couldn't locate the exact directory of the files. Even though I copied and pasted the directory by "get info" tab on the file, the program still couldn't recognize it. I eventually solved the problem by incorporating both the information from the last link with the directory that I copied from the file (https://www.josharcher.uk/code/find-path-to-folder-on-mac/) and it worked.//
During the process of finding the learning rate, I faced a potential mismatch in batch sizes (I wasn't sure about the problem). I guess that it also results from the addition of the new folder since the dimensions may be different. //
I will work on fixing the mismatch tomorrow. Once I have it fixed, I can complete the training process and hopefully get training data.

<img src="/images/rename.png" width="600"/>
<img src="/images/classes.png" width="600"/>
<img src="/images/batch.png" width="600"/>

**January 10th**
I solved the problem from yesterday and printed some of my data. After fitting the model, I graphed different learning rates to find the best learning rate. I used 1e-03 as my learning rate because it was approximately the middle point of the downward slope. Applying the learning rate to the training set, I trained 10 times and successfully reduced my error rate from about 0.182 to 0.075. However, the training time was very long, and the longest training session took more than an hour. Therefore, I doubted a little that the learning rate was too slow. I also figured out the most confused categories of my data. It looked like the plastic category was most likely to be mistakenly classified and the metal category was most likely to be mistakenly classified as. 
The problem I encountered yesterday was on the size mismatch of images instead of batches. Therefore, I restricted image sizes in my codes instead of batch sizes so that all the images are of the same size. Although I learned to restrict sizes of images, I realized that the process would be much easier if I could have restrict image sizes during preprocessing because then I could address all of the potential mismatches in all three sets. 
Over the weekend, I will start to fit the model on my testing set. 

<img src="/images/Learning rate.png" width="600"/>
<img src="/images/Training1.png" width="600"/>
<img src="/images/Training2.png" width="600"/>
<img src="/images/Training3.png" width="600"/>

**January 13th**
After training my data for 10 rounds, I used my testing set to test my model. I printed out all of the predictions, and compared the first five of them with the actual categories of the trash, and they all turned out to be the same. I also printed out a confusion matrix which gives me the details of errors my model made on the testing data for calculating test accuracy. Finally, my testing accuracy turned out to be about 91%.
When I was first testing my model from my testing set, two of the images couldn't be processed into the system because they had a different file type than the other images. In order to solve the problem, I first changed the file type manually, but the images were still invisible. Therefore, I took two other images from the original dataset I downloaded that I didn't use instead and the results were shown. 
I will start to do some data analysis from tomorrow. 

<img src="/images/Result.png" width="600"/>
<img src="/images/Testing accuracy.png" width="600"/>

**January 15th**
I start my data analysis process after I got my testing accuracy. For printed quantitative data such as train_loss, valid_loss, error_rate and time, I plotted them on a histogram, line chart and scatter chart against their corresponding number of epoch. According to the graphs, it's clear that train_loss, valid_loss and error_rate generally followed a decrease trend with a seemingly exponential decay. The training time doesn't follow any obvious trend, but in general they are ranged from 40-50 minutes, which means that it takes a long time for the computer to learn the data, possibility due to the fact that I set a low learning rate. Since my sample code also includes codes to print the most confused categories, I acquired data of the categories misclassified and being misclassified to over two times. And it's evident that plastic is the category that gets misclassified mostly easily, and metal and paper are the categories that are easiest to be misclassified as. A point to note is that food images never got misclassified or be misclassified as more than once. To get a sense of how well my algorithms did, I created an actual vs predicted chart for the training and testing sets. It looks like there are only small differences between the actual and predicted amount of items in each category. 
I will do more data analysis tomorrow.

<img src="/images/Train_loss.png" width="600"/>
<img src="/images/Valid_loss.png" width="600"/>
<img src="/images/Error_rate.png" width="600"/>
<img src="/images/Time.png" width="600"/>
<img src="/images/Misclassification.png" width="600"/>
<img src="/images/Actual vs Predicted (Training).png" width="600"/>
<img src="/images/Actual vs Predicted (Testing).png" width="600"/>

**January 16th**
I continued to work on my data analysis. With my previous knowledge in Logistic Regression, I calculated the statistical values including accuracy, recall/TPR, precision, FPR, specificity and a lot of other values for training and testing data separately. The values were calculated from the confusion matrix I created. After I had a chart with all the statistical values, I plotted the values as data points on a dot plot. It looks like although they are all quite close to 1 (FPR close to 0), the values didn't vary with a certain trend. The difference between training and testing sets was obvious.

<img src="/images/Training.png" width="600"/>
<img src="/images/Training Chart.png" width="600"/>
<img src="/images/Testing.png" width="600"/>
<img src="/images/Testing Chart.png" width="600"/>

**January 17th**