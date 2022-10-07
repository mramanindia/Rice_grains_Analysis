Download Data: https://drive.google.com/drive/folders/14ARDU8JgOE9PwjhQN_3ZYMJNGeHsEfRL?usp=sharing

# Counting_rice_grain
Counting rice grain and detecting the broken rice grains in the image. Solving the Touching grain problems using WaterShed algorithm.


## Note:

This Notebook Aims to solve two objectives:
* Objective 1: Count the number of rice grains in the Image.
* Objective 2: Find the number of broken grains in the Image.


Technology used:  Computer Vision, OpenCv, WaterShed-Algorithm, Image Pre-processing, Image Segmentation, and others.
The Approach of the objectives are well elucidated and have clear Visualization for better Insights into the working of each notebook cell.

\
I hope you will love the approach and the presentation of the solution.
\
Thanks & Regards,\
Aman India.

\
**My handles**
> LinkedIn: https://www.linkedin.com/in/mramanindia/
\
> Github: https://github.com/mramanindia
\
> Mail: amanindiamuzz@gmail.com
\
> Kaggle: https://www.kaggle.com/amanindiamuz

---
# Image Information
* The background will always be blue.
* There will be a mix of broken and non-broken rice grains.
* The grains will not overlap but can touch each other.

<img src="https://i.ibb.co/z5X92Bq/image-1.jpg" alt="image-1" border="0">

# My Approach (Solution)
---

## The Steps involved in solving the Objectives are as follows:
1. **Importing Required Libraries**
2. **Defining Required Function**
    *  Defining custom "show" function for Image Visualization
2. **Image Pre-Processing**
    * GrayScale Conversion
    * Image Thresholding
    * Morphological Transformations (Noise Removal)
3. **Counting rice grains using the Contours method**
    * Working over Clear image to get insight into grain touching problem
3. **Applying Watershed Algorithm** (Solving grains touching problem)
    * Applying Watershed Algorithm for Solving Touching rice grains problem
  
4. **Counting total Rice grains and Broken Rice grains using the contour area**
    * For total rice grains counting: the Watershed method
    * For broken rice grains counting: A filter of an average area of broken rice grain.

# Explanation
<a href="https://www.youtube.com/watch?v=5BAdC-UXpEQ"><img src="https://i.ibb.co/kqg4Jpb/Counting-RIce-Grains.png" alt="Counting-RIce-Grains" border="0"></a>
## Video Explanation: https://www.youtube.com/watch?v=5BAdC-UXpEQ
The main Idea behind solving the objectives(Counting rice grains) is to make the provided image in the best possible format. \
If there would be clarity in the image, and rice grains are well separated from the background image then there would be ease in counting them.

Then, Solving the Corner cases and hence building the soluction.


**There are a total 3 major and challenging parts in building solutions:**
1. Image Preprocessing
2. Solving Grains touching problem
3. Counting broken rice

## Image Preprocessing
Image preprocessing is one of the vital parts of the solution, as, on this itself, Whole Ideology relies.

If the image is perfectly tuned as per the needs then it becomes easy to work further with the approaches.

The crucial part of Image preprocessing is tuning the Image, it takes a lot of trail and error to fix the parameter to the required value.

As part of Solution, I have used:
* Conversion of BGR Image to Grayscale Image
* Image Thresholding
* And removing noise from the thresholded image using morphologyEx (Opening)

After all the processes, the clear Image was ready for further use. 


## Solving Grains touching Problem
After successfully Pre-processing the image, there comes the challenging part of the problem statement.

"**Counting the rice grains that are touching each other**" 

It is not even easy for a human eye in manual inspection process to count the rice grains. The small size and white color creates illusion.

Well for Machines,\
Counting Rice grains are quite easy if they are well separated. The reason, is there are lots of algorithms out there and various techniques that can come in help.

But when there is an object touching or overlapping problem then there needs a lot of effort in grains classification.

In our case, it becomes more difficult as the rice grains are quite small in size.


Because of its small in size,
We can't apply processes like erosion to get the touching corner part separated.

So,
For Solving this problem, I have applied the WaterSheld Algorithm:

WaterSheld Algorithm is based on extracting sure background and foreground and then using markers will make the watershed algorithm run and detect the exact boundaries.

It is like, filling the valleys and then separating hills out of that.

## Counting broken rice
After using the Watersheld algorithm, We will get the total number of rice present in the image, but counting broken rice grains are one of the typical tasks.

I used an area-based approach, where I put a threshold after several trail and errors that helps in classifying the rice grains into two categories.
<center> **Either Broken rice grain or Full rice grain**. </center>

If the area of the Image is below the provided threshold then it is counted in the broken rice category.

Thus with this, we are done with the solutions of both of the objectives .\
Well,\
I have added more approaches that came to my mind in the later section of this notebook.
That too can be Implemented but I found this approach more Profound, thus it is part of the solution.










