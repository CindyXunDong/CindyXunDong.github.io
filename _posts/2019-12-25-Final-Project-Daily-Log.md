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

**January 13th**

**January 15th**

**January 16th**

**January 17th**