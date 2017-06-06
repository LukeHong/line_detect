# **Finding Lane Lines on the Road**

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidYellowCurve2.jpg "Processed"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale and did the gaussian blur, then I set the region of interest to reduce computation time. Third, I used canny edge to get the edges in the region, then use the hough lines to draw a "lane line" image.  Finally, by using the weighted image to combine the original image and the image of lines as result.

The slope of left lines will be positive most of the time and the slope of right lines will be negative, so I could set different color according to whether the slope is positive or negative.


![Result][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there is a car in the region of interest, then the result of hough lines will be quite a mess.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to tuning the parameter of canny edge and hough lines.
