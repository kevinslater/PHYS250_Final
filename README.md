# PHYS250_Final

### Introduction:
Compressing an image reduces the space it takes to store while minimizing loss in visual quality.
The techniques analyzed here are incredibly widespread, forming the basis for common file formats such as `.JPG`, `.GIF`, and `.PNG`, as well as more complex compression algorithms.
Additionally, these same techniques arise often in machine learning applications, such as image segmentation and unsupervised learning.

### Goal:
The goal of this project is to implement and compare different image compression techniques. 
Specifically, I will focus on three different "lossy" compression techniques, each of which selectively and irreversibly prunes data from the original image.

1) The <b>JPEG algorithm</b> uses a discrete cosine transform (DCT) to shift the image to frequency space. High-frequency components, which are difficult for our eyes to percieve, are eliminated. An inverse-DCT is then used to revert the image to regular color space. The large reduction in final size at the cost of an imperceptible reduction in image quality makes the `.JPG` one of the most widespread image file formats.  
2) Color quantization techniques, such as the <b>k-means clustering algorithm</b>, reduce image size by replacing a large set of similar colors with their average value. This is a critical step for `.GIF` and often `.PNG` image formats, which are limited to displaying 256 colors. This technique can also be applied to look for related clusters in any data set, making it an important tool in unsupervised learning.   
3) <b>Principle component analysis (PCA)</b> is a dimension-reduction technique that can be applied to image compression. Starting with a matrix of pixel values, PCA identifies the eigenvectors that account for the greatest variance in the image and elimates the rest. This allows us to break up an image into its most important components. PCA has widespread applications, and can be useful anytime we want to reduce the dimension of a dataset before analyzing it.

For an objective measure of each technique, I will consider the compression ratio and peak signal-to-noise ratio. This provides a measure of the reduction in quality that we are getting as a result of the reduction in size.
I plan to test each technique on a handful of images -- this will hopefully let me compare the strengths and weaknesses of each technique, as well as suggest potential use cases.
