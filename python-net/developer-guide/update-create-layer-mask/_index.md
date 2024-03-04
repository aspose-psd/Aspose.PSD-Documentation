---
title: Working with masks in Aspose.PSD for Python
weight: 100
type: docs
description: Examples of how to work with Clipping, Raster and Vector Masks within PSD File
keywords: [masks, layer mask, vector mask, clipping mask, psd, psd api, python, code sample]
url: python-net/update-create-layer-mask/
---

## **Overview**

**Overview**
	
	There are 3 types of masks in PSD files:
	1. Clipping Masks
	2. Raster Masks
	3. Vector Masks
	
	This article covers all 3 types.


** Clipping Masks **

Clipping masks are a powerful feature in graphic design and image editing software. They allow you to control the visibility of one layer based on the shape and content of another layer. In other words, a clipping mask restricts the visibility of a layer to the shape of another layer below it.

To create a clipping mask, you first need two layers: the base layer and the layer you want to clip. The base layer defines the shape or area that will be visible, while the layer you want to clip contains the content that will be clipped to the shape of the base layer.

When you apply a clipping mask, the content of the clipped layer is only visible within the boundaries of the base layer. Any content outside the base layer's boundaries will be hidden or clipped.

Clipping masks are particularly useful when you want to apply an effect, such as a texture or pattern, to a specific area of an image or artwork. By using a clipping mask, you can confine the effect to the desired area without affecting the rest of the image.

Please check example at the end of page

** Raster Masks ** 

Raster masks in PSD files are used to control the visibility of specific areas within a layer. Unlike vector masks, which use mathematical shapes to define the masked areas, raster masks utilize pixel-based information to determine which parts of a layer are visible or hidden.

A raster mask consists of a grayscale image that is applied to a layer. The white areas of the mask represent the visible portions, while the black areas represent the hidden portions. Shades of gray in between can be used to create partial transparency or semi-visible areas.

Please check example at the end of page

** Vector masks **

Vector masks in PSD files are a versatile tool used to define the visibility of specific areas within a layer based on mathematical shapes. Unlike raster masks, which use pixel-based information, vector masks utilize paths and curves to create smooth and scalable masked areas.

A vector mask is essentially a path that is applied to a layer. The shape of the path determines which parts of the layer are visible and which parts are hidden. By manipulating the path's control points and curves, you can create precise and intricate masked areas.

Please check the [Vector Masks page](psd/net/layer-vector-mask/) to get information about how the vector masks can be added using resources.


## **Example**
{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-update-create-layer-mask.py" >}}