---
title: Aspose.PSD for .NET 18.10 - 릴리즈 노트
type: docs
weight: 30
url: /ko/net/aspose-psd-for-net-18-10-release-notes/
---

|**키**|**개요**|**카테고리**|
| :- | :- | :- |
|PSDNET-14|일반 이외의 블렌드 모드 지원 추가|기능|
|PSDNET-69|색 오버레이 효과 지원 추가|기능|
|PSDNET-70|그림자 효과 지원 추가|기능|
|PSDNET-71|색 오버레이 효과 내보내기용 랜더링|기능|
|PSDNET-72|그림자 효과 내보내기용 랜더링|기능|
|PSDNET-74|실행 시 레이어 효과 추가 지원|기능|
|PSDNET-73|osTypeStructures를 포함하는 리소스의 로딩 성능 최적화|버그|
|PSDNET-79|LayerAndMaskInfo에서의 리팩터링 및 메모리 누수 수정|향상|

## **사용 예시:**
**PSDNET-14 일반 이외의 블렌드 모드 지원 추가**

{{< highlight java >}}

 var files = new string[]

{

    "일반",

    "해산",

    "어둠",

    "곱하기",

    "색 태우기",

    "선형 홍보",

    "어둡게 한 색상",

    "밝게 하기",

    "화면",

    "색상 홍보",

    "선형 홍보 추가",

    "색상 밝게하기",

    "오버레이",

    "부드러운 빛",

    "강한 빛",

    "선명한 빛",

    "선형 빛",

    "핀 빛",

    "합성",

    "차이",

    "제외",

    "뺄셈",

    "나누기",

    "색조",

    "채도",

    "색깔",

    "밝기",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // PNG로 내보내기

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "블랜드모드" + fileName + "_테스트100.png";

        im.Save(pngExportPath100, saveOptions);

        // 불투명도 50%로 설정

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "블랜드모드" + fileName + "_테스트50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 색 오버레이 효과 지원 추가**

{{< highlight java >}}

     // 색 오버레이 효과 편집

    string sourceFileName = "ColorOverlay.psd";

    string psdPathAfterChange = "ColorOverlayChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlay)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       colorOverlay.Color = Color.Green;

       colorOverlay.Opacity = 128;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}

**PSDNET-70 그림자 효과 지원 추가**

{{< highlight java >}}

     // 그림자 효과 편집

    string sourceFileName = "그림자.psd";

    string psdPathAfterChange = "그림자변경됨.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       shadowEffect.Color = Color.Green;

       shadowEffect.Opacity = 128;

       shadowEffect.Distance = 11;

       shadowEffect.UseGlobalLight = false;

       shadowEffect.Size = 9;

       shadowEffect.Angle = 45;

       shadowEffect.Spread = 3;

       shadowEffect.Noise = 50;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}



**PSDNET-71 색 오버레이 효과 내보내기용 랜더링**

{{< highlight java >}}

    // 색 오버레이 효과 편집

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // PNG로 내보내기

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 그림자 효과 내보내기용 랜더링**

{{< highlight java >}}

     // 그림자 내보내기

    string sourceFileName = "Shadow.psd";

    string pngExportPath = "Shadow.png";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       // PNG로 내보내기

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 실행 시 레이어 효과 추가 지원**

{{< highlight java >}}

     // 런타임에서 색 오버레이 레이어 효과 추가

    string sourceFileName = "레이어효과있는3개의일반레이어.psd";

    string psdExportPath = "레이어효과있는3개의일반레이어변경됨.psd";

    string pngExportPath = "레이어효과있는3개의일반레이어변경됨.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };



    var testFolder = string.Empty;

    var im = (PsdImage)Image.Load(testPath, loadOptions) 

    using (im)

    {

        var effect = im.Layers[1].BlendingOptions.AddColorOverlay();

        effect.Opacity = 128;

        effect.Color = Color.Green;

        effect.BlendMode = BlendMode.Normal;

        var effect = im.Layers[1].BlendingOptions.AddDropShadow();

        effect.Color = Color.Red;

        effect.Opacity = 128;

        effect.BlendMode = BlendMode.Normal;



        // PSD로 저장    

        im.Save(psdExportPath);



        // PNG로 저장

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

