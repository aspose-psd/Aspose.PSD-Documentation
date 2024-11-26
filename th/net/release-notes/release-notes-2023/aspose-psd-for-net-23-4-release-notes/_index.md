---
title: Aspose.PSD for .NET 23.4 - บันทึกการอัปเดต
type: docs
weight: 90
url: /th/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-1409|ออกแบบคลาส RawColor สำหรับ API สาธารณะเพื่อใช้ใน PSD API แทน Color struct ที่ล้าสมัย|การปรับปรุง|
|PSDNET-1332|ผสานระดับความชัดของแผนที่การปรับแต่งแบบ Gradient Map จากการทดสอบเข้ากับโค้ดหลักของ Aspose.PSD|คุณลักษณะ|
|PSDNET-1448|การแก้ไขข้อความโดยใช้ Text Portions ไม่บันทึกผลลัพธ์ที่ถูกต้อง|บั๊ก|
|PSDNET-1449|จุดเริ่มต้นและสิ้นสุดของสไตล์หรือย่อหน้าปรากฏในตำแหน่งไม่ถูกต้องเมื่อแก้ไข Text Layer โดย ITextPortion|บั๊ก|
|PSDNET-1509|การจัดรูปแบบเมื่อแก้ไขใน Photoshop|บั๊ก|


## **การเปลี่ยนแปลงใน Public API**
# **เพิ่ม APIs:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor


# **API ที่ถูกลบออก:**
- None


## **ตัวอย่างการใช้:**

**PSDNET-1332. ผสานระดับความชัดของแผนที่การปรับแต่งแบบ Gradient Map จากการทดสอบเข้ากับโค้ดหลักของ Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // ตรวจสอบค่าปัจจุบัน
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);

    grdmResource.Reverse = true;
    // สีแดงสำหรับจุดสีโทนที่สอง
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // ตรวจสอบค่าที่เปลี่ยนแล้ว
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1409. ออกแบบคลาส RawColor สำหรับ API สาธารณะเพื่อใช้ใน PSD API แทน Color struct ที่ล้าสมัย**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}

var color = new RawColor(PixelDataFormat.Rgba32Bpp);
var oldColor = Color.FromArgb(5, 1, 2, 3);

var argbValue = oldColor.ToArgb();
color.SetAsInt(argbValue);

AssertAreEqual("ARGB", color.GetColorModeName());
AssertAreEqual(32, color.GetBitDepth());
AssertAreEqual("A Alpha", color.Components[0].FullName);
AssertAreEqual(5, (int)color.Components[0].Value);
AssertAreEqual("R Red", color.Components[1].FullName);
AssertAreEqual(1, (int)color.Components[1].Value);
AssertAreEqual("G Green", color.Components[2].FullName);
AssertAreEqual(2, (int)color.Components[2].Value);
AssertAreEqual("B Blue", color.Components[3].FullName);
AssertAreEqual(3, (int)color.Components[3].Value);

AssertAreEqual(argbValue, color.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. การแก้ไขข้อความโดยใช้ Text Portions ไม่บันทึกผลลัพธ์ที่ถูกต้อง**

{{< highlight csharp >}}
string sourceFile = "originalv5.psd";
string psdExportPath = "export.psd";

using (var imageTestEmail = (PsdImage)Image.Load(sourceFile))
{
    var layers = imageTestEmail.Layers;
    foreach (var layerItem in layers)
    {
        var isTextLayer = layerItem.GetType() == typeof(TextLayer) ? true : false;
        if (isTextLayer)
        {
            var layerTLToUpdateText = (TextLayer)layerItem;

            // ค้นหาข้อความ lsak
            if (layerTLToUpdateText.Text.Contains("lsak"))
            {
                var textDataTL = layerTLToUpdateText.TextData;

                if (textDataTL.Text.Contains("lsak") && textDataTL.Text.Contains("\r"))
                {
                    // แทนที่ข้อความ
                    replaceLsakText(textDataTL);
                    // จัดรูปแบบข้อความ
                    formatStyleText(textDataTL);
                }
            }
        }
    }

    imageTestEmail.Save(psdExportPath, new PsdOptions());
}

string[] texts = new string[]
{
    "Power play.",
    "//Πιο επεκτατικοί κόσμοι. Γρήγοροι χρόνοι φόρτωสีกว้าง. คอมพิวเตอร์ที่ใช้ระบบปฏิบัติการ Windows เสมอจะเป็นแพลตฟอรัง/เกม—และใน Windows 11, มันกลายเป็นดีไ/่ง/ี้ขึ้น/"
};

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(psdExportPath))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 9500; i < bytes.Length; i++)
    {
        if ((char)bytes[i] == '\0')
        {
            txt2Data += "0";
        }
        else
        {
            txt2Data += (char)bytes[i];
        }
    }

    string key0 = @" >> /1 " + texts[0].Length + " >>";       // เติมคำนำหน้าให้กับความยาวของข้อความแรก
    string key1 = @" >> /1 " + texts[1].Length + " >>";       // เติมคำนำหน้าให้กับความยาวของข้อความที่สอง

    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    if (index0 < 0)
    {
        throw new Exception("ค้นหาความยาวของสไตล์ข้อความแรกไม่พบ ต้องเท่ากับ " + texts[0].Length);
    }

    if (index1 < 0)
    {
        throw new Exception("ค้นหาความยาวของสไตล์ข้อความที่สองไม่พบ ต้องเท่ากับ " + texts[1].Length); ;
    }
}
{{< /highlight >}}

**PSDNET-1449. จุดเริ่มต้นและสิ้นสุดของสไตล์หรือย่อหน้าปรากฏในตำแหน่งไม่ถูกต้องเมื่อแก้ไข Text Layer โดย ITextPortion**

{{< highlight csharp >}}
string sourceFilePSDEmail = "inputv2.psd";
string outputFile = "export.psd";

using (PsdImage imageTestEmail = (PsdImage)Aspose.PSD.Image.Load(sourceFilePSDEmail))
{
    var layers = imageTestEmail.Layers;

    foreach (var layerItem in layers)
    {
        var layerTLToUpdateText = layerItem as TextLayer;

        if (layerTLToUpdateText == null)
        {
            continue;
        }

        //Buscar lsak text
        if (!layerTLToUpdateText.Text.Contains("lsak") ||
            !layerTLToUpdateText.TextData.Text.Contains("lsak"))
        {
            continue;
        }

        var textDataTL = layerTLToUpdateText.TextData;

        //Step: Replace text
        ReplaceLsakFourthMethod(textDataTL);

        System.Console.WriteLine("Replaced text " + textDataTL.Text);

        //Step: Format text
        FormatLsakFourthMethod(textDataTL);

        System.Console.WriteLine("Formated text " + textDataTL.Text);

        //Step: Center textlayer
        if (layerTLToUpdateText.DisplayName.Equals("cc") ||
            layerTLToUpdateText.DisplayName.Equals("tl") ||
            layerTLToUpdateText.DisplayName.Equals("cl"))
        {
            //old Values
            var boundBoxOld = layerTLToUpdateText.TextBoundBox;
            var OldY = layerTLToUpdateText.Top;

            textDataTL.UpdateLayerData();

            // new values
            var wordSize = layerTLToUpdateText.Size;
            var newSize = new Aspose.PSD.Size((int)Math.Ceiling(boundBoxOld.Width), wordSize.Height);
            var beforePoint = CenterInRectangle(wordSize,
                new Aspose.PSD.RectangleF(layerTLToUpdateText.Left, layerTLToUpdateText.Top,
                    layerTLToUpdateText.Width, boundBoxOld.Height));

            layerTLToUpdateText.TextBoundBox =
                new Aspose.PSD.RectangleF(new Aspose.PSD.PointF(0, beforePoint.Y - OldY),
                    newSize);

            var newPoint = CenterInRectangle(wordSize,
                new Aspose.PSD.RectangleF(layerTLToUpdateText.Left, layerTLToUpdateText.Top,
                    layerTLToUpdateText.Width, boundBoxOld.Height));

            layerTLToUpdateText.Left = (int)newPoint.X;
            layerTLToUpdateText.Top = (int)newPoint.Y;

            textDataTL.UpdateLayerData();

            System.Console.WriteLine("Center text");
        }
    }

    imageTestEmail.Save(outputFile);
}

Aspose.PSD.PointF CenterInRectangle(Aspose.PSD.Size Inner, Aspose.PSD.RectangleF Outer)
{
    return new Aspose.PSD.PointF()
    {
        X = (Outer.X + (Outer.Width - Inner.Width) / 2),
        Y = (Outer.Y + (Outer.Height - Inner.Height) / 2)
    };
}

void ReplaceLsakFourthMethod(IText textData)
{
    //validar si tiene tags

    var countPortions = textData.Items.Length;
    ITextStyle defaultStyle = textData.Items[0].Style;
    ITextParagraph defaultParagraph =