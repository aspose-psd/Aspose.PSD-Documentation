---
title: Aspose.PSD Адаптеры для .NET 24.4 - Примечания к выпуску
type: документация
weight: 100
url: /ru/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к версии [Aspose.PSD Адаптеров для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Key**     | **Summary**                                                          | **Category** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Начальная публикация Aspose.PSD.Adapters.Imaging в Nuget            | Улучшение |


## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**

Пожалуйста, проверьте [страницу документации Aspose.PSD.Adapters](/ru/psd/net/adapters)

**PSDNET-1985. Самый полный пример использования Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Добавьте активацию адаптеров в свою конфигурацию инициализации
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// дополнительно активировать Экспортеры
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Для работы с адаптерами вам нужны лицензии как Aspose.PSD, так и адаптируемого продукта
// Вот как применить лицензию Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Вот пример применения лицензии Adaptee для Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Затем вы можете запускать любой код адаптеров или библиотеки PSD или Imaging

// После этого все эти файлы можно открывать с помощью Aspose.PSD без какого-либо дополнительного кода, просто используйте
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // После выполнения этого кода вы получите файл PSD, созданный из WEBP, и можете применить любые фильтры, слои и настройки Aspose.PSD, включая трансформацию Warp
}

// Вы также можете создавать изображения адаптируемых экспортеров в формат PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Используйте Aspose.Imaging API для редактирования файла WEBP с функциями, специфическими для Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Затем просто используйте метод ToPsdImage() и редактируйте файл как PSD с функциями, подобными Photoshop, включая слои, умные фильтры и умные объекты.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Некоторый текст", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Сохраните окончательный файл PSD с помощью Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Если вам не нужно использовать Погрузчики или Экспортеры, предоставленные адаптерами, просто отключите их
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
