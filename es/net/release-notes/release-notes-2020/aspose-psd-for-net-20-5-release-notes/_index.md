---
title: Aspose.PSD para .NET 20.5 - Notas de la versión
type: docs
weight: 80
url: /es/net/aspose-psd-para-net-20-5-notas-de-la-version/
---

{{% alert color="primary" %}} 

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-595|Soporte de Máscaras de Capa para Grupos de Capas|Característica|
|PSDNET-201|Soporte para progreso de conversión de documentos|Característica|
|PSDNET-275|Soporte de Recurso Nvrt (Recurso de Capa de Ajuste de Inversión)|Característica|
|PSDNET-124|Soporte de Guardado de Imagen PSD con Modo de Color Escala de Grises de 16 bits por canal|Característica|
|PSDNET-589|Refactorización de Ejemplos en GitHub|Mejora|
|PSDNET-587|La alineación de texto a través de ITextPortion no funciona para idiomas de derecha a izquierda. El archivo de salida está dañado.|Error|
|PSDNET-604|Excepción al intentar abrir un archivo Psd en particular con Color Lab y 8 bits/canal|Error|
|PSDNET-598|Corregir guardado de imagen PSD con Modo de Color Escala de Grises de 16 bits por canal a formato PSD Escala de Grises de 8 bits por canal|Error|
|PSDNET-599|Corregir guardado de imagen PSD con Modo de Color Escala de Grises de 16 bits por canal a formato PSD RGB de 16 bits por canal|Error|

## Cambios en la API pública
# **APIs añadidas:**
- Ninguna
# **APIs eliminadas:**
- Ninguna

## Ejemplos de uso:
**PSDNET-595. Soporte de Máscaras de Capa para Grupos de Capas**

{{< highlight java >}}

 string archivoFuente = "psdnet595.psd";

string salidaPng = "salida.png";

string salidaPsd = "salida.psd";

using (var entrada = (PsdImage)Image.Load(archivoFuente))

{

     entrada.Save(salidaPng, new PngOptions());

     entrada.Save(salidaPsd);

}

{{< /highlight >}}

**PSDNET-201. Soporte para progreso de conversión de documentos**

{{< highlight java >}}

 string rutaArchivoFuente = "Apple.psd";

Stream flujoSalida = new MemoryStream();

ProgressEventHandler manejadorProgresoLocal = delegate(ProgressEventHandlerInfo infoProgreso)

{

      string mensaje = string.Format(

           "{0} {1}: {2} de {3}",

           infoProgreso.Descripción,

           infoProgreso.TipoEvento,

           infoProgreso.Valor,

           infoProgreso.ValorMáximo);

      Console.WriteLine(mensaje);

};

Console.WriteLine("---------- Cargando Apple.psd ----------");

var opcionesCarga = new PsdLoadOptions() { ProgressEventHandler = manejadorProgresoLocal };

using (PsdImage imagen = (PsdImage)Image.Load(rutaArchivoFuente, opcionesCarga))

{

      Console.WriteLine("---------- Guardando Apple.psd en formato PNG ----------");

      imagen.Save(

           flujoSalida,

           new PngOptions()

           {

                 TipoColor = PngColorType.Truecolor, ProgressEventHandler = manejadorProgresoLocal

           });

      Console.WriteLine("---------- Guardando Apple.psd en formato PSD ----------");

      imagen.Save(

           flujoSalida,

           new PsdOptions()

           {

                 ModoColor = ColorModes.Rgb,

                 RecuentoCanales = 4,

                 ProgressEventHandler = manejadorProgresoLocal

           });

}

{{< /highlight >}}

**PSDNET-275. Soporte de Recurso Nvrt (Recurso de Capa de Ajuste de Inversión)**

{{< highlight java >}}

 using (var imagenPsd = (PsdImage)Image.Load("CapaAjusteInversión.psd"))

{

      foreach (var capa in imagenPsd.Capas)

      {

           if (capa is InvertAdjustmentLayer)

           {

                 foreach (var recursoCapa in capa.Recursos)

                 {

                      if (recursoCapa is NvrtResource)

                      {

                           // El recurso NvrtResource es compatible.

                           var recurso = (NvrtResource)recursoCapa;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. Corregir guardado de imagen PSD con Modo de Color Escala de Grises de 16 bits por canal a formato PSD Escala de Grises de 8 bits por canal**

{{< highlight java >}}

 void GuardarACargarYGuardarAImagenPng(

    string archivo,

    ColorModes modoColor,

    short recuentoBitsCanal,

    short recuentoCanales,

    CompressionMethod compresión,

    int númeroCapa)

{

    string rutaArchivo = archivo + ".psd";

    string sufijo = modoColor.ToString() + recuentoBitsCanal + "_" + recuentoCanales + "_" + compresión;

    string rutaExportación = @"Salida\" + archivo + sufijo + ".psd";

    PsdOptions opcionesPsd = new PsdOptions()

    {

        ModoColor = modoColor,

        RecuentoBitsCanal = recuentoBitsCanal,

        RecuentoCanales = recuentoCanales,

        MétodoCompresión = compresión

    };

    using (PsdImage imagen = (PsdImage)Image.Load(rutaArchivo))

    {

        RasterCachedImage raster = númeroCapa >= 0 ? (RasterCachedImage)imagen.Capas[númeroCapa] : imagen;

        Aspose.PSD.Graphics gráficos = new Graphics(raster);

        int ancho = raster.Ancho;

        int altura = raster.Altura;

        Rectangle rectángulo = new Rectangle(

            ancho / 3,

            altura / 3,

            ancho - (2 * (ancho / 3)) - 1,

            altura - (2 * (altura / 3)) - 1);

        gráficos.DibujarRectángulo(new Aspose.PSD.Pen(Color.GrisOscuro, 1), rectángulo);

        imagen.Save(rutaExportación, opcionesPsd);

    }

    string rutaExportaciónPng = Path.ChangeExtension(rutaExportación, "png");

    using (PsdImage imagen = (PsdImage)Image.Load(rutaExportación))

    {

        // Aquí no debería haber ninguna excepción.

        imagen.Save(rutaExportaciónPng, new PngOptions() { TipoColor = PngColorType.EscalaGrisesConAlfa });

    }

}

GuardarACargarYGuardarAImagenPng("escalaGrises5x5", ColorModes.Cmyk, 16, 5, CompressionMethod.RLE, 0);

GuardarACargarYGuardarAImagenPng("argb16bit_5x5", ColorModes.EscalaGrises, 16, 2, CompressionMethod.RLE, 0);

GuardarACargarYGuardarAImagenPng("argb16bit_5x5_sin_capas", ColorModes.EscalaGrises, 16, 2, CompressionMethod.RLE, -1);

GuardarACargarYGuardarAImagenPng("argb8bit_5x5", ColorModes.EscalaGrises, 16, 2, CompressionMethod.RLE, 0);

GuardarACargarYGuardarAImagenPng("argb8bit_5x5_sin_capas", ColorModes.EscalaGrises, 16, 2, CompressionMethod.RLE, -1);

GuardarACargarYGuardarAImagenPng("cmyk16bit_5x5_sin_capas", ColorModes.EscalaGrises, 16, 2, CompressionMethod.RLE, -1);

GuardarACargarYGuardarAImagenPng("índice8bit_5x5", ColorModes.EscalaGrises, 16, 2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDNET-587. La alineación de texto a través de ITextPortion no funciona para idiomas de derecha a izquierda. El archivo de salida está dañado.**

{{< highlight java >}}

 string nombreArchivoFuente = "bidi.psd";

string nombreArchivoSalida = "salidaBidi.psd";

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))

{

    var capa = (TextLayer)imagen.Capas[2];

    var porciones = capa.TextData.Items;

    porciones[0].Paragraph.Justificación = 2;

    capa.TextData.UpdateLayerData();

    imagen.Save(nombreArchivoSalida);

}

{{< /highlight >}}

` `**PSDNET-604. Excepción al intentar abrir un archivo Psd en particular con Color Lab y 8 bits/canal**

{{< highlight java >}}

 string archivoFuente = "SinTítulo-1.psd";

string archivoSalidaPsd = "salida.psd";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))

{

    imagenPsd.Save(archivoSalidaPsd);

}

// Archivo LAB cargado y guardado sin lanzar excepciones.

{{< /highlight >}}

**PSDNET-598. Corregir guardado de imagen PSD con Modo de Color Escala de Grises de 16 bits por canal a formato PSD Escala de Grises de 8 bits por canal**

{{< highlight java >}}

 string nombreArchivoFuente = "escalaGrises16bit.psd";

string nombreArchivoExportación = "escalaGrises16bit_salida.psd";

PsdOptions opcionesPsd = new PsdOptions()

{

    ModoColor = ColorModes.EscalaGrises,

    RecuentoBitsCanal = 8,

    RecuentoCanales = 2

};

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))

{

    RasterCachedImage raster = imagen.Capas[0];

    Aspose.PSD.Graphics gráficos = new Graphics(raster);

    int ancho = raster.Ancho;

    int altura = raster.Altura;

    Rectangle rectángulo = new Rectangle(ancho / 3, altura / 3, ancho - (2 * (ancho / 3)) - 1, altura - (2 * (altura / 3)) - 1);

    gráficos.DibujarRectángulo(new Aspose.PSD.Pen(Color.GrisOscuro, 1), rectángulo);

    imagen.Save(nombreArchivoExportación, opcionesPsd);

}

string rutaExportaciónPng = Path.ChangeExtension(nombreArchivoExportación, "png");

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoExportación))

{

    // Aquí no debería haber ninguna excepción.

    imagen.Save(rutaExportaciónPng, new PngOptions() { TipoColor = PngColorType.EscalaGrisesConAlfa });

}

{{< /highlight >}}

**PSDNET-599. Corregir guardado de imagen PSD con Modo de Color Escala de Grises de 16 bits por canal a formato PSD RGB de 16 bits por canal**

{{< highlight java >}}

 string nombreArchivoFuente = "escalaGrises16bit.psd";

string nombreArchivoExportación = "escalaGrises16bit_salida.psd";

PsdOptions opcionesPsd = new PsdOptions()

{

    ModoColor = ColorModes.Rgb,

    RecuentoBitsCanal = 8,

    RecuentoCanales = 4

};

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))

{

    RasterCachedImage raster = imagen.Capas[0];

    Aspose.PSD.Graphics gráficos = new Graphics(raster);

    int ancho = raster.Ancho;

    int altura = raster.Altura;

    Rectangle rectángulo = new Rectangle(ancho / 3, altura / 3, ancho - (2 * (ancho / 3)) - 1, altura - (2 * (altura / 3)) - 1);

    gráficos.DibujarRectángulo(new Aspose.PSD.Pen(Color.GrisOscuro, 1), rectángulo);

    imagen.Save(nombreArchivoExportación, opcionesPsd);

}

string rutaExportaciónPng = Path.ChangeExtension(nombreArchivoExportación, "png");

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoExportación))

{

    // Aquí no debería haber ninguna excepción.

    imagen.Save(rutaExportaciónPng, new PngOptions() { TipoColor = PngColorType.EscalaGrisesConAlfa });

}

{{< /highlight >}}
