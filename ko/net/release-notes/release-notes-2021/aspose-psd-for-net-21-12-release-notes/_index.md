---
title: Aspose.PSD for .NET 21.12 - 릴리스 노트
type: docs
weight: 10
url: /ko/net/aspose-psd-for-net-21-12-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 21.12](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-997|폰트 제한을 프로그래밍적으로 추가|기능|
|PSDNET-785|Aspose.PSD 20.10: PSD 로드 실패|버그|
|PSDNET-812|PSD 로딩 시 ImageLoad 예외|버그|
|PSDNET-870|지원되지 않는 CompressionMethod를 사용한 PSD 레이어 로드 시 ImageLoad 예외|버그|
|PSDNET-918|Aspose.PSD 21.6: PSD 파일에 대한 Compression method가 지원되지 않음|버그|
|PSDNET-984|마스크가 있는 벡터 경로의 잘못된 저장|버그|
|PSDNET-1001|특정 파일의 TextPortion에 있는 잘못된 폰트|버그|
|PSDNET-1031|이미지 로딩 시 Compression method가 지원되지 않는 예외|버그|
|PSDNET-1033|특정 파일에 저장 시 범위 이탈|버그|
|PSDNET-1036|로드 파일 오류를 피하기 위한 PathStructure 지원 추가|버그|

## **공용 API 변경 사항**
# **추가된 API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Prefix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.StructureKey
- M:Aspose.PSD.FontSettings.SetAllowedFonts(System.String[])
- M:Aspose.PSD.FontSettings.IsFontAllowed(System.String)
- M:Aspose.PSD.FontSettings.GetReplacementFont(System.String)
- M:Aspose.PSD.FontSettings.GetFontReplacements(System.String)
- M:Aspose.PSD.FontSettings.SetFontReplacements(System.String,System.String[])
- M:Aspose.PSD.FontSettings.ClearFontReplacements

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-785. Aspose.PSD 20.10: PSD 로드 실패**

{{< highlight csharp >}}
            string src = "ShimadzuLetterhead100.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src, new PsdLoadOptions() { ReadOnlyMode = true }))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-812. PSD 로딩 시 ImageLoad 예외**

{{< highlight csharp >}}
            string src = "5-MX10600_Amazon_DEVICES_2_1000x1000.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-870. 지원되지 않는 CompressionMethod를 사용한 PSD 레이어 로드 시 ImageLoad 예외**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-918. Aspose.PSD 21.6: PSD 파일에 대한 Compression method가 지원되지 않음**

{{< highlight csharp >}}
            string srcFile = "Fb-blue-jury (1).psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-984. 마스크가 있는 벡터 경로의 잘못된 저장**

{{< highlight csharp >}}
            string srcFile = "PsdConvertToPngExample.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                psdImage.Save(
                    outputFilePng,
                    new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha, Progressive = true, CompressionLevel = 9 });
            }
{{< /highlight >}}

**PSDNET-997. 폰트 제한을 프로그래밍적으로 추가**

{{< highlight csharp >}}
            string srcFile = "fonts_com_updated.psd";
            string output = "etalon_fonts_com_updated.psd.png";

            try
            {
                var fontList = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                FontSettings.SetAllowedFonts(fontList);

                var myriadReplacement = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                var calibriReplacement = new string[] { "Webdings", "Courier New", "Bookman Old Style" };
                var arialReplacement = new string[] { "Bookman Old Style", "Courier New", "Webdings" };
                var timesReplacement = new string[] { "Arial", "NotExistedFont", "Courier New" };

                FontSettings.SetFontReplacements("MyriadPro-Regular", myriadReplacement);
                FontSettings.SetFontReplacements("Calibri", calibriReplacement);
                FontSettings.SetFontReplacements("Arial", arialReplacement);
                FontSettings.SetFontReplacements("Times New Roman", timesReplacement);

                using (PsdImage image = (PsdImage)Image.Load(srcFile))
                {
                    image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            } 
            finally
            {
                FontSettings.SetAllowedFonts(null);
                FontSettings.ClearFontReplacements();
            }
{{< /highlight >}}

**PSDNET-1001. 특정 파일의 TextPortion에 있는 잘못된 폰트**

{{< highlight csharp >}}
            string srcFile = "fonts_com.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                var tl = (TextLayer)image.Layers[1];
                var fontName = tl.TextData.Items[0].Style.FontName;
                if (fontName != "MyriadPro-Regular")
                {
                    throw new Exception("Incorrect font");
                }

                // 예상되는 Myriad Pro를 얻어야 하지만 AdobeInvisFont를 확인함
                image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1031. 이미지 로딩 시 Compression method가 지원되지 않는 예외**

{{< highlight csharp >}}
            string srcFile = "shirt-error.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-1033. 특정 파일에 저장 시 범위 이탈**

{{< highlight csharp >}}
            string srcFile = "237708.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1036. 로드 파일 오류를 피하기 위한 PathStructure 지원 추가**

{{< highlight csharp >}}
            string srcFile = "shirt-color.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}
