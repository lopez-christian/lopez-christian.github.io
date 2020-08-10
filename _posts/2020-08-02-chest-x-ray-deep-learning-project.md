---
layout: post
published: true
title: "Chest X-Ray Deep Learning Project"
date: '2020-08-10'
---
## Building Image Classifier with Keras Using Chest X-Ray Images (Pneumonia) Dataset to Detect Pneumonia 

<p align="center">
<img width="1086" alt="Screen Shot 2020-08-10 at 1 15 15 PM" src="https://user-images.githubusercontent.com/53641091/89826737-8de5eb00-db0b-11ea-80f7-5e934e86c3dd.png">
</p>

My intent with this project was to build a simple deep learning neural network that would be capable of performing binary classification on Chest X-Ray Images (Pneumonia) from Kaggle.com [click here](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia). I had to import a module that would serve as an operating system interface from python in the form of OS in order to interact directly with the directories located on my computer. Keras was used extensively in this project in order to make use of all of its deep learning capabilities. Numpy was used in the manipulation of images in the form of arrays. Pandas, Matplotlib, Seaborn, and Plotly were utilized in the exploratory phase of this project in order to visualize the data. 

<p align="center">
<img width="1075" alt="Screen Shot 2020-08-10 at 2 14 45 PM" src="https://user-images.githubusercontent.com/53641091/89832147-dd301980-db13-11ea-84bc-0e05292404b3.png">
</p>

I started with importing the necessary modules and libraries needed for this project. I then went ahead and performed the rudimentary data exploration phase by reading in some images as examples of what the data looks like. I also assigned certain directories to their respective variables in order to make use of them in the visualization and deep learning model building stages. I then went ahead and created simple histograms and pie charts comparing people with and without pneumonia lung disease in each of the 3 directories (train, test, and val).

<p align="center">
<img width="458" alt="Screen Shot 2020-08-10 at 2 34 46 PM" src="https://user-images.githubusercontent.com/53641091/89833864-a8719180-db16-11ea-8dd5-32b1fa958806.png">
</p>

<p align="center">
<img width="1078" alt="Screen Shot 2020-08-10 at 2 16 35 PM" src="https://user-images.githubusercontent.com/53641091/89832465-36984880-db14-11ea-98b3-f4bac8acbc10.png">
</p>

<p align="center">
<img width="1078" alt="Screen Shot 2020-08-10 at 2 16 52 PM" src="https://user-images.githubusercontent.com/53641091/89832589-6e06f500-db14-11ea-8bab-c292ab5db21f.png">
</p>

<p align="center">
<img width="1078" alt="Screen Shot 2020-08-10 at 2 17 16 PM" src="https://user-images.githubusercontent.com/53641091/89832684-8840d300-db14-11ea-8d18-b47f0bc3e607.png">
</p>

<p align="center">
<img width="503" alt="Screen Shot 2020-08-10 at 2 22 23 PM" src="https://user-images.githubusercontent.com/53641091/89832944-02715780-db15-11ea-9f8c-e0203d1293de.png">
</p>

<p align="center">
<img width="1056" alt="Screen Shot 2020-08-10 at 2 25 08 PM" src="https://user-images.githubusercontent.com/53641091/89833081-4fedc480-db15-11ea-826d-306cd0e18edf.png">
</p>

Arguably, the most difficult part of this project was constructing the deep learning convolutional neural network to classify the images. I played around with certain parameters in terms of batch size and epochs. There were a lot of moving pieces when it came to initializing this model in order to make it the most efficient possible. I made use of sigmoid and relu activation functions. The final stage was to evaluate my model and the accuracy percentage turned out to be ~90% and the loss percentage was ~36%. In conclusion, I would say that the model turned out alright, although I'd like expand on this work in the future and see if there is any way I could descrease the loss at all. The weights are saved under model_parameters.h5 after running this project in its entirety.

<p align="center">
<img width="563" alt="Screen Shot 2020-08-10 at 2 26 56 PM" src="https://user-images.githubusercontent.com/53641091/89833385-cab6df80-db15-11ea-9c14-3be18e9520e5.png">
</p>

<p align="center">
<img width="994" alt="Screen Shot 2020-08-10 at 2 27 58 PM" src="https://user-images.githubusercontent.com/53641091/89833392-cee2fd00-db15-11ea-908c-b2a1df52cd4f.png">
</p>

<p align="center">
<img width="994" alt="Screen Shot 2020-08-10 at 2 28 27 PM" src="https://user-images.githubusercontent.com/53641091/89833399-d1dded80-db15-11ea-9c17-2c856dcf701f.png">
</p>

The model performed quite well in the training phase as it shows it improved in accuracy as the epochs increased, while also reducing the loss. The model accuracy of ~90% and model loss of ~36% on the test data suggests that the model did quite well in classifying the images it was provided with. We would able to rely on this model to classify the images with significant amount of certainty whether it is an image showing lungs as being either positive or negative for Pneumonia. These types of results are what we are looking for when conducting tests based on model performance. This type of neural network algorithm can be of great help to any medical professional working in the field and attempting to diagnose a patient. 

<p align="center">
<img width="749" alt="Screen Shot 2020-08-10 at 2 30 33 PM" src="https://user-images.githubusercontent.com/53641091/89833628-3731de80-db16-11ea-8a81-fb61a92f21d5.png">
</p>

<p align="center">
<img width="392" alt="Screen Shot 2020-08-10 at 2 30 55 PM" src="https://user-images.githubusercontent.com/53641091/89833632-3ac56580-db16-11ea-9783-4fa56546d5ab.png">
</p>

<p align="center">
<img width="741" alt="Screen Shot 2020-08-10 at 2 31 13 PM" src="https://user-images.githubusercontent.com/53641091/89833641-3e58ec80-db16-11ea-89dc-f4f2fba28b68.png">
</p>

<p align="center">
<img width="388" alt="Screen Shot 2020-08-10 at 2 31 28 PM" src="https://user-images.githubusercontent.com/53641091/89833649-4153dd00-db16-11ea-9bf7-3600abe15a28.png">
</p>

## Key takeways:

*1. The neural network may be used to aid the healthcare professional in stream-lining the diagnosing process when classifying images. This may allow for a quicker return time and greater patient satisfaction. Which would, in turn, lead to the potential for more positive outcomes because the positive patients can begin treatment right away as opposed to waiting lenghty periods of time for the results to arrive.*

*2. There is the prospect of less mistakes being made while also looking at a greater amount of pictures at any given time. Having a doctor look at countless pictures of patients' lungs can be quite a lengthy process, which can lead to many errors being made along the way. A neural network can be employed in order to cut out some of the work and make initial deductions. This would relieve any doctor's stress at having to sift through a great deal of images. The neural network would be able to assign probabilities to each image and then the doctor can step in and look at each image with a more rigorous eye to determine the diagnosis.*

*3. Implementing a neural network can prove to yield a greater ROI for the institution in the long-run. Therefore, the doctors would be allowed more time to invest or focus their time on less repetitive tasks that cannot be automated. The less time the doctors expend looking at images to arrive at a diagnosis, the more time they can allocate to dealing with more demanding procedures.*

<p align="center">
<img width="661" alt="Screen Shot 2020-08-10 at 2 42 42 PM" src="https://user-images.githubusercontent.com/53641091/89834895-8842d200-db18-11ea-98c5-4f01d9642f56.png">
</p>

[Chest X-Ray Deep Learning Project](https://github.com/lopez-christian/Chest-X-Ray-Deep-Learning-Project)
