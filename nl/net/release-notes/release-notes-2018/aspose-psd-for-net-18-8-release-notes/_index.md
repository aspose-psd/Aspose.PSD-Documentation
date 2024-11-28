---
title: Aspose.PSD voor .NET 18.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/net/aspose-psd-voor-net-18-8-release-opmerkingen/
---

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-68|Ondersteuning van de eigenschap LayerCreationDateTime.|Functie|
|PSDNET-67|Ondersteuning van het markeren van SheetColor|Functie|
|PSDNET-66|Mogelijkheid om lagen samen te voegen|Functie|
|PSDNET-65|Gedeeltelijke ondersteuning van de eigenschap Text Layer BoundBox|Functie|
|PSDNET-64|Toevoegen van ondersteuning voor IopaResource|Functie|
|PSDNET-56|Ondersteuning van laageffecten voor PSD-indeling|Functie|
|PSDNET-55|Ondersteuning van InterruptMonitor voor .Net|Functie|
|PSDNET-50|Mogelijkheid om lagen samen te voegen|Functie|
|PSDNET-49|Toevoegen van de weergave van de vuldoorzichtigheidseigenschap in lagen.|Functie|
|PSDNET-43|Implementatie van de weergave van Curves Adjustment Layer|Functie|
|PSDNET-42|Toevoegen van ondersteuning voor Curves Adjustment Layer|Functie|
|PSDNET-41|Implementatie van de weergave van Levels Adjustment Layer|Functie|
|PSDNET-40|Toevoegen van ondersteuning voor Levels Adjustment Layer|Functie|
|PSDNET-37|Toevoegen van ondersteuning voor Channel Mixer Adjustment Layer|Functie|
|PSDNET-35|Toevoegen van ondersteuning voor Hue/Saturation Adjustment Layer|Functie|
|PSDNET-34|Implementatie van de weergave van Exposure Adjustment Layer voor export.|Functie|
|PSDNET-31|Toevoegen van ondersteuning voor export van ChannelMixer-afstemmingseffectlaag|Functie|
|PSDNET-26|Ondersteuning toevoegen van Clipping mask|Functie|
|PSDNET-13|Ondersteuning toevoegen van de laagmasker|Functie|
|PSDNET-9|Toevoegen van ondersteuning voor Photo Filter aanpassingslaag|Functie|
|PSDNET-8|Toevoegen van ondersteuning voor Channel mixer afstemmingseffectlaag|Functie|
|PSDNET-7|Toevoegen van ondersteuning voor Exposure aanpassingslaag|Functie|
|PSDNET-6|Toevoegen van ondersteuning voor Brightness/Contrast aanpassingslaag|Functie|
|PSDNET-5|Gedeeltelijke ondersteuning toevoegen van aanpassingslagen|Functie|
|PSDNET-3|Toevoegen van ondersteuning voor PSD NoBreak-tekstoptie|Functie|
|PSDNET-2|Mogelijkheid om tekstlaag toe te voegen tijdens runtime|Functie|
|PSDNET-62|TIFF-codec kan geen 16-bits kanaalbeeld opslaan|Verbetering|
|PSDNET-61|Opslaan van PSD-beeld produceert ongeldige afbeeldingskleuren|Verbetering|
|PSDNET-60|Coördinaat van linkerbovenhoek is incorrect bij bijwerken|Verbetering|
|PSDNET-59|Uitzondering bij bijwerken van tekstlagen|Verbetering|
|PSDNET-58|Blootstellen Codec-eigenschap van JPEG2000-beeld naar openbaar|Verbetering|
|PSDNET-57|Fix 24bpp-opties instellen voor export naar BMP|Verbetering|
|PSDNET-46|Aanpassingslaag genegeerd voor CMYK PSD-conversie naar TIFF of JPG|Verbetering|

## **Gebruik voorbeelden:**
**PSDNET-68 Ondersteuning van de eigenschap LayerCreationDateTime**

{{< highlight java >}}

 // Voorbeeld van het gebruik van LayerCreationDateTime-eigenschap

string sourceFileName = "EenLaag.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var laag = im.Lagen[0];

    var creationDateTime = laag.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var nu = DateTime.Now;

    var gemaakteLaag = im.AddLevelsAdjustmentLayer();

    // Controleren of de creatiedatum en tijd is bijgewerkt op nieuw gemaakte lagen

    Assert.True(nu <= gemaakteLaag.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Ondersteuning van het markeren van SheetColor Highlighting**

{{< highlight java >}}

 // Voorbeeld van het gebruik van de SheetColorHighlight-eigenschap

string sourceFileName = "VoorbeeldVanSheetColorHighlight.psd";

string exportPath = "GewijzigdVoorbeeldVanSheetColorHighlight.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var laag1 = im.Lagen[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, laag1.SheetColorHighlight);

    var laag2 = im.Lagen[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, laag2.SheetColorHighlight);



    laag1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);  

}

{{< /highlight >}}

**PSDNET-66 Mogelijkheid om lagen samen te voegen**

{{< highlight java >}}

 // Voorbeeld van het samenvoegen van twee lagen

var sourceFile1 = "VoorbeeldVanFillOpacity.psd";

var sourceFile2 = "DrieReguliereLagenHalfDoorzichtig.psd";

var exportPath = "SamengevoegdeLagenUitTweeVerschillendePsd.psd";

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var laag1 = im1.Lagen[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var laag2 = im2.Lagen[0];

        laag1.MergeLayerTo(laag2);

        im2.Save(exportPath);  

    }

}

{{< /highlight >}}

**PSDNET-65 Gedeeltelijke ondersteuning van de eigenschap Text Layer BoundBox**

{{< highlight java >}}

 // Voorbeeld van Tekst BoundBox

string sourceFileName = "LaagMetTekst.psd";

var correcteOptischeGrootte = new Size(127, 45);

var correcteBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var tekstLaag = (TekstLaag)im.Lagen[1];

    // De grootte van de laag is de grootte van het weergegeven gebied

    var optischeGrootte = tekstLaag.Grootte;

    Assert.AreEqual(correcteOptischeGrootte, optischeGrootte);

    // TextBoundBox is de maximale laaggrootte voor Text Layer. 

    // In dit gebied zal PS proberen uw tekst te passen

    var boundBox = tekstLaag.TextBoundBox;

    Assert.AreEqual(correcteBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Toevoegen van ondersteuning voor IopaResource**

{{< highlight java >}}

 // Verandering van de vuldoorzichtigheidseigenschap door de IopaResource-wijziging

string sourceFileName = "VoorbeeldVanFillOpacity.psd";

string exportPath = "GewijzigdVoorbeeldVanFillOpacity.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var laag = im.Lagen[2];



    var resources = laag.Resources;

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

**PSDNET-56 Ondersteuning van laageffecten voor PSD-indeling**

{{< highlight java >}}

 using (

    PsdImage afbeelding = 

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    afbeelding.Save(

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

**PSDNET-55 InterruptMonitor ondersteuning voor .Net**

{{< highlight java >}}

         public void InterruptMonitorTest(string map, string uitvoerMap)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(map + "groot.psb", map + "groot_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // De time-out moet minder zijn dan de tijd die nodig is voor volledige afbeeldingsconversie (zonder onderbreking).

                System.Threading.Thread.Sleep(3000);

                // Onderbreek het proces

                monitor.Onderbreken();

                System.Console.WriteLine("Onderbreek de opslagthread #{0} op {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Wachten op onderbreking...

                thread.Join();

            }

            finally

            {

                // Als het te verwijderen bestand niet bestaat, wordt er geen uitzondering gegenereerd.

                System.IO.File.Delete(map + "groot_out.png");

            }

        }

        /// <summary>

        /// Start beeldconversie en wacht op onderbreking.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Het pad naar de invoerafbeelding.

            /// </summary>

            privé readonly string inputPad;

            /// <summary>

            /// Het pad naar de uitvoerafbeelding.

            /// </summary>

            privé readonly string uitvoerPad;

            /// <summary>

            /// De onderbrekingsmonitor.

            /// </summary>

            privé readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// De opslagopties.

            /// </summary>

            privé readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Initialiseert een nieuw exemplaar van de klasse SaveImageWorker.

            /// </summary>

            /// <param name="inputPath">Het pad naar de invoerafbeelding.</param>

            /// <param name="outputPath">Het pad naar de uitvoerafbeelding.</param>

            /// <param name="saveOptions">De opslagopties.</param>

            /// <param name="monitor">De onderbrekingsmonitor.</param>

            public SaveImageWorker(string inputPad, string uitvoerPad, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                dit.inputPad = inputPad;

                dit.uitvoerPad = uitvoerPad;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Probeert de afbeelding van het ene formaat naar het andere te converteren. Handelt onderbreking af. 

            /// </summary>

            public void ThreadProc()

            {

                Gebruikmakend van afbeelding = Beeld.Laden(this.inputPad)

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    probeer

                    {

                        image.Save(this.uitvoerPad, this.saveOptions);

                        Assert.Fail("Onderbreking verwacht.");

                    }

                    vangt (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("De opslagthread #{0} eindigt op {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    vangt (Systeem.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    ten slotte

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 Mogelijkheid om lagen samen te voegen**

{{< highlight java >}}

 // Samenvoegen van hele PSD

string sourceFileName = "DrieReguliereLagenHalfDoorzichtig.psd";

string exportPath = "DrieReguliereLagenHalfDoorzichtigSamengevoegd.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);    

}

// Voeg een laag samen in een andere

string sourceFileName = "DrieReguliereLagenHalfDoorzichtig.psd";

string exportPath = "DrieReguliereLagenHalfDoorzichtigPerLaagSamengevoegd.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var ondersteLaag = im.Lagen[0];

    var middelsteLaag = im.Lagen[1];

    var bovensteLaag = im.Lagen[2];

    var laag1 = im.MergeLayers(ondersteLaag, middelsteLaag);

    var laag2 = im.MergeLayers(laag1, bovensteLaag);

    // Stel samengevoegde lagen in

    im.Lagen = new Laag[] { laag2 };



    im.Save(exportPath);    

}

{{< /highlight >}}

**PSDNET-49 Toevoegen van de weergave van de vuldoorzichtigheidseigenschap in lagen.**

{{< highlight java >}}

 // Verander de vuldoorzichtigheidseigenschap

string sourceFileName = "VoorbeeldVanFillOpacity.psd";

string exportPath = "GewijzigdVoorbeeldVanFillOpacity.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var laag = im.Lagen[2];

    laag.FillOpacity = 5;

    im.Save(exportPath);   

}

{{< /highlight >}}

**PSDNET-43 Implementatie van de weergave van Curves Adjustment Layer**

{{< highlight java >}}

 // Curvenlaag bewerking

string sourceFileName = "CurvesAdjustmentLayer";

string psdPadNaWijziging = "GewijzigdCurvesAdjustmentLayer";

string pngExportPad = "GewijzigdCurvesAdjustmentLayer";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var laag in im.Lagen)

    {

            if (laag is CurvesLayer)

        {

                 var curvesLayer = (CurvesLayer)laag;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 anders

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }



    // Opslaan PSD

    im.Save(psdPadNaWijziging + j.ToString() + ".psd");



    // Opslaan PNG

    var saveOpties = nieuwe PngOpties();

    saveOpties.Kleurtype = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPad + j.ToString() + ".png", saveOpties);

}

{{< /highlight >}}

**PSDNET-42 Toevoegen van ondersteuning voor Curves Adjustment Layer**

{{< highlight java >}}

 // Curvenlaag bewerking

string sourceFileName = "CurvesAdjustmentLayer";

string psdPadNaWijziging = "GewijzigdCurvesAdjustmentLayer";

voor (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

         foreach (var laag in im.Lagen)

    {

            if (laag is CurvesLayer)

        {

                 var curvesLayer = (CurvesLayer)laag;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 anders

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

    }

    }



    // Opslaan PSD

    im.Save(psdPadNaWijziging + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Implementatie van de weergave van Levels Adjustment Layer**

{{< highlight java >}}

 // Levelslag bewerking

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPadNaWijziging = "GewijzigdLevelsAdjustmentLayer.psd";

string pngExportPad = "GewijzigdLevelsAdjustmentLayer.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var laag in im.Lagen)

    {

        if (laag is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)laag;

            var kanaal = levelsLayer.GetChannel(0);

            kanaal.InputMidtoneLevel = 2.0f;

            kanaal.InputShadowLevel = 10;

            kanaal.InputHighlightLevel = 230;

            kanaal.OutputShadowLevel = 20;

            kanaal.OutputHighlightLevel = 200;

        }

    }



    // Opslaan PSD

    im.Save(psdPadNaWijziging);



    // Opslaan PNG

    var saveOpties = nieuwe PngOpties();

    saveOpties.Kleurtype = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPad, saveOpties);

}

**PSDNET-40 Toevoegen van ondersteuning voor Levels Adjustment Layer**

{{< highlight java >}}

 // Levelslaag bewerking

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPadNaWijziging = "GewijzigdLevelsAdjustmentLayer.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var laag in im.Lagen)

    {

        if (laag is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)laag;

            var kanaal = levelsLayer.GetChannel(0);

            kanaal.InputMidtoneLevel = 2.0f;

            kanaal.InputShadowLevel = 10;

            kanaal.InputHighlightLevel = 230;

            kanaal.OutputShadowLevel = 20;

            kanaal.OutputHighlightLevel = 200;

        }

    }



    // Opslaan PSD

    im.Save(psdPadNaWijziging);

}

{{< /highlight >}}

**PSDNET-37 Toevoegen van ondersteuning voor Channel Mixer Adjustment Layer**

{{< highlight java >}}

// Rgb Kanaalmixer

string sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

string psdPadNaWijziging = "GewijzigdChannelMixerAdjustmentLayerRgb.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var laag in im.Lagen)

    {

         if (laag is RgbChannelMixerLayer)

         {

              var rgbLaag = (RgbChannelMixerLayer)laag;

              rgbLaag.RedChannel.Blue = 100;

              rgbLaag.BlueChannel.Green = -100;

              rgbLaag.GreenChannel.Constant = 50;

         }

    }



    im.Save(psdPadNaWijziging);

}

// Cmyk Kanaalmixer

string sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

string psdPadNaWijziging = "GewijzigdChannelMixerAdjustmentLayerCmyk.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var laag in im.Lagen)

    {

         if (laag is CmykChannelMixerLayer)

         {

             var cmykLaag = (CmykChannelMixerLayer)laag;

             cmykLaag.CyanChannel.Black = 20;

             cmykLaag.MagentaChannel.Yellow = 50;

             cmykLaag.YellowChannel.Cyan = -25;

             cmykLaag.BlackChannel.Yellow = 25;

         }

    }



    im.Save(psdPadNaWijziging);

}



// Het toevoegen van de nieuwe laag(Cmyk in dit voorbeeld)

string sourceFileName = "CmykMetAlpha.psd";

string psdPadNaWijziging = "GewijzigdChannelMixerAdjustmentLayerCmyk.psd";

using (var im = LoadFile(sourceFileName))

{

    var nieuweLaag = im.AddChannelMixerAdjustmentLayer();

    nieuweLaag.GetChannelByIndex(2).Constant = 50;

    nieuweLaag.GetChannelByIndex(0).Constant = 50;



    im.Save(psdPadNaWijziging);

}    

{{< /highlight >}}

**PSDNET-35 Toevoegen van ondersteuning voor Hue/Saturation Adjustment Layer**

{{< highlight java >}}

 // HSL-laagbewerking

string sourceFileName = "HueSaturationAdjustmentLayer.psd";

string psdPadNaWijziging = "GewijzigdHueSaturationAdjustmentLayer.psd";

using (var im = LoadFile(sourceFileName))

{

     foreach (var laag in im.Lagen)

     {

           if (laag is HueSaturationLayer)

           {

                var hueLaag = (HueSaturationLayer)laag;

                hueLaag.Hue = -25;

                hueLaag.Saturation = -12;

                hueLaag.Lightness = 67;

                var kleurbereik = hueLaag.GetRange(2);

                kleurbereik.Hue = -40;

                kleurbereik.Saturation = 50;

                kleurbereik.Lightness = -20;

                kleurbereik.MostLeftBorder = 300;

           }

      }

      im.Save(psdPadNaWijziging);

}



// HSL-laag toevoegen

string sourceFileName = "VoorbeeldFoto.psd";

string psdPadNaWijziging = "VoorbeeldFotoToegevoegdHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveVoorVisueleTest(im, this.UitvoerPad, voorvoegsel + bestand, "voor");

     var hueLaag = im.AddHueSaturationAdjustmentLayer();

     hueLaag.Hue = -25;

     hueLaag.Saturation = -12;

     hueLaag.Lightness = 67;

     var kleurbereik = hueLaag.GetRange(2);

     kleurbereik.Hue = -160;

     kleurbereik.Saturation = 100;

     kleurbereik.Lightness = 20;

     kleurbereik.MostLeftBorder = 300;



     im.Save(psdPadNaWijziging);

}

{{< /highlight >}}