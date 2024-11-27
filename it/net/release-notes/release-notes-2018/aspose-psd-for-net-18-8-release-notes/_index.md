---
title: Note sulla versione Aspose.PSD per .NET 18.8
type: docs
weight: 50
url: /it/net/aspose-psd-for-net-18-8-note-sulla-versione/
---

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-68|Supporto della proprietà LayerCreationDateTime.|Funzionalità|
|PSDNET-67|Supporto dell'Evidenziazione del colore del foglio|Funzionalità|
|PSDNET-66|Possibilità di unire i livelli tra loro|Funzionalità|
|PSDNET-65|Aggiunto il supporto parziale della proprietà BoundBox del livello di testo|Funzionalità|
|PSDNET-64|Aggiunto il supporto per IopaResource|Funzionalità|
|PSDNET-56|Supporto degli effetti del livello per il formato PSD|Funzionalità|
|PSDNET-55|Supporto InterruptMonitor per .Net|Funzionalità|
|PSDNET-50|Possibilità di appiattire i livelli|Funzionalità|
|PSDNET-49|Aggiunta della resa della proprietà opacità di riempimento nei livelli.|Funzionalità|
|PSDNET-43|Implementazione della resa del livello di regolazione delle curve|Funzionalità|
|PSDNET-42|Aggiunto il supporto del livello di regolazione delle curve|Funzionalità|
|PSDNET-41|Implementazione della resa del livello di regolazione dei livelli|Funzionalità|
|PSDNET-40|Aggiunto il supporto del livello di regolazione dei livelli|Funzionalità|
|PSDNET-37|Aggiunto il supporto del livello di regolazione del mixer dei canali|Funzionalità|
|PSDNET-35|Aggiunto il supporto del livello di regolazione dell'Hue/Saturation|Funzionalità|
|PSDNET-34|Implementazione della resa del livello di regolazione dell'esposizione per l'esportazione.|Funzionalità|
|PSDNET-31|Aggiunto il supporto della resa per l'esportazione del livello di regolazione del mixer dei canali|Funzionalità|
|PSDNET-26|Aggiunto il supporto del mascheramento di ritaglio|Funzionalità|
|PSDNET-13|Aggiunto il supporto del maschera del livello|Funzionalità|
|PSDNET-9|Aggiunto il supporto del livello di regolazione del filtro fotografico|Funzionalità|
|PSDNET-8|Aggiunto il supporto del livello di regolazione del mixer dei canali|Funzionalità|
|PSDNET-7|Aggiunto il supporto del livello di regolazione dell'esposizione|Funzionalità|
|PSDNET-6|Aggiunto il supporto del livello di regolazione della luminosità/contrasto|Funzionalità|
|PSDNET-5|Aggiunto il supporto parziale dei livelli di regolazione|Funzionalità|
|PSDNET-3|Aggiunto il supporto per l'opzione di testo NoBreak di PSD|Funzionalità|
|PSDNET-2|Possibilità di aggiungere un livello di testo in fase di esecuzione|Funzionalità|
|PSDNET-62|Il codec TIFF non può salvare l'immagine a canale a 16 bit|Potenziamento|
|PSDNET-61|Il salvataggio di un'immagine PSD produce colori dell'immagine non validi|Potenziamento|
|PSDNET-60|Coordinate dell'angolo in alto a sinistra non corrette durante l'aggiornamento|Potenziamento|
|PSDNET-59|Eccezione durante l'aggiornamento dei livelli di testo|Potenziamento|
|PSDNET-58|Esposizione della proprietà Codec dell'immagine JPEG2000 al pubblico|Potenziamento|
|PSDNET-57|Risolvere le impostazioni di opzioni a 24 bpp per l'esportazione in BMP|Potenziamento|
|PSDNET-46|Il livello di regolazione viene ignorato per la conversione PSD CMYK in TIFF o JPG|Potenziamento|

## **Esempi d'uso:**
**PSDNET-68 Supporto della proprietà LayerCreationDateTime**

{{< highlight java >}}

 // Esempio di utilizzo della proprietà LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Verifica se la data di creazione è stata aggiornata sui nuovi livelli creati

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Supporto dell'Evidenziazione del colore del foglio**

{{< highlight java >}}

 // Esempio di utilizzo della proprietà SheetColorHighlight

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

**PSDNET-66 Possibilità di unire i livelli tra loro**

{{< highlight java >}}

 // Esempio di unione di due livelli

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

**PSDNET-65 Aggiunto il supporto parziale della proprietà BoundBox del livello di testo**

{{< highlight java >}}

 // Esempio di BoundBox del testo

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // La dimensione del livello è la dimensione dell'area renderizzata

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox è la dimensione massima del livello per il livello di testo.
    // In quest'area PS tenterà di adattare il testo

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Aggiunto il supporto per IopaResource**

{{< highlight java >}}

 // Cambia la proprietà di opacità di riempimento tramite il cambio di IopaResource

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

**PSDNET-56 Supporto degli Effetti del Livello per il formato PSD**

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

**PSDNET-55 Supporto InterruptMonitor per .Net**

{{< highlight java >}}

         public void TestInterruptMonitor(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // Il timeout dovrebbe essere inferiore al tempo richiesto per la conversione completa dell'immagine (senza interruzioni).

                System.Threading.Thread.Sleep(3000);

                // Interrompe il processo

                monitor.Interrupt();

                System.Console.WriteLine("Interrompo il thread di salvataggio #{0} a {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Attendere l'interruzione...

                thread.Join();

            }

            finally

            {

                // Se il file da eliminare non esiste, non viene generata alcuna eccezione.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// Avvia la conversione dell'immagine e attendi la sua interruzione.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Il percorso dell'immagine di input.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Il percorso dell'immagine di output.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Il monitor di interruzione.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Le opzioni di salvataggio.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Inizializza una nuova istanza della classe SaveImageWorker.

            /// </summary>

            /// <param name="inputPath">Il percorso dell'immagine di input.</param>

            /// <param name="outputPath">Il percorso dell'immagine di output.</param>

            /// <param name="saveOptions">Le opzioni di salvataggio.</param>

            /// <param name="monitor">Il monitor di interruzione.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Tenta di convertire l'immagine da un formato all'altro. Gestisce l'interruzione.

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Interruzione prevista.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("Il thread di salvataggio #{0} termina alle {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

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

**PSDNET-50 Possibilità di appiattire i livelli**

{{< highlight java >}}

 // Appiattire l'intero PSD

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// Unisci un livello in un altro

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // Imposta i livelli uniti

    im.Layers = new Layer[] { layer2 };

    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Aggiunta della resa della proprietà opacità di riempimento nei livelli**

{{< highlight java >}}

 // Cambia la proprietà di opacità di riempimento

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Implementazione della resa del livello di regolazione delle curve**

{{< highlight java >}}

 // Modifica livello di curve

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



    // Salva PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // Salva PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Aggiunta del supporto del livello di regolazione delle curve**

{{< highlight java >}}

 // Modifica livello di curve

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



    // Salva PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Implementazione della resa del livello di regolazione dei livelli**

{{< highlight java >}}

 // Modifica livello di livellamento

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



    // Salva PSD

    im.Save(psdPathAfterChange);



    // Salva PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

**PSDNET-40 Aggiunto il supporto del livello di regolazione dei livelli**

{{< highlight java >}}

 // Modifica del livello di livellamento

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



    // Salva PSD

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-37 Aggiunto il supporto del livello di regolazione del mixer dei canali**

{{< highlight java >}}



// Mixer dei canali Rgb

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



// Mixer dei canali Cmyk

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





// Aggiungere il nuovo livello (Cmyk per questo esempio)

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

**PSDNET-35 Aggiunto il supporto del livello di regolazione dell'Hue/Saturation**

{{< highlight java >}}

 // Modifica livello di Hue/Saturation

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



// Aggiunta di un livello di Hue/Saturation

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveForVisualTest(im, this.OutputPath, prefix + file, "prima");

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