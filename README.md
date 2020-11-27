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

First, let's look at dandelions when they are yellow. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionCloseUpYellowTrained.png)

As we can see here, the algorithm produces a very high probability of the flower being a dandelion at a 95.6% likelihood. 

What about when they are in their puffy seed stage? 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionHeadOnTrained.png)

Again, the algorithm does very well. But both of these images were taken of a head on view of the flower. 
What happens when we take in a picture of a dandelion from a side view?

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionSideTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionTrained1.png)

Here we see the accuracy drop by quite a bit. The yellow dandelion shows the highest likelihood towards a sunflower rather than a dandelion, 
which it has at a 12.7% likelihood. It is possible this is due to the images in the sunflower training dataset. When the flower looks flat and yellow it produces a 
higher likelihood for sunflowers over other flowers. 
But the accuracy also drops for dandelions in the seeded state. Here the likelihood percentage is dropped to 55% likelihood. This still does produce a higher likelihood for the correct answer, but the percentage of accuracy is still low. 

So, we can conclude that the algorithm does not work well for side profiles of dandelions in both stages. 

Now, let's look at how the algorithm does with multiple dandelions close up and far away.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/Dandelion2TypesTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionDistanceTrained.png)

As we can see from above, the image where there are both yellow and seeded dandelions does very well with a 99.3% likelihood of the flowers being dandelions. 
The photo where the dandelions are seeded and seedless that are further away does not do as well, only producing a 52% likelihood towards them being dandelions.
The second highest likelihood being 46.2% towards them being tulips.
This is likely because the shape of the seedless dandelions, from a distance, are similar to that of tulips. 

So, the algorithm does well when it is produced with an image showing both a yellow dandelion along with a seeded dandelion.
It does not do as well when the dandelions are further away. 

How does the algorithm do when it sees just a single almost seedless dandelion?

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionDeadTrained.png)

As we can see above, the algorithm is able to identify the dandelion when it is at the final stages of the flower.
So, the algorithm works well individual on all three stages of the dandelion. 

The algorithm even does well when the photos are in black and white. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/DandelionBlackWhiteTrained.png)

Producing a 99.1% likelihood of the flower being a dandelion. This flower does much better than the daisy which had a 1.2% likelihood of the flower being a daisy. 

Overall, the algorithm does very well with most dandelion photos. It has a little bit of trouble with side views of all three stages of the flower, 
but it does well with multiple dandelions and close up photos. 

## Sunflowers

At first glanse the algorithm appears to do well with sunflowers. With the original image producing a 98.3% likelihood of the flowers being sunflowers. 
But let's see how the algorithm does with different angles and lighting on the sunflowers. 

First let's see how the algoirthm does with both yellow centered sunflowers and black centered sunflowers.

