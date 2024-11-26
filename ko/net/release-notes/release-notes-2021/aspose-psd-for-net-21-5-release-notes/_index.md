---
title: Aspose.PSD for .NET 21.5 - 릴리스 노트
type: docs
weight: 80
url: /ko/net/aspose-psd-for-net-21-5-release-notes/
---

{{% alert color="primary" %}} 

이 페이지는 [Aspose.PSD for .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트를 포함하고 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-758|벡터 경로를 가진 모양 레이어의 크기 조정 지원|기능|
|PSDNET-862|레이어가 조정될 때 벡터 경로를 가진 모양 레이어의 크기 조정 지원|기능|
|PSDNET-578|중단된 텍스트 문자열|버그|

## **공개 API 변경**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-578. 중단된 텍스트 문자열**

{{< highlight csharp >}}
            string srcFile = "grinched-regular-font.psd";
            string output = "output_grinched-regular-font.psd.png";

            // 글꼴 경로 설정
            System.Collections.Generic.List<string> fonts = new System.Collections.Generic.List<string>();
            fonts.AddRange(FontSettings.GetDefaultFontsFolders());
            fonts.Add(@"Fonts\");
            FontSettings.SetFontsFolders(fonts.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. 벡터 경로를 가진 모양 레이어의 크기 조정 지원**

{{< highlight csharp >}}
            string sourceFileName = "vectorShapes.psd";
            string outputFileName = "out_vectorShapes.psd";
            string dataDir = "PSDNET758_1";
            string sourcePath = Path.Combine(dataDir, sourceFileName);
            string outputPath = Path.Combine(dataDir, outputFileName);
            using (var psdImage = (PsdImage)Image.Load(sourcePath))
            {
                foreach (var layer in psdImage.Layers)
                {
                    layer.Resize(layer.Width * 5 / 4, layer.Height / 2);
                }

                psdImage.Save(outputPath);
                psdImage.Save(Path.ChangeExtension(outputPath, ".png"), new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-862. 레이어가 조정될 때 벡터 경로를 가진 모양 레이어의 크기 조정 지원**

{{< highlight csharp >}}
            // 이 예제는 PSD 이미지에서 Vogk 및 벡터 경로 리소스를 가진 레이어 크기를 조정하는 방법을 보여줍니다
            float scaleX = 0.45f;
            float scaleY = 1.60f;
            string dataDir = "PSDNET862_1";
            string sourceFileName = Path.Combine(dataDir, "vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                for (int layerIndex = 1; layerIndex < image.Layers.Length; layerIndex++, scaleX += 0.25f, scaleY -= 0.25f)
                {
                    var layer = image.Layers[layerIndex];
                    var newWidth = (int)Math.Round(layer.Width * scaleX);
                    var newHeight = (int)Math.Round(layer.Height * scaleY);
                    layer.Resize(newWidth, newHeight);

                    Thread.CurrentThread.CurrentCulture = CultureInfo.CreateSpecificCulture("en-GB");
                    string outputName = string.Format("resized_{0}_{1}_{2}", layerIndex, scaleX, scaleY);
                    string outputPath = Path.Combine(dataDir, outputName + ".psd");
                    string outputPngPath = Path.Combine(dataDir, outputName + ".png");
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
