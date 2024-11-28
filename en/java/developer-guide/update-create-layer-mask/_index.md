---
title: Working with masks in Aspose.PSD for Java
weight: 100
type: docs
description: Examples of how to work with Clipping, Raster and Vector Masks within PSD File
keywords: [masks, layer mask, vector mask, clipping mask, psd, psd api, java, code sample]
url: java/update-create-layer-mask/
---

## **Overview**

**Overview**
	
	There are 3 types of masks in PSD files:
	1. Clipping Masks
	2. Raster Masks
	3. Vector Masks
	
	This article covers all 3 types.


** Clipping Masks **

Clipping masks are a robust feature in graphic design and image editing software, particularly in Java. They enable precise control over the visibility of one layer based on the shape and content of another layer. Essentially, a clipping mask restricts the visibility of a layer to the shape of another layer beneath it.

To implement a clipping mask in Java, you'll first need two layers: the base layer and the layer you intend to clip. The base layer defines the shape or area that will remain visible, while the layer to be clipped contains the content that will conform to the shape of the base layer.

When a clipping mask is applied in Java, the content of the clipped layer is only visible within the boundaries of the base layer. Any content outside these boundaries will be hidden or clipped.

Clipping masks prove especially valuable when applying effects, such as textures or patterns, to specific areas of an image or artwork. By employing a clipping mask, you can confine the effect to the desired area without impacting the rest of the image.

Please refer to the example at the end of the page for clarification.

** Raster Masks ** 

Raster masks in Java files are employed to manage the visibility of specific areas within a layer. Unlike vector masks, which utilize mathematical shapes to define masked areas, raster masks rely on pixel-based information to determine visible or hidden regions.

A raster mask comprises a grayscale image applied to a layer. White areas of the mask denote visibility, while black areas represent hidden portions. Shades of gray in between can create partial transparency or semi-visible regions.

Please refer to the example at the end of the page for better understanding.

** Vector masks **

Vector masks in Java files are versatile tools used to delineate the visibility of specific areas within a layer based on mathematical shapes. Unlike raster masks, which depend on pixel-based data, vector masks employ paths and curves to create smooth and scalable masked areas.

A vector mask essentially consists of a path applied to a layer. The shape of this path determines which parts of the layer are visible and which are hidden. By manipulating the control points and curves of the path, precise and intricate masked areas can be created.

Please refer to the [Vector Masks page](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) for information on adding vector masks using resources.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-update-create-layer-mask.java" >}}