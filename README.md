# Seam-Carving
Seam Carving using C++ and OpenCV

Image retargeting is the process of pasting the content of an image of certain size to a canvas of a different size. Figure 1 illustrates this process: the goal is to take the content of Image 1a) and paste it to a canvas that is shorter along the x axis. Common methods include non-uniform scaling (Figure 1b) or cropping (Figure 1c). However, both have their shortcomings. Non-uniform scaling may distort the proportions of the objects in the scene and cropping might remove important content. A better solution is seam-carving

Here a simple seam carving technique is implemented using dynamic programming and the OpenCV library. 
 
The seam carving algorithm uses horizontal or vertical seams (Figure 2(red)) to iteratively reduce the size of the image. A seam is a pixel thick cut through the image that stretches either from left to right or from up to down (depending on the orientation of the seam). Removing the seam reduces the image by one unit. 

The main idea is to find the seams that cut through the non-salient content of the image.

Specifications 
 
The program has 3 arguments: an input image, width of the new target, height of the new target, output image. 
 
Example: ./sc castle.png 300 200 castle2.png 
 
