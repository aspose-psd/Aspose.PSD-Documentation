---
title: Оголошення версії Aspose.PSD для .NET 21.9
type: docs
weight: 40
url: /uk/net/aspose-psd-dlya-net-21-9-oholoshennya-pro-vypusk/
---

{{% alert color="primary" %}} 

Ця сторінка містить оголошення про [Aspose.PSD для .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :-| :-| :-|
|PSDNET-574|Зробіть стиснення RLE за замовчуванням для збереження PSD, щоб уникнути великого вихідного файлу PSD|Особливість|
|PSDNET-747|Підтримка ефектів шару з оверлеєм у режимі багатоканального кольору в файлі PSD|Особливість|
|PSDNET-951|Після створення нового шару його властивість Ресурси дорівнює null, що унеможливлює маніпулювання (наприклад, зміна розміру)|Помилка|
|PSDNET-955|Непідтримка методів стиснення ZipWithPrediction для 8 біт|Помилка|

## **Зміни у публічному API**
# **Додані API:**
- Немає

# **Вилучені API:**
- Немає

## **Приклади використання:**

**PSDNET-574. Зробіть стиснення RLE за замовчуванням для збереження PSD, щоб уникнути великого вихідного файлу PSD**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Підтримка ефектів шару з оверлеєм у режимі багатоканального кольору в файлі PSD**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Не повинно кидатися виняток
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Не повинно кидатися виняток
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. Після створення нового шару його властивість Ресурси дорівнює null, що унеможливлює маніпулювання (наприклад, зміна розміру)**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ЗамінитиКолір(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // Червоний
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Зелений
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Синій
                    var b = (byte)(pixels[i] & 0xff);

                    int фактичнаРізниця = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (фактичнаРізниця <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Шар2 = null;
            Layer Шар3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Додавання Шару 1

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Шар2 = new Layer(stream);

                    Шар2.Resize(image.Width, image.Height);
                    var width = Шар2.Width;
                    var height = Шар2.Height;

                    Шар2.Left = 675;
                    Шар2.Top = 0;

                    Шар2.Right = Шар2.Left + width;
                    Шар2.Bottom = Шар2.Top + height;

                    image.AddLayer(Шар2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Шар3 = new Layer(stream);
                    // Заміна білого кольору на прозорий
                    ЗамінитиКолір(Шар3, Color.White, 256, Color.Transparent);
                    Шар2.DrawImage(new Point(0, 0), Шар3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Непідтримка методів стиснення ZipWithPrediction для 8 біт**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
