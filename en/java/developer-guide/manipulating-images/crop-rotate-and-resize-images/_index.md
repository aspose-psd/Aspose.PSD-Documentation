---
title: Crop, Rotate and Resize Images
type: docs
weight: 40
url: /java/crop-rotate-and-resize-images/
---

## **Cropping Images**
Image cropping usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used for to cut out some portion of an image to increase the focus on a particular area. Aspose.PSD API supports two different approaches to image cropping: by shifts and rectangle.
### **Cropping by Shifts**
The RasterImage class provides an overloaded version of the Crop method that accepts 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the Crop method moves the image boundaries towards the center of the image while discarding the outer portion. The code snippet below demonstrates how to crop an image by shifts.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Cropping by Rectangle**
The RasterImage class provides another overloaded version of the Crop method that accepts an instance of the Rectangle class. You can cut out any portion of an image by providing the desired boundaries to the Rectangle object. The code snippet below demonstrates how to Crop any image by Rectangle.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Rotate and Flip an Image**
Aspose.PSD for Java is an easy to use library because it provides simple methods to perform complex operations. For instance, Aspose.PSD for Java has provided RotateFlip method for its base class Image if an application requires rotating an image. Irrespective of the image format, the library can perform specific Rotate & Flip procedure on it.
### **Rotating an Image**
The Image.RotateFlip method can be used to rotate the image by 90/180/270-degrees and flip the image horizontally or vertically. Image.RotateFlip method accepts a parameter of RotateFlipType that specifies the type of rotation and flip to apply to the image. The steps to perform Rotate & Flip are as simple as below,

1. Load in image using the factory method Load exposed by Image class.
1. Call the Image.RotateFlip method while specifying the appropriate RotateFlipType.
1. Save the results.

The following code example demonstrates how to set the RotateFlip property of an Image and the RotateFlipType enumeration.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Rotating an Image on a Specific Angle**
Aspose.PSD for Java API exposing the RasterImage.Rotate method to facilitate its users who wish to rotate an image on a specific angle. Unlike the RasterImage.RotateFlip method, the RasterImage.Rotate method accepts three parameters:

1. Rotation angle: A float type parameter that specifies the rotation angle to which the image has to be rotated. A positive value rotates the image clockwise; a negative value performs an anticlockwise rotation.
1. Resize proportionally: A Boolean type parameter specifies if the image size has to changed according to the rotated rectangle (corner points) projections. If set to false, the image dimensions would be untouched and only internal image contents are rotated.
1. Background color: A Color type parameter specifies the color to be filled in the background of the rotated image.

The code snippet below demonstrates the usage of RasterImage.Rotate method.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Resizing Images**
This article demonstrates the usage of Aspose.PSD for Java to perform Resize operation on an image. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD for Java has exposed the Resize method for the Image class that can be used to re-size existing images on the fly. There are two overloads of the Resize method to suit the application needs.
### **Simple Resizing**
The steps to perform Resize are as simple as below:

1. Load in image using the factory method Load exposed by Image class.
1. Call the Image.Resize method while specifying new Height & Width.
1. Save the results.

The following code example demonstrates how to Resize an image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Resizing with ResizeType Enumeration**
Aspose.PSD API has exposed ResizeType enumeration that can be used with Image.Resize to achieve desired results. Below provided code snippet demonstrates the usage of ResizeType enumeration, whereas the details of ResizeType enumeration members can be found at the bottom of this page.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



If you intend to get quality result after applying the re-size then it is suggested that you should always use ResizeType.LanczosResample because it will output highly qualitative results but may work slower than ResizeType.NearestNeighbourResample. On the other hand, ResizeType.NearestNeighbourResample algorithm is specifically used for fast re-sizing while compromising on the image quality. This method may be useful for thumbnail generation in real time or similar processes where performance is required.
## **Resize Image Proportionally**
You can resize images by passing new height and width values as parameters to the Image.Resize method but in that case you have to calculate the aspect ratio yourself. This is because when the width or height of an image is altered, the image is either scaled or shrink to fill the new size . If the changes to the width and height of an image are not in proportion this can lead to stretched and distorted result. This article demonstrates the use of Aspose.PSD for Java API to resize images by passing either new height or width while allowing the API to automatically calculate the other proportional value.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType Enumeration**
ResizeType determines the type of re-sizing to be performed on the image based on the selected filter.

Members of ResizeType Enumeration

|**Member Name**|**Value**|**Description**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Left top point of the new image will coincide with the left top point of the original image. Crop will occur if required.|
|RightTopToRightTop|1|Right top point of the new image will coincide with the right top point of the original image. Crop will occur if required.|
|RightBottomToRightBottom|2|Right bottom point of the new image will coincide with the right bottom point of the original image. Crop will occur if required.|
|LeftBottomToLeftBottom|3|Left bottom point of the new image will coincide with the left bottom point of the original image. Crop will occur if required.|
|CenterToCenter|4|Center of the new image will coincide with the center of the original image. Crop will occur if required.|
|LanczosResample|5|Resample using Lanczos algorithm using 7x7 mask.|
|NearestNeighbourResample|6|Resample using nearest neighbour algorithm.|

