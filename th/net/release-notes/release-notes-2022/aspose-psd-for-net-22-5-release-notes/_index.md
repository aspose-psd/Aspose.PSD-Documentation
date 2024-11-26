---
title: หมายเหตุการปล่อย Aspose.PSD สำหรับ .NET 22.5
type: เอกสาร
weight: 80
url: /th/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีหมายเหตุการปล่อยสำหรับ [Aspose.PSD สำหรับ .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-952|เพิ่มคุณสมบัติ EffectType ใน ILayerEffect Interface|คุณลักษณะ|
|PSDNET-1146|การ Refactoring ของคลาส ChannelData|พัฒนา|
|PSDNET-657|ทำให้คุณสมบัติการทำงานของ Opacity สำหรับ DropShadowEffect|บั๊ก|
|PSDNET-825|การวาดรูปอย่างไม่ถูกต้องของชั้นปรับเข้าร่างผ่านชั้นเรียบๆ ในกรณีเฉพาะ|บั๊ก|
|PSDNET-1168|ปรับปรุงเมธอด Colorize โดย Colorize เทา + ตั้งค่าสีที่ถูกต้องเมื่อความอิ่มสีไม่ได้เป็น 100|บั๊ก|
|บทความ|[วิธีการทำงาน Aspose.PSD ใน Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|เอกสาร|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor(Aspose.PSD.FileFormats.Psd.CompressionMethod,System.Int32,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ILayerEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.DropShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EffectType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.DropShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.OuterGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.PatternOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.GradientOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.ColorOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Satin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Stroke
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.BevelEmboss

# **API ที่ถูกลบ:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)

## **ตัวอย่างการใช้:**

**PSDNET-657. ทำให้คุณสมบัติ Opacity ทำงานสำหรับ DropShadowEffect**

{{< highlight csharp >}}
string inputFile = "input.psd";
string outputImage20 = "outputImage20.png";
string outputImage200 = "outputImage200.png";

using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    Layer workLayer = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;

    // ตัวอย่างที่มี Opacity = 20
    dropShadowEffect.Opacity = 20;
    psdImage.Save(outputImage20, new PngOptions());

    // ตัวอย่างที่มี Opacity = 200
    dropShadowEffect.Opacity = 200;
    psdImage.Save(outputImage200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. การวาดรูปอย่างไม่ถูกต้องของชั้นปรับเข้าร่างผ่านชั้นเรียบๆ ในกรณีเฉพาะ**

{{< highlight csharp >}}
string sourceFile = "input_825.psd";
string outputPng = "out_psdnet825.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    foreach (var item in psdImage.Layers)
    {
        item.IsVisible = false;
    }
    var layer = psdImage.Layers[3];
    psdImage.Layers[1].IsVisible = true;
    psdImage.Layers[3].IsVisible = true;
    psdImage.Layers[4].IsVisible = true;
    psdImage.Layers[7].IsVisible = true;

    var width = layer.Width;
    var height = layer.Height;
    var layerBounds = new Rectangle(layer.Left, layer.Top, width, height);
    var bounds = new Rectangle(0, 0, width, height);
    var image = new PsdImage(bounds.Width, bounds.Height);

    image.SaveArgb32Pixels(bounds, psdImage.LoadArgb32Pixels(layerBounds));

    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. เพิ่มคุณสมบัติ EffectType ใน ILayerEffect Interface**

{{< highlight csharp >}}
string inputFile = "input.psd";
string outputWithout = "outputWithout.png";
string outputWith = "outputWith.png";

using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    psdImage.Save(outputWithout, new PngOptions());

    Layer workLayer = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;
    dropShadowEffect.Opacity = 20;

    foreach (ILayerEffect iEffect in workLayer.BlendingOptions.Effects)
    {
        if (iEffect.EffectType == LayerEffectsTypes.DropShadow)
        {
            // มันถูกจับ
            psdImage.Save(outputWith, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. ปรับปรุงเมธอด Colorize. Colorize เทา + ตั้งค่าสีที่ถูกต้องเมื่อความอิ่มสีไม่ได้เป็น 100**

{{< highlight csharp >}}
string srcFile = "Colorize.psd";            
string outputSimple = "output_simple.png";
string outputColorize = "output_colorize.png";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    // รูปภาพโดยไม่มี Colorize property
    psdImage.Save(outputSimple, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // ตั้งค่า Colorize property
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)layer;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // รูปภาพที่มี Colorize property
    psdImage.Save(outputColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
