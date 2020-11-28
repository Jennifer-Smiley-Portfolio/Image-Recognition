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

At first glance the algorithm appears to do well with sunflowers. With the original image producing a 98.3% likelihood of the flowers being sunflowers. 
But let's see how the algorithm does with different angles and lighting on the sunflowers. 

First let's see how the algorithm does with both yellow centered sunflowers and black centered sunflowers.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerYellowTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerBlackTrained.png)

As we can see from above, the yellow centered sunflower has a slightly higher percent likelihood compared to the black centered sunflower.
This is slightly surprising because usually when you think of sunflowers you think of the black centered sunflowers.
So, I was predicting the black centered sunflowers to have had a higher percent likelihood, in comparison to the yellow centered sunflowers.

Now that we know the algorithm does well with both types of sunflowers, let's see how it does with side views and lower views of a sunflower.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerSideTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerLowViewTrained.png)

Similarly to the dandelions, the algorithm does not appear to do well with side views of sunflowers.
Only producing a 6.9% likelihood of the flower being a sunflower in comparison to the algorithms higher likelihood of it being a rose, 
where it produces a likelihood of 91.1%.

So, again the algorithm appears to have difficulties with the side views of flowers. 

Looking at the second image where the photo is taken slightly below the sunflower, the algorithm does a better job. 
Here is produces a 99.5% accuracy towards the flower being a sunflower, which is correct.

Now let's see how the algorithm does when the photos are zoomed in on the flower and zoomed out on a field of sunflowers.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerZoomedInTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerZoomedOutTrained.png)

With the zoomed in photo, we can see that the algorithm is having a difficult time.
The algorithm only produces a likelihood of 33.9% towards the flower being a sunflower in comparison to the 62% likelihood of the flower being a rose.
I wonder if it is predicting a rose over the sunflower because the petals are slightly translucent, just like they were with the side view of the sunflower. 

When we look at the zoomed-out photo of the field of sunflowers we see the algorithm did a good job.
Predicting that the flowers in the field have an 87.2% likelihood of them being sunflowers over the other 4 types of flowers in the model. 

From the two above results, we can conclude that the algorithm does well with zoomed out photos of sunflowers but does not do well with zoomed in photos of sunflowers. 

Lastly, let's see how the algorithm does when the sunflower is closed and when the photo of the sunflower is taken in the dark.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerClosedTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/SunflowerDarkTrained.png)

Again, the algorithm appears to have trouble with the flower in its closed position. 
Producing a likelihood percentage of 11.2% of the flower being a sunflower, 
in comparison to what it believes with a higher likelihood that the flower is a daisy with an 87.7% likelihood. 

On the other hand, the algorithm does quite nicely with the dark photo of the sunflowers, producing a 85% likelihood towards the flowers being sunflowers.

Overall, the sunflowers are easily identifiable for the algorithm. Unless the sunflowers are in a closed position, seen directly from the side, or are super zoomed in. 

## Roses

Moving on to roses. There are two things that might end up confusing the algorithm. 
One thing that might confuse the algorithm are the different colors of roses. 
Roses come in all different colors so if the algorithm relies heavily on color this will cause a problem. 
The other thing that might confuse the algorithm are the different shapes of roses. 
For example, dog-roses and beach roses both have a larger center with fewer petals. 
Whereas classic roses have more petals, and their centers are often hidden by the petals. 

So, let's first see how the algorithm deals with the first problem of the different colors. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RosePinkTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseRedTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseTrained1.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseYellowTrained.png)

The algorithm appears to do the best with the pink and purple roses, identifying them with the highest levels of likelihood.
The red rose then comes next with a 95.9% likelihood of it being a rose. Followed up with the yellow rose at 80.5% likelihood. 
The second most likely flower for the pink, purple, and red roses are tulips which makes sense because some roses do look similar to tulips in shape. 
So, it makes sense that the algorithm would have it in the second spot. 
The yellow rose has a dandelion as the second spot, likely due to the color as one stage of dandelions are yellow. 

Now, let's see how the algorithm does when there are different shapes of roses and when the photo is black and white. 

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseOldTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseBouquetTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseBlackWhiteTrained.png)

The first photo is a rose nearing the end of its life span and the algorithm does a pretty good job with this one, producing a 95% likelihood of the flower being a rose.
The next photo is one of a bouquet of roses. I chose this photo because I was sure the algorithm would think they were tulips by the shape of the roses, but I was wrong.
The algorithm did a good job of recognizing they were roses with a 84.2% likelihood and it only had tulips at a 13.4% likelihood.
The third photo is a black and white photo of a different type of rose, one that is more open with fewer petals and a larger center. 
As we can see, the algorithm did have a little more trouble with this photo. 
Only producing a 46.5% likelihood of the flower being a rose with the second highest likelihood of 43.6% toward it being a dandelion. 
So, the algorithm did a better job with roses than it did with daisies for black and white images but it was not as good as the other two flowers.

Finally, let's look at how the algorithm does with roses at a distance and up close.

![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseDistanceTrained.png)
![alt text]( https://github.com/jsmiley2/CDS490Project/blob/main/Results/RoseZoomedInTrained.png)

Similarly, to the distance results from the dandelions, the algorithm is also having a difficult time with the roses at a distance. 
The algorithm barely thinks that flowers are roses over tulips with a 45.7% toward roses and a 45.5% toward tulips. 
On the other hand, the algorithm appears to do very well with roses close up. Producing a 97% likelihood toward the flower being a rose.

Overall, the algorithm was able to correctly guess the correct flower with all of the above images although it had some trouble with the black and white photos and the roses at a distance. 

## Tulips

Like roses, tulips have different shapes. 
There is the classic tulip shape where the petals are upright, then there are tulips that resemble lilies where the petals are open. 
