# smatter
Smatter is a very small language focused on writing image processing "kernels". 

## Rationale

A great deal of image processing operations are of two kinds:

- **point operations**: e.g saturation, which only rely on the pixel colour and is wholly independent of the other pixel values.
- **neighbour operations**: neighbouring image data is used to compute the new pixel data. Prime examples include blur, many kinds of edge detection, etc.

Thus many operations only need two things: the current pixel value and a way to sample neighbours. Some operations require data that can't be computed as a function of the pixel value and its neighbours, but the final processing step usually can be. So smatter should accomodate for this too by meshing well with C.

The main use case of smatter is writing these kernels.



## The name
In swedish smatter usually refers to the blare of small things hitting a surface, like rain on a window sill. The english interpretation works too :)
