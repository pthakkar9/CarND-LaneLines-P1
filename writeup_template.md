# **Writeup for Finding Lane Lines on the Road Project** 
## Parva Thakkar

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. My pipeline and solution approach.

You can find following pipeline in `find_lanes_image` function.

- Convert *image* to gray scale with `grayscale` function.
- Apply [Gaussian Smoothing](https://en.wikipedia.org/wiki/Gaussian_blur) to *gray scale image* with `gaussian_blur` function
- Apply [Canny Edge Detection](https://en.wikipedia.org/wiki/Canny_edge_detector) with `canny` function
- Define area of interest by defining polygon and using `region_of_interest` function
- Draw Hough Lines by applying [Hough Transform](https://en.wikipedia.org/wiki/Hough_transform) algorithm with `hough_lines` function with defined thickness
- Create *final image* by adding Hough Lines on original image by using `weighted_img` function

### 2. Identify potential shortcomings with your current pipeline

- This solution doesn't work on portrait images. I tested on some of them.
- This solution doesn't create edges on extra curved lanes i.e. challenge video.


### 3. Possible improvements to this pipeline

- Add threshold for slope detection. This will add lines only if slope of given line is greater than the threshold. This will improve result of **challenge** video solution
- Check the orientation of image before creating *final image* as described in the last step of the pipeline section.

### 4. Extra note

- I have added extra photos and videos of my own. I have also attached result files after running my solution on them.
- I have added a couple of portrait images and their results to prove the shortcoming I listed above.
