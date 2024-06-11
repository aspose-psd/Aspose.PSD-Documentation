---
title: Working with masks in Aspose.PSD for С#
weight: 100
type: docs
description: Examples of how to work with Clipping, Raster and Vector Masks within PSD File
keywords: [masks, layer mask, vector mask, clipping mask, psd, psd api, C#, csharp, code sample]
url: net/update-create-layer-mask/
---

## Overview

There are three types of masks in PSD files:
1. Clipping Masks
2. Raster Masks
3. Vector Masks

This article covers all three types.

### Clipping Masks

Clipping masks are a powerful feature in graphic design and image editing software that allow you to control the visibility of one layer based on the shape and content of another layer. Essentially, a clipping mask restricts the visibility of a layer to the shape defined by another layer below it.

To create a clipping mask, you need two layers: the base layer and the clipping layer. The base layer defines the shape or area that will be visible, while the clipping layer contains the content that will be confined to the shape of the base layer.

When you apply a clipping mask, the content of the clipping layer is only visible within the boundaries of the base layer. Any content outside the base layer’s boundaries is hidden or clipped.

Clipping masks are particularly useful for applying effects, such as textures or patterns, to specific areas of an image or artwork. By using a clipping mask, you can ensure the effect is confined to the desired area without impacting the rest of the image.

### Raster Masks

Raster masks in PSD files are essential for controlling the visibility of specific areas within a layer. Unlike vector masks, which use mathematical shapes to define masked areas, raster masks use pixel-based information to determine which parts of a layer are visible or hidden.

A raster mask consists of a grayscale image applied to a layer. The white areas of the mask represent the visible portions, while the black areas represent the hidden portions. Shades of gray in between create partial transparency or semi-visible areas.

Using raster masks, you can achieve intricate masking effects, allowing for precise control over layer visibility based on pixel-level details. This feature is particularly useful for tasks that require detailed editing and blending within an image.

### Vector Masks

Vector masks in PSD files are a versatile tool used to define the visibility of specific areas within a layer based on mathematical shapes. Unlike raster masks, which use pixel-based information, vector masks utilize paths and curves to create smooth and scalable masked areas.

A vector mask is essentially a path applied to a layer. The shape of the path determines which parts of the layer are visible and which are hidden. By manipulating the path’s control points and curves, you can create precise and intricate masked areas.

Vector masks are particularly useful for creating clean, scalable masks that can be easily adjusted without loss of quality. This feature is ideal for tasks requiring high precision and flexibility in defining visible areas within a layer.

For more information on adding vector masks, please visit the [Vector Masks page](psd/net/layer-vector-mask/).

## Example
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).

