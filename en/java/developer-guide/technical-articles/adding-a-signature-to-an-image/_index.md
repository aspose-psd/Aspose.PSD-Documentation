---
title: Adding a Signature to an Image
type: docs
weight: 10
url: /java/adding-a-signature-to-an-image/
---

## **Adding a Signature**


Adding a signature to an image is sometimes required to digitally sign the images to avoid counterfeiting. Another thought could be to treat the image more like it is being shown in a gallery. Which ever the reason is, the Aspose.PSD APIs provide the feature to add signature on an image using simplest mechanism as explained below. Please note, this example make use of the Graphics class to draw another image with signature on to the original image's surface. To demonstrate the operation, we will load a PSD image from disk and draw another image as signature on to the original image's surface using the Graphics class DrawImage method. We will save the resultant image in PNG format using the PngOptions class. Below is a code example that demonstrates how to add a signature to an image. The example source code has been split into parts to make it easy to follow. Step by step, the example shows how to:

- Load the primary and secondary (signature) images.
- Create and initialize a Graphics object.
- Draw image using the Graphics class DrawImage method.
- Save result in PNG format.
### **Program Samples**
#### **Loading Images**
First, create instances of Image class to load the sample images from disk.
#### **Creating and Initializing a Graphic Object**
After loading the images, create and initialize a Graphics class object while using the object of the primary image.
#### **Drawing Secondary Image onto the Primary Image**
Then using the Graphics class DrawImage method, add the secondary image on to the primary image. There are several overloads of the DrawImage method that accept an object of the Image as first parameter whereas all other parameters correspond to the location where the image has to be drawn. For the sake of demonstration, the following code uses the overload version of DrawImage that accepts an object of the Point as second parameter and tries to draw the signature on the lower right corner of the primary image.
#### **Saving the Image**
Finally, save the image back to the local disk as a PNG file using the PngOptions class.
#### **Complete Source**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}
