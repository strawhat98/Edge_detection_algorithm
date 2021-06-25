# Edge_detection_algorithm
Implementation of Edge Detection Algorithm
# INTRODUCTION:-
## Image Processing:-
An Image may be defined as a two dimensional function, f(x, y), where x and y are spatial (plane) coordinates, and the amplitude of f at any pair of coordinates (x, y) is called the intensity or gray level of the image at that point.
The field of digital image processing refers to processing digital images by means of a digital computer.
## Origins of Digital Image:-
One of the first application of digital image was on Newspaper industry when pictures were first sent by submarine cable between LONDON and NEW YORK. 
It was the first time Bartlane cable picture transmission system was introduced(early 1920s). Some of the initial problems in improving visual quality of these early digital pictures were related to selection of the printing procedures. And the distribution of intensity levels.
![image](https://user-images.githubusercontent.com/39863708/123435725-80cecf00-d5eb-11eb-9dae-aea76e497cb4.png)
 1921, Coded Tape by telegraph printer
 ![image](https://user-images.githubusercontent.com/39863708/123435769-90e6ae80-d5eb-11eb-9e74-76fa8dd5cead.png)
       1922, McFarlane.      



Bartlane System was capable of coding images in five distinct levels of gray. This five levels had been increased to 15 levels in 1929.During this period, introduction of a system for developing a film plate via light beams.

Bartlane System was capable of coding images in five distinct levels of gray. This five levels had been increased to 15 levels in 1929.During this period, introduction of a system for developing a film plate via light beams that were modulated by the coded picture tape improved the reproduction process considerably. 
First computer to power enough to carry out meaningful image processing task appeared in 1960 and after extensive research throughout multiple decades in the history of computer science, Different Sectors of image processing appeared.
![image](https://user-images.githubusercontent.com/39863708/123435856-a8259c00-d5eb-11eb-894e-958035727804.png)
   Gamma ray imaging, Medical Science
![image](https://user-images.githubusercontent.com/39863708/123435920-b673b800-d5eb-11eb-9cc6-54f5edb0952b.png)
   Gamma ray imaging, Radiology
![image](https://user-images.githubusercontent.com/39863708/123435944-bc699900-d5eb-11eb-929c-52e8ace58a01.png)
   Gamma ray imaging, Circuit Board
 X ray imaging, Gamma Ray imaging all these were introduced based on the electromagnetic energy spectrum and modeling synthetic images were introduced with the extensive knowledge different Energy radiation of a photo.

# Modern Image Processing Fundamentals:-
1) 2D convolution.
2) Gaussian Filter.
3) Edge Detection on an image.                         
4) Motion Blur.
5)Sharpen and Emboss.
6) Erode and Dilate.
7) Vignette filter.
8) Image Contrast.

 ![image](https://user-images.githubusercontent.com/39863708/123436024-d3a88680-d5eb-11eb-9450-10bafd228a02.png)


## Main Highlight of this project:-
Edge Detection in Image Processing using SOBEL Operator, CANNY Operator, PREWITT Operator, Laplace Operator.

# Aim:-
aim of an edge detector is to identify points on a digital image in which the brightness of the image changes either dramatically or has discontinued.
Morphological Gradient Approach:-
Edges are some form discontinuity,
    • Surface Normal Discontinuity.
    • Surface color / appearance discontinuity.
    • Depth Discontinuity (gaps between artifacts)
    • Illumination discontinuity (shadows)

![image](https://user-images.githubusercontent.com/39863708/123436084-e91db080-d5eb-11eb-834d-b22582f3e5ea.png)

![image](https://user-images.githubusercontent.com/39863708/123436095-eae77400-d5eb-11eb-8176-1aa76e029ca9.png)
Intensity Function of the matrix if f(x, y) then the partial derivative function of intensity gradient is,
    
![image](https://user-images.githubusercontent.com/39863708/123436121-f20e8200-d5eb-11eb-8019-9d139145ca03.png)
![image](https://user-images.githubusercontent.com/39863708/123436130-f470dc00-d5eb-11eb-89fe-96249b5052ec.png)

## Sobel Operator: 
It is a discrete differentiation operator. It computes the gradient approximation of image intensity function for image edge detection. At the pixels of an image, the Sobel operator produces either the normal to a vector or the corresponding gradient vector. It uses two 3×3 kernels or masks which are convoluted with the input image to calculate the vertical and horizontal derivative approximations respectively-
Sobel Kernel Operator,
![image](https://user-images.githubusercontent.com/39863708/123436202-0a7e9c80-d5ec-11eb-8d20-68a14b4671f6.png)
![image](https://user-images.githubusercontent.com/39863708/123436217-0ce0f680-d5ec-11eb-9570-e84d45cb8c76.png)
## Advantages:

    1. Simple and time efficient computation
    2. Very easy at searching for smooth edges
## Limitations:
    • Diagonal direction points are not preserved always
    • Highly sensitive to noise
    • Not very accurate in edge detection
    • Detect with thick and rough edges does not give appropriate results
## Disadvantages:-
Real world pictures have lot of noise and for this reason finding perfect edge gradient is impossible as it gives noisy output. For this reason smoothing by Gaussian filter is used again to suppress the noise. For this reason canny is introduced to filter out the problem easily and detect edges with less noise compared to Sobel operator.

## Canny Operator: 
It is a Gaussian-based operator in detecting edges. This operator is not susceptible to noise. It extracts image features without affecting or altering the feature. Canny edge detector have advanced algorithm derived from the previous work of Laplacian of Gaussian operator. It is widely used an optimal edge detection technique. 
It detects edges based on three criteria:
    • Low error rate
    • Edge points must be accurately localized
    • There should be just one single edge response
![image](https://user-images.githubusercontent.com/39863708/123436278-18ccb880-d5ec-11eb-863b-999c1169dd7b.png)
## Process:-
i) Noise Reduction.
ii) Gradient Computation.  
iii) Non-max Suppression.
iv)Hysteresis Threshold.
## Advantages:

    1. It has good localization
    2. It extract image features without altering the features
    3. Less Sensitive to noise

## Limitations:

    1. There is false zero crossing.
    2. Complex computation and time consuming.
## Prewitt Operator: 
This operator is almost similar to the Sobel operator. It also detects vertical and horizontal edges of an image. It is one of the best ways to detect the orientation and magnitude of an image. It uses the kernels or masks – 



## Advantages:

    1. Good performance on detecting vertical and horizontal edges
    2. Best operator to detect the orientation of an image
## Limitations:
    • The magnitude of coefficient is fixed and cannot be changed
    • Diagonal direction points are not preserved always.
## Process:-
       Multiplication of an image matrix with 3×3 kernel filter to detect edge.
![image](https://user-images.githubusercontent.com/39863708/123436572-6517f880-d5ec-11eb-90b0-e3f048b02afa.png)
![image](https://user-images.githubusercontent.com/39863708/123436600-6ba67000-d5ec-11eb-9714-b5014cb9c79b.png)
Laplacian Operator:-
Laplacian Operator is also a derivative operator which is used to find edges in an image. The major difference between Laplacian and other operators like Prewitt, Sobel, Robinson and Kirsch is that these all are first order derivative masks but Laplacian is a second order derivative mask. In this mask we have two further classifications one is Positive Laplacian Operator and other is Negative Laplacian Operator. 
Laplacian Operator take out two types of edges from an image
    • Inward Edges
    • Outward Edges
 ![image](https://user-images.githubusercontent.com/39863708/123436726-8d075c00-d5ec-11eb-9e8f-7d215cba8a30.png)
 Procedure:-Laplacian is a derivative operator; its uses highlight gray level discontinuities in an image and try to deemphasize regions with slowly varying gray levels. This operation in result produces such images which have grayish edge lines and other discontinuities on a dark background. This produces inward and outward edges in an image 
## Method:-
    • Dilates image by specific structuring element.
    • Equalizes histogram of a gray scale image.
    • Convolves image with kernel.
    • Blurs image with Gaussian filter.
    • Calculate integral of image.
## Some Real-world Applications of Image Edge Detection:

    • medical imaging, study of anatomical structure
    • locate an object in satellite images
    • automatic traffic controlling system.face recognition, and fingerprint recognition

## Sobel Edge Detection Algorithm:       
       ![image](https://user-images.githubusercontent.com/39863708/123436886-bb853700-d5ec-11eb-972a-752ff053a11f.png)
       ![image](https://user-images.githubusercontent.com/39863708/123436900-be802780-d5ec-11eb-90a6-537ce5eb0207.png)
![image](https://user-images.githubusercontent.com/39863708/123436919-c213ae80-d5ec-11eb-82bf-07945595b9e9.png)
![image](https://user-images.githubusercontent.com/39863708/123436926-c4760880-d5ec-11eb-8b9a-ca113cb87ae4.png)
![image](https://user-images.githubusercontent.com/39863708/123437174-043cf000-d5ed-11eb-8c85-83d6b6c3aead.png)
![image](https://user-images.githubusercontent.com/39863708/123437190-07d07700-d5ed-11eb-8760-f072e7f8f77b.png)

## Canny Edge Detection Algorithm:
![image](https://user-images.githubusercontent.com/39863708/123436961-cc35ad00-d5ec-11eb-924a-1bfeca882069.png)
![image](https://user-images.githubusercontent.com/39863708/123437240-14ed6600-d5ed-11eb-8acc-27299740428b.png)

## Prewitt Edge Detection Algorithm:
horizontal operator
![image](https://user-images.githubusercontent.com/39863708/123436998-d5267e80-d5ec-11eb-92d9-1d0fbadfa4c3.png)
vertical operator
![image](https://user-images.githubusercontent.com/39863708/123437014-d9529c00-d5ec-11eb-8bc0-47e603ac4b73.png)
![image](https://user-images.githubusercontent.com/39863708/123437271-1fa7fb00-d5ed-11eb-8a9d-a63d1db8dacc.png)
![image](https://user-images.githubusercontent.com/39863708/123437285-22a2eb80-d5ed-11eb-91b4-b05fb673a993.png)

## LAPLACIAN EDGE DETECTION:
![image](https://user-images.githubusercontent.com/39863708/123437074-ebccd580-d5ec-11eb-9da7-ac8a6b3eda0a.png)
![image](https://user-images.githubusercontent.com/39863708/123437386-3f3f2380-d5ed-11eb-90e3-5df73bb041b7.png)
![image](https://user-images.githubusercontent.com/39863708/123437398-423a1400-d5ed-11eb-98f2-78a21dcededd.png)


REFERENCE :
    • For pgm-image sourcing: https://people.sc.fsu.edu/~jburkardt/data/pgma/pgma.html
    • For general description & formulation: https://en.wikipedia.org/wiki/Sobel_operator
    • The understanding of the project & Bear images is sourced from: https://www.youtube.com/watch?v=uihBwtPIBxM
    • This project will be an extension of the work of Aaron(aka Zoltack429) https://www.youtube.com/user/MrZoltack/about
    • https://en.wikipedia.org/wiki/Edge_detection
    • https://www.udemy.com/course/digital-image-processing-from-ground-up-in-python/?src=sac&kw=python+digital+im
    

## ALL-in-one Operator:-
![image](https://user-images.githubusercontent.com/39863708/123437368-3b130600-d5ed-11eb-84e4-2abeab95acd7.png)

