---
title: Catatan Rilis Aspose.PSD untuk .NET 18.8
type: docs
weight: 50
url: /id/net/aspose-psd-for-net-18-8-release-notes/
---

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-68|Dukungan untuk properti LayerCreationDateTime.|Fitur|
|PSDNET-67|Dukungan untuk Highlighting Warna SheetColor|Fitur|
|PSDNET-66|Kemampuan untuk menggabungkan layer satu dengan yang lain|Fitur|
|PSDNET-65|Menambahkan dukungan parsial properti BoundBox Layer Teks|Fitur|
|PSDNET-64|Menambahkan dukungan untuk IopaResource|Fitur|
|PSDNET-56|Dukungan untuk Efek Layer untuk format PSD|Fitur|
|PSDNET-55|Dukungan Monitor Interupsi untuk .Net|Fitur|
|PSDNET-50|Membuat kemungkinan meratakan layer|Fitur|
|PSDNET-49|Menambahkan pengaturan opasitas pengisian dalam layer.|Fitur|
|PSDNET-43|Menerapkan rendering dari Kurva Penyesuaian Layer|Fitur|
|PSDNET-42|Menambahkan dukungan dari Kurva Penyesuaian Layer|Fitur|
|PSDNET-41|Menerapkan rendering dari Layer Penyesuaian Level|Fitur|
|PSDNET-40|Menambahkan dukungan dari Layer penyesuaian Level|Fitur|
|PSDNET-37|Menambahkan dukungan dari Layer Penyesuaian Mixer Saluran|Fitur|
|PSDNET-35|Menambahkan dukungan dari Layer Penyesuaian Hue/Saturasi|Fitur|
|PSDNET-34|Menerapkan rendering dari Layer Penyesuaian Paparan untuk ekspor.|Fitur|
|PSDNET-31|Menambahkan dukungan untuk eksport dari ChannelMixer adjustment layer|Fitur|
|PSDNET-26|Menambahkan dukungan dari masker Pengguntingan|Fitur|
|PSDNET-13|Menambahkan dukungan dari layer mask|Fitur|
|PSDNET-9|Menambahkan dukungan dari layer penyesuaian Filter Foto|Fitur|
|PSDNET-8|Menambahkan dukungan dari layer penyesuaian Channel Mixer|Fitur|
|PSDNET-7|Menambahkan dukungan dari layer penyesuaian Paparan|Fitur|
|PSDNET-6|Menambahkan dukungan dari layer penyesuaian Kecerahan/Kontras|Fitur|
|PSDNET-5|Menambahkan dukungan parsial dari layers penyesuaian|Fitur|
|PSDNET-3|Menambahkan dukungan untuk opsi teks PSD NoBreak|Fitur|
|PSDNET-2|Kemampuan untuk menambahkan Layer Teks saat runtime|Fitur|
|PSDNET-62|Codec TIFF tidak dapat menyimpan gambar kanal 16-bit|Peningkatan|
|PSDNET-61|Menyimpan gambar PSD menghasilkan warna gambar yang tidak valid|Peningkatan|
|PSDNET-60|Koordinat sudut kiri atas tidak benar pada pembaruan|Peningkatan|
|PSDNET-59|Exception saat memperbarui layer teks|Peningkatan|
|PSDNET-58|Expose Properti Codec dari gambar JPEG2000 ke publik|Peningkatan|
|PSDNET-57|Memperbaiki opsi 24bpp untuk ekspor ke BMP|Peningkatan|
|PSDNET-46|Layer penyesuaian diabaikan untuk konversi PSD CMYK ke TIFF atau JPG|Peningkatan|

## **Contoh Penggunaan:**
**PSDNET-68 Dukungan untuk properti LayerCreationDateTime**

{{< highlight java >}}

 // Contoh penggunaan properti LayerCreationDateTime

string sourceFileName = "SatuLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Periksa apakah Tanggal Pembuatan Telah Diperbarui pada layer yang baru dibuat

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Dukungan untuk Highlighting Warna SheetColor**

{{< highlight java >}}

 // Contoh penggunaan properti SheetColorHighlight

string sourceFileName = "ContohSheetColorHighlight.psd";

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

**PSDNET-66 Kemampuan untuk menggabungkan layer satu ke layer lain**

{{< highlight java >}}

 // Contoh penggabungan dua layer

var sourceFile1 = "ContohPengisianOpasitas.psd";

var sourceFile2 = "TigaLayerBiasaSemiTransparan.psd";

var exportPath = "LayerBergabungDariDuaPsdBerbeda.psd" 

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

**PSDNET-65 Menambahkan dukungan parsial dari properti BoundBox Layer Teks**

{{< highlight java >}}

 // Contoh BoundBox TextLayer

string sourceFileName = "LayerDenganTeks.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // Ukuran layer adalah ukuran area yang dirender

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox adalah ukuran maksimum layer untuk Text Layer. 

    // Di dalam area ini PS akan mencoba mencocokkan teks Anda

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Menambahkan dukungan untuk IopaResource**

{{< highlight java >}}

 // Mengubah properti Opasitas Pengisian melalui perubahan IopaResource

string sourceFileName = "ContohPengisianOpasitas.psd";

string exportPath = "ContohPengisianOpasitasBerubah.psd";

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

**PSDNET-56 Dukungan Efek Layer untuk format PSD**

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

**PSDNET-55 Dukungan Monitor Interupsi untuk .Net**

{{< highlight java >}}

         public void UjiMonitorInterupsi(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "besar.psb", dir + "besar_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // Batas waktu harus kurang dari waktu yang dibutuhkan untuk konversi gambar lengkap (tanpa interupsi).

                System.Threading.Thread.Sleep(3000);

                // Interupsi proses

                monitor.Interrupt();

                System.Console.WriteLine("Menginterupsi thread simpan #{0} di {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Tunggu untuk interupsi...

                thread.Join();

            }

            finally

            {

                // Jika file yang akan dihapus tidak ada, tidak ada pengecualian yang dilemparkan.

                System.IO.File.Delete(dir + "besar_out.png");

            }

        }

        /// <summary>

        /// Memulai konversi gambar dan menunggu interupsinya.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Path ke gambar masukan.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Path ke gambar keluaran.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Monitor interupsi.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Opsi penyimpanan.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Inisialisasi instance baru dari kelas SaveImageWorker.

            /// </summary>

            /// <param name="inputPath">Path ke gambar masukan.</param>

            /// <param name="outputPath">Path ke gambar keluaran.</param>

            /// <param name="saveOptions">Opsi penyimpanan.</param>

            /// <param name="monitor">Monitor interupsi.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Mencoba untuk mengonversi gambar dari satu format ke format lain. Menangani interupsi. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Interupsi yang diharapkan.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("Thread simpan #{0} selesai di {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

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

**PSDNET-50 Membuat kemungkinan untuk meratakan layer**

{{< highlight java >}}

 // Meratakan seluruh PSD

string sourceFileName = "TigaLayerBiasaSemiTransparan.psd";

string exportPath = "TigaLayerSemiTransparanMeratakan.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// Menggabungkan satu layer dengan layer lain

string sourceFileName = "TigaLayerBiasaSemiTransparan.psd";

string exportPath = "TigaLayerSemiTransparanPerLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // Menyiapkan lapisan yang digabungkan

    im.Layers = new Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Menambahkan pengaturan opasitas pengisian dalam layer.**

{{< highlight java >}}

 // Mengubah properti Opasitas Pengisian

string sourceFileName = "ContohPengisianOpasitas.psd";

string exportPath = "ContohPengisianOpasitasBerubah.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);

}

{{< /highlight >}}

**PSDNET-43 Menerapkan rendering dari Kurva Penyesuaian Layer**

{{< highlight java >}}

 // Pengeditan layer Kurva

string sourceFileName = "LayerPenyesuaianKurva";

string psdPathAfterChange = "LayerPenyesuaianKurvaBerubah";

string pngExportPath = "LayerPenyesuaianKurvaBerubah";

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



    // Simpan PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // Simpan PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Menambahkan dukungan dari Layer Penyesuaian Kurva**

{{< highlight java >}}

 // Pengeditan layer Kurva

string sourceFileName = "LayerPenyesuaianKurva";

string psdPathAfterChange = "LayerPenyesuaianKurvaBerubah";

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



    // Simpan PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Menerapkan rendering dari Layer Penyesuaian Level**

{{< highlight java >}}

 // Pengeditan layer Level

string sourceFileName = "LayerPenyesuaianLevel.psd";

string psdPathAfterChange = "LayerPenyesuaianLevelBerubah.psd";

string pngExportPath = "LayerPenyesuaianLevelBerubah.png";

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



    // Simpan PSD

    im.Save(psdPathAfterChange);



    // Simpan PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-40 Menambahkan dukungan dari Layer penyesuaian Level**

{{< highlight java >}}

 // Pengeditan layer Level

string sourceFileName = "LayerPenyesuaianLevel.psd";

string psdPathAfterChange = "LayerPenyesuaianLevelBerubah.psd";

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



    // Simpan PSD

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-37 Menambahkan dukungan dari Layer Penyesuaian Mixer Saluran**

{{< highlight java >}}



// Rgb Channel Mixer

string sourceFileName = "ChannelMixerPenyesuaianLayerRgb.psd";

string psdPathAfterChange = "ChannelMixerPenyesuaianLayerRgbBerubah.psd";

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

string sourceFileName = "ChannelMixerPenyesuaianLayerCmyk.psd";

string psdPathAfterChange = "ChannelMixerPenyesuaianLayerCmykBerubah.psd";

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





// Menambahkan layer baru(Cmyk untuk contoh ini)

string sourceFileName = "CmykDenganAlpha.psd";

string psdPathAfterChange = "ChannelMixerPenyesuaianLayerCmykBerubah.psd";

using (var im = LoadFile(sourceFileName))

{

    var newlayer = im.AddChannelMixerAdjustmentLayer();

    newlayer.GetChannelByIndex(2).Constant = 50;

    newlayer.GetChannelByIndex(0).Constant = 50;



    im.Save(psdPathAfterChange);

}		

{{< /highlight >}}

**PSDNET-35 Menambahkan dukungan dari Layer Penyesuaian Hue/Saturasi**

{{< highlight java >}}

 // Pengeditan layer Hue/Saturasi

string sourceFileName = "HueSaturationPenyesuaianLayer.psd";

string psdPathAfterChange = "HueSaturationPenyesuaianLayerBerubah.psd";

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



// Menambahkan layer Hue/Saturasi

string sourceFileName = "ContohFoto.psd";

string psdPathAfterChange = "ContohFotoDitambahkanHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveForVisualTest(im, this.OutputPath, prefix + file, "sebelum");

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

**PSDNET-34 Menerapkan rendering dari Layer Penyesuaian Paparan untuk ekspor.**

{{< highlight java >}}

 // Pengeditan layer Paparan

string sourceFileName = "LayerPenyesuaianExposure.psd";

string psdPathAfterChange = "LayerPenyesuaianExposureBerubah.psd";

string pngExportPath = "LayerPenyesuaianExposureBerubah.png";

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



    // Simpan PSD

    im.Save(psdPathAfterChange);

	end

    // Simpan PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}



// Layer paparan tambahan

string sourceFileName = "ContohFoto.psd";

string psdPathAfterChange = "ContohFotoDitambahkanExposure.psd";

string pngExportPath = "ContohFotoDitambahkanExposure.png";



using (PsdImage im = LoadFile(sourceFileName))

{

     var newlayer = im.AddExposureAdjustmentLayer();

     newlayer.Exposure = 2;

     newlayer.Offset = -0.25f;

     newlayer.GammaCorrection = 2f;



     // Simpan PSD

     im.Save(psdPathAfterChange);



     // Simpan PNG

     var saveOptions = new PngOptions();

     saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

     im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-31 Menambahkan dukungan untuk eksport dari ChannelMixer adjustment layer**

{{< highlight java >}}



// Rgb Channel Mixer

string sourceFileName = "ChannelMixerPenyesuaianLayerRgb.psd";

string psdPathAfterChange = "ChannelMixerPenyesuaianLayerRgbBerubah.psd";

string pngExportPath = "ChannelMixerPenyesuaianLayerRgbBerubah.png";

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



	// Simpan PSD

    im.Save(psdPathAfterChange);



	// Simpan PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

// Cmyk Channel Mixer

string sourceFileName = "ChannelMixerPenyesuaianLayerCmyk.psd";

string psdPathAfterChange = "ChannelMixerPenyesuaianLayerCmykBerubah.psd";

string pngExportPath = "ChannelMixerPenyesuaianLayerCmykBerubah.png";

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



	// Simpan PSD

    im.Save(psdPathAfterChange);



	// Simpan PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}



{{< /highlight >}}