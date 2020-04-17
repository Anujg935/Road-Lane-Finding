# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to HSV color space (i found value to be better to use), then I used guassian blur to decrease any unwanted noise in the input image after that the image is fed to canny edge detector to detect edges in the image with a threshold value.Next found vertices for finding the region of intered=st and fetd the vertices to the fuction for finding and cropiung the ROI. FInnally used houhlines with tunned input parameters to dray the line.Special thing is to find the line that is continous in drawline function.

For that i firstly difeerentiate the left line and right line points on the basis of +ve and-ve slope and after that chgooses ymax and ymin according to image frame.and with polyfit and poy1d functions found out other x coordinares than call cv2.draw to continous lines.



### 2. Identify potential shortcomings with your current pipeline

I think shortcoming is that its not very much prone to change in brightness and intensity.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make this intelligent and dynamic not just base don fixed mathematical modelas or algorithms.
