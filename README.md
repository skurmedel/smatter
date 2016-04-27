# smatter
Smatter is a very small language focused on writing image processing "kernels". 

# Design goals

A great deal of image processing operations are of two kinds:

- point operations: e.g saturation, which only rely on the pixel colour and is wholly independent of the other pixel values.
- filter operations: a filter uses neighbouring image data to compute the new pixel data. Prime examples include blur, many kinds of edge detection, etc.

__Note that the everyday usage of the word "filter" usually refers to any kind of image operation. This is different to the technical definition.__

Thus many operations only need two things: the current pixel value and a way to sample neighbours. Some operations require data that can't be computed as a function of the pixelvalue and its neighbours, but the final processing step usually can be. So smatter should accomodate for this too by meshing well with C.


# The name
In English, a smatter is a small amount of something. In Swedish smatter usually refers to the blare of small things hitting a surface, like rain on a window sill. I thought both of these interpretations where apt for the intended application.
