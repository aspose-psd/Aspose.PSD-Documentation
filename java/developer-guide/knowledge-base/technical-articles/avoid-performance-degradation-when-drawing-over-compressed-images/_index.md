---
title: Avoid Performance Degradation when Drawing over Compressed Images
type: docs
weight: 40
url: /java/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **Avoid Performance Degradation when Drawing over Compressed Images**
There are times when you want to perform extremely extensive graphic operations on a compressed image. When Aspose.PSD has to compress and decompress images on the fly, performance degradation may occur. Drawing over compressed images may also carry a performance penalty.
### **Solution**
To avoid performance degradation, we recommend that you convert the image to an uncompressed, or raw, format before performing graphic operations.
### **Using File Path**
In the example that follows, a PSD image is converted to raw format (no compression) and saved to disk. The uncompressed image is then loaded back before graphic operations are performed on it. The same technique applies for BMP and GIF files.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Using a Stream Object**
The following code snippet shows you how to PSD image is converted to raw format (no compression) and saved to disk using Stream.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
