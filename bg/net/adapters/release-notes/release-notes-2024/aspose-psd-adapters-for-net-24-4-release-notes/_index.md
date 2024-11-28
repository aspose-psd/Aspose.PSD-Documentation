---
title: Aspose.PSD Адаптери за .NET 24.4 - Бележки за изданието
type: docs
weight: 100
url: /bg/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD Адаптери за .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Ключ**    | **Резюме**                                                          | **Категория** |
|:-----------|:------------------------------------------------------------------|:------------|
| PSDNET-1985 | Пускане за пръв път на Aspose.PSD.Adapters.Imaging в Nuget        | Подобрение |


## **Промени в публичния API**
# **Добавени API:** 
- Няма

# **Премахнати API:** 
- Няма

## **Примери за използване:**

Моля, проверете [страницата с документация на Aspose.PSD.Adapters](/psd/bg/net/adapters)

**PSDNET-1985. Най-пълен пример за използване на Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Добавяне на възможност за адаптери във вашата конфигурация за инициализиране 
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// допълнително разрешаване на износители
Aspose.PSD.Adapters.Imaging.EnableExporters();

// За да работите с адаптери, ви трябват лицензи както на Aspose.PSD, така и на адаптираната програма
// Ето как да приложите лиценза на Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Ето пример как да приложите лиценз на адаптирования продукт за Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// След това можете да изпълните код на адаптерите или библиотеката PSD или Imaging

// След това всички тези файлове могат да бъдат отворени от Aspose.PSD без допълнителен код, само използвайте
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // След изпълнението на този код ще получите създадения PSD файл от WEBP и можете да приложите всички филтри, слоеве и настройки на Aspose.PSD, включително Преобразуване на изкривяване
}

// Можете допълнително да създавате изображения от адаптираните износители във формат PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Използвайте Aspose.Imaging API за редактиране на WEBP файл с функции, специфични за Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // След това просто използвайте метода ToPsdImage() и редактирайте файл като PSD със функции, подобни на Photoshop, включително слоеве, умни филтри и умни обекти.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Някой текст", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Запаметете окончателния PSD файл, използвайки Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Ако не ви трябват Зареждащите и Износителните функции, предоставени от адаптерите, просто ги деактивирайте
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
