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

## Daisies

The next few images look at the daisy flower from different perspectives. 
The first shows the result from the ImageAI testing on a photo of daisies in black and white. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DaisyBlackWhiteTrained.png)

Notice how the algorithm is predicting that the flowers shown are most likely roses, not daisies. 
Daisies are actually second to last on the list, with a score of 1.2025244534015656% likelihood of the flower being a daisy. 
Whereas roses are shown with the highest percentage at a 92.7% likelihood. 

This means that the algorithm likely has a difficult time working with black and white photos as most image recognition software does. 

If we look at another angle of the daisy does it still produce an accurate result?

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DaisySideTrained.png)

The above shows, yes, it does. Although it is no longer with such a high accuracy as the first head on daisy photo we entered into the database.
Although, it still has an accuracy score of 83.6% likelihood of the flower being a daisy, which is still fairly high and it does produce the correct result. 

This proves that the algorithm, with daisies anyways, does work well with side profiles of flowers. 

Lastly what if we were to look at how the algorithm does when it is presented with flowers at a distance.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DaisyDistanceTrained.png)

Again, we see that the algorithm does very well with images of daisies at a distance. 
Producing a 99.3% likelihood of the flower being a daisy. 

## Dandelions

Moving on to dandelions. This was the most difficult flower for the algorithm. 
Which makes sense, the flower has three different stages, blooming while yellow, blooming while white and puffy, and lastly when all the seeds have fallen off. 
So, we need to see how the algorithm does with these different stages. 
