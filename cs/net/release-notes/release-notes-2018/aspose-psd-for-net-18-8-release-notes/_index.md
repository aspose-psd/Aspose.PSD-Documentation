---
title: Aspose.PSD pro .NET 18.8 - Poznámky k vydání
type: docs
weight: 50
url: /cs/net/aspose-psd-pro-net-18-8-poznamky-k-vydani/
---

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-68|Podpora vlastnosti LayerCreationDateTime.|Funkce|
|PSDNET-67|Podpora SheetColor Highlighting.|Funkce|
|PSDNET-66|Schopnost sloučit vrstvy mezi sebou.|Funkce|
|PSDNET-65|Částečná podpora vlastnosti Text Layer BoundBox.|Funkce|
|PSDNET-64|Podpora IopaResource.|Funkce|
|PSDNET-56|Podpora efektů vrstev pro formát PSD.|Funkce|
|PSDNET-55|Podpora InterruptMonitor pro .Net.|Funkce|
|PSDNET-50|Možnost sloučit vrstvy.|Funkce|
|PSDNET-49|Přidání vykreslování vlastnosti plné průhlednosti vrstev.|Funkce|
|PSDNET-43|Implementace vykreslování vrstvy úpravy křivek.|Funkce|
|PSDNET-42|Podpora vrstvy úpravy křivek.|Funkce|
|PSDNET-41|Implementace vykreslování vrstvy úpravy úrovní.|Funkce|
|PSDNET-40|Podpora vrstvy úpravy úrovní.|Funkce|
|PSDNET-37|Podpora vrstvy úpravy směsi kanálů.|Funkce|
|PSDNET-35|Podpora vrstvy úpravy odstínu/sytosti.|Funkce|
|PSDNET-34|Implementace vykreslování vrstvy úpravy expozice pro export.|Funkce|
|PSDNET-31|Podpora vykreslování pro export vrstvy úpravy směsi kanálů.|Funkce|
|PSDNET-26|Podpora maskování se zářezem.|Funkce|
|PSDNET-13|Podpora masky vrstvy.|Funkce|
|PSDNET-9|Podpora vrstvy úpravy fotofiltru.|Funkce|
|PSDNET-8|Podpora vrstev úpravy směsi kanálů.|Funkce|
|PSDNET-7|Podpora vrstvy úpravy expozice.|Funkce|
|PSDNET-6|Podpora vrstvy úpravy jasu/kontrastu.|Funkce|
|PSDNET-5|Částečná podpora vrstev úprav.|Funkce|
|PSDNET-3|Podpora volby PSD NoBreak text.|Funkce|
|PSDNET-2|Schopnost přidat textovou vrstvu za běhu.|Funkce|
|PSDNET-62|TIFF Codec nemůže uložit 16bitový kanálový obraz.|Vylepšení|
|PSDNET-61|Ukládání obrázku PSD produkuje neplatné barvy obrázku.|Vylepšení|
|PSDNET-60|Souřadnice levého horního rohu jsou nesprávné při aktualizaci.|Vylepšení|
|PSDNET-59|Výjimka při aktualizaci textových vrstev.|Vylepšení|
|PSDNET-58|Vystavit vlastnost Codec obrázku JPEG2000 veřejnosti.|Vylepšení|
|PSDNET-57|Oprava nastavení 24bpp možností pro export do BMP.|Vylepšení|
|PSDNET-46|Vrstva úpravy ignorována při konverzi CMYK PSD do TIFF nebo JPG.|Vylepšení|

## **Příklady použití:**
**PSDNET-68 Podpora vlastnosti LayerCreationDateTime**

{{< highlight java >}}

 // Příklad vlastnosti LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Ověření, zda se Datum a čas vytvoření aktualizoval na nově vytvořené vrstvy

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Podpora SheetColor Highlighting**

{{< highlight java >}}

 // Příklad vlastnosti SheetColor Highlight

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

**PSDNET-66 Schopnost sloučit vrstvy mezi sebou**

{{< highlight java >}}

 // Příklad sloučení dvou vrstev

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

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

**PSDNET-65 Přidat částečnou podporu vlastnosti Text Layer BoundBox**

{{< highlight java >}}

 // Příklad BoundBoxu textové vrstvy

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // Velikost vrstvy je velikost renderované oblasti

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox je maximální velikost vrstvy pro vrstvu textu. 

    // V této oblasti se bude snažit PS přizpůsobit váš text

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Přidat podporu pro IopaResource**

{{< highlight java >}}

 // Úprava vlastnosti Fill Opacity pomocí změny IopaResource

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

**PSDNET-56 Podpora efektů vrstev pro formát PSD**

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

**PSDNET-55 Podpora InterruptMonitor pro .Net**

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

                // Časový limit by měl být menší než doba potřebná pro úplnou konverzi obrázku (bez přerušení).

                System.Threading.Thread.Sleep(3000);

                // Přerušení procesu

                monitor.Interrupt();

                System.Console.WriteLine("Přerušení ukládacího vlákna #{0} v {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Čekání na přerušení...

                thread.Join();

            }

            finally

            {

                // Pokud soubor, který se má smazat, neexistuje, není vyvolána žádná výjimka.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// Začne s konverzí obrázku a čeká na jeho přerušení.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Cesta k vstupnímu obrázku.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Cesta k výstupnímu obrázku.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Monitor přerušení.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Nastavení ukládání.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Inicializuje novou instanci třídy <see cref="SaveImageWorker" />.

            /// </summary>

            /// <param name="inputPath">Cesta k vstupnímu obrázku.</param>

            /// <param name="outputPath">Cesta k výstupnímu obrázku.</param>

            /// <param name="saveOptions">Nastavení ukládání.</param>

            /// <param name="monitor">Monitor přerušení.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Pokusí se konvertovat obrázek z jednoho formátu do druhého. Řeší přerušení. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Očekáváno přerušení.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("VLákno ukládání #{0} končí v {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

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

**PSDNET-50 Možnost sloučit vrstvy**

{{< highlight java >}}

 // Změnit celé PSD

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// Sloučit jednu vrstvu s druhou

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // Nastavit sloučené vrstvy

    im.Layers = new Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Přidat vykreslování vlastnosti průhlednosti vrstev**

{{< highlight java >}}

 // Změnit vlastnost Fill Opacity

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Implementace vykreslování vrstvy úpravy křivek**

{{< highlight java >}}

 // Úprava vrstvy křivek

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

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

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



    // Uložit PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // Uložit PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Přidat podporu pro vrstvu úpravy křivek**

{{< highlight java >}}

 // Úprava vrstvy křivek

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

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

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



    // Uložit PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Implementace vykreslování vrstvy úpravy úrovní**

{{< highlight java >}}

 // Úprava vrstvyúrovní

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



    // Uložit PSD

    im.Save(psdPathAfterChange);



    // Uložit PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

**PSDNET-40 Přidat podporu vrstvy úpravy úrovní**

{{< highlight java >}}

 // Úprava vrstvy úrovní

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

**PSDNET-37 Přidat podporu vrstvy úpravy směsi kanálů**

{{< highlight java >}}



// Rgb Channel Mixer

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

// Cmyk Channel Mixer

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





// Přidání nové vrstvy (Cmyk v tomto příkladu)

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

**PSDNET-35 Přidat podporu vrstvy úpravy odstínu/sytosti**

{{< highlight java >}}

 // Úprava vrstvy odstínu/sytosti

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



// Přidání vrstvy úpravy odstínu/sytosti

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