---
title: Aspose.PSD за .NET 23.4 - Бележки за изданието
type: docs
weight: 90
url: /bg/net/aspose-psd-za-net-23-4-belezhki-za-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-1409|Проектиране на RawColor класа за публичното API, за да се използва в PSD API вместо застарялата Color структура|Подобрение|
|PSDNET-1332|Интегриране на слоя за настройка на картата на градиента от Пробация до основния код на Aspose.PSD|Функционалност|
|PSDNET-1448|Редактирането на текст, използвайки порции текст, не запазва правилния резултат|Проблем|
|PSDNET-1449|Началото и краят на стиловете или параграфите се появяват на неправилното място при редактиране на текстов слой чрез ITextPortion|Проблем|
|PSDNET-1509|Форматирането се премества при редактиране в Photoshop|Проблем|


## Промени в публичното API
# **Добавени API:**
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


# **Премахнати API:**
- Нито едно


## **Примери за използване:**

**PSDNET-1332. Интеграция на слоя за настройка на картата на градиента от Пробация в основния код на Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // проверка на текущите стойности
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);

    grdmResource.Reverse = true;
    // Червен цвят за втората точка за цвят на градиента
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // проверка