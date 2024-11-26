---
title: Примітки до випуску Aspose.PSD для .NET 20.2
type: docs
weight: 110
url: /uk/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску [Aspose.PSD для .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-206|Покращення здатності рендерингу тексту різних кольорів у верхньому шарі тексту|Функція|
|PSDNET-369|Підтримка ресурсу clbl (Ресурс шару містить інформацію про обрізання змішування елементів)|Функція|
|PSDNET-274 |Підтримка ресурсу blwh (Ресурс містить дані про шар коригування чорного та білого)|Функція|
|PSDNET-230|Здатність експорту шару групи в формати Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Функція|
|PSDNET-372|Підтримка ресурсу lspf (Містить налаштування щодо налаштування захищеності шару)|Функція|
|PSDNET-370|Підтримка ресурсу infx (Містить дані про змішування внутрішніх елементів)|Функція|
|PSDNET-251|Рефакторинг PsdImage та Layer для зміни поведінки трансформації (Правильний розмір/обертання/обрізання для масок шарів у разі окремої трансформації одного шару)|Поліпшення|
|PSDNET-276 |У деяких налаштуваннях глобалізації, растровий зображення AI не може бути відкритий|Помилка|
|PSDNET-194|Після виконання операції FlipRotate на шару, PSD-зображення стає нерозпізнаване|Помилка|
|PSDNET-177. |System.ArgumentException під час завантаження файлу PSD|Помилка|
|PSDNET-249|Після використання методу трансформації лише для шару, збережений шар має неправильні межі або маску|Помилка|

## **Зміни у публічному API**
# **Додані API:**
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
# **Видалені API:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **Приклади використання:**
**PSDNET-206. Покращення здатності рендерингу тексту різних кольорів у верхньому шарі тексту**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("text_ethalon_different_colors.psd"))

{

    var txtLayer = (TextLayer)psdImage.Layers[1];

    txtLayer.TextData.UpdateLayerData();

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Підтримка ресурсу clbl (Ресурс шару містить інформацію про обрізання змішування елементів)**

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

            // Test editing and saving

            resource.BlendClippedElements = false;

            im.Save(destinationFileName);

        }

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(!resource.BlendClippedElements, "The ClblResource.BlendClippedElements should change to false");

        }

{{< /highlight >}}

**PSDNET-274. Підтримка ресурсу blwh (Ресурс містить дані про шар коригування чорного та білого)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Expected property value is not equal to actual value";

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        void ExampleSupportOfBlwhResource(...

{{< /highlight >}}

**PSDNET-230. Здатність експорту шару групи в формати Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("1.psd"))

            {

                // folder with background

                LayerGroup bg_folder = (LayerGroup)psdImage.Layers[0];

                // folder with content

                LayerGroup content_folder = (LayerGroup)psdImage.Layers[4];

                bg_folder.Save("background.png", new PngOptions());

                content_folder.Save("content.png", new PngOptions());

            }

{{< /highlight >}}

` `**PSDNET-372. Підтримка ресурсу lspf (Містить налаштування щодо налаштування захищеності шару)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Expected property value is not equal to actual value";

...

{{< /highlight >}}

` `**PSDNET-370. Підтримка ресурсу infx (Містить дані про змішування внутрішніх елементів)**

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

...

{{< /highlight >}}

**PSDNET-251. Рефакторинг PsdImage та Layer для зміни поведінки трансформації (Правильний розмір/обертання/обрізання для масок шарів у разі окремої трансформації одного шару)**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-276. У деяких налаштуваннях глобалізації, растровий зображення AI не може бути відкритий**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-194. Після виконання операції FlipRotate на шару, PSD-зображення стає нерозпізнаване**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-177. System.ArgumentException під час завантаження файлу PSD**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-249. Після використання методу трансформації лише для шару, збережений шар має неправильні межі або маску**

{{< highlight java >}}

...

{{< /highlight >}}---
title: Примітки до випуску Aspose.PSD для .NET 20.2
type: docs
weight: 110
url: /uk/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску [Aspose.PSD для .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-206|Покращення здатності рендерингу тексту різних кольорів у верхньому шарі тексту|Функція|
|PSDNET-369|Підтримка ресурсу clbl (Ресурс шару містить інформацію про обрізання змішування елементів)|Функція|
|PSDNET-274 |Підтримка ресурсу blwh (Ресурс містить дані про шар коригування чорного та білого)|Функція|
|PSDNET-230|Здатність експорту шару групи в формати Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Функція|
|PSDNET-372|Підтримка ресурсу lspf (Містить налаштування щодо налаштування захищеності шару)|Функція|
|PSDNET-370|Підтримка ресурсу infx (Містить дані про змішування внутрішніх елементів)|Функція|
|PSDNET-251|Рефакторинг PsdImage та Layer для зміни поведінки трансформації (Правильний розмір/обертання/обрізання для масок шарів у разі окремої трансформації одного шару)|Поліпшення|
|PSDNET-276 |У деяких налаштуваннях глобалізації, растровий зображення AI не може бути відкритий|Помилка|
|PSDNET-194|Після виконання операції FlipRotate на шару, PSD-зображення стає нерозпізнаване|Помилка|
|PSDNET-177. |System.ArgumentException під час завантаження файлу PSD|Помилка|
|PSDNET-249|Після використання методу трансформації лише для шару, збережений шар має неправильні межі або маску|Помилка|

## **Зміни у публічному API**
# **Додані API:**
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
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#