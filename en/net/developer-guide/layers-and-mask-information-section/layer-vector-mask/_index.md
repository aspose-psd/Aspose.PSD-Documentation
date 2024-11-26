---
title: Layer Vector Mask
type: docs
weight: 10
url: /net/layer-vector-mask/
---

## **Layer Vector Mask Overview**
A vector mask is a resolution-independent path that clips out the contents of the layer. Vector masks are usually more accurate than those created with pixel-based tools. You create vector masks with the pen or shapes tools.

Aspose.PSD supports rendering and applying of vector masks. You can edit vector masks through editing of Vector Paths.
## **Vector path in Aspose.PSD**
Access to vector paths in Aspose.PSD is provided through [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) and [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) resources that are child classes of [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **How to edit a vector path?**
### **Vector path struct**
Base struct to manipulate paths is [VectorPathRecord.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord) But for your convenience, the following solution is suggested.

For easy editing of vector paths, you should use the [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) class, which contains methods for comfy editing of vector data in resources derived from VectorPathDataResource

Get started with creating an object of type VectorPath.

For convenience, you can use the static method [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), it will find a vector resource in the input layer and create a VectorPath object based on it.



After all edits, you can apply the VectorPath object with changes back to layer using static method [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

The VectorPath type contains a list of [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) elements and describes a whole vector image that can consist of one or more shapes.

![todo:image_alt_text](layer-vector-mask_1.png)



Each PathShape is a vector figure that consists of a separate set of bezier knots(point).

Knots are objects of type [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) that are essentially the points from which the figure is building.

![todo:image_alt_text](layer-vector-mask_2.png)

The following code example shows how to access a figure and points.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **How to create a shape?**
To edit a shape, you need to gets an existing one from the [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) list, or add a new shape by creating a [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) instance and adding it to the [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) list.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **How to add knots (points)?**
You can manipulate the points of shape as elements of a regular List using the PathShape.Points property, for example, you can add shape points:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}



BezierKnot contains Anchor point and two Control points.

![todo:image_alt_text](layer-vector-mask_3.png)

If anchor and control points have the same values, then that node will have an acute angle.

To change the anchor point position along with the control points (similar to how it happens in Photoshop), the BezierKnot has a Shift method.

The following code example demonstrates moving whole bezier knot vertical up by Y coordinate:

You can manipulate the points of shape as elements of a regular List using the PathShape.Points property, for example, you can add shape points:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **PathShape properties**
PathShape editing is not limited to editing nodes, this type also has other properties.
### **PathOperations (Boolean operations)**
The [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) property is a so-called boolean operation, changing the value of which defines how multiple shapes are mixed.

There are the following possible values:

- 0 = ExcludeOverlappingShapes (XOR operation).
- 1 = CombineShapes (OR operation).
- 2 = SubtractFrontShape (NOT operation).
- 3 = IntersectShapeAreas (AND operation).

![todo:image_alt_text](layer-vector-mask_4.png)
### **IsClosed Property**
Also, using the PathShape.IsClosed property, we can determine whether the first and last knot of a shape are connected.

|**Closed shape**|**Opened shape**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **FillColor Property**
No figure can have its own color, so you can change the color of the whole vector path with the VectorPath.FillColor property.

You can manipulate the points of shape as elements of a regular List using the PathShape.Points property, for example, you can add shape points:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Here you will find the source code of VectorDataProvider and related classes:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
