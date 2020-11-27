# CDS490Project
AI Image Recognition Project

Using the package ImageAI to learn and train the model. 

Unfortunatly the data files are too large to put into GitHub.
Here is the link to the data files, https://www.kaggle.com/alxmamaev/flowers-recognition. 

From there each flower group was split into a test folder and a train folder. I.e. Daisy-test, Daisy-train, etc.

Each flower is producing very high levels of accuracy, except for the dandelion which is only showing a 55% accuracy score. 
All the other flowers are producing recognition scores around 99% accuracy. The results from the first run are seen below. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DaisyTrained1.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionTrained1.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerTrained1.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseTrained1.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/TulipTrained1.png)

Let's take a closer look at each flower type, starting with daisies.
The next few images look at the daisy flower from different perspectives. 
The first shows the result from the ImageAI testing on a photo of daisies in black and white. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DaisyBlackWhiteTrained.png)

Notice how the algorithm is predicting that the flowers shown are roses, not daisies. 
Daisies are actually second to last on the list, with a score of 1.2025244534015656% likelihood of the flower being a daisy. 
