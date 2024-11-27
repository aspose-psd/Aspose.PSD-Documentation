---
title: Aspose.PSD für .NET 18.8 - Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-psd-fuer-net-18-8-release-notes/
---

| **Schlüssel** | **Zusammenfassung** | **Kategorie** |
| :- | :- | :- |
|PSDNET-68|Unterstützung der LayerCreationDateTime-Eigenschaft.|Feature|
|PSDNET-67|Unterstützung der SheetColor-Hervorhebung|Feature|
|PSDNET-66|Möglichkeit, Ebenen miteinander zu verschmelzen.|Feature|
|PSDNET-65|Teilweise Unterstützung der Textlayer BoundBox-Eigenschaft|Feature|
|PSDNET-64|Unterstützung von IopaResource|Feature|
|PSDNET-56|Unterstützung von Ebeneneffekten für PSD-Format|Feature|
|PSDNET-55|InterruptMonitor-Unterstützung für .Net|Feature|
|PSDNET-50|Möglichkeit, Ebenen zu vereinfachen|Feature|
|PSDNET-49|Hinzufügen der Darstellung der Fülldeckkraft-Eigenschaft in Ebenen.|Feature|
|PSDNET-43|Implementierung der Darstellung des Kurven-Anpassungseben-Layers|Feature|
|PSDNET-42|Hinzufügen der Unterstützung des Kurven-Anpassungsebenen-Layers|Feature|
|PSDNET-41|Implementierung der Darstellung des Levels-Anpassungseben-Layers|Feature|
|PSDNET-40|Hinzufügen der Unterstützung des Levels-Anpassungsebenen-Layers|Feature|
|PSDNET-37|Hinzufügen der Unterstützung des Kanalmixer-Anpassungsebenen-Layers|Feature|
|PSDNET-35|Hinzufügen der Unterstützung des Farbton/Sättigung-Anpassungseben-Layers|Feature|
|PSDNET-34|Implementierung der Darstellung des Belichtungs-Anpassungseben-Layers für den Export.|Feature|
|PSDNET-31|Hinzufügen der Unterstützung für den Export des ChannelMixer-Anpassungsebenen-Layers|Feature|
|PSDNET-26|Hinzufügen der Unterstützung für Clipping-Masken|Feature|
|PSDNET-13|Hinzufügen der Unterstützung der Ebenenmasken|Feature|
|PSDNET-9|Hinzufügen der Unterstützung des Fotofilter-Anpassungsebenen-Layers|Feature|
|PSDNET-8|Hinzufügen der Unterstützung für den Channel-Mixer-Anpassungsebenen-Layer|Feature|
|PSDNET-7|Hinzufügen der Unterstützung der Belichtungs-Anpassungsebenen-Layer|Feature|
|PSDNET-6|Hinzufügen der Unterstützung des Helligkeit/Kontrast-Anpassungsebenen-Layers|Feature|
|PSDNET-5|Teilweise Unterstützung von Anpassungsebenen|Feature|
|PSDNET-3|Hinzufügen der Unterstützung für die PSD-Option "Kein Zeilenumbruch"|Feature|
|PSDNET-2|Möglichkeit, Textlayer zur Laufzeit hinzuzufügen|Feature|
|PSDNET-62|Das TIFF-Codec kann kein 16-Bit-Kanalbild speichern|Verbesserung|
|PSDNET-61|Die Speicherung des PSD-Bildes liefert ungültige Bildfarben|Verbesserung|
|PSDNET-60|Koordinate der linken oberen Ecke ist bei der Aktualisierung inkorrekt|Verbesserung|
|PSDNET-59|Ausnahme beim Aktualisieren von Textlayern|Verbesserung|
|PSDNET-58|Exponieren der Codec-Eigenschaft des JPEG2000-Bilds für die Öffentlichkeit|Verbesserung|
|PSDNET-57|Beheben der 24-Bit-Optionseinstellung für den Export nach BMP|Verbesserung|
|PSDNET-46|Anpassungsebene wird bei der Konvertierung von CMYK-PSD in TIFF oder JPG ignoriert|Verbesserung|

## **Beispiele zum Verwenden:**
**PSDNET-68 Unterstützung der LayerCreationDateTime-Eigenschaft**

{{< highlight java >}}

    // Beispiel für die Verwendung der LayerCreationDateTime-Eigenschaft

    string sourceFileName = "OneLayer.psd";

    using (var im = (PsdImage)(Image.Load(sourceFileName)))
    {

        var layer = im.Layers[0];

        var creationDateTime = layer.LayerCreationDateTime;

        var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

        Assert.AreEqual(expectedDateTime, creationDateTime);

        var now = DateTime.Now;

        var createdLayer = im.AddLevelsAdjustmentLayer();

        // Überprüfen, ob das Erstellungsdatum in neu erstellten Ebenen aktualisiert wurde

        Assert.True(now <= createdLayer.LayerCreationDateTime);
    }
{{< /highlight >}}

**PSDNET-67 Unterstützung der SheetColor-Hervorhebung**

{{< highlight java >}}

    // Beispiel für die Verwendung der SheetColorHighlight-Eigenschaft

    string sourceFileName = "SheetColorHighlightExample.psd";

    string exportPath = "SheetColorHighlightExampleChanged.psd";

    using (var im = (PsdImage)(Image.Load(sourceFileName)))
    {

        var layer1 = im.Layers[0];

        Assert.AreEqual(SheetColorHighlightEnum.Violett, layer1.SheetColorHighlight);

        var layer2 = im.Layers[1];

        Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);

        layer1.SheetColorHighlight = SheetColorHighlightEnum.Gelb;

        im.Save(exportPath);	
    }
{{< /highlight >}}

**PSDNET-66 Möglichkeit, Ebenen miteinander zu verschmelzen**

{{< highlight java >}}

    // Verschmelzen von zwei Ebenen

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

**PSDNET-65 Teilweise Unterstützung der Textlayer BoundBox-Eigenschaft**

{{< highlight java >}}

    // Beispiel für Text-BoxBounds

    string sourceFileName = "LayerWithText.psd";

    var correctOpticalSize = new Size(127, 45);

    var correctBoundBox = new Size(172, 62);

    using (var im = (PsdImage)(Image.Load(sourceFileName)))
    {

        var textLayer = (TextLayer)im.Layers[1];

        // Die Größe der Ebene entspricht der Größe des gerenderten Bereichs

        var opticalSize = textLayer.Size;

        Assert.AreEqual(correctOpticalSize, opticalSize);

        // TextBoundBox ist die maximale Ebenengröße für den Textlayer. 

        // Hier wird versucht, Ihren Text anzupassen

        var boundBox = textLayer.TextBoundBox;

        Assert.AreEqual(correctBoundBox, boundBox);
    }
{{< /highlight >}}

**PSDNET-64 Hinzufügen der Unterstützung für IopaResource**

{{< highlight java >}}

    // Ändern der Fülldeckkraft-Eigenschaft durch die Änderung von IopaResource

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

**PSDNET-56 Unterstützung von Ebeneneffekten für das PSD-Format**

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

**PSDNET-55 InterruptMonitor-Unterstützung für .Net**

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

                // Die Zeitüberschreitung sollte kürzer sein als die Zeit, die für die vollständige Bildkonvertierung erforderlich ist.

                System.Threading.Thread.Sleep(3000);

                // Prozess unterbrechen

                monitor.Interrupt();

                System.Console.WriteLine("Unterbrechen des Speicherthreads #{0} um {1}", thread.ManagedThreadId, System.DateTime.Now);

                //Auf die Unterbrechung warten...

                thread.Join();

            }

            finally

            {

                // Falls die zu löschende Datei nicht existiert, wird keine Exception ausgelöst.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// Initiieren der Bildkonvertierung und Warten auf ihre Unterbrechung.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Der Pfad zum Eingabebild.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Der Pfad zum Ausgabebild.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Der Unterbrechungsmonitor.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Die Speicheroptionen.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Initialisiert eine neue Instanz der Klasse <see cref="SaveImageWorker" />.

            /// </summary>

            /// <param name="inputPath">Der Pfad zum Eingabebild.</param>

            /// <param name="outputPath">Der Pfad zum Ausgabebild.</param>

            /// <param name="saveOptions">Die Speicheroptionen.</param>

            /// <param name="monitor">Der Unterbrechungsmonitor.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Versucht, das Bild von einem Format in ein anderes zu konvertieren. Behandelt Unterbrechungen. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Unterbrechung erwartet.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("Der Speicherthread #{0} endet um {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

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

**PSDNET-50 Möglichkeit, Ebenen zu vereinfachen**

{{< highlight java >}}

    // Gesamte PSD vereinfachen

    string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

    string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

    using (var im = (PsdImage)(Image.Load(sourceFileName)))
    {

        im.FlattenImage();

        im.Save(exportPath);	 
    }

    // Eine Ebene in eine andere einfügen

    string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

    string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

    using (var im = (PsdImage)(Image.Load(sourceFileName)))
    {

        var bottomLayer = im.Layers[0];

        var middleLayer = im.Layers[1];

        var topLayer = im.Layers[2];

        var layer1 = im.MergeLayers(bottomLayer, middleLayer);

        var layer2 = im.MergeLayers(layer1, topLayer);

        // Zusammengeführte Ebenen einrichten

        im.Layers = new Layer[] { layer2 };

        im.Save(exportPath);	 
    }
{{< /highlight >}}

**PSDNET-49 Hinzufügen der Darstellung der Fülldeckkraft-Eigenschaft in Ebenen.**

{{< highlight java >}}

    // Ändern der Fülldeckkraft-Eigenschaft

    string sourceFileName = "FillOpacitySample.psd";

    string exportPath = "FillOpacitySampleChanged.psd";

    using (var im = (PsdImage)(Image.Load(sourceFileName)))
    {

        var layer = im.Layers[2];

        layer.FillOpacity = 5;

        im.Save(exportPath);	
    }
{{< /highlight >}}

**PSDNET-43 Implementierung der Darstellung des Kurven-Anpassungseben-Layers**

{{< highlight java >}}

    // Kurvenebenenbearbeitung

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



    // PSD speichern

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // PNG speichern

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);
}
{{< /highlight >}}

**PSDNET-42 Hinzufügen der Unterstützung des Kurven-Anpassungseben-Layers**

{{< highlight java >}}

    // Kurvenebenenbearbeitung

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



    // PSD speichern

    im.Save(psdPathAfterChange + j.ToString() + ".psd");
}
{{< /highlight >}}

**PSDNET-41 Implementierung der Darstellung des Levels-Anpassungseben-Layers**

{{< highlight java >}}

    // Ebenenbearbeitung

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

                channel.InputShadow Level = 230;

                channel.OutputShadowLevel = 20;

                channel.OutputHighlightLevel = 200;

            }

        }



        // PSD speichern

        im.Save(psdPathAfterChange);



        // PNG speichern

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        im.Save(pngExportPath, saveOptions);

    }
{{< /highlight >}}

**PSDNET-40 Hinzufügen der Unterstützung des Levels-Anpassungseben-Layers**

{{< highlight java >}}

    // Ebenenbearbeitung

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



        // PSD speichern

        im.Save(psdPathAfterChange);

    }
{{< /highlight >}}

**PSDNET-37 Hinzufügen der Unterstützung des Kanalmixer-Anpassungseben-Layers**

{{< highlight java >}}

    // RGB-Kanalmixer

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

    // CMYK-Kanalmixer

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



    // Hinzufügen der neuen Ebene (Cmyk für dieses Beispiel)

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