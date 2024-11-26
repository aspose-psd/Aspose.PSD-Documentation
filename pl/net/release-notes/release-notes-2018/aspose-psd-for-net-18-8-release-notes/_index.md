---
title: Aspose.PSD dla .NET 18.8 - Notatki dotyczące wersji
type: docs
weight: 50
url: /pl/net/aspose-psd-dla-net-18-8-notatki-o-wydaniu/
---

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-68|Wsparcie dla właściwości LayerCreationDateTime.|Funkcja|
|PSDNET-67|Wsparcie dla podświetlenia koloru SheetColor.|Funkcja|
|PSDNET-66|Możliwość łączenia warstw ze sobą.|Funkcja|
|PSDNET-65|Częściowe wsparcie dla właściwości Text Layer BoundBox.|Funkcja|
|PSDNET-64|Dodanie obsługi dla IopaResource.|Funkcja|
|PSDNET-56|Wsparcie dla efektów warstw w formacie PSD.|Funkcja|
|PSDNET-55|Wsparcie dla InterruptMonitor w .Net.|Funkcja|
|PSDNET-50|Umożliwienie spłaszczenia warstw.|Funkcja|
|PSDNET-49|Dodanie renderowania właściwości wypełnienia warstw.|Funkcja|
|PSDNET-43|Implementacja renderowania warstwy korekty krzywych.|Funkcja|
|PSDNET-42|Dodanie wsparcia dla warstwy korekty krzywych.|Funkcja|
|PSDNET-41|Implementacja renderowania warstwy korekty poziomów.|Funkcja|
|PSDNET-40|Dodanie wsparcia dla warstwy korekty poziomów.|Funkcja|
|PSDNET-37|Dodanie wsparcia dla warstwy miksowania kanałów.|Funkcja|
|PSDNET-35|Dodanie wsparcia dla warstwy korekty odcieni i saturacji.|Funkcja|
|PSDNET-34|Implementacja renderowania warstwy korekty ekspozycji do eksportu.|Funkcja|
|PSDNET-31|Dodanie wsparcia dla eksportu warstwy adjustacji Mixer kanałów.|Funkcja|
|PSDNET-26|Dodanie wsparcia dla maski obcinania.|Funkcja|
|PSDNET-13|Dodanie wsparcia dla warstwy maski.|Funkcja|
|PSDNET-9|Dodanie wsparcia dla warstwy filtru fotograficznego.|Funkcja|
|PSDNET-8|Dodanie wsparcia dla warstwy adjustacji miksera kanałów.|Funkcja|
|PSDNET-7|Dodanie wsparcia dla warstwy adjustacji ekspozycji.|Funkcja|
|PSDNET-6|Dodanie wsparcia dla warstwy adjustacji jasności/kontrastu.|Funkcja|
|PSDNET-5|Częściowe wsparcie dla warstw adjustacji.|Funkcja|
|PSDNET-3|Dodanie wsparcia dla opcji tekstu PSD NoBreak.|Funkcja|
|PSDNET-2|Możliwość dodawania warstwy tekstu w czasie wykonywania.|Funkcja|
|PSDNET-62|Kodek TIFF nie może zapisać obrazu 16-bitowego kanału.|Usprawnienie|
|PSDNET-61|Zapis obrazu PSD powoduje nieprawidłowe kolory obrazu.|Usprawnienie|
|PSDNET-60|Błędne jest ustawienie kordynatów lewego górnego rogu podczas aktualizacji.|Usprawnienie|
|PSDNET-59|Wyjątek podczas aktualizacji warstw tekstowych.|Usprawnienie|
|PSDNET-58|Eksponowanie właściwości kodera obrazu JPEG2000 publicznie.|Usprawnienie|
|PSDNET-57|Popraw ustawienia opcji 24-bitowych dla eksportu do BMP.|Usprawnienie|
|PSDNET-46|Warstwa adjustacji jest ignorowana podczas konwersji PSD CMYK na TIFF lub JPG.|Usprawnienie|

## **Przykłady użycia:**
**PSDNET-68 Wsparcie dla właściwości LayerCreationDateTime**

{{< highlight java >}}

 // Przykład użycia właściwości LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Sprawdzenie, czy data utworzenia warstwy została zaktualizowana na nowo utworzonych warstwach

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Wsparcie dla podświetlenia koloru SheetColor**

{{< highlight java >}}

 // Przykład użycia właściwości SheetColorHighlight

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);



    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 Możliwość łączenia warstw ze sobą**

{{< highlight java >}}

 // Przykład łączenia dwóch warstw

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd";

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

	    im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 Częściowe wsparcie dla właściwości Text Layer BoundBox**

{{< highlight java >}}

 // Przykład ramki tekstowej

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // Rozmiar warstwy to rozmiar obszaru renderowania

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox to maksymalny rozmiar warstwy tekstowej. 

    // W tym obszarze PS spróbuje umieścić Twój tekst

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Dodanie wsparcia dla IopaResource**

{{< highlight java >}}

 // Zmiana właściwości Fill Opacity poprzez zmianę zasobu IopaResource

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

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

**PSDNET-56 Wsparcie dla efektów warstw w formacie PSD**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 Wsparcie dla InterruptMonitor w .Net**

{{< highlight java >}}

         public void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // Timeout powinien być krótszy niż czas potrzebny na pełną konwersję obrazu (bez przerwania).

                System.Threading.Thread.Sleep(3000);

                // Przerwij proces

                monitor.Interrupt();

                System.Console.WriteLine("Interrupting the save thread #{0} at {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Poczekaj na przerwanie...

                thread.Join();

            }

            finally

            {

                // Jeśli plik do usunięcia nie istnieje, nie będzie zgłaszany żaden wyjątek.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// Rozpoczyna konwersję obrazu i oczekuje na jej przerwanie.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Ścieżka do obrazu wejściowego.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Ścieżka do obrazu wyjściowego.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Monitor przerwań.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Opcje zapisu.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Inicjalizuje nowe wystąpienie klasy SaveImageWorker.

            /// </summary>

            /// <param name="inputPath">Ścieżka do obrazu wejściowego.</param>

            /// <param name="outputPath">Ścieżka do obrazu wyjściowego.</param>

            /// <param name="saveOptions">Opcje zapisu.</param>

            /// <param name="monitor">Monitor przerwań.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Próbuje przekonwertować obraz z jednego formatu na inny. Obsługuje przerwanie. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Oczekiwane przerwanie.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("The save thread #{0} finishes at {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 Umożliwienie spłaszczenia warstw**

{{< highlight java >}}

 // Spłaszcz całe PSD

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// Połącz jedną warstwę z drugą

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // Konfiguracja połączonych warstw

    im.Layers = new Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Dodanie renderowania właściwości wypełnienia warstw**

{{< highlight java >}}

 // Zmień właściwość Fill Opacity

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Implementacja renderowania warstwy korekty krzywych**

{{< highlight java >}}

 // Edycja warstwy krzywych

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

string pngExportPath = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var layer in im.Layers)

	{

            if (layer is CurvesLayer)

            {

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



    // Zapisz PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");
    


    // Zapisz PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Dodanie wsparcia dla warstwy korekty krzywych**

{{< highlight java >}}

 // Edycja warstwy krzywych

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

         foreach (var layer in im.Layers)

	 {

            if (layer is CurvesLayer)

            {

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



    // Zapisz PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Implementacja renderowania warstwy korekty poziomów**

{{< highlight java >}}

 // Edycja warstwy poziomów

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

string pngExportPath = "LevelsAdjustmentLayerChanged.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

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



    // Save PSD

    im.Save(psdPathAfterChange);



    // Save PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-40 Dodanie wsparcia dla warstwy korekty poziomów**

{{< highlight java >}}

 // Edycja warstwy poziomów

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

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



    // Save PSD

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-37 Dodanie wsparcia dla warstwy miksowania kanałów**

{{< highlight java >}}



// Rgb Mixer kanałów

string sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerRgbChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is RgbChannelMixerLayer)

         {

              var rgbLayer = (RgbChannelMixerLayer)layer;

              rgbLayer.RedChannel.Blue = 100;

              rgbLayer.BlueChannel.Green = -100;

              rgbLayer.GreenChannel.Constant = 50;

         }

    }



    im.Save(psdPathAfterChange);

}

// Cmyk Mixer kanałów

string sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is CmykChannelMixerLayer)

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





// Dodanie nowej warstwy (Cmyk w tym przykładzie)

string sourceFileName = "CmykWithAlpha.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    var newlayer = im.AddChannelMixerAdjustmentLayer();

    newlayer.GetChannelByIndex(2).Constant = 50;

    newlayer.GetChannelByIndex(0).Constant = 50;



    im.Save(psdPathAfterChange);

}		

{{< /highlight >}}

**PSDNET-35 Dodanie wsparcia dla warstwy korekty odcieni i saturacji**

{{< highlight java >}}

 // Edycja warstwy odcieni i saturacji

string sourceFileName = "HueSaturationAdjustmentLayer.psd";

string psdPathAfterChange = "HueSaturationAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is HueSaturationLayer)

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



// Dodanie warstwy odcieni i saturacji

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

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

**PSDNET-34 Implementacja renderowania warstwy korekty ekspozycji do eksportu**

{{< highlight java >}}

 // Edycja warstwy ekspozycji

string sourceFileName = "ExposureAdjustmentLayer.psd";

string psdPathAfterChange = "ExposureAdjustmentLayerChanged.psd";

string pngExportPath = "ExposureAdjustmentLayerChanged.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is ExposureLayer)

        {

	    var expLayer = (ExposureLayer)layer;

            expLayer.Exposure = 2;

            expLayer.Offset = -0.25f;

            expLayer.GammaCorrection = 0.5f;

        }

    }



    // Save PSD

    im.Save(psdPathAfterChange);



    // Save PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}



// Dodanie warstwy ekspozycji

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedExposure.psd";

string pngExportPath = "PhotoExampleAddedExposure.png";



using (PsdImage im = LoadFile(sourceFileName))

{

     var newlayer = im.AddExposureAdjustmentLayer();

     newlayer.Exposure = 2;

     newlayer.Offset = -0.25f;

     newlayer.GammaCorrection = 2f;



     // Save PSD

     im.Save(psdPathAfterChange);



     // Save PNG

     var saveOptions = new PngOptions();

     saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

     im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}