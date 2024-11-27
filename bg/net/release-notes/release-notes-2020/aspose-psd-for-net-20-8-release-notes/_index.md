---
title: Aspose.PSD за .NET 20.8 - Бележки за изданието
type: docs
weight: 50
url: /bg/net/aspose-psd-za-net-20-8-belejki-za-izdanieto/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-390|Поддръжка на PlLdResource (ресурс на поставения слой за Smart Object Layer)|Функционалност|
|PSDNET-400|Поддръжка на SoLdResource (ресурс на данни за Smart Object Layer)|Функционалност|
|PSDNET-693|Добавяне на поддръжка за структурите Object Array и Unit Array: ObAr / UnFl|Функционалност|
|PSDNET-600|Поправка на запазването на промененото изображение в PSD формат с CMYK ColorMode 16 бита на канал|Проблем|
|PSDNET-664|Подчертаването и зачертаването се губят след фокусиране върху текста в файл, запазен с Aspose.PSD|Проблем|
|PSDNET-710|Регресия: Aspose.PSD 20.7.0 нарушава размерите на шрифтовете за по-старите файлове|Проблем|

## **Промени в общественото API**
# **Добавени API:**
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

# **Премахнати API:**
- Няма

## **Примери за използване:**
**PSDNET-390. Поддръжка на PlLdResource (ресурс на поставения слой за Smart Object Layer)**
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
                    string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
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
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
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

                            // Бъдете внимателни с някои параметри: изображението може да стане неразличимо от Adobe® Photoshop®
                            ////resource.UOrder = 6;
                            ////resource.VOrder = 9;

                            // Не променяйте това, в противен случай няма да можете да използвате свободно преобразуване
                            // или да промените подчертаващият смарт обект към векторен тип
                            ////resource.PlacedLayerType = PlacedLayerType.Vector;

                            // Трябва да има валиден PlLdResource с този уникален идентификатор
                            ////resource.UniqueId = new Guid("98765432-10fe-cba0-1234-56789abcdef0");

                        break;
                    }
                }
            }

            AssertAreEqual(true, resource != null);
            image.Save(outputFilePath, new PsdOptions(image));
        }
{{< /highlight >}}
**PSDNET-400. Поддръжка на SoLdResource (ресурс на данни за Smart Object Layer)**
{{< highlight csharp >}}
        /* Този пример показва как да получите или зададете свойствата за данните на смарт обектния слой от PSD файл. */

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
                    string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
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
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
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
                0.0,
                0.0,
                0.0,
                0d,
                0d,
                721d,
                1280d,
                4,
                4,
                1,
                0,
                600,
                0,
                600,
                1,
                1280d,
                721d,
                72d,
                UnitTypes.Density,
                -1,
                -1,
                -1,
                "625cc4b9-2c5f-344f-8636-03caf2bd3489",
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
            SoLdResource resource = null;
            int index = 0;
            foreach (Layer imageLayer in image.Layers)
            {
                foreach (var imageResource in imageLayer.Resources)
                {
                    resource = imageResource as SoLdResource;
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

                        AssertAreEqual(expectedValue[16], resource.Crop);
                        AssertAreEqual(expectedValue[17], resource.FrameStepNumerator);
                        AssertAreEqual(expectedValue[18], resource.FrameStepDenominator);
                        AssertAreEqual(expectedValue[19], resource.DurationNumerator);
                        AssertAreEqual(expectedValue[20], resource.DurationDenominator);
                        AssertAreEqual(expectedValue[21], resource.FrameCount);
                        AssertAreEqual(expectedValue[22], resource.Width);
                        AssertAreEqual(expectedValue[23], resource.Height);
                        AssertAreEqual(expectedValue[24], resource.Resolution);
                        AssertAreEqual(expectedValue[25], resource.ResolutionUnit);
                        AssertAreEqual(expectedValue[26], resource.Comp);
                        AssertAreEqual(expectedValue[27], resource.CompId);
                        AssertAreEqual(expectedValue[28], resource.OriginalCompId);
                        AssertAreEqual(expectedValue[29], resource.PlacedId.ToString());
                        AssertAreEqual((IEnumerable)expectedValue[30], resource.NonAffineTransformMatrix);
                        if (resource.IsCustom)
                        {
                            AssertAreEqual(expectedValue[31], resource.HorizontalMeshPointUnit);
                            AssertAreEqual((double[])expectedValue[32], resource.HorizontalMeshPoints);
                            AssertAreEqual(expectedValue[33], resource.VerticalMeshPointUnit);
                            AssertAreEqual((double[])expectedValue[34], resource.VerticalMeshPoints);
                            var temp = resource.VerticalMeshPoints;
                            resource.VerticalMeshPoints = resource.HorizontalMeshPoints;
                            resource.HorizontalMeshPoints = temp;
                        }

                        // Тези стойности трябва да се променят в PlLdResource (със специфичния UniqueId) също
                        // и някои от тях трябва да бъдат в съответствие с поддържащият смарт обект в LinkDataSource
                        resource.PageNumber = 2;
                        resource.TotalPages = 3;
                        resource.AntiAliasPolicy = 0;
                        resource.Value = 1.23456789;
                        resource.Perspective = 0.123456789;
                        resource.PerspectiveOther = 0.987654321;
                        resource.Top = -126;
                        resource.Left = -215;
                        resource.Bottom = 248;
                        resource.Right = 145;
                        resource.Crop = 4;
                        resource.FrameStepNumerator = 1;
                        resource.FrameStepDenominator = 601;
                        resource.DurationNumerator = 2;
                        resource.DurationDenominator = 602;
                        resource.FrameCount = 11;
                        resource.Width = 541;
                        resource.Height = 249;
                        resource.Resolution = 144;
                        resource.Comp = 21;
                        resource.CompId = 22;
                        resource.TransformMatrix = new double[8]
                        {
                            12.937922786050663,
                            19.419959734187131,
                            2.85445817782261,
                            1.0540625423957124,
                            7.20861031651307,
                            14.634102808208553,
                            17.292074924741144,
                            4
                        };
                        resource.NonAffineTransformMatrix = new double[8]
                        {
                            129.937922786050663,
                            195.419959734187131,
                            26.85445817782261,
                            12.0540625423957124,
                            72.20861031651307,
                            147.634102808208553,
                            175.292074924741144,
                            42
                        };

                        // Този уникален идентификатор трябва да бъде променен в референциите, ако има такива
                        resource.PlacedId = new Guid("12345678-9abc-def0-9876-54321fecba98");

                        // Бъдете внимателни с някои параметри: изображението може да стане неразличимо от Adobe® Photoshop®
                        ////resource.UOrder = 6;
                        ////resource.VOrder = 9;

                        // Не променяйте това, иначе няма да можете да използвате свободно преобразуване
                        // или да промените подчертаващият смарт обект към векторен тип
                        ////resource.PlacedLayerType = PlacedLayerType.Vector;

                        // Трябва да има валиден PlLdResource с този уникален идентификатор
                        ////resource.UniqueId = new Guid("98765432-10fe-cba0-1234-56789abcdef0");

                        break;
                    }
                }
            }

            AssertAreEqual(true, resource != null);
            image.Save(outputFilePath, new PsdOptions(image));
        }
{{< /highlight >}}
**PSDNET-693. Добавяне на поддръжка за структурите Object Array и Unit Array: ObAr / UnFl**
{{< highlight csharp >}}
            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
                }
            }

            string dataDir = "PSDNET693_1\\";
            var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                UnitArrayStructure verticalStructure = null;
                foreach (Layer imageLayer in image.Layers)
                {
                    foreach (var imageResource in imageLayer.Resources)
                    {
                        var resource = imageResource as PlLdResource;
                        if (resource != null && resource.IsCustom)
                        {
                            foreach (OSTypeStructure structure in resource.Items)
                            {
                                if (structure.KeyName.ClassName == "customEnvelopeWarp")
                                {
                                    AssertAreEqual(typeof(DescriptorStructure), structure.GetType());
                                    var custom = (DescriptorStructure)structure;
                                    AssertAreEqual(custom.Structures.Length, 1);
                                    var mesh = custom.Structures[0];
                                    AssertAreEqual(typeof(ObjectArrayStructure), mesh.GetType());
                                    var meshObjectArray = (ObjectArrayStructure)mesh;
                                    AssertAreEqual(meshObjectArray.Structures.Length, 2);
                                    var vertical = meshObjectArray.Structures[1];
                                    AssertAreEqual(typeof(UnitArrayStructure), vertical.GetType());
                                    verticalStructure = (UnitArrayStructure)vertical;
                                    AssertAreEqual(verticalStructure.UnitType, UnitTypes.Pixels);
                                    AssertAreEqual(verticalStructure.ValueCount, 16);

                                    break;
                                }
                            }
                        }
                    }
                }

                AssertAreEqual(true, verticalStructure != null);
            }
{{< /highlight >}}
**PSDNET-600. Поправка на запазването на промененото изображение в PSD формат с CMYK ColorMode 16 бита на канал**
{{< highlight csharp >}}
           using (PsdImage image = (PsdImage)Image.Load("cub16bit_cmyk.psd"))
            {
                RasterCachedImage raster = image.Layers[0];
                Aspose.PSD.Graphics graphics = new Graphics(raster);
                int width = raster.Width;
                int height = raster.Height;
                Rectangle rect = new Rectangle(width / 3, height / 3, width```csharp
                int height / 3);

                // Изтрийте пикселите на квадрата
                for (int y = rect.Top; y <= rect.Bottom; y++)
                {
                    for (int x = rect.Left; x <= rect.Right; x++)
                    {
                        raster[x, y] = Color.Transparent;
                    }
                }

                image.Save("cub16bit_cmyk_output.psd");
            }
```
**PSDNET-664. Подчертаването и зачертаването се губят след фокусиране върху текста в файл, запазен с Aspose.PSD**
```csharp
            using (PsdImage image = (PsdImage)Image.Load("text.psd"))
            {
                RasterLayer textLayer = (RasterLayer)image.Layers[0];
                textLayer.FillColor = Color.Black;
                textLayer.BackgroundColor = Color.White;
                textLayer.FontStyle.EmphasisMark = FontStyles.EmphasisMarkOverSolidCircle;
                textLayer.FontStyle.FontSize = 24;
                textLayer.FontStyle.Overline = true;

                PsdImage textImage = new PsdImage(image.Width, image.Height);
                textImage.AddLayer(textLayer);
                textImage.Save("text_output.psd");
            }
```
**PSDNET-710. Регресия: Aspose.PSD 20.7.0 нарушава размерите на шрифтовете за по-старите файлове**
```csharp
            using (PsdImage image = (PsdImage)Image.Load("old_file.psd"))
            {
                RasterLayer textLayer = (RasterLayer)image.Layers[0];
                textLayer.FontStyle.FontSize = 18;
                textLayer.FontStyle.Bold = true;
                textLayer.FontStyle.Italic = true;

                PsdImage updatedImage = new PsdImage(image.Width, image.Height);
                updatedImage.AddLayer(textLayer);
                updatedImage.Save("old_file_updated.psd");
            }
``````csharp
## **Промени в общественото API**
# **Добавени API:**
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
```