---
title: Aspose.PSD for .NET 19.12 - 릴리스 노트
type: docs
weight: 10
url: /ko/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-11|[링크된 레이어 지원](/psd/ko/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|기능|
|PSDNET-131|[SoCoResource 지원](/psd/ko/net/support-of-socoresource/)|기능|
|PSDNET-115|TextLayer가 문자열로 업데이트될 때 기존 LineBreaks에 추가됨|버그|
|PSDNET-157|PSB를 PNG로 저장할 때 무결성|버그|
|PSDNET-250|레이어가 없는 CMYK PSD 파일을 RLE 압축으로로드 시 예외 발생|버그|
|PSDNET-161|텍스트 레이어를 업데이트할 때 예외 발생|버그|
|PSDNET-222|레이어 마스크가 있는 일부 PSD 파일을 리사이징하면 잘못된 동작|버그|
|PSDNET-244|Globalization.CultureInfo.CurrentCulture로 PSD 저장 시 로드 시 예외 발생|버그|

## **공개 API 변경**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **제거된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **사용 예시:**
**PSDNET-11. 링크된 레이어 지원**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("example.psd"))

            {

                Layer[] layers = psd.Layers;

                // link all layers in one linked group

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // gets id for one layer

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");

                }

                // gets all linked layers by link group id.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // unlink each layer from group

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // retrieves NULL for a link group ID that has no layers in the group.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("The linkedLayers field is not NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. SoCoResource 지원**

{{< highlight java >}}

      // SoCoResource 지원

    string sourceFileName = "ColorFillLayer.psd";

    string exportPath = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var layer in im.Layers)

        {

            if (layer is FillLayer)

            {

                var fillLayer = (FillLayer)layer;

                foreach (var resource in fillLayer.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(exportPath);

        }

    }

{{< /highlight >}}

**PSDNET-115. TextLayer가 문자열로 업데이트될 때 기존 LineBreaks에 추가됨**

{{< highlight java >}}

           const 문자열 NewText = "abcdef\rzxcvbn";

        string sourceFilePath = "TestFileForAsianChars.psd");

        string outputFilePath = "result.psd";

        using (var image = (PsdImage)Image.Load(sourceFilePath))

        {

            var layer = (TextLayer)image.Layers[0];

            var imageOptions = new PsdOptions(image);

            layer.UpdateText(NewText);

            image.Save(outputFilePath, imageOptions);

        }

        using (var createdImage = (PsdImage)Image.Load(outputFilePath))

        {

            var createdLayer = (TextLayer)createdImage.Layers[0];

            if (NewText != createdLayer.Text)

            {

                throw new InvalidDataException("Updated text is invalid");

            }

        }

{{< /highlight >}}

**PSDNET-157. PSB를 PNG로 저장할 때 무결성**

{{< highlight java >}}

       // PSB를 PNG로 저장

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}


` `**PSDNET-250. CMYK PSD 파일을 RLE 압축으로로드시 예외**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string sourcePath = "CmykWithAlpha.psd";

            using (RasterImage image = (RasterImage)Image.Load(sourcePath))

            {

                var rawDataSettings = image.RawDataSettings;

                RawDataTester loader = new RawDataTester();

                image.LoadRawData(image.Bounds, rawDataSettings, loader);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end)

            {

            }

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. 텍스트 레이어를 업데이트할 때 예외**

{{< highlight java >}}

      // PSD 파일을 이미지로 로드하고 PsdImage로 캐스트

    using (PsdImage psdImage = (PsdImage)Image.Load("example.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("test update", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("UpdateTextLayerInPSDFile_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. 일부 PSD 파일을 레이어 마스크로 리사이징하면 잘못된 동작**

{{< highlight java >}}

     int scale = 2;

        string[] names = {

                             "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                             "LevelsLayerWithLayerMaskRgb",

                             "LevelsLayerWithLayerMaskCmyk",

                             "ColorBalanceAdjustmentLayer"

                         };

        for (int i = 0; i < names.Length; i++)

        {

            string sourceFilePath = names[i] + ".psd";

            string outputFilePath = "output_" + sourceFilePath;

            string outputPngFilePath = "output_" + names[i] + ".png";

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))

            {

                image.Resize(image.Width * scale, image.Height * scale);

                image.Save(outputFilePath, new PsdOptions());

                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}


**PSDNET-244. 일부 Globalization.CultureInfo.CurrentCulture로 PSD 저장 시 로드시 예외**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string sourceFileName = string.Format("example-{0}.psd", i);

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdSaveOptions = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string outputFileName = "output-" + sourceFileName;

            // PSD 파일을 이미지로 로드하고 PsdImage로 캐스트

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentUICulture = culture;

            // PSD 파일을 이미지로 로드하고 PsdImage로 캐스트

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}
