---
title: Aspose.PSD для .NET 18.8 - Примечания к выпуску
type: docs
weight: 50
url: /ru/net/aspose-psd-for-net-18-8-release-notes/
---

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-68|Поддержка свойства LayerCreationDateTime.|Функционал|
|PSDNET-67|Поддержка выделения Цвета Листа|Функционал|
|PSDNET-66|Возможность объединения слоев один с другим|Функционал|
|PSDNET-65|Добавление частичной поддержки свойства Предел Слоя Текста|Функционал|
|PSDNET-64|Добавление поддержки IopaResource|Функционал|
|PSDNET-56|Поддержка эффектов слоев для формата PSD|Функционал|
|PSDNET-55|Поддержка InterruptMonitor для .Net|Функционал|
|PSDNET-50|Возможность объединения слоев|Функционал|
|PSDNET-49|Добавление рендеринга свойства непрозрачности заполнения в слоях.|Функционал|
|PSDNET-43|Реализация рендеринга Слоя Коррекции Кривых|Функционал|
|PSDNET-42|Добавление поддержки Слоя Коррекции Кривых|Функционал|
|PSDNET-41|Реализация рендеринга Слоя Коррекции Уровней|Функционал|
|PSDNET-40|Добавление поддержки Слоя Коррекции Уровней|Функционал|
|PSDNET-37|Добавление поддержки Слоя Коррекции Канала Микшера|Функционал|
|PSDNET-35|Добавление поддержки Слоя Коррекции Оттенка/Насыщенности|Функционал|
|PSDNET-34|Реализация рендеринга Слоя Коррекции Экспозиции для экспорта.|Функционал|
|PSDNET-31|Добавление поддержки рендеринга для экспорта слоя коррекции канала микшера|Функционал|
|PSDNET-26|Добавление поддержки маскирования|Функционал|
|PSDNET-13|Добавить поддержку маски слоя|Функционал|
|PSDNET-9|Добавление поддержки Слоя Коррекции Фотофильтра|Функционал|
|PSDNET-8|Добавление поддержки слоя коррекции канала микшера|Функционал|
|PSDNET-7|Добавление поддержки слоя коррекции экспозиции|Функционал|
|PSDNET-6|Добавление поддержки слоя коррекции яркости/контрастности|Функционал|
|PSDNET-5|Добавить частичную поддержку слоев коррекции|Функционал|
|PSDNET-3|Добавление поддержки опции текста PSD без переноса|Функционал|
|PSDNET-2|Возможность добавления текстового слоя на лету|Функционал|
|PSDNET-62|Кодек TIFF не может сохранить изображение канала 16 бит|Улучшение|
|PSDNET-61|Сохранение изображения PSD приводит к неверным цветам изображения|Улучшение|
|PSDNET-60|Некорректно указано местоположение левого верхнего угла при обновлении|Улучшение|
|PSDNET-59|Исключение при обновлении текстовых слоев|Улучшение|
|PSDNET-58|Отображение свойства Codec для изображения JPEG2000|Улучшение|
|PSDNET-57|Исправление настроек 24bpp для экспорта в BMP|Улучшение|
|PSDNET-46|Слой коррекции не учитывается при конвертации CMYK PSD в TIFF или JPG|Улучшение|

## **Примеры использования:**
**PSDNET-68 Поддержка свойства LayerCreationDateTime**

{{< highlight java >}}

 // Пример свойства LayerCreationDateTime

Строка sourceFileName = "OneLayer.psd";

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Проверка, что дата создания обновлена на вновь созданных слоях

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Поддержка выделения цвета Листа**

{{< highlight java >}}

 // Пример использования свойства SheetColorHighlight

Строка sourceFileName = "SheetColorHighlightExample.psd";

Строка exportPath = "SheetColorHighlightExampleChanged.psd";

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);



    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 Возможность объединения слоев один с другим**

{{< highlight java >}}

 // Пример слияния двух слоев

Строка sourceFile1 = "FillOpacitySample.psd";

Строка sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

Строка exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

используя (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    используя (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

	im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 Добавление частичной поддержки свойства Предел Слоя Текста**

{{< highlight java >}}

 // Пример Text BoxBounds

Строка sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // Размер слоя - это размер области рендеринга

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox - максимальный размер слоя для слоя текста

    // В этой области PS попытается вписать ваш текст

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Добавление поддержки IopaResource**

{{< highlight java >}}

 // Изменение свойства непрозрачности заполнения через изменение IopaResource

Строка sourceFileName = "FillOpacitySample.psd";

Строка exportPath = "FillOpacitySampleChanged.psd";

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];



    var resources = layer.Resources;

    foreach (var resource in resources)

    {

        if (resource is IopaResource)

        {

            var iopaResource = (IopaResource)resource;

            iopaResource.FillOpacity = 200;

        }

    }



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 Поддержка эффектов слоев для формата PSD**

{{< highlight java >}}

 используя (

    PsdImage image =



        (PsdImage)

        Aspose.PSD.Image.Load(



            sourceFileName,



            новые Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,



                новые Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 Поддержка InterruptMonitor для .Net**

{{< highlight java >}}

         публичный void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = новые ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = новый Multithreading.InterruptMonitor();

            SaveImageWorker worker = новый SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = новый System.Threading.Thread(новый System.Threading.ThreadStart(worker.ThreadProc));

            попробовать

            {

                thread.Start();

                // Тайм-аут должен быть меньше времени, необходимого для полного преобразования изображения (без прерывания).

                System.Threading.Thread.Sleep(3000);

                // Прерывание процесса

                monitor.Interrupt();

                System.Console.WriteLine("Прерывание потока сохранения #{0} в {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Ожидание прерывания...

                thread.Join();

            }

            finally

            {

                // Если файл, который должен быть удален, не существует, исключение не генерируется.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// Инициирует преобразование изображения и ожидает его прерывание.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Путь к исходному изображению.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Путь к выходному изображению.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Монитор прерывания.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Опции сохранения.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Инициализирует новый экземпляр класса <see cref="SaveImageWorker" />.

            /// </summary>

            /// <param name="inputPath">Путь к исходному изображению.</param>

            /// <param name="outputPath">Путь к выходному изображению.</param>

            /// <param name="saveOptions">Опции сохранения.</param>

            /// <param name="monitor">Монитор прерывания.</param>

            публичный SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Пытается конвертировать изображение из одного формата в другой. Обрабатывает прерывание. 

            /// </summary>

            публичный void ThreadProc()

            {

                используя (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    попробовать

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Ожидаемое прерывание.");

                    }

                    поймать (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("Поток сохранения #{0} завершается в {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    поймать (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    наконец

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 Создание возможности слияния слоев**

{{< highlight java >}}

 // Объединить весь PSD

Строка sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

Строка exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// Объединить один слой с другим

Строка sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

Строка exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // Настройка объединенных слоев

    im.Layers = новые Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Добавление рендеринга свойства непрозрачности заполнения в слоях**

{{< highlight java >}}

 // Изменение свойства непрозрачности заполнения

Строка sourceFileName = "FillOpacitySample.psd";

Строка exportPath = "FillOpacitySampleChanged.psd";

используя (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Реализация рендеринга Слоя Коррекции Кривых**

{{< highlight java >}}

 // Редактирование слоя кривых

Строка sourceFileName = "CurvesAdjustmentLayer";

Строка psdPathAfterChange = "CurvesAdjustmentLayerChanged";

Строка pngExportPath = "CurvesAdjustmentLayerChanged";

для (int j = 1; j < 2; j++)

{

    используя (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        для каждого (var layer в im.Layers)

	{

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      для (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 еще

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }



    // Сохранить PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");
	


    // Сохранить PNG

    var saveOptions = новые PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Добавление поддержки Слоя Коррекции Кривых**

{{< highlight java >}}

 // Редактирование слоя кривых

Строка sourceFileName = "CurvesAdjustmentLayer";

Строка psdPathAfterChange = "CurvesAdjustmentLayerChanged";

для (int j = 1; j < 2; j++)

{

    используя (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

         для каждого (var layer в im.Layers)

	 {

            if (layer is CurvesLayer            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

	}

    }



    // Сохранить PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Реализация рендеринга Слоя Коррекции Уровней**

{{< highlight java >}}

 // Редактирование слоя уровней

Строка sourceFileName = "LevelsAdjustmentLayer.psd";

Строка psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

Строка pngExportPath = "LevelsAdjustmentLayerChanged.png";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

        если (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }



    // Сохранить PSD

    im.Save(psdPathAfterChange);



    // Сохранить PNG

    var saveOptions = новые PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-40 Добавление поддержки Слоя Коррекции Уровней**

{{< highlight java >}}

 // Редактирование слоя уровней

Строка sourceFileName = "LevelsAdjustmentLayer.psd";

Строка psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

        если (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }



    // Сохранить PSD

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-37 Добавление поддержки Слоя Коррекции Канала Миксера**

{{< highlight java >}}



// Rgb Канал Миксера

Строка sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

Строка psdPathAfterChange = "ChannelMixerAdjustmentLayerRgbChanged.psd";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

         если (layer is RgbChannelMixerLayer)

         {

              var rgbLayer = (RgbChannelMixerLayer)layer;

              rgbLayer.RedChannel.Blue = 100;

              rgbLayer.BlueChannel.Green = -100;

              rgbLayer.GreenChannel.Constant = 50;

         }

    }



    im.Save(psdPathAfterChange);

}

// Cmyk Канал Миксера

Строка sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

Строка psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

         если (layer is CmykChannelMixerLayer)

         {

             var cmykLayer = (CmykChannelMixerLayer)layer;

             cmykLayer.CyanChannel.Black = 20;

             cmykLayer.MagentaChannel.Yellow = 50;

             cmykLayer.YellowChannel.Cyan = -25;

             cmykLayer.BlackChannel.Yellow = 25;

         }

    }



    im.Save(psdPathAfterChange);

}





// Добавление нового слоя(Cmyk для этого примера)

Строка sourceFileName = "CmykWithAlpha.psd";

Строка psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

используя (var im = LoadFile(sourceFileName))

{

    var newlayer = im.AddChannelMixerAdjustmentLayer();

    newlayer.GetChannelByIndex(2).Constant = 50;

    newlayer.GetChannelByIndex(0).Constant = 50;



    im.Save(psdPathAfterChange);

}		

{{< /highlight >}}

**PSDNET-35 Добавление поддержки Слоя Коррекции Оттенка/Насыщенности**

{{< highlight java >}}

 // Редактирование слоя оттенка/насыщенности

Строка sourceFileName = "HueSaturationAdjustmentLayer.psd";

Строка psdPathAfterChange = "HueSaturationAdjustmentLayerChanged.psd";

используя (var im = LoadFile(sourceFileName))

{

     для каждого (var layer в im.Layers)

     {

           если (layer is HueSaturationLayer)

           {

                var hueLayer = (HueSaturationLayer)layer;

                hueLayer.Hue = -25;

                hueLayer.Saturation = -12;

                hueLayer.Lightness = 67;

                var colorRange = hueLayer.GetRange(2);

                colorRange.Hue = -40;

                colorRange.Saturation = 50;

                colorRange.Lightness = -20;

                colorRange.MostLeftBorder = 300;

           }

      }

      im.Save(psdPathAfterChange);

}



// Добавление слоя оттенка/насыщенности

Строка sourceFileName = "PhotoExample.psd";

Строка psdPathAfterChange = "PhotoExampleAddedHueSaturation.psd";



используя (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveForVisualTest(im, this.OutputPath, prefix + file, "before");

     var hueLayer = im.AddHueSaturationAdjustmentLayer();

     hueLayer.Hue = -25;

     hueLayer.Saturation = -12;

     hueLayer.Lightness = 67;

     var colorRange = hueLayer.GetRange(2);

     colorRange.Hue = -160;

     colorRange.Saturation = 100;

     colorRange.Lightness = 20;

     colorRange.MostLeftBorder = 300;



     im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-34 Реализация рендеринга Слоя Коррекции Экспозиции для экспорта.**

{{< highlight java >}}

 // Редактирование слоя экспозиции

Строка sourceFileName = "ExposureAdjustmentLayer.psd";

Строка psdPathAfterChange = "ExposureAdjustmentLayerChanged.psd";

Строка pngExportPath = "ExposureAdjustmentLayerChanged.png";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

        если (layer is ExposureLayer)

        {

	    var expLayer = (ExposureLayer)layer;

            expLayer.Exposure = 2;

            expLayer.Offset = -0.25f;

            expLayer.GammaCorrection = 0.5f;

        }

    }



    // Сохранить PSD

    im.Save(psdPathAfterChange);



    // Сохранить PNG

    var saveOptions = новые PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}



// Добавление слоя экспозиции

Строка sourceFileName = "PhotoExample.psd";

Строка psdPathAfterChange = "PhotoExampleAddedExposure.psd";

Строка pngExportPath = "PhotoExampleAddedExposure.png";

используя (PsdImage im = LoadFile(sourceFileName))

{

     var newlayer = im.AddExposureAdjustmentLayer();

     newlayer.Exposure = 2;

     newlayer.Offset = -0.25f;

     newlayer.GammaCorrection = 2f;



     // Сохранить PSD

     im.Save(psdPathAfterChange);



     // Сохранить PNG

     var saveOptions = новые PngOptions();

     saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

     im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-31 Добавление поддержки рендеринга для экспорта слоя коррекции канала микшера**

{{< highlight java >}}



// Rgb Канал Миксера

Строка sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

Строка psdPathAfterChange = "ChannelMixerAdjustmentLayerRgbChanged.psd";

Строка pngExportPath = "ChannelMixerAdjustmentLayerRgbChanged.png";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

         если (layer is RgbChannelMixerLayer)

         {

              var rgbLayer = (RgbChannelMixerLayer)layer;

              rgbLayer.RedChannel.Blue = 100;

              rgbLayer.BlueChannel.Green = -100;

              rgbLayer.GreenChannel.Constant = 50;

         }

    }



	// Сохранить PSD

    im.Save(psdPathAfterChange);



	// Сохранить PNG

    var saveOptions = новые PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

// Cmyk Канал Миксера

Строка sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

Строка psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

Строка pngExportPath = "ChannelMixerAdjustmentLayerCmykChanged.png";

используя (var im = LoadFile(sourceFileName))

{

    для каждого (var layer в im.Layers)

    {

         если (layer is CmykChannelMixerLayer)

         {

             var cmykLayer = (CmykChannelMixerLayer)layer;

             cmykLayer.CyanChannel.Black = 20;

             cmykLayer.MagentaChannel.Yellow = 50;

             cmykLayer.YellowChannel.Cyan = -25;

             cmykLayer.BlackChannel.Yellow = 25;

         }

    }



	// Сохранить PSD

    im.Save(psdPathAfterChange);



	// Сохранить PNG

    var saveOptions = новые PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}



{{< /highlight >}}