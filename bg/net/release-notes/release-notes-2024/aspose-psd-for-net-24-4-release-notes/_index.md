---
title: Aspose.PSD за .NET 24.4 - Бележки за изданието
type: docs
weight: 90
url: /bg/net/aspose-psd-za-net-24-4-belejki-za-izdanie/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Резюме**                                             | **Категория** |
|:------------|:-------------------------------------------------------|:-------------|
| PSDNET-1871 | Добавяне на обработка на ресурса XObjectForm [AI Format]  | Функционалност |
| PSDNET-1961 | Добавяне на конструктор за ShapeLayer                   | Функционалност |
| PSDNET-1879 | Оправяне на конвертирането на файл Psd от RGB към CMYK  | Проблем     |
| PSDNET-1966 | Специфичния PSD файл не може да се експортира с помощта на Aspose.PSD | Проблем     |

## **Промени в публичното API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Премахнати API:**
- None

## **Примери за използване:**

**PSDNET-1871. [AI Format] Добавяне на обработката на ресурса XObjectForm**

{{< highlight csharp >}}
string изходенФайл = Path.Combine(базовПапка, "пример.ai");
string файлЗаИзход = Path.Combine(папкаЗаИзход, "пример.png");

using (AiImage изображение = (AiImage)Image.Load(изходенФайл))
{
    изображение.Save(файлЗаИзход, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. Оправяне на конвертирането на Psd файл от RGB към CMYK**

{{< highlight csharp >}}
// Проверете, че psd файлът, конвертиран в CMYK + RLE 4 канала от psd файл в RGB + RLE 4 канала, наистина има 4 канала
// и HasTransparencyData == false.

string изходенФайл = Path.Combine(базовПапка, "frog_nosymb.psd");
string изходенФайлСменен = Path.Combine(папкаЗаИзход, "frog_nosymb_output.psd");

using (PsdImage psdИзображение = (PsdImage)Image.Load(изходенФайл))
{
    psdИзображение.HasTransparencyData = false;

    PsdOptions psdОпции = new PsdOptions(psdИзображение)
    {
        ColorMode = ColorModes.Cmyk,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
    };

    psdИзображение.Save(изходенФайлСменен, psdОпции);
}

using (PsdImage psdИзображение = (PsdImage)Image.Load(изходенФайлСменен))
{
    AssertAreEqual(false, psdИзображение.HasTransparencyData);
    AssertAreEqual((ushort)4, psdИзображение.Layers[0].ChannelsCount);
}

void AssertAreEqual(object очаквано, object фактическо, string съобщение = null)
{
    if (!object.Equals(очаквано, фактическо))
    {
        throw new Exception(съобщение ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}

**PSDNET-1961. Добавяне на конструктор за ShapeLayer**

{{< highlight csharp >}}
string изходенФайл = Path.Combine(папкаЗаИзход, "AddShapeLayer_output.psd");

const int ImgToPsdRatio = 256 * 65535;

using (PsdImage новPsd = new PsdImage(600, 400))
{
    ShapeLayer слой = новPsd.AddShapeLayer();

    var новФорма = GenerateNewShape(новPsd.Size);
    List<IPathShape> новиФорми = new List<IPathShape>();
    новиФорми.Add(новФорма);
    слой.Path.SetItems(новиФорми.ToArray());

    слой.Update();

    новPsd.Save(изходенФайл);
}

using (PsdImage изображение = (PsdImage)Image.Load(изходенФайл))
{
    AssertAreEqual(2, изображение.Layers.Length);

    ShapeLayer shapeLayer = изображение.Layers[1] as ShapeLayer;
    ColorFillSettings internalFill = shapeLayer.Fill as ColorFillSettings;
    IStrokeSettings strokeSettings = shapeLayer.Stroke;
    ColorFillSettings strokeFill = shapeLayer.Stroke.Fill as ColorFillSettings;

    AssertAreEqual(1, shapeLayer.Path.GetItems().Length); // 1 Форма
    AssertAreEqual(3, shapeLayer.Path.GetItems()[0].GetItems().Length); // 3 възела във формата

    AssertAreEqual(-16127182, internalFill.Color.ToArgb()); // ff09eb32

    AssertAreEqual(7.41, strokeSettings.Size);
    AssertAreEqual(false, strokeSettings.Enabled);
    AssertAreEqual(StrokePosition.Center, strokeSettings.LineAlignment);
    AssertAreEqual(LineCapType.ButtCap, strokeSettings.LineCap);
    AssertAreEqual(LineJoinType.MiterJoin, strokeSettings.LineJoin);
    AssertAreEqual(-16777216, strokeFill.Color.ToArgb()); // ff000000
}

PathShape GenerateNewShape(Size размерНаИзображението)
{
    var новФорма = new PathShape();

    PointF точка1 = new PointF(20, 100);
    PointF точка2 = new PointF(200, 100);
    PointF точка3 = new PointF(300, 10);

    BezierKnotRecord[] кривиКонтролниТочки = new BezierKnotRecord[]
    {
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(точка1, размерНаИзображението),
                          PointFToResourcePoint(точка1, размерНаИзображението),
                          PointFToResourcePoint(точка1, размерНаИзображението),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(точка2, размерНаИзображението),
                          PointFToResourcePoint(точка2, размерНаИзображението),
                          PointFToResourcePoint(точка2, размерНаИзображението),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(точка3, размерНаИзображението),
                          PointFToResourcePoint(точка3, размерНаНаИзображението),
                          PointFToResourcePoint(точка3, размерНаИзображението),
                      }
         },
    };

    новФорма.SetItems(кривиКонтролниТочки);

    return новФорма;
}

Point PointFToResourcePoint(PointF точка, Size размерНаИзображението)
{
    return new Point(
        (int)Math.Round(точка.Y * (ImgToPsdRatio / размерНаИзображението.Height)),
        (int)Math.Round(точка.X * (ImgToPsdRatio / размерНаИзображението.Width)));
}

void AssertAreEqual(object очаквано, object фактическо, string съобщение = null)
{
    if (!object.Equals(очаквано, фактическо))
    {
        throw new Exception(съобщение ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}

**PSDNET-1966. Специфичният PSD файл не може да се експортира с помощта на Aspose.PSD**

{{< highlight csharp >}}
string изходенФайл = Path.Combine(базовПапка, "1966изходен.psd");
string изходPng = Path.Combine(папкаЗаИзход, "изход.png");

using (var psdИзображение = (PsdImage)Image.Load(изходенФайл, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdИзображение.Save(изходPng, new PngOptions());
}
{{< /highlight >}}
