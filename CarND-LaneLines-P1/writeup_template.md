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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I define range of color in HSV
second, Define color selection criteria for yellow and white .
third, Bitwise-or of yellow mask and white mask and then and with original image to get the boosted_lanes
fourth, canny edge detection, i define kernel_size = 5 
fifth, Define the Hough transform parameters with     rho = 1, theta = np.pi/180, threshold = 15, min_line_length = 60, max_line_gap = 30

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when we have curved lane line that time it might be fail 



### 3. Suggest possible improvements to your pipeline

A possible improvement would be to set hough  transform parameters to get the constant line  

Another potential improvement could be in draw_line()
