# ImageEnhancement
Image enhancement is an important task in image processing, which aims to improve the visual quality 
of images by reducing noise, improving contrast, and enhancing details. In this project, we will explore
two approaches for image enhancement: traditional image processing techniques and a pretrained model 
called MIRNet using Deep Learning.

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
  ### In this section, linear noise smoothing is performed using a Gaussian blur filter. The code snippet includes the following steps:

      Loading the image as a NumPy array with a data type of np.float32
      
      Scaling the pixel values to the range [0, 1]
      
      Applying a Gaussian blur filter with a radius of 2
      
      Saving the linear-smoothed image to the output directory


## Nonlinear Noise Smoothing - Smoothing with PIL and Median Filter
   ### In this section, nonlinear noise smoothing is performed using a median filter. The code snippet includes the following steps:

            Loading the image as a NumPy array with a data type of np.float32
            
            Scaling the pixel values to the range [0, 1]
            
            Applying a median filter with a kernel size of 3
            
            Saving the median-smoothed image to the output directory

## mage Derivatives - Gradient
   ### In this section, the gradient magnitude of the image is computed to enhance the edges. The code snippet includes the following steps:

            Loading the image as a NumPy array with a data type of np.float32
            
            Scaling the pixel values to the range [0, 1]
            
            Computing the gradient magnitude of the image using the Sobel operator
            
            Normalizing the gradient values to the range [0, 1]
            
            Saving the gradient image to the output directory

## Sharpening and Unsharp Masking
   ### In this section, sharpening and unsharp masking techniques are applied to enhance the image details. The code snippet includes the following steps:

            Loading the image using PIL and converting it to a NumPy array with a data type of np.float32
            
            Scaling the pixel values to the range [0, 1]
            
            Applying the sharpening kernel or unsharp masking kernel to the image
            
            Saving the sharpened or unsharpened image to the output directory

## MIRNet for Low-Light Image Enhancement
   ### In this section, the MIRNet model is used to enhance low-light images. The code snippet includes the following steps:

            Loading the MIRNet model from the Hugging Face Model Hub
            
            Preprocessing the low-light image by resizing and converting it to a NumPy array
            
            Normalizing the pixel values to the range [0, 1]
            
            Performing model inference to enhance the low-light image
            
            Saving the enhanced image to the output directory
            
            Calculating the evaluation metrics (PSNR, MSE, SSIM) between the original and enhanced images


## Evaluation Metrics
   ### In this section, the evaluation metrics (MSE, PSNR, SSIM) are calculated for each image enhancement technique. The code snippet includes the following steps:

            Loading the original and processed images using PIL
            
            Calculating the evaluation metrics between the original and processed images
            
            Appending the evaluation metrics to the respective lists

## Visualizations
   ### In this section, visualizations are created to compare the evaluation metrics for different image enhancement techniques
