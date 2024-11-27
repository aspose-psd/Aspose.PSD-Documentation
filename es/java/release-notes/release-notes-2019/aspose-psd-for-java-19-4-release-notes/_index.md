---
title: Notas de la versión de Aspose.PSD para Java 19.4
type: docs
weight: 20
url: /es/java/aspose-psd-para-java-19-4-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de Aspose.PSD para Java 19.4

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-1|Crear una función para cargar archivos de imagen JPEG/PNG/etc en PsdImage sin carga directa (lo cual no es compatible en Aspose.PSD)|Característica|
|PSDJAVA-2|Soporte de modo de color RGB con 16 bits por canal (64 bits por color)|Característica|
|PSDJAVA-3|Soporte de máscaras vectoriales de capa y FlipRotate personalizado de capa de texto|Característica|
|PSDJAVA-4|Todos los caracteres asiáticos no se representan correctamente|Error|
|PSDJAVA-5|Los símbolos \r\n se interpretan como doble salto de línea, lo cual es incorrecto|Error|
|PSDJAVA-6|Si la capa de texto se actualiza con una cadena que contiene saltos de línea, el archivo PSD se vuelve ilegible|Error|
|PSDJAVA-7|Si la capa de texto se actualiza con una cadena que contiene símbolos de tabulación, el procesamiento falla con una excepción|Error|
# **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **APIs eliminadas:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FormatoDeArchivo
- P:Aspose.PSD.FileFormats.Gif.GifImage.DatosXmp
- P:Aspose.PSD.FileFormats.Gif.GifImage.TieneTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletaOrdenada
- P:Aspose.PSD.FileFormats.Gif.GifImage.ResoluciónEnBitsDeColorDePaleta
- P:Aspose.PSD.FileFormats.Gif.GifImage.Ancho
- P:Aspose.PSD.FileFormats.Gif.GifImage.Altura
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPorPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Bloques
- P:Aspose.PSD.FileFormats.Gif.GifImage.MarcoActivo
- P:Aspose.PSD.FileFormats.Gif.GifImage.ColorDeFondo
- P:Aspose.PSD.FileFormats.Gif.GifImage.ÍndiceDeColorDeFondo
- P:Aspose.PSD.FileFormats.Gif.GifImage.ProporciónDePíxeles
- P:Aspose.PSD.FileFormats.Gif.GifImage.EsCaché
- P:Aspose.PSD.FileFormats.Gif.GifImage.TieneColorTransparente
- P:Aspose.PSD.FileFormats.Gif.GifImage.ColorTransparente
- P:Aspose.PSD.FileFormats.Gif.GifImage.TieneColorDeFondo
- P:Aspose.PSD.FileFormats.Gif.GifImage.OpacidadDeImagen
- M:Aspose.PSD.FileFormats.Gif.GifImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.DatosCaché
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlipTodo(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.OrdenarBloques
- M:Aspose.PSD.FileFormats.Gif.GifImage.EliminarBloque(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Girar(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Redimensionar(System.Int32,System.Int32,Aspose.PSD.TipoDeRedimensionamiento)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Redimensionar(System.Int32,System.Int32,Aspose.PSD.ConfiguracionesDeRedimensionamientoDeImagen)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RedimensionarProporcionalmente(System.Int32,System.Int32,Aspose.PSD.TipoDeRedimensionamiento)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Recortar(Aspose.PSD.Rectángulo)
- M:Aspose.PSD.FileFormats.Gif.GifImage.EscalaDeGrises
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarioFijo(System.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizarOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizarBradley(System.Double)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AjustarBrillo(System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AjustarContraste(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AjustarGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AjustarGamma(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filtrar(Aspose.PSD.Rectángulo,Aspose.PSD.FiltrosDeImagen.OpcionesDeFiltro.OpcionesDeFiltroBase)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReemplazarColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReemplazarColoresNoTransparentes(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarioBradley(System.Double,System.Int32)
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.TieneCanalAlfa
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.TieneColorTransparente
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.FormatoDeArchivo
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.PremultiplicarComponentes
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ByteOrden
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ResoluciónHorizontal
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ResoluciónVertical
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ColorDeFondo
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BitsPorPixel
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.MarcoActivo
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Frames
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Altura
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Ancho
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.EsCaché
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.DatosExif
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.OpacidadDeImagen
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.DatosXmp
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AlinearResoluciones
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Dither(Aspose.PSD.MétodoDeDithering,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.EstablecerResolución(System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.DatosCaché
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlipTodo(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Girar(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AgregarMarco(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Agregar(Aspose.PSD.FileFormats.Tiff.TiffImage)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AgregarMarcos(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.InsertarMarco(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.QuitarMarco(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.QuitarMarco(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Redimensionar(System.Int32,System.Int32,Aspose.PSD.TipoDeRedimensionamiento)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Redimensionar(System.Int32,System.Int32,Aspose.PSD.ConfiguracionesDeRedimensionamientoDeImagen)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RedimensionarAnchoProporcionalmente(System.Int32,Aspose.PSD.TipoDeRedimensionamiento)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RedimensionarAlturaProporcionalmente(System.Int32,Aspose.PSD.TipoDeRedimensionamiento)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RedimensionarProporcionalmente(System.Int32,System.Int32,Aspose.PSD.TipoDeRedimensionamiento)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Recortar(Aspose.PSD.Rectángulo)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.EscalaDeGrises
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarioFijo(System.Byte)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizarOtsu
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizarBradley(System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Cortar(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AjustarBrillo(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AjustarContraste(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AjustarGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AjustarGamma(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Filtrar(Aspose.PSD.Rectángulo,Aspose.PSD.FiltrosDeImagen.OpcionesDeFiltro.OpcionesDeFiltroBase)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReemplazarColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReemplazarColoresNoTransparentes(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReemplazarMarco(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
# **Ejemplos de uso:**

**PSDJAVA-1. Crear una función para cargar archivos de imagen JPEG/PNG/etc en PsdImage sin carga directa (lo cual no es compatible en Aspose.PSD)**

{{< highlight java >}}

 String filePath = "EjemploPsd.psd";

    String rutaArchivoResultado = "ResultadoPsd.psd";

    PsdImage imagen = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(filePath);

         try 

         {

              Layer capa = null;

              try

              {

                  capa = new Layer((RasterImage)im);

                  imagen.addLayer(capa);

                  imagen.save(rutaArchivoResultado);

              }

              catch

              {

                  if (capa != null)

                  {

                       capa.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         imagen.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Soporte de modo de color RGB con 16 bits por canal (64 bits por color)**

{{< highlight java >}}

  // Soporte de modo de color RGB con 16 bits por canal (64 bits por color)

        String nombreArchivoFuente = "enRgb16.psd";

        String rutaArchivoJpg = "salidaRgb16.jpg";

        String rutaArchivoPsd = "salidaRgb16.psd";

        PsdLoadOptions opciones = new PsdLoadOptions();

        PsdImage imagen = (PsdImage)Image.load(nombreArchivoFuente, opciones);

        try

        {

            PsdOptions opcionesPsd = new PsdOptions(imagen);

            imagen.save(rutaArchivoPsd, opcionesPsd);



            JpegOptions opcionesJpeg = new JpegOptions();

            opcionesJpeg.setQuality(100);

            imagen.save(rutaArchivoJpg);

        }

        finally 

        {

             imagen.dispose();

        }

    // Los archivos deben abrirse sin excepción y deben ser legibles para Photoshop    

   imagen = Image.load(rutaArchivoPsd));

   imagen.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Soporte de máscaras vectoriales de capa y FlipRotate personalizado de capa de texto**

{{< highlight java >}}

 // La operación RotateFlip no funciona como se espera en PSD

    String archivoFuente = "1.psd";

    String rutaPng = "PruebaGiro2617.png";

    String rutaPsd = "PruebaGiro2617.psd";

    int tipoGiro = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(archivoFuente));



    try

    {

        im.rotateFlip(tipoGiro);

        PngOptions opciones = new PngOptions();

        opciones.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(rutaPng, opciones);

        im.save(rutaPsd);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJava-4. Todos los caracteres asiáticos no se representan correctamente**

[**Por favor, revise el ejemplo adjunto**](attachments/92602686/92766213.java)

**PSDJAVA-5. Los símbolos \r\n se interpretan como doble salto de línea, lo cual es incorrecto**

{{< highlight java >}}

 // Los símbolos \r\n se interpretan como doble salto de línea, lo cual es incorrecto

            String nombreArchivoFuente = "PruebaTexto.psd";

            String rutaExportación = "Resultado.psd";



            PsdImage imagen = (PsdImage)Image.load(nombreArchivoFuente);

            TextLayer capa = (TextLayer)imagen.getLayers()[0];

            PsdOptions opcionesImagen = new PsdOptions(imagen);

            try

            {

                capa.updateText("Primer Párrafo\r\nSegundo Párrafo\rTercer párrafo\nCuarto Párrafo");

                imagen.save(rutaExportación, opcionesImagen);

                // La imagen creada debe ser legible por Aspose.PSD/Aspose.Imaging y por Photoshop

                PsdImage imagenCreada = (PsdImage)Image.load(rutaExportación);

                imagenCreada.dispose();

            }

            finally

            {

                imagen.dispose();

            }

{{< /highlight >}}



**PSDJAVA-6. Si la capa de texto se actualiza con una cadena que contiene saltos de línea, el archivo PSD se vuelve ilegible**

{{< highlight java >}}

 // Si la capa de texto se actualiza con una cadena que contiene saltos de línea, el archivo PSD se vuelve ilegible.

            String nombreArchivoFuente = "PruebaTexto.psd";

            String rutaExportación = "Resultado.psd";



            PsdImage imagen = (PsdImage)Image.load(nombreArchivoFuente);

            TextLayer capa = (TextLayer)imagen.getLayers()[0];

            PsdOptions opcionesImagen = new PsdOptions(imagen);

            try

            {

                capa.updateText("Primer Párrafo\r\nSegundo Párrafo\r\nTercer párrafo\r\nCuarto Párrafo");

                imagen.save(rutaExportación, opcionesImagen);

                // La imagen creada debe ser legible por Aspose.PSD/Aspose.Imaging y por Photoshop

                PsdImage imagenCreada = (PsdImage)Image.load(rutaExportación);

                imagenCreada