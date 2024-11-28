---
title: Aspose.PSD для .NET 20.2 - Примечания к выпуску
type: docs
weight: 110
url: /ru/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-206|Улучшение возможности отображения текста разных цветов в слое текста|Функциональность|
|PSDNET-369|Поддержка ресурса clbl (Ресурс слоя, содержащий информацию о элементах обрезки наложения)|Функциональность|
|PSDNET-274 |Поддержка ресурса blwh (Ресурс, содержащий данные слоя коррекции черного и белого)|Функциональность|
|PSDNET-230|Возможность экспорта группы слоев в Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Функциональность|
|PSDNET-372|Поддержка ресурса lspf (Содержит параметры настройки защищенного слоя)|Функциональность|
|PSDNET-370|Поддержка ресурса infx (Содержит данные об смешивании внутренних элементов)|Функциональность|
|PSDNET-251|Рефакторинг PsdImage и Layer для изменения поведения трансформации (Правильное изменение размера/поворот/обрезка для масок слоев при трансформации одного слоя отдельно)|Улучшения|
|PSDNET-276 |В некоторых настройках глобализации растровое изображение AI не может быть открыто|Ошибка|
|PSDNET-194|` `После выполнения операции FlipRotate на слое PSD изображение становится неразборчивым|Ошибка|
|PSDNET-177. |System.ArgumentException во время загрузки файла PSD|Ошибка|
|PSDNET-249|После использования метода трансформации только для слоя, сохраненный слой имеет некорректные границы или маску|Ошибка|

## **Изменения в общедоступном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykColor.Equals(System.Object)
- T:Aspose.PSD.CompositeException
- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)
- F:Aspose.PSD.FileFormat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler
- P:Aspose.PSD.LoadOptions.ProgressEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.ProgressEventHandler
- T:Aspose.PSD.ProgressManagement.EventType
- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress
- F:Aspose.PSD.ProgressManagement.EventType.StageChange
- F:Aspose.PSD.ProgressManagement.EventType.Initialization
- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing
- F:Aspose.PSD.ProgressManagement.EventType.Processing
- F:Aspose.PSD.ProgressManagement.EventType.Finalization
- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value
- M:Aspose.PSD.RasterImage.GetSkewAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)
# **Удаленные API:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **Примеры использования:**
**PSDNET-206. Улучшение возможности отображения текста разных цветов в слое текста**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("text_ethalon_different_colors.psd"))

{

    var txtLayer = (TextLayer)psdImage.Layers[1];

    txtLayer.TextData.UpdateLayerData();

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Поддержка ресурса clbl (Ресурс слоя, содержащий информацию о элементах обрезки наложения)**

{{< highlight java >}}

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "SampleForResource.psd";

        string destinationFileName = "Output" + sourceFileName;

        ClblResource GetClblResource(PsdImage im)

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is ClblResource)

                    {

                        return (ClblResource)layerResource;

                    }

                }

            }

            throw new Exception("The specified ClblResource not found");

        }

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(resource.BlendClippedElements, "The ClblResource.BlendClippedElements should be true");

            // Тестирование изменения и сохранения

            resource.BlendClippedElements = false;

            im.Save(destinationFileName);

        }

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(!resource.BlendClippedElements, "The ClblResource.BlendClippedElements should change to false");

        }

{{< /highlight >}}

**PSDNET-274. Поддержка ресурса blwh (Ресурс, содержащий данные слоя коррекции черного и белого)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Expected property value is not equal to actual value";

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        void ExampleSupportOfBlwhResource(

            string sourceFileName,

            int reds,

            int yellows,

            int greens,

            int cyans,

            int blues,

            int magentas,

            bool useTint,

            int bwPresetKind,

            string bwPresetFileName,

            double tintColorRed,

            double tintColorGreen,

            double tintColorBlue,

            int tintColor,

            int newTintColor)

        {

            string destinationFileName = "Output" + sourceFileName;

            bool isRequiredResourceFound = false;

            using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

            {

                foreach (var layer in im.Layers)

                {

                    foreach (var layerResource in layer.Resources)

                    {

                        if (layerResource is BlwhResource)

                        {

                            var blwhResource = (BlwhResource)layerResource;

                            var blwhLayer = (BlackWhiteAdjustmentLayer)layer;

                            isRequiredResourceFound = true;

                            AssertIsTrue(blwhResource.Reds == reds, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Yellows == yellows, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Greens == greens, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Cyans == cyans, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Blues == blues, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Magentas == magentas, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.UseTint == useTint, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.TintColor == tintColor, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BwPresetKind == bwPresetKind, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BlackAndWhitePresetFileName == bwPresetFileName, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorRed - tintColorRed) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorGreen - tintColorGreen) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorBlue - tintColorBlue) < 1e-6, ActualPropertyValueIsWrongMessage);

                            // Тестирование изменения и сохранения

                            blwhResource.Reds = reds - 15;

                            blwhResource.Yellows = yellows - 15;

                            blwhResource.Greens = greens + 15;

                            blwhResource.Cyans = cyans + 15;

                            blwhResource.Blues = blues - 15;

                            blwhResource.Magentas = magentas - 15;

                            blwhResource.UseTint = !useTint;

                            blwhResource.BwPresetKind = 4;

                            blwhResource.BlackAndWhitePresetFileName = "bwPresetFileName";

                            blwhLayer.TintColorRed = tintColorRed - 60;

                            blwhLayer.TintColorGreen = tintColorGreen - 60;

                            blwhLayer.TintColorBlue = tintColorBlue - 60;

                            im.Save(destinationFileName);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(isRequiredResourceFound, "The specified BlwhResource not found");

            isRequiredResourceFound = false;

            using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

            {

                foreach (var layer in im.Layers)

                {

                    foreach (var layerResource in layer.Resources)

                    {

                        if (layerResource is BlwhResource)

                        {

                            var blwhResource = (BlwhResource)layerResource;

                            var blwhLayer = (BlackWhiteAdjustmentLayer)layer;

                            isRequiredResourceFound = true;

                            AssertIsTrue(blwhResource.Reds == reds - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Yellows == yellows - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Greens == greens + 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Cyans == cyans + 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Blues == blues - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Magentas == magentas - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.UseTint == !useTint, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.TintColor == newTintColor, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BwPresetKind == 4, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BlackAndWhitePresetFileName == "bwPresetFileName", ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorRed - tintColorRed + 60) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorGreen - tintColorGreen + 60) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorBlue - tintColorBlue + 60) < 1e-6, ActualPropertyValueIsWrongMessage);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(isRequiredResourceFound, "The specified BlwhResource not found");

        }

        ExampleSupportOfBlwhResource(

            "BlackWhiteAdjustmentLayerStripesMask.psd",

            0x28,

            0x3c,

            0x28,

            0x3c,

            0x14,

            0x50,

            false,

            1,

            "\0",

            225.00045776367188,

            211.00067138671875,

            179.00115966796875,

            -1977421,

            -5925001);

        ExampleSupportOfBlwhResource(

            "BlackWhiteAdjustmentLayerStripesMask2.psd",

            0x80,

            0x40,

            0x20,

            0x10,

            0x08,

            0x04,

            true,

            4,

            "\0",

            239.996337890625,

            127.998046875,

            63.9990234375,

            -1015744,

            -4963324);

        Console.WriteLine("Обновление ресурса Blwh работает ожидаемым образом. Нажмите любую клавишу.");

{{< /highlight >}}

**PSDNET-230. Возможность экспорта группы слоев в Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("1.psd"))

            {

                // папка с фоном

                LayerGroup bg_folder = (LayerGroup)psdImage.Layers[0];

                // папка с содержимым

                LayerGroup content_folder = (LayerGroup)psdImage.Layers[4];

                bg_folder.Save("background.png", new PngOptions());

                content_folder.Save("content.png", new PngOptions());

            }

{{< /highlight >}}

` `**PSDNET-372. Поддержка ресурса lspf (Содержит параметры настройки защищенного слоя)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Expected property value is not equal to actual value";

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "SampleForResource.psd";

        string destinationFileName = "Output" + sourceFileName;

        bool isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is LspfResource)

                    {

                        var resource = (LspfResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        // Тестирование изменения и сохранения

                        resource.IsCompositeProtected = true;

                        AssertIsTrue(true == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        resource.IsCompositeProtected = false;

                        resource.IsPositionProtected = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(true == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        resource.IsPositionProtected = false;

                        resource.IsTransparencyProtected = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(true == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        resource.IsCompositeProtected = true;

                        resource.IsPositionProtected = true;

                        resource.IsTransparencyProtected = true;

                        im.Save(destinationFileName);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "The specified LspfResource not found");

        isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is LspfResource)

                    {

                        var resource = (LspfResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "The specified LspfResource not found");

        Console.WriteLine("Обновление ресурса Lspf работает ожидаемым образом. Нажмите любую клавишу.");

{{< /highlight >}}

` `**PSDNET-370. Поддержка ресурса infx (Содержит данные о смешивании внутренних элементов)**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "SampleForResource.psd";

        string destinationFileName = "Output" + sourceFileName;

        bool isRequiredResourceFound = false;