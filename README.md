# image-pre-processing

#exp 1 image resizing
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

#exp 1c image translation
