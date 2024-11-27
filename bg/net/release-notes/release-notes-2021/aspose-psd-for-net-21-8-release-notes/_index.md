---
title: Aspose.PSD за .NET 21.8 - Бележки за Изданието
type: docs
weight: 50
url: /bg/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-698|Поддръжка на методи за компресия ZipWithPrediction|Функционалност|
|PSDNET-663|Разтоянието на текста е неправилно в генерирания PSD|Проблем|
|PSDNET-685|Изключение при запазване на PSD|Проблем|
|PSDNET-927|Неправилно разстояние между редове и символи в Aspose.PSD когато го използваме без лиценз|Проблем|

## **Промени в Публичното API**
# **Добавени API:**
- Няма

# **Премахнати API:**
- Няма

## **Примери за Използване:**

**PSDNET-663. Разтоянието на текста е неправилно в генерирания PSD**

{{< highlight csharp >}}
            string изходно_име_на_файла = "изходен.psd";
            string име_на_изходен_файл = "изход.png";

            using (PsdImage изображение = (PsdImage)Image.Load(изходно_име_на_файла))
            {
                изображение.Save(име_на_изходен_файл, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Изключение при запазване на PSD**

{{< highlight csharp >}}
            string изходен_файл = "Файл.psd";
            string изходен_файл2 = "Файл2.psd";

            using (PsdImage изображение = (PsdImage)Image.Load(изходен_файл))
            {
                var слой1 = (TextLayer)изображение.Layers[1];
                слой1.TextData.UpdateLayerData();

                изображение.Save(изходен_файл2);
            }
{{< /highlight >}}

**PSDNET-698. Поддръжка на методи за компресия ZipWithPrediction**

{{< highlight csharp >}}
            string път_към_входния_файл = "zipTest698.psd";

            string изходен_PNG = "изход.png";
            string изходен_Raw = "изходен_Raw.psd";
            string изходен_Zip = "изходен_Zip.psd";

            using (Image изображение = Image.Load(път_към_входния_файл))
            {
                изображение.Save(изходен_PNG, new PngOptions());

                изображение.Save(изходен_Raw, new PsdOptions() { Метод_на_компресия = Метод_на_компресия.Raw });
                изображение.Save(изходен_Zip, new PsdOptions() { Метод_на_компресия = Метод_на_компресия.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Неправилно разстояние между редове и символи в Aspose.PSD когато го използваме без лиценз**

{{< highlight csharp >}}
            bool[] състояния_на_лиценза = new bool[] { false, true };
            for (int i = 0; i < състояния_на_лиценза.Length; i++)
            {
                bool тест_лиценз = състояния_на_лиценза[i];
                if (тест_лиценз)
                {
                    License лиценз = new License();
                    лиценз.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string изходен_файл = "psdnetTest927.psd";
                string изходен_файл2 = "out_" + тест_лиценз.ToString() + "_psdnetTest927.png";

                using (var изображение = (PsdImage)Image.Load(изходен_файл))
                {
                    изображение.Save(изходен_файл2, new PngOptions());
                }
            }
{{< /highlight >}}
