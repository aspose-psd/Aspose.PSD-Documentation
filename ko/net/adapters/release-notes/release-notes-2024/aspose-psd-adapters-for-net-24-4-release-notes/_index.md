---
title: Aspose.PSD .NET용 어댑터 24.4 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD .NET용 어댑터 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키 값**    | **요약**                                                            | **카테고리** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Aspose.PSD.Adapters.Imaging의 Nuget에 대한 첫 출시                     | 향상        |


## **공개 API 변경 사항**
# **추가된 APIs:**
- 없음

# **제거된 APIs:**
- 없음

## **사용 예시:**

[Aspose.PSD.Adapters 문서 페이지](/psd/ko/net/adapters)를 확인하세요

**PSDNET-1985. Aspose.PSD.Adapters 사용 예시**

{{< highlight csharp >}}
// 초기화 구성에서 어댑터 활성화 추가
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// 추가로 Exporters 활성화
Aspose.PSD.Adapters.Imaging.EnableExporters();

// 어댑터를 사용하려면 Aspose.PSD 및 adaptee Licenses가 필요합니다
// Aspose.PSD License 적용 방법
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Aspose.Imaging의 Adaptee License를 적용하는 예시
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// 그런 다음, Adapters나 PSD 또는 Imaging 라이브러리의 모든 코드를 실행할 수 있습니다

// 이후 모든 이 파일들은 어떠한 추가 코드 없이도 Aspose.PSD를 사용하여 열 수 있습니다
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // 이 코드 실행 이후, 웹피에서 생성된 PSD 파일을 얻을 수 있으며, Aspose.PSD 필터, 레이어 및 변형을 포함한 다양한 Aspose.PSD 기능을 적용할 수 있습니다
}

// 또한 Export Adaptee 이미지를 PSD 형식으로 만들 수 있습니다
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Aspose.Imaging API를 사용하여 웹피 파일을 Imaging 특화 기능을 사용하여 편집할 수 있습니다
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // 그런 다음, ToPsdImage() 메서드를 사용하여 PSD와 유사한 기능을 갖는 Photoshop 기능을 포함한 이미지를 편집할 수 있습니다
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Aspose.PSD를 사용하여 최종 PSD 파일 저장
        psdImage.Save("output.psd");
    }
}

// 어댑터가 제공하는 Loaders나 Exporters를 사용하지 않을 경우 비활성화
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
