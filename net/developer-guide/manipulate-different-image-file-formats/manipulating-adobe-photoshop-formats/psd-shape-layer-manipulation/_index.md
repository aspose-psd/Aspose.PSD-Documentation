---
title: Shape Layer Manipulation in Aspose.PSD for C#
weight: 100
type: docs
description: Examples of how to manipulate Shape Layers of PSD File
keywords: [shape layer, curve, bezier curve, Anchor Point, bezier knots, psd api, C#, csharp, code sample]
url: net/psd-shape-layer-manipulation/
---

## Overview
Shape Layers are a significant feature in Aspose.PSD for C# that allow you to create and manipulate vector shapes within a PSD image. This article explores how to manipulate Shape Layers using the Aspose.PSD library. Topics covered include accessing Shape Layers, modifying path shapes, and updating the image.

### Applications of Shape Layers in Aspose.PSD for C#:

- **Creating Custom Shapes**: Shape Layers enable the creation of custom vector shapes within a PSD image. Define the shape's path by specifying Bezier curves and anchor points, offering flexibility to create complex shapes like polygons, stars, or custom logos.
  
- **Modifying Existing Shapes**: Shape Layers allow modification of existing shapes' properties. Change the position, size, rotation, and other attributes to achieve the desired visual effect. Resize, rotate, or skew shapes to create various effects.
  
- **Applying Styles and Effects**: Shape Layers support various styles and effects such as gradients, strokes, shadows, enhancing the appearance of shapes. This feature enables the creation of visually stunning designs and illustrations.
  
- **Combining Shapes**: Combine multiple shapes to create complex compositions. Merge shapes to create compound shapes or use Boolean operations to subtract, intersect, or exclude shapes from each other, enabling intricate designs by combining simple shapes creatively.

For more detailed examples and information, please refer to the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).

## Example

```csharp
using Aspose.PSD;![img.png](img.png)
using Aspose.PSD.FileFormats.Core.VectorPaths;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;

class Program
{
    static void Main()
    {
        string sourceFileName = "ShapeLayerTest.psd";
        string updatedOutput = "ShapeLayerTest_Res_up.psd";

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))
        {
            foreach (var layer in im.Layers)
            {
                // Finding Shape Layer
                if (layer is ShapeLayer shapeLayer)
                {
                    var path = shapeLayer.Path;
                    IPathShape[] pathShapes = path.GetItems();
                    List<BezierKnotRecord> knotsList = new List<BezierKnotRecord>();
                    foreach (var pathShape in pathShapes)
                    {
                        var knots = pathShape.GetItems();
                        knotsList.AddRange(knots);
                    }

                    // Change Path Shape properties
                    PathShape newShape = new PathShape();

                    BezierKnotRecord bn1 = new BezierKnotRecord
                    {
                        IsLinked = true,
                        Points = new Point[]
                        {
                            PointFToResourcePoint(new PointF(20, 100), shapeLayer.Container.Size),
                            PointFToResourcePoint(new PointF(20, 100), shapeLayer.Container.Size),
                            PointFToResourcePoint(new PointF(20, 100), shapeLayer.Container.Size)
                        }
                    };

                    BezierKnotRecord bn2 = new BezierKnotRecord
                    {
                        IsLinked = true,
                        Points = new Point[]
                        {
                            PointFToResourcePoint(new PointF(20, 490), shapeLayer.Container.Size),
                            PointFToResourcePoint(new PointF(20, 490), shapeLayer.Container.Size),
                            PointFToResourcePoint(new PointF(20, 490), shapeLayer.Container.Size)
                        }
                    };

                    BezierKnotRecord bn3 = new BezierKnotRecord
                    {
                        IsLinked = true,
                        Points = new Point[]
                        {
                            PointFToResourcePoint(new PointF(490, 20), shapeLayer.Container.Size),
                            PointFToResourcePoint(new PointF(490, 20), shapeLayer.Container.Size),
                            PointFToResourcePoint(new PointF(490, 20), shapeLayer.Container.Size)
                        }
                    };

                    List<BezierKnotRecord> bezierKnots = new List<BezierKnotRecord> { bn1, bn2, bn3 };
                    newShape.SetItems(bezierKnots.ToArray());

                    List<IPathShape> newShapes = new List<IPathShape>(pathShapes)
                    {
                        newShape
                    };

                    path.SetItems(newShapes.ToArray());

                    shapeLayer.Update();

                    im.Save(updatedOutput);

                    break;
                }
            }
        }
        
        Point PointFToResourcePoint(PointF point, Size imageSize)
        {
            const int ImgToPsdRatio = 256 * 65535;
            return new Point((int)(point.Y * (ImgToPsdRatio / imageSize.Height)), (int)(point.X * (ImgToPsdRatio / imageSize.Width)));
        }
    }
}
```

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).
