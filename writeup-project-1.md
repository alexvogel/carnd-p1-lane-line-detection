#**Finding Lane Lines on the Road** 

##Writeup Template

###You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image0]: ./myexamples/original.jpg "Original"
[image1]: ./myexamples/grayscale.jpg "Grayscale"
[image2]: ./myexamples/gaussianblur.jpg "Gaussian Blur"
[image3]: ./myexamples/edges.jpg "Edges"
[image4]: ./myexamples/mask.jpg "Region of Interest"
[image5]: ./myexamples/hough.jpg "Hough Lines"
[image6]: ./myexamples/polyfit.jpg "Polyfit"
[image7]: ./myexamples/result.jpg "Detected Lines"

---

### Reflection

###1. Pipeline For Lane-Line-Detection

My pipeline consisted of 6 steps.

Step 1: Converting to grayscale

![Original][image0]
![Grayscale][image1]

Step 2: Applying Gaussian Blur

![Gaussian Blur][image2]

Step 3: Detecting Edges

![Edges][image3]

Step 4: Masking Region of Interest

![Region of Interest][image4]

Step 5: Drawing Hough Lines

![Hough Lines][image5]

Step 6: The hough lines are used for generating (regression) two lines which aproximate the lane lines. Hough lines on the left half of the image are used for the left lane-line and the hough lines on the right half of the image are used for the right lane-line.

![Polyfit][image6]

Step 7: Masking the Regression Lines

![Mask2][image7]

Result: The Lane-Lines are properly detected

![Result][image8]

###2. Potential shortcomings with current pipeline


One potential shortcoming would be in sharp curves, when the lane lines are so heavily bend, that the corresponding hough lines cross the center line of the image. In this case, the regression/polyfit result will get increasingly inaccurate and the correct detection of the lane lines could fail.


###3. Possible improvements to pipeline

- ?
