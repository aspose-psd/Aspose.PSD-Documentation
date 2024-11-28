---
title: Примітки до випуску Aspose.PSD Адаптерів для .NET 24.4
type: docs
weight: 100
url: /uk/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску [Aspose.PSD Адаптерів для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Ключ**    | **Опис**                                                              | **Категорія** |
|:------------|:-----------------------------------------------------------------------|:-------------|
| PSDNET-1985 | Початкове опублікування Aspose.PSD.Adapters.Imaging в Nuget           | Покращення  |


## **Зміни у публічному API**
# **Додані API:**
- Жодних

# **Видалені API:**
- Жодних

## **Приклади використання:**

Будь ласка, перевірте [сторінку документації з адаптерами Aspose.PSD](/uk/psd/net/adapters)

**PSDNET-1985. Найповниший приклад використання Aspose.PSD Адаптерів**

{{< highlight csharp >}}
// Додайте активацію адаптерів у свій init config
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// додатково активуйте Експортери
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Для роботи з адаптерами вам потрібні ліцензії як для Aspose.PSD, так і для адаптованого об'єкта
// Ось як застосувати ліцензію Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Ось приклад застосування ліцензії адаптований об'єкт для Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Потім ви можете запускати будь-який код адаптерів або бібліотеки PSD чи Imaging

// Після цього всі ці файли можуть бути відкриті за допомогою Aspose.PSD без будь-якого додаткового коду, просто використовуйте
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Після виконання цього коду ви отримаєте файл PSD, створений з WEBP і зможете застосовувати будь-які фільтри, шари та налаштування Aspose.PSD включаючи трансформацію Warp
}

// Ви можете додатково створити зображення експортерів в формат PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Використовуйте Aspose.Imaging API для редагування файлу WEBP з особливостями, специфічними для Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Потім просто використовуйте метод ToPsdImage() і редагуйте файл, як PSD з функціями, схожими на Photoshop, включаючи шари, інтелектуальні фільтри та об'єкти з
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Деякий текст", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Збережіть остаточний файл PSD за допомогою Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Якщо вам не потрібно використовувати Погрузальники або Експортери, які надаються Адаптерами, просто вимкніть їх
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
