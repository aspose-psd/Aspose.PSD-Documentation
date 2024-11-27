---
title: دستاوردهای انتشار Aspose.PSD برای .NET 20.8
type: docs
weight: 50
url: /fa/net/aspose-psd-for-net-20-8-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD برای .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-390|پشتیبانی از PlLdResource (منبع لایه قرار داده شده برای لایه شیء هوشمند)|ویژگی|
|PSDNET-400|پشتیبانی از SoLdResource (منبع داده لایه شیء هوشمند)|ویژگی|
|PSDNET-693|افزودن پشتیبانی از ساختارهای آرایه شیء و آرایه واحد: امضای ObAr / UnFl|ویژگی|
|PSDNET-600|رفع باگ در ذخیره تصویر PSD اصلاح شده با CMYK ColorMode 16 بیت در کانال|باگ|
|PSDNET-664|خط زیر و خط خورده پس از تمرکز بر روی متن در فایل ذخیره شده با Aspose.PSD از بین می‌روند|باگ|
|PSDNET-710|رگرسیون: Aspose.PSD 20.7.0 اندازه فونت را برای فایل‌های قدیمی شکسته می‌کند|باگ|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Structures
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitTypes,System.Double[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.UnitType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.Values
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.ValueCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnitArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.Unknown
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.Vector
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.Raster
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.ImageStack
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Items
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.NonAffineTransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Crop
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Resolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.ResolutionUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameStepNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameStepDenominator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.DurationNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.DurationDenominator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TypeToolKey

# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**
**PSDNET-390. پشتیبانی از PlLdResource (منبع لایه قرار داده شده برای لایه شیء هوشمند)**
{{< highlight csharp >}}
        void AssertAreEqual(object actual, object expected)
        {
            var areEqual = object.Equals(actual, expected);
            if (!areEqual && actual is Array && expected is Array)
            {
                var actualArray = (Array)actual;
                var expectedArray = (Array)actual;
                if (actualArray.Length == expectedArray.Length)
                {
                    for (int i = 0; i < actualArray.Length; i++)
                    {
                        if (!object.Equals(actualArray.GetValue(i), expectedArray.GetValue(i)))
                        {
                            break;
                        }
                    }

                    areEqual = true;
                }
            }

            if (!areEqual)
            {
                throw new FormatException(
                    string.Format("مقدار واقعی {0} با مقدار مورد انتظار {1} برابر نیست.", actual, expected));
            }
        }


        string dataDir = "PSDNET390_1\\";
        var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
        var outputFilePath = dataDir + "LayeredSmartObjects8bit2_output.psd";
        var expectedValues = new object[]
        {
            new object[]
            {
                true,
                "76f05a3b-7523-5e42-a1bb-27f4735bffa0",
                1,
                1,
                0x10,
                PlacedLayerType.Raster,
                new double[8]
                {
                    29.937922786050663,
                    95.419959734187131,
                    126.85445817782261,
                    1.0540625423957124,
                    172.20861031651307,
                    47.634102808208553,
                    75.292074924741144,
                    142
                },
                0d,
                0d,
                0d,
                0d,
                0d,
                149d,
                310d,
                4,
                4,
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d
                },
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 0.0d, 0.0d, 0.0d,
                    49.666666666666664d, 49.666666666666664d, 49.666666666666664d, 49.666666666666664d,
                    99.333333333333329d, 99.333333333333329d, 99.333333333333329d, 99.333333333333329d,
                    149, 149, 149, 149,
                },
            },
            new object[]
            {
                true,
                "cf0477a8-8f92-ac4f-9462-f78e26234851",
                1,
                1,
                0x10,
                PlacedLayerType.Raster,
                new double[8]
                {
                    37.900314592235681,
                    -0.32118219433001371,
                    185.94210608826535,
                    57.7076819802063,
                    153.32047433609358,
                    140.9311755779743,
                    5.2786828400639294,
                    82.902311403437977,
                },
                0d,
                0d,
                0d,
                0d,
                0d,
                721d,
                1280d,
                4,
                4,
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0, 426.66666666666663, 853.33333333333326, 1280,
                    0.0, 426.66666666666663, 853.33333333333326, 1280,
                    0.0, 426.66666666666663, 853.33333333333326, 1280,
                    0.0, 426.66666666666663, 853.33333333333326, 1280,
                },
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0, 0.0, 0.0, 0.0,
                    240.33333333333331, 240.33333333333331, 240.33333333333331, 240.33333333333331,
                    480.66666666666663, 480.66666666666663, 480.66666666666663, 480.66666666666663,
                    721, 721, 721, 721,
                },
                0,
                0
            }
        };

        using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
        {
            PlLdResource resource = null;
            int index = 0;
            foreach (Layer imageLayer in image.Layers)
            {
                foreach (var imageResource in imageLayer.Resources)
                {
                    resource = imageResource as PlLdResource;
                    if (resource != null)
                    {
                        var expectedValue = (object[])expectedValues[index++];
                        AssertAreEqual(expectedValue[0], resource.IsCustom);
                        AssertAreEqual(expectedValue[1], resource.UniqueId.ToString());
                        AssertAreEqual(expectedValue[2], resource.PageNumber);
                        AssertAreEqual(expectedValue[3], resource.TotalPages);
                        AssertAreEqual(expectedValue[4], resource.AntiAliasPolicy);
                        AssertAreEqual(expectedValue[5], resource.PlacedLayerType);
                        AssertAreEqual(8, resource.TransformMatrix.Length);
                        AssertAreEqual((double[])expectedValue[6], resource.TransformMatrix);
                        AssertAreEqual(expectedValue[7], resource.Value);
                        AssertAreEqual(expectedValue[8], resource.Perspective);
                        AssertAreEqual(expectedValue[9], resource.PerspectiveOther);
                        AssertAreEqual(expectedValue[10], resource.Top);
                        AssertAreEqual(expectedValue[11], resource.Left);
                        AssertAreEqual(expectedValue[12], resource.Bottom);
                        AssertAreEqual(expectedValue[13], resource.Right);
                        AssertAreEqual(expectedValue[14], resource.UOrder);
                        AssertAreEqual(expectedValue[15], resource.VOrder);
                        if (resource.IsCustom)
                        {
                            AssertAreEqual(expectedValue[16], resource.HorizontalMeshPointUnit);
                            AssertAreEqual((double[])expectedValue[17], resource.HorizontalMeshPoints);
                            AssertAreEqual(expectedValue[18], resource.VerticalMeshPointUnit);
                            AssertAreEqual((double[])expectedValue[19], resource.VerticalMeshPoints);
                            var temp = resource.VerticalMeshPoints;
                            resource.VerticalMeshPoints = resource.HorizontalMeshPoints;
                            resource.HorizontalMeshPoints = temp;
                        }

                        resource.PageNumber = 2;
                        resource.TotalPages = 3;
                        resource.AntiAliasPolicy = 30;
                        resource.Value = 1.23456789;
                        resource.Perspective = 0.123456789;
                        resource.PerspectiveOther = 0.987654321;
                        resource.Top = -126;
                        resource.Left = -215;
                        resource.Bottom = 248;
                        resource.Right = 145;

                        break;
                    }
                }
            }

            AssertAreEqual(true, resource != null);
            image.Save(outputFilePath, new PsdOptions(image));
        }
{{< /highlight >}}
**PSDNET-400. پشتیبانی از SoLdResource (منبع داده لایه شیء هوشمند)**
{{< highlight csharp >}}
        // این مثال نحوه دریافت یا تنظیم ویژگی‌های داده لایه شیء هوشمند فایل PSD را نشان می‌دهد.

        void AssertAreEqual(object actual, object expected)
        {
            if (!object.Equals(actual, expected))
            {
                throw new FormatException(string.Format("مقدار واقعی {0} با مقدار مورد انتظار {1} برابر نیست.", actual, expected));
            }
        }

        string dataDir = "PSDNET400_1\\";
        var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
        var outputFilePath = dataDir + "LayeredSmartObjects8bit2_output.psd";
        var expectedValues = new object[]
        {
            new object[]
            {
                true,
                "76f05a3b-7523-5e42-a1bb-27f4735bffa0",
                1,
                1,
                0x10,
                PlacedLayerType.Raster,
                new double[8]
                {
                    29.937922786050663,
                    95.419959734187131,
                    126.85445817782261,
                    1.0540625423957124,
                    172.20861031651307,
                    47.634102808208553,
                    75.292074924741144,
                    142
                },
                0.0,
                0.0,
                0.0,
                0d,
                0d,
                149d,
                310d,
                4,
                4,
                1,
                0,
                600,
                0,
                600,
                1,
                310d,
                149d,
                72d,
                UnitTypes.Density,
                -1,
                -1,
                -1,
                "d3388655-19e4-9742-82f2-f553bb01046a",
                new double[8]
                {
                    29.937922786050663,
                    95.419959734187131,
                    126.85445817782261,
                    1.0540625423957124,
                    172.20861031651307,
                    47.634102808208553,
                    75.292074924741144,
                    142
                },
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 103.333333333333