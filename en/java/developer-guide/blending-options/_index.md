---
title: Psd Blending Options Manipulation
weight: 100
type: docs
description: Aspose.PSD for Java can assist you in adjusting blending options with a straightforward code snippet.
keywords: [blend options, blending, add effects, change opacity, change color of shadow, add shadow, psd api, java, code sample]
url: java/blending-options/
---

## **Overview**
With Aspose.PSD for Java, you have the capability to modify blending options to enhance the appearance of layers within your PSD image. Below is a Java code example illustrating various methods to utilize blending options.

Initially, the code loads a PSD image and saves it as an original PNG file. Subsequently, it alters the opacity and blending mode of specific layers. For instance, it sets the opacity of the second layer to 100 and changes the blending mode of the fifth layer to Hue.

Moreover, the code incorporates blending effects to designated layers. Utilizing the `addDropShadow()` method, it introduces a drop shadow effect to the seventh layer, specifying a shadow angle of 30 degrees and a shadow color of RGB(255, 0, 0).

Furthermore, the code adjusts the blending mode of the ninth layer to Lighten. Additionally, it applies a color overlay effect to the fifth layer through the `addColorOverlay()` method, setting the color overlay to RGB(30, 50, 0) with an opacity of 150.

Finally, the code saves the modified image as an updated PNG file.

In essence, Aspose.PSD for Java offers a diverse array of blending options to manipulate the appearance of layers within your PSD images. These options encompass modifying opacity, altering blending modes, and implementing various blending effects like drop shadow and color overlay.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-blending-options.java" >}}