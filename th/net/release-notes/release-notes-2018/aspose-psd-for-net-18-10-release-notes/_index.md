---
title: บันทึกการออก Aspose.PSD for .NET 18.10
type: docs
weight: 30
url: /th/net/aspose-psd-for-net-18-10-release-notes/
---

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-14|เพิ่มการสนับสนุนของโหมดผสมนอกเหนือจาก Normal|คุณลักษณะ|
|PSDNET-69|เพิ่มการสนับสนุนของเอฟเฟกต์ Color Overlay|คุณลักษณะ|
|PSDNET-70|เพิ่มการสนับสนุนของเอฟเฟกต์ Drop Shadow|คุณลักษณะ|
|PSDNET-71|การเรนเดอร์สำหรับส่งออกเอฟเฟกต์ Color Overlay|คุณลักษณะ|
|PSDNET-72|การเรนเดอร์สำหรับส่งออกเอฟเฟกต์ Drop Shadow|คุณลักษณะ|
|PSDNET-74|การสนับสนุนการเพิ่มเอฟเฟกต์เลเยอร์ในเวลาการทำงาน|คุณลักษณะ|
|PSDNET-73|การปรับปรุงประสิทธิภาพการโหลดของทรัพยากรที่มีโครงสร้าง osTypeStructure|จุดบกพร่อง|
|PSDNET-79|การจัดระเบียบโค้ดใหม่และแก้ไขรั่วของหน่วยข้อมูลเลเยอร์และมาสก์|การปรับปรุง|

## **ตัวอย่างการใช้:**
**PSDNET-14 เพิ่มการสนับสนุนของโหมดผสมนอกเหนือจาก Normal**

{{< highlight java >}}

 var files = new string[]

{

    "Normal",

    "Dissolve",

    "Darken",

    "Multiply",

    "ColorBurn",

    "LinearBurn",

    "DarkerColor",

    "Lighten",

    "Screen",

    "ColorDodge",

    "LinearDodgeAdd",

    "LightenColor",

    "Overlay",

    "SoftLight",

    "HardLight",

    "VividLight",

    "LinearLight",

    "PinLight",

    "HardMix",

    "Difference",

    "Exclusion",

    "Subtract",

    "Divide",

    "Hue",

    "Saturation",

    "Color",

    "Luminosity",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // ส่งออกเป็น PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // ตั้งค่าความทึบ 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 เพิ่มการสนับสนุนของเอฟเฟกต์ Color Overlay**

{{< highlight java >}}

     // แก้ไขเอฟเฟกต์ ColorOverlay

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

**PSDNET-70 เพิ่มการสนับสนุนของเอฟเฟกต์ Drop Shadow**

{{< highlight java >}}

     // แก้ไขเอฟเฟกต์ DropShadow

    string sourceFileName = "Shadow.psd";

    string psdPathAfterChange = "ShadowChanged.psd";

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

**PSDNET-71 การเรนเดอร์สำหรับส่งออกเอฟเฟกต์ Color Overlay**

{{< highlight java >}}

    // แก้ไขเอฟเฟกต์ Color Overlay

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // บันทึก PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 การเรนเดอร์สำหรับส่งออกเอฟเฟกต์ Drop Shadow**

{{< highlight java >}}

     // ส่งออก DropShadow

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

       // บันทึก PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 การสนับสนุนการเพิ่มเอฟเฟกต์เลเยอร์ในเวลาการทำงาน**

{{< highlight java >}}

     // เพิ่มเอฟเฟกต์เลเยอร์ Color Overlay ในเวลาการทำงาน

    string sourceFileName = "ThreeRegularLayersWithLayerEffect.psd";

    string psdExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    string pngExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

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



        // บันทึก PSD    

        im.Save(psdExportPath);



        // บันทึก PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

