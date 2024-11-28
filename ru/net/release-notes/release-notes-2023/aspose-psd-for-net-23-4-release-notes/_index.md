---
title: Aspose.PSD для .NET 23.4 - Примечания к выпуску
type: docs
weight: 90
url: /ru/net/aspose-psd-dlya-net-23-4-primetniya-k-vypusku/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к [Aspose.PSD для .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-1409|Разработка класса RawColor для использования в общедоступном API в PSD API вместо устаревшей структуры Color|Улучшение|
|PSDNET-1332|Интеграция слоя коррекции градиента карты из Отсроченного испытания в основной код Aspose.PSD|Функция|
|PSDNET-1448|Редактирование текста с использованием частей текста не сохраняет правильный результат|Ошибка|
|PSDNET-1449|Начало и конец стилей или абзацев появляются в неправильном месте при редактировании текстового слоя с помощью ITextPortion|Ошибка|
|PSDNET-1509|Изменение форматирования при редактировании в Photoshop|Ошибка|

## **Изменения в публичном API**
# **Добавленные API:**
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
...
...

**PSDNET-1449. Начало и конец стилей или абзацев появляются в неправильном месте при редактировании текстового слоя с помощью ITextPortion**

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

        //Поиск текста "lsak"
        if (!layerTLToUpdateText.Text.Contains("lsak") ||
            !layerTLToUpdateText.TextData.Text.Contains("lsak"))
        {
            continue;
        }

        var textDataTL = layerTLToUpdateText.TextData;

        //Шаг: Замена текста
        ReplaceLsakFourthMethod(textDataTL);

        System.Console.WriteLine("Замененный текст " + textDataTL.Text);

        //Шаг: Форматирование текста
        FormatLsakFourthMethod(textDataTL);

        System.Console.WriteLine("Отформатированный текст " + textDataTL.Text);

        //Шаг: Центрирование текстового слоя
        if (layerTLToUpdateText.DisplayName.Equals("cc") ||
            layerTLToUpdateText.DisplayName.Equals("tl") ||
            layerTLToUpdateText.DisplayName.Equals("cl"))
        {
...
...
...
{{< /highlight >}}