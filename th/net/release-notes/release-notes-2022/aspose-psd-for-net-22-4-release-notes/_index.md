---
title: บันทึกการเปลี่ยนแปลง Aspose.PSD สำหรับ .NET 22.4
type: docs
weight: 90
url: /th/net/aspose-psd-for-net-22-4-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการเปลี่ยนแปลงสำหรับ [Aspose.PSD สำหรับ .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-261|การเรนเดอร์เอฟเฟค Outer Glow Layer|คุณลักษณะ|
|PSDNET-1123|เพิ่มการสนับสนุนใบอนุญาต Sha256|พัฒนา|
|PSDNET-1107|การจัดตำแหน่งข้อความหลายบรรทัดไม่ตรงกับผลลัพธ์ใน Photoshop|บั๊ก|
|PSDNET-1113|ปัญหาในการโหลดไฟล์ PSD ในการวิเคราะห์ข้อมูลทรัพยากรข้อความ|บั๊ก|
|PSDNET-1129|ตำแหน่งไม่ถูกต้องของรูปแบบที่กำหนดเองหลังจากบันทึกเป็น PSD|บั๊ก|


## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Left
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Right
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Center
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Noise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsSoftBlend
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Range
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Jitter


# **API ที่ถูกลบออก:**
- None


## **ตัวอย่างการใช้:**

**PSDNET-261. การเรนเดอร์เอฟเฟค Outer Glow Layer**
{{< highlight csharp >}}
string src = "GreenLayer.psd";
string output = "output261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
    effect.Range = 10;
    effect.Spread = 10;
    ((IColorFillSettings)effect.FillColor).Color = Color.Red;
    effect.Opacity = 128;
    effect.BlendMode = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. การจัดตำแหน่งข้อความหลายบรรทัดไม่ตรงกับผลลัพธ์ใน Photoshop**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Text line1\rText line2\rText line3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Left;
   portions[1].Paragraph.Justification = JustificationMode.Right;
   portions[2].Paragraph.Justification = JustificationMode.Center;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1113. ปัญหาในการโหลดไฟล์ PSD ในการวิเคราะห์ข้อมูลทรัพยากรข้อความ**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // โหลดสำเร็จ
}
{{< /highlight >}}


**PSDNET-1129. ตำแหน่งไม่ถูกต้องของรูปแบบที่กำหนดเองหลังจากบันทึกเป็น PSD**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
