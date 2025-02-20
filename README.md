# image-pre-processing

#exp 1a image resizing
Scaling operations increase or reduce the size of an image. 

The cv2.resize() function is used to resize an python image in OpenCV. It takes the following arguments:
cv2.resize(src, dsize,interpolation)
Here,
src          :The image to be resized.
dsize        :The desired width and height of the resized image.
interpolation:The interpolation method to be used.
When the python image is resized, the interpolation method defines how the new pixels are computed. There are several interpolation techniques, each of which has its own quality vs. speed trade-offs.
It is important to note that resizing an image can reduce its quality. This is because the new pixels are calculated by interpolating between the existing pixels, and this can introduce some blurring.

#exp 1b image rotation
Images can be rotated to any degree clockwise or otherwise. We just need to define rotation matrix listing rotation point, degree of rotation and the scaling factor. 

The cv2.getRotationMatrix2D() function is used to create a rotation matrix for an image. It takes the following arguments:
The center of rotation for the image.
The angle of rotation in degrees.
The scale factor.
The cv2.warpAffine() function is used to apply a transformation matrix to an image. It takes the following arguments:
The python image to be transformed.
The transformation matrix.
The output image size.
The rotation angle can be positive or negative. A positive angle rotates the image clockwise, while a negative angle rotates the image counterclockwise.
The scale factor can be used to scale the image up or down. A scale factor of 1 will keep the image the same size, while a scale factor of 2 will double the size of the python image.

#exp1c image translation
Image shearing is a geometric transformation that skews an image along one or both axes i.e x or y axis.

To shear an image using OpenCV, we need to create a transformation matrix. This matrix is a 2×3 matrix that specifies the amount of shearing in each direction.
The cv2.warpAffine() function is used to apply a transformation matrix to an image. It takes the following arguments:
The image to be transformed.
The transformation matrix.
The output image size.
The shearing parameters are specified in the transformation matrix as the shearX shearY elements. The shearX element specifies the amount of shearing in the x-axis, while the shearY element specifies the amount of shearing in the y-axis.

#exp1d image normalization
Image normalization is a process of scaling the pixel values in an image to a specific range.This is often done to improve the performance of image processing algorithms, as many algorithms work better when the pixel values are within a certain range.

In OpenCV, the cv2.normalize() function is used to normalize an image. This function takes the following arguments:
The input image.
The output image.
The minimum and maximum values of the normalized image.
The normalization type.
The dtype of the output image.
The normalization type specifies how the pixel values are scaled. There are several different normalization types available, each with its own trade-offs between accuracy and speed.
Image normalization is a common preprocessing step in many image processing tasks. It can help to improve the performance of algorithms such as image classification, object detection, and image segmentation.

#exp 1e image edge
The process of image edge detection involves detecting sharp edges in the image. This edge detection is essential in the context of image recognition or object localization/detection. There are several algorithms for detecting edges due to its wide applicability.

In image processing and computer vision applications, Canny Edge Detection is a well-liked edge detection approach. In order to detect edges, the Canny edge detector first smoothes the image to reduce noise, then computes its gradient, and then applies a threshold to the gradient. The multi-stage 

#exp1f image blurring
Image blurring is the technique of reducing the detail of an image by averaging the pixel values in the neighborhood. This can be done to reduce noise, soften edges, or make it harder to identify a picture. In many image processing tasks, image blurring is a common preprocessing step. It is useful in the optimization of algorithms such as image classification, object identification, and image segmentation. In OpenCV, a variety of different blurring methods are available, each with a particular trade-off between blurring strength and speed.


#exp1g Morphological Image Processing
Morphological image processing is a set of python image processing techniques based on the geometry of objects in an image. These procedures are commonly used to eliminate noise, separate objects, and detect edges in images.

Two of the most common morphological operations are:

Dilation: This operation expands the boundaries of objects in an image.
Erosion: This operation shrinks the boundaries of objects in an image.

#exp1h image shearing
Image shearing is a geometric transformation that skews an image along one or both axes i.e x or y axis.

To shear an image using OpenCV, we need to create a transformation matrix. This matrix is a 2×3 matrix that specifies the amount of shearing in each direction.
The cv2.warpAffine() function is used to apply a transformation matrix to an image. It takes the following arguments:
The image to be transformed.
The transformation matrix.
The output image size.
The shearing parameters are specified in the transformation matrix as the shearX shearY elements. The shearX element specifies the amount of shearing in the x-axis, while the shearY element specifies the amount of shearing in the y-axis.
