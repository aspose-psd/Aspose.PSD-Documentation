---
title: Aspose.PSD for .NET 21.9 - 릴리스 노트
type: docs
weight: 40
url: /ko/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-574|PSD 저장 시 거대한 출력 PSD를 피하기 위해 RLE 압축을 기본으로 설정|기능|
|PSDNET-747|PSD 파일의 다중채널 색상 모드에서 오버레이 패턴 레이어 효과 지원|기능|
|PSDNET-951|새 레이어를 생성한 후 해당 리소스 속성이 null이므로 조작을 방해하는 버그(예: 조정) 수정 필요|버그|
|PSDNET-955|8비트에 대한 ZipWithPrediction 압축 방법의 지원되지 않는 버그 수정 필요|버그|

## **공용 API 변경점**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예제:**

**PSDNET-574. PSD 저장 시 거대한 출력 PSD를 피하기 위해 RLE 압축을 기본으로 설정**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. PSD 파일의 다중채널 색상 모드에서 오버레이 패턴 레이어 효과 지원**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // 예외가 발생하지 않아야 함
            using (var im = Image.Load(fileName, loadOptions))
            {
                // 예외가 발생하지 않아야 함
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. 새 레이어를 생성한 후 해당 리소스 속성이 null이므로 조작을 방해하는 버그(예: 조정) 수정 필요**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // 빨간색
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // 녹색
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // 파란색
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                ...
            }
{{< /highlight >}}

**PSDNET-955. 8비트에 대한 ZipWithPrediction 압축 방법의 지원되지 않는 버그 수정 필요**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                ...
            }
{{< /highlight >}}
