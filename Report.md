
# **Finding Lane Lines on the Road** 

## Report

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


## Reflection 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I only keep the white and yellow pixels of the image. Then, I converted the images to grayscale, then I applied Gaussian smoothing. Then I applied Canny Edges. And final steps is to filter based on region of interest. In current project, the region of interest can be roughly assumed as trapezium shape I.e. the road. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by finding the slope of left and right lanes.
For each line in the input, slope greater than zero is for left lane while slope smaller than zero is for right lane.
For each lane(left and right), I use polyfit() from numpy to perform curve fitting to find the slope and b values in  # y = m*x + b.

## Reflection 2. Identify potential shortcomings with your current pipeline 

One potential shorting coming would be what would happen when the number of 'valid' lines input is insufficient to draw a proper lane lines.

## Reflection 3 . Suggest possible improvements to your pipeline 

possible improvement could be using a better slope_threshold value and not drawing the lane lines if the number of valid input is not passing certain threshold value.


```python

```
