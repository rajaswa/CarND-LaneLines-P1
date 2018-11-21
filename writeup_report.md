# **Finding Lane Lines on the Road** 

## Writeup Report


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report






---

### Reflection

### 1. Pipeline Description

First of all, to get a better view, I increased the thickness of lines to 8 in draw_lines() function.

Next, I did some major changes to the hough_lines() function. To keep the actual code of hough_lines() short, I implemented my own functions just above the cell of helper functions.

I introduced a new variable 'flag' to check the sign of the slope while calculating intercept and slope. This flag helped in eliminating any unwanted or irredular cases of hough lines.

Next, I used a very simple average() function to simply decrease number of lines of code and convenience. This was done to calculate the average of multiple hough lines obtained to get the best fit single line.

Finally got the complete extended line by using the slope and intercept calculated before in the getline() function.




### 2. Potential shortcomings


One of the major shortcoming which is clearly visible is the lack of versatility of the pipeline.
The pipeline fails to work properly on many instances in the challenge video. Mostly due to visual obstructions on the left lane.
Also, fitting to major curvature of lanes is an issue.


### 3. Possible Improvements

To resolve the issue of fitting curvatures of lanes, we can possibly plot a curve instead of a line.
Curve can be obtained by combination of multiple short lines as far as I know.
