# **Finding Lane Lines on the Road** 

## Writeup

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road in images/videos
1. Convert to grayscale.
2. Apply Gaussian smoothing / blurring
3. Apply the Canny transform for the edge detection
4. Region masking, only keep the region of the image defined by the polygon
5. Using the Hough Transform to Find Lines from Canny Edges
6. Draw the lines on the origianl images

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

[image1]: ./pipeline_example/gray.png "Grayscale"
[image2]: ./pipeline_example/blurring.png "Blurring"
[image3]: ./pipeline_example/edges.png "Edges"
[image4]: ./pipeline_example/masked_edge.png "Masked edges"
[image5]: ./pipeline_example/lines.png "Lines"
[image6]: ./pipeline_example/res.png "Result"
[image7]: ./pipeline_example/afteropt.png "Improve the draw_lines() function"


#### My pipeline consisted of 6 steps. </br>
I converted the images to grayscale</br>
![alt text][image1]</br>
Apply Gaussian smoothing / blurring</br>
![alt text][image2]</br>
Apply the Canny transform for the edge detection</br>
![alt text][image3]</br>
Region masking, only keep the region of the image defined by the polygon</br>
![alt text][image4]</br>
Using the Hough Transform to Find Lines from Canny Edges</br>
![alt text][image5]</br>
Draw the lines on the origianl images</br>
![alt text][image6]</br>
In order to draw a single line on the left and right lanes, I modified the draw_lines() function by calculating the average slope and filter some noised lines by defining the slope range.</br>
![alt text][image7]</br>


### 2. Identify potential shortcomings with your current pipeline
It's not so robust when I test with the challenge videos.

### 3. Suggest possible improvements to your pipeline
Improving the pipeline to make it more robust with different roads.
