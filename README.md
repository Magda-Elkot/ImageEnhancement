# ImageEnhancement
Image enhancement is an important task in image processing, which aims to improve the visual quality 
of images by reducing noise, improving contrast, and enhancing details. In this project, we will explore
two approaches for image enhancement: traditional image processing techniques and a pretrained model 
called MirNet using Deep Learning.

## Importing Libraries
### The necessary libraries are imported for image processing and evaluation metrics. The libraries used include:

os: for file and directory operations

cv2: for image processing tasks

numpy: for array manipulation

PIL: for image manipulation

skimage: for image processing and evaluation metrics

sklearn: for evaluation metrics

matplotlib: for visualization

## Input and Output Folders
### The input and output folders are defined to specify the location of the input images 
### and the location where the processed images will be saved.

## Histogram Processing
### This section includes two types of histogram processing techniques: histogram equalization and contrast stretching.

## Histogram Equalization

    Histogram equalization is applied to enhance the contrast of the image. 
    The code snippet includes the following steps:

      Splitting the image into its RGB channels
      
      Applying histogram equalization to each channel
      
      Merging the equalized channels to obtain the equalized image
      
      Saving the equalized image to the output directory

## Contrast Stretching

    Contrast stretching is applied to further enhance the contrast of the image. The code snippet includes the following steps:

      Applying automatic contrast stretching to each channel
      
      Merging the stretched channels to obtain the stretched image
      
      Saving the stretched image to the output directory

## Point-wise Intensity Transformations - Log Transform
  ### In this section, a log transformation is applied to enhance the details in the image. The code snippet includes the following steps:

      Converting the image to grayscale
      
      Applying a log transformation to the grayscale image
      
      Normalizing the log-transformed image
      
      Saving the log-transformed image to the output directory

## Linear Noise Smoothing - Smoothing with PIL and ImageFilter.BLUR
  ###In this section, linear noise smoothing is performed using a Gaussian blur filter. The code snippet includes the following steps:

      Loading the image as a NumPy array with a data type of np.float32
      
      Scaling the pixel values to the range [0, 1]
      
      Applying a Gaussian blur filter with a radius of 2
      
      Saving the linear-smoothed image to the output directory
