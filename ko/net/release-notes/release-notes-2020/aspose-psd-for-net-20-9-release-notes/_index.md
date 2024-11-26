---
title: Aspose.PSD for .NET 20.9 - 릴리스 노트
type: docs
weight: 40
url: /ko/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키워드**|**요약**|**범주**|
| :- | :- | :- |
|PSDNET-408|SoLEResource (Smart Object Layer 외부 리소스) 지원|기능|
|PSDNET-614|연결된 스마트 오브젝트 지원|기능|
|PSDNET-615|포함된 스마트 오브젝트 지원|기능|
|PSDNET-690|제공된 PSD 파일에서 텍스트 업데이트 및 저장 시 일부 레이어 및 많은 텍스트 매개변수가 변경됩니다|버그|
|PSDNET-696|FillLayer가 생성 후 업데이트되지 않아 제대로 렌더링되지 않음|버그|
|PSDNET-712|특정 PSD 파일에서 TextLayer 크기 조정 시 위치 값이 손상됨|버그|
|PSDNET-714|특정 PSD 파일에서 TextLayer 크기 조정 시 위치 값이 손상됨|버그|

## **공용 API 변경사항**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
...
...

## **사용 예시:**
**PSDNET-408. SoLEResource (Smart Object Layer 외부 리소스) 지원**
{{< highlight csharp >}}
            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("예상된 true"));
                }
            }
...
...

**PSDNET-614. 연결된 스마트 오브젝트 지원**
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
                    string.Format("실제 값 {0}가 예상과 동일하지 않습니다.", actual, expected));
            }
        }
...
...
{{< /highlight >}}
**PSDNET-615. 포함된 스마트 오브젝트 지원**
{{< highlight csharp >}}
            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("실제 값 {0}가 예상과 동일하지 않습니다.", actual, expected));
                }
            }
...
...

**PSDNET-696. FillLayer가 생성 후 업데이트되지 않아 제대로 렌더링되지 않음**
{{< highlight csharp >}}
            string srcFile = "TestSimple.psd";
            string outputFile = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                for (int i = 0; i < image.Layers.Length; i++)
                {
                    var layer = image.Layers[i] as FillLayer;
                    if (layer != null)
                    {
                        layer.Update();
                    }
                }

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-712. Regression: Aspose.PSD 20.8.0 파일 열 수 없음**
{{< highlight csharp >}}
            string dataDir = "PSDNET712_1\\";
            string filePath = dataDir + "sample2.psd";
            using (var _ = (PsdImage)Image.Load(filePath))
            {
            }
{{< /highlight >}}
**PSDNET-714. 특정 PSD 파일에서 TextLayer 크기 조정 시 위치 값이 손상됨**
{{< highlight csharp >}}
            string srcFile = "A.psd";
            string outputFile = "output.psd";

            RectangleF oldBoxBounds = new RectangleF(16852.8613f, 16861.332f, 17.4458752f, 14.327f);
            RectangleF newBoxBounds = new RectangleF(PointF.Empty, oldBoxBounds.Size);

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                // 텍스트 상자 경계 값을 0 위치로 이동하여 수정합니다.
                textLayer.TextBoundBox = newBoxBounds;
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFile);
            }
{{< /highlight >}}**PSDNET-690. 제공된 PSD 파일에서 텍스트 업데이트 및 저장 시 레이어 및 많은 텍스트 매개변수가 변경됩니다**
{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(
                        string.Format("실제 값 {0}가 예상과 동일하지 않습니다.", actual, expected));
                }
            }

            string srcFile = "A.psd";
            string outputFile = "output.psd";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];
                textLayer.UpdateText("abc");

                psdImage.Save(outputFile);
            }

            // 값 확인
            using (var srcImage = (PsdImage)Image.Load(srcFile))
            {
                var srcTextLayer = (TextLayer)srcImage.Layers[1];
                var etalonStyle = srcTextLayer.TextData.Items[0].Style;

                using (var outImage = (PsdImage)Image.Load(outputFile))
                {
                    var outTextLayer = (TextLayer)outImage.Layers[1];
                    var resultStyle = outTextLayer.TextData.Items[0].Style;

                    AssertAreEqual(etalonStyle.AutoLeading, resultStyle.AutoLeading);
                    AssertAreEqual(etalonStyle.FontIndex, resultStyle.FontIndex);
                    AssertAreEqual(etalonStyle.Underline, resultStyle.Underline);
                    AssertAreEqual(etalonStyle.Strikethrough, resultStyle.Strikethrough);
                    AssertAreEqual(etalonStyle.AutoKerning, resultStyle.AutoKerning);
                    AssertAreEqual(etalonStyle.StandardLigatures, resultStyle.StandardLigatures);
                    AssertAreEqual(etalonStyle.DiscretionaryLigatures, resultStyle.DiscretionaryLigatures);
                    AssertAreEqual(etalonStyle.ContextualAlternates, resultStyle.ContextualAlternates);
                    AssertAreEqual(etalonStyle.LanguageIndex, resultStyle.LanguageIndex);
                    AssertAreEqual(etalonStyle.VerticalScale, resultStyle.VerticalScale);
                    AssertAreEqual(etalonStyle.HorizontalScale, resultStyle.HorizontalScale);
                    AssertAreEqual(etalonStyle.Fractions, resultStyle.Fractions);
                }
            }
{{< /highlight >}}
**PSDNET-696. FillLayer 생성 후 업데이트되지 않고 제대로 렌더링되지 않는 문제**
{{< highlight csharp >}}
            string srcFile = "TestSimple.psd";
            string outputFile = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                for (int i = 0; i < image.Layers.Length; i++)
                {
                    var layer = image.Layers[i] as FillLayer;
                    if (layer != null)
                    {
                        layer.Update();
                    }
                }

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-712. 회귀: Aspose.PSD 20.8.0 파일 열 수 없는 문제**
{{< highlight csharp >}}
            string dataDir = "PSDNET712_1\\";
            string filePath = dataDir + "sample2.psd";
            using (var _ = (PsdImage)Image.Load(filePath))
            {
            }
{{< /highlight >}}
**PSDNET-714. 특정 PSD 파일에서 TextLayer의 크기를 조정하면 위치 값이 손상되는 문제**
{{< highlight csharp >}}
            string srcFile = "A.psd";
            string outputFile = "output.psd";

            RectangleF oldBoxBounds = new RectangleF(16852.8613f, 16861.332f, 17.4458752f, 14.327f);
            RectangleF newBoxBounds = new RectangleF(PointF.Empty, oldBoxBounds.Size);

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                // 텍스트 상자 경계 값을 0 위치로 이동하여 수정합니다.
                textLayer.TextBoundBox = newBoxBounds;
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFile);
            }
{{< /highlight >}}