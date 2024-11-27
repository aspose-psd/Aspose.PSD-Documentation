---
title: Notas de la versión de Aspose.PSD para .NET 19.5
type: docs
weight: 80
url: /es/net/aspose-psd-para-net-19-5-notas-de-version/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión de Aspose.PSD para .NET 19.5

{{% /alert %}} 

|**Clave**|**Descripción**|**Categoría**|
| :- | :- | :- |
|PSDNET-133|Agregar soporte de capas de Relleno: Patrón|Característica|
|PSDNET-138|Soporte de PtFlResource|Característica|
|PSDNET-129|Implementar método de Recorte correcto para archivos PSD|Característica|
|PSDNET-140|Soporte de VsmsResource|Característica|
|PSDNET-121|Las capas visibles en la subcarpeta visible en la carpeta invisible se renderizan, pero no deberían|Error|
|PSDNET-119|PSD (modo RGB 16 bits por canal) no se convierte correctamente a JPG|Error|

## **Cambios en la API pública**
# **APIs agregadas:**
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
- M:Aspose.PSD.Image.DoAfterCreate(System.Int64@,System.Int64)
- P:Aspose.PSD.ImageOptionsBase.BufferSizeHint
- M:Aspose.PSD.Metered.GetConsumptionCredit
# **APIs eliminadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Ejemplos de uso:**

**PSDNET-133. Agregar soporte de capas de Relleno: Patrón**

{{< highlight java >}}

 // Agregar soporte de capas de Relleno: Patrón

    string nombreArchivoFuente = "CapaRellenoPatron.psd";

    string rutaExportacion = "CapaRellenoPatron_Editada.psd";

    double tolerancia = 0.0001;

    var im = (PsdImage)Image.Load(nombreArchivoFuente);

    using (im)

    {

         foreach (var capa in im.Layers)

         {

             if (capa is FillLayer)

             {

                  FillLayer capaRelleno = (FillLayer)capa;

                  PatternFillSettings configuracionRelleno = (PatternFillSettings)capaRelleno.FillSettings;

                  if (configuracionRelleno.HorizontalOffset != -46 || 

                      configuracionRelleno.VerticalOffset != -45 || 

                      configuracionRelleno.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      configuracionRelleno.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      configuracionRelleno.AlignWithLayer != true ||

                      configuracionRelleno.Linked != true ||

                      configuracionRelleno.PatternHeight != 64 ||

                      configuracionRelleno.PatternWidth != 64 ||

                      configuracionRelleno.PatternData.Length != 4096 ||

                      Math.Abs(configuracionRelleno.Scale - 50) > tolerancia) 

                      {

                          throw new Exception("La imagen PSD se leyó incorrectamente");

                      }

                  // Edición 

                  configuracionRelleno.Scale = 300;

                  configuracionRelleno.HorizontalOffset = 2;

                  configuracionRelleno.VerticalOffset = -20;

                  configuracionRelleno.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  configuracionRelleno.PatternHeight = 3;

                  configuracionRelleno.PatternWidth = 3;

                  configuracionRelleno.AlignWithLayer = false;

                  configuracionRelleno.Linked = false;

                  configuracionRelleno.PatternId = Guid.NewGuid().ToString();

                  capaRelleno.Update();

                  break;

             }

         }

         im.Save(rutaExportacion);

    }

{{< /highlight >}}

**PSDNET-138. Soporte de PtFlResource**

{{< highlight java >}}

  // Soporte de PtFlResource

    string nombreArchivoFuente = "CapaRellenoPatron.psd";

    string rutaExportacion = "PtFlResource_Editada.psd";

    double tolerancia = 0.0001;

    var im = (PsdImage)Image.Load(nombreArchivoFuente);

    using (im)

    {

         foreach (var capa in im.Layers)

         {

             if (capa is FillLayer)

             {

                var capaRelleno = (FillLayer)capa;

                var recursos = capaRelleno.Resources;

                foreach (var res in recursos)

                {

                    if (res is PtFlResource)

                    {

                        // Lectura

                        PtFlResource recurso = (PtFlResource)res;

                        if (

                            recurso.Offset.X != -46 || 

                            recurso.Offset.Y != -45 || 

                            recurso.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            recurso.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            recurso.AlignWithLayer != true ||

                            recurso.IsLinkedWithLayer != true ||

                            !(Math.Abs(recurso.Scale - 50) < tolerancia)) {

                                throw new Exception("El recurso PtFl se leyó incorrectamente");

                            }

                        // Edición

                        recurso.Offset = new Point(-11, 13);

                        recurso.Scale = 200;

                        recurso.AlignWithLayer = false;

                        recurso.IsLinkedWithLayer = false;

                        capaRelleno.Resources = capaRelleno.Resources;

                        // No tenemos datos de patrón en PattResource, así que podemos agregarlo.

                        var configuracionRelleno = (PatternFillSettings)capaRelleno.FillSettings;

                        configuracionRelleno.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        configuracionRelleno.PatternHeight = 1;

                        configuracionRelleno.PatternWidth = 4;

                        configuracionRelleno.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        configuracionRelleno.PatternId = Guid.NewGuid().ToString() + "\0";

                        capaRelleno.Update();

                    }

                    break;

                }

                break;

            }

         }

         im.Save(rutaExportacion);

    } 

{{< /highlight >}}

**PSDNET-129. Implementar método de Recorte correcto para archivos PSD**

{{< highlight java >}}

             // Implementar método de Recorte correcto para archivos PSD.

            string nombreArchivoFuente = "1.psd";

            string rutaExportacionPsd = "PruebaRecorte.psd";

            string rutaExportacionPng = "PruebaRecorte.png";

            using (RasterImage imagen = Image.Load(nombreArchivoFuente) as RasterImage)

            {

                imagen.Crop(new Rectangle(10, 30, 100, 100));

                imagen.Save(rutaExportacionPsd, new PsdOptions());

                imagen.Save(rutaExportacionPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Soporte de VsmsResource**

{{< highlight java >}}

 // Soporte de VsmsResource

        static void EjemploDeSoporteDeVsmsResource()

        {

            string nombreArchivoFuente = "RectanguloVacio.psd";

            string rutaExportacion = "RectanguloVacio_cambiado.psd";

            var im = (PsdImage)Image.Load(nombreArchivoFuente);

            using (im)

            {

                var recurso = ObtenerVsmsResource(im);

                // Lectura

                if (recurso.IsDisabled != false ||

                    recurso.IsInverted != false ||

                    recurso.IsNotLinked != false ||

                    recurso.Paths.Length != 7 ||

                    recurso.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    recurso.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    recurso.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    recurso.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    recurso.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    recurso.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    recurso.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("El recurso Vsms se leyó incorrectamente");

                }

                var pathFillRule = (PathFillRuleRecord)recurso.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)recurso.Paths[1];

                var subpathLength = (LengthRecord)recurso.Paths[2];

                // La regla de relleno de ruta no contiene información adicional

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("Los caminos del recurso Vsms se leyeron incorrectamente");

                }

                // Edición

                recurso.IsDisabled = true;

                recurso.IsInverted = true;

                recurso.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)recurso.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)recurso.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                im.Save(rutaExportacion);

            }         

        }

        static VsmsResource ObtenerVsmsResource(PsdImage imagen)

        {

            var capa = imagen.Layers[1];

            VsmsResource recurso = null;

            var recursos = capa.Resources;

            for (int i = 0; i < recursos.Length; i++)

            {

                if (recursos[i] is VsmsResource)

                {

                    recurso = (VsmsResource)recursos[i];

                    break;

                }

            }

            if (recurso == null)

            {

                throw new Exception("Recurso Vsms no encontrado");

            }

            return recurso;

        }   

{{< /highlight >}}

**PSDNET-121: Las capas visibles en la subcarpeta visible en la carpeta invisible se renderizan, pero no deberían**

{{< highlight java >}}

 // Las capas visibles en la subcarpeta visible en la carpeta invisible se renderizan, pero no deberían

            string nombreArchivoFuente = "MuchasCarpetas.psd.psd";

            string rutaArchivoSalidaJpg = "carpetasSalida.jpg";

            string rutaArchivoSalidaPsd = "carpetasSalida.psd";

            var opciones = new PsdLoadOptions();

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente, opciones))

            {

                imagen.Save(rutaArchivoSalidaPsd, new PsdOptions(imagen));

                imagen.Save(rutaArchivoSalidaJpg, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}

**PSDNET-119. PSD (modo RGB 16 bits por canal) no se convierte correctamente a JPG**

{{< highlight java >}}

  // PSD no se convierte correctamente a jpg

            string nombreArchivoFuente = "in.psd";

            string rutaExportacion = "outRgb.jpg";

            var opciones = new PsdLoadOptions();

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente, opciones))

            {

                imagen.Save(rutaExportacion, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}