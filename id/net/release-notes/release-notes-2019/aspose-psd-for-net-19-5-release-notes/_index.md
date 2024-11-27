---
title: Catatan Rilis Aspose.PSD untuk .NET 19.5
type: docs
weight: 80
url: /id/net/aspose-psd-for-net-19-5-release-notes/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk Aspose.PSD untuk .NET 19.5

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-133|Menambahkan dukungan untuk layer Pengisian: Pola|Fitur|
|PSDNET-138|Dukungan untuk PtFlResource|Fitur|
|PSDNET-129|Menerapkan metode Pemangkasan yang benar untuk file PSD|Fitur|
|PSDNET-140|Dukungan untuk VsmsResource|Fitur|
|PSDNET-121|Layer Terlihat di Subfolder Terlihat dalam Folder Tak Terlihat dirender, tetapi seharusnya tidak|Bug|
|PSDNET-119|PSD (mode RGB 16 bit per saluran) tidak dikonversi dengan benar ke JPG|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternHeight
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternHeight
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.#ctor(System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.IsLinkedWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternId
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.TypeToolKey
-M:Aspose.PSD.Image.DoAfterCreate(System.Int64@,System.Int64)
- P:Aspose.PSD.ImageOptionsBase.BufferSizeHint
- M:Aspose.PSD.Metered.GetConsumptionCredit
# **API Dihapus:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Contoh Penggunaan:**
**PSDNET-133. Menambahkan dukungan untuk layer Pengisian: Pola**

{{< highlight java >}}

 // Menambahkan dukungan untuk layer Pengisian: Pola

    string sourceFileName = "LayerPengisianPola.psd";

    string exportPath = "LayerPengisianPola_Diedit.psd";

    double tolerance = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                  FillLayer fillLayer = (FillLayer)layer;

                  PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                  if (fillSettings.HorizontalOffset != -46 || 

                      fillSettings.VerticalOffset != -45 || 

                      fillSettings.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      fillSettings.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      fillSettings.AlignWithLayer != true ||

                      fillSettings.Linked != true ||

                      fillSettings.PatternHeight != 64 ||

                      fillSettings.PatternWidth != 64 ||

                      fillSettings.PatternData.Length != 4096 ||

                      Math.Abs(fillSettings.Scale - 50) > tolerance) 

                      {

                          throw new Exception("Gambar PSD dibaca dengan salah");

                      }

                  // Pengeditan 

                  fillSettings.Scale = 300;

                  fillSettings.HorizontalOffset = 2;

                  fillSettings.VerticalOffset = -20;

                  fillSettings.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  fillSettings.PatternHeight = 3;

                  fillSettings.PatternWidth = 3;

                  fillSettings.AlignWithLayer = false;

                  fillSettings.Linked = false;

                  fillSettings.PatternId = Guid.NewGuid().ToString();

                  fillLayer.Update();

                  break;

             }

         }

         im.Save(exportPath);

    }

{{< /highlight >}}

**PSDNET-138. Dukungan untuk PtFlResource**

{{< highlight java >}}

  // Dukungan untuk PtFlResource

    string sourceFileName = "LayerPengisianPola.psd";

    string exportPath = "PtFlResource_Diedit.psd";

    double tolerance = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                var fillLayer = (FillLayer)layer;

                var resources = fillLayer.Resources;

                foreach (var res in resources)

                {

                    if (res is PtFlResource)

                    {

                        // Membaca

                        PtFlResource resource = (PtFlResource)res;

                        if (

                            resource.Offset.X != -46 || 

                            resource.Offset.Y != -45 || 

                            resource.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            resource.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            resource.AlignWithLayer != true ||

                            resource.IsLinkedWithLayer != true ||

                            !(Math.Abs(resource.Scale - 50) < tolerance)) {

                                throw new Exception("PtFl Resource dibaca dengan tidak benar");

                            }

                        // Pengeditan

                        resource.Offset = new Point(-11, 13);

                        resource.Scale = 200;

                        resource.AlignWithLayer = false;

                        resource.IsLinkedWithLayer = false;

                        fillLayer.Resources = fillLayer.Resources;

                        // Kami tidak memiliki data pola di PattResource, jadi kami bisa menambahkannya.

                        var fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                        fillSettings.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        fillSettings.PatternHeight = 1;

                        fillSettings.PatternWidth = 4;

                        fillSettings.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        fillSettings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                    }

                    break;

                }

                break;

            }

         }

         im.Save(exportPath);

    } 

{{< /highlight >}}

**PSDNET-129. Menerapkan metode Pemangkasan yang benar untuk file PSD**

{{< highlight java >}}

             // Menerapkan metode Pemangkasan yang benar untuk file PSD.

            string sourceFileName = "1.psd";

            string exportPathPsd = "UjiPemangkasan.psd";

            string exportPathPng = "UjiPemangkasan.png";

            using (RasterImage image = Image.Load(sourceFileName) as RasterImage)

            {

                image.Crop(new Rectangle(10, 30, 100, 100));

                image.Save(exportPathPsd, new PsdOptions());

                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Dukungan untuk VsmsResource**

{{< highlight java >}}

 // Dukungan untuk VsmsResource

        static void ContohDukunganVsmsResource()

        {

            string sourceFileName = "PersegiKosong.psd";

            string exportPath = "PersegiKosong_diubah.psd";

            var im = (PsdImage)Image.Load(sourceFileName);

            using (im)

            {

                var resource = GetVsmsResource(im);

                // Membaca

                if (resource.IsDisabled != false ||

                    resource.IsInverted != false ||

                    resource.IsNotLinked != false ||

                    resource.Paths.Length != 7 ||

                    resource.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    resource.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    resource.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    resource.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    resource.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    resource.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    resource.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("VsmsResource dibaca dengan salah");

                }

                var pathFillRule = (PathFillRuleRecord)resource.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)resource.Paths[1];

                var subpathLength = (LengthRecord)resource.Paths[2];

                // Aturan pengisian path tidak mengandung informasi tambahan

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("Path VsmsResource dibaca dengan salah");

                }

                // Pengeditan

                resource.IsDisabled = true;

                resource.IsInverted = true;

                resource.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)resource.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)resource.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                im.Save(exportPath);

            }         

        }

        static VsmsResource GetVsmsResource(PsdImage image)

        {

            var layer = image.Layers[1];

            VsmsResource resource = null;

            var resources = layer.Resources;

            for (int i = 0; i < resources.Length; i++)

            {

                if (resources[i] is VsmsResource)

                {

                    resource = (VsmsResource)resources[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("VsmsResource tidak ditemukan");

            }

            return resource;

        }   

{{< /highlight >}}

**PSDNET-121: Layer Terlihat di Subfolder Terlihat dalam Folder Tak Terlihat dirender, tetapi seharusnya tidak**

{{< highlight java >}}

 // Layer Terlihat di Subfolder Terlihat dalam Folder Tak Terlihat dirender, tetapi seharusnya tidak

            string sourceFileName = "BanyakFolder.psd.psd";

            string outputFilePathJpg = "outBanyakFolder.jpg";

            string outputFilePathPsd = "outBanyakFolder.psd";

            var options = new PsdLoadOptions();

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

            {

                image.Save(outputFilePathPsd, new PsdOptions(image));

                image.Save(outputFilePathJpg, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}

**PSDNET-119. PSD (mode RGB 16 bit per saluran) tidak dikonversi dengan benar ke JPG**

{{< highlight java >}}

  // Psd tidak dikonversi dengan benar ke jpg

            string sourceFileName = "dalam.psd";

            string exportPath = "keluarRgb.jpg";

            var options = new PsdLoadOptions();

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

            {

                image.Save(exportPath, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}
