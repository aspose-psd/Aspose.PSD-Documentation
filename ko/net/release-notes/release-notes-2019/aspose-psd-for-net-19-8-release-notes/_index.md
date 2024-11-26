---
title: Aspose.PSD for .NET 19.8 - 릴리스 노트
type: docs
weight: 50
url: /ko/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

이 페이지는 Aspose.PSD for .NET 19.8의 릴리스 노트를 포함합니다

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-184|스트림에서 JPEG, PNG 및 기타 이미지 파일을 PsdImage로 로드|기능|
|PSDNET-134|채우기 레이어 렌더링 구현: 그라데이션|기능|
|PSDNET-166|PSD를 PDF로 저장할 때 선택 가능한 텍스트 제공 안 함|기능|
|PSDNET-158|PSB를 PDF로 저장하는 것 지원|기능|
|PSDNET-189|ReadOnly 모드로 PSD를 로드 시 메모리 사용량이 높음|개선|
|PSDNET-171|새로운 TextLayer를 생성한 후 PSD 파일이 PS에서 읽을 수 없음|버그|
|PSDNET-156|PSD를 로드하는 중 예외 발생|버그|

## **공개 API 변경 사항**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **제거된 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **사용 예시:**
**PSDNET-184. JPEG, PNG 및 기타 이미지 파일을 스트림에서 PsdImage로 로드**

{{< highlight java >}}

    // JPEG, PNG 및 기타 이미지 파일을 스트림에서 PsdImage로 로드

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. 채우기 레이어 렌더링 구현: 그라데이션**

{{< highlight java >}}

             // 채우기 레이어 렌더링 구현: 그라데이션

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. PSD를 PDF로 저장할 때 선택 가능한 텍스트 제공 안 함**

{{< highlight java >}}

  // PSD를 PDF로 저장할 때 선택 가능한 텍스트 제공 안 함

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. 새로운 TextLayer를 생성한 후 PSD 파일이 PS에서 읽을 수 없음**

{{< highlight java >}}

 // 빌드 서버에서 새로운 TextLayer를 생성한 후 PSD 파일이 PS에서 읽을 수 없음

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}

**PSDNET-156. PSD를 로드하는 중 예외 발생**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. ReadOnly 모드로 PSD를 로드할 때 높은 메모리 사용량**

{{< highlight java >}}

 // ReadOnly 모드로 PSD를 로드할 때 Aspose.PSD의 높은 메모리 사용량

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // 이 예시는 메모리 사용량이 100MB 미만이어야 함

            if (memoryUsed > 100)

            {

                throw new Exception("메모리 사용량이 너무 큼");

            }

{{< /highlight >}}

**PSDNET-158. PSB를 PDF로 저장하는 것 지원**

{{< highlight java >}}

 // PSB를 PDF로 저장하는 것 지원

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

