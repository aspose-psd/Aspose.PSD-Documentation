---
title: Aspose.PSD para .NET 23.10 - Notas de la versión
type: docs
weight: 30
url: /es/net/aspose-psd-para-net-23-10-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**     | **Resumen**                                                                                                                | **Categoría** |
|:------------|:------------------------------------------------------------------------|:--------|
| PSDNET-692 | Soporte de dirección de texto vertical | Característica |
| PSDNET-1402 | Usar ajustes de contorno de recurso vstk en el renderizado de contorno de forma | Característica |
| PSDNET-1607 | Implementar renderizado del área interna de formas de contorno | Característica |
| PSDNET-1644 | No repintar capa de forma si no ha sido modificada | Característica |
| PSDNET-1696 | [Formato AI] Agregar soporte para lectura de encabezado en archivos AI basados en PDF | Característica |
| PSDNET-1560 | Varias formas de establecer la resolución del archivo Psd no funcionan | Error |
| PSDNET-1728 | FontSettings.SetFontsFolders no funciona o Aspose.PSD utiliza una fuente incorrecta | Error |
| PSDNET-1739 | Regresión. Corregir excepción de referencia nula al guardar PsdImage con capa de forma | Error |


## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **APIs eliminadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Ejemplos de uso:**

**PSDNET-692. Soporte de dirección de texto vertical**

{{< highlight csharp >}}
string archivoFuente = "692_lt1.psd";
string archivoSalida = "692_output.png";
string carpetaFuentes = "692_Fonts";

var carpetasFuentes = new List<string>(FontSettings.GetFontsFolders());
carpetasFuentes.Add(carpetaFuentes);
FontSettings.SetFontsFolders(carpetasFuentes.ToArray(), true);

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    imagenPsd.Save(archivoSalida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. Usar ajustes de contorno del recurso vstk en el renderizado de contorno de forma**

{{< highlight csharp >}}
string archivoFuente = "StrokeShapeTest.psd";
string archivoPsdSalida = "StrokeShapeTest.out.psd";
string archivoPngSalida = "StrokeShapeTest.out.png";

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    Layer capa = imagen.Layers[1];
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    ColorFillSettings ajustesRelleno = (ColorFillSettings)capaForma.Fill;
    ajustesRelleno.Color = Color.GreenYellow;
    capaForma.Update();

    ShapeLayer capaForma2 = (ShapeLayer)imagen.Layers[3];
    GradientFillSettings ajustesDegradado = (GradientFillSettings)capaForma2.Fill;
    ajustesDegradado.Dither = true;
    ajustesDegradado.Reverse = true;
    ajustesDegradado.AlignWithLayer = false;
    ajustesDegradado.Angle = 20;
    ajustesDegradado.Scale = 50;
    ajustesDegradado.ColorPoints[0].Location = 100;
    ajustesDegradado.ColorPoints[1].Location = 4000;
    ajustesDegradado.TransparencyPoints[0].Location = 200;
    ajustesDegradado.TransparencyPoints[1].Location = 3800;
    ajustesDegradado.TransparencyPoints[0].Opacity = 90;
    ajustesDegradado.TransparencyPoints[1].Opacity = 10;
    capaForma2.Update();

    ShapeLayer capaForma3 = (ShapeLayer)imagen.Layers[5];
    StrokeSettings ajustesContorno = (StrokeSettings)capaForma3.Stroke;
    ajustesContorno.Size = 15;
    ColorFillSettings ajustesRellenoContorno = (ColorFillSettings)ajustesContorno.Fill;
    ajustesRellenoContorno.Color = Color.GreenYellow;
    capaForma3.Update();

    imagen.Save(archivoPsdSalida);
    imagen.Save(archivoPngSalida, new PngOptions());
}

// Verificar datos cambiados.
using (PsdImage imagen = (PsdImage)Image.Load(archivoPsdSalida))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    ColorFillSettings ajustesRelleno = (ColorFillSettings)capaForma.Fill;
    AssertAreEqual(Color.GreenYellow, ajustesRelleno.Color);

    ShapeLayer capaForma2 = (ShapeLayer)imagen.Layers[3];
    GradientFillSettings ajustesDegradado = (GradientFillSettings)capaForma2.Fill;
    AssertAreEqual(true, ajustesDegradado.Dither);
    AssertAreEqual(true, ajustesDegradado.Reverse);
    AssertAreEqual(false, ajustesDegradado.AlignWithLayer);
    AssertAreEqual(20.0, ajustesDegradado.Angle);
    AssertAreEqual(50, ajustesDegradado.Scale);
    AssertAreEqual(100, ajustesDegradado.ColorPoints[0].Location);
    AssertAreEqual(4000, ajustesDegradado.ColorPoints[1].Location);
    AssertAreEqual(200, ajustesDegradado.TransparencyPoints[0].Location);
    AssertAreEqual(3800, ajustesDegradado.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, ajustesDegradado.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, ajustesDegradado.TransparencyPoints[1].Opacity);

    ShapeLayer capaForma3 = (ShapeLayer)imagen.Layers[5];
    StrokeSettings ajustesContorno = (StrokeSettings)capaForma3.Stroke;
    ColorFillSettings ajustesRellenoContorno = (ColorFillSettings)ajustesContorno.Fill;
    AssertAreEqual(15.0, ajustesContorno.Size);
    AssertAreEqual(Color.GreenYellow, ajustesRellenoContorno.Color);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1607. Implementar el renderizado del área interna de formas de contorno**

{{< highlight csharp >}}
string archivoFuente = "ShapeInternalGradient.psd";
string archivoSalida = "ShapeInternalGradient.out.psd";

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    GradientFillSettings ajustesRelleno = (GradientFillSettings)capaForma.Fill;
    ajustesRelleno.Dither = true;
    ajustesRelleno.Reverse = true;
    ajustesRelleno.AlignWithLayer = false;
    ajustesRelleno.Angle = 20.0;
    ajustesRelleno.Scale = 50;
    ajustesRelleno.ColorPoints[0].Location = 100;
    ajustesRelleno.ColorPoints[1].Location = 4000;
    ajustesRelleno.TransparencyPoints[0].Location = 200;
    ajustesRelleno.TransparencyPoints[1].Location = 3800;
    ajustesRelleno.TransparencyPoints[0].Opacity = 90.0;
    ajustesRelleno.TransparencyPoints[1].Opacity = 10.0;

    capaForma.Update();

    imagen.Save(archivoSalida);
}

// Verificar datos cambiados.
using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    GradientFillSettings ajustesRelleno = (GradientFillSettings)capaForma.Fill;

    AssertAreEqual(true, ajustesRelleno.Dither);
    AssertAreEqual(true, ajustesRelleno.Reverse);
    AssertAreEqual(false, ajustesRelleno.AlignWithLayer);
    AssertAreEqual(20.0, ajustesRelleno.Angle);
    AssertAreEqual(50, ajustesRelleno.Scale);
    AssertAreEqual(100, ajustesRelleno.ColorPoints[0].Location);
    AssertAreEqual(4000, ajustesRelleno.ColorPoints[1].Location);
    AssertAreEqual(200, ajustesRelleno.TransparencyPoints[0].Location);
    AssertAreEqual(3800, ajustesRelleno.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, ajustesRelleno.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, ajustesRelleno.TransparencyPoints[1].Opacity);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1644. No repintar capa de forma si no ha sido modificada**

{{< highlight csharp >}}
string archivoFuente = "ShapeInternalSolid.psd";
string archivoSalida = "ShapeInternalSolid.out.psd";

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    ColorFillSettings ajustesRelleno = (ColorFillSettings)capaForma.Fill;
    ajustesRelleno.Color = Color.Red;

    // No utilizar la actualización de la capa Shape antes de guardar

    imagen.Save(archivoSalida);

    // Verificar renderizado del archivo guardado
}

// Verificar que los datos de la capa de forma permanecen sin cambios.
using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    ColorFillSettings ajustesRelleno = (ColorFillSettings)capaForma.Fill;

    AssertAreEqual(Color.FromArgb(45, 211, 31), ajustesRelleno.Color);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1696. [AI Formato] Agregar soporte para lectura de encabezado de archivos AI basados en PDF**

{{< highlight csharp >}}
string archivoFuente = "ai_source.ai";

void AssertIsNotNull(object esperado)
{
    if (esperado == null)
    {
        throw new Exception("El objeto es nulo.");
    }
}

using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    AssertIsNotNull(imagen);
    AssertIsNotNull(imagen.Header);
    AssertIsNotNull(imagen.Header.BoundingBox);
}
{{< /highlight >}}

**PSDNET-1560. Varias formas de establecer la resolución del archivo Psd no funcionan**

{{< highlight csharp >}}
string salida1 = "1560_1_output.psd";
string salida2 = "1560_2_output.psd";
string salida3 = "1560_3_output.psd";

using (PsdImage nuevoPsd = (PsdImage)new PsdImage(600, 400))
{
    nuevoPsd.ImageResources = new ResourceBlock[] { new ResolutionInfoResource() };
    nuevoPsd.VerticalResolution = 100;
    nuevoPsd.HorizontalResolution = 100;
    nuevoPsd.Save(salida1);
}

using (PsdImage nuevoPsd = (PsdImage)new PsdImage(600, 400))
{
    nuevoPsd.SetResolution(200, 200);
    nuevoPsd.Save(salida2);
}

using (PsdImage nuevoPsd = (PsdImage)new PsdImage(600, 400))
{
    PsdOptions opcionesPsd = new PsdOptions()
    {
        ResolutionSettings = new ResolutionSetting()
        {
            HorizontalResolution = 300,
            VerticalResolution = 300
        }
    };
    nuevoPsd.Save(salida3, opcionesPsd);
}

using (var psdImagen1 = (PsdImage)Image.Load(salida1))
{
    var recursoRes = psdImagen1.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(recursoRes);
    AreEqual(100, recursoRes.VDpi.Integer);
    AreEqual(100, recursoRes.HDpi.Integer);
}

using (var psdImagen2 = (PsdImage)Image.Load(salida2))
{
    var recursoRes = psdImagen2.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(recursoRes);
    AreEqual(200, recursoRes.VDpi.Integer);
    AreEqual(200, recursoRes.HDpi.Integer);
}

using (var psdImagen3 = (PsdImage)Image.Load(salida3))
{
    var recursoRes = psdImagen3.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(recursoRes);
    AreEqual(300, recursoRes.VDpi.Integer);
    AreEqual(300, recursoRes.HDpi.Integer);
}

void IsNotNull(object obj)
{
    if (obj == null)
    {
        throw new NullReferenceException();
    }
}

void AreEqual(object esperado, object actual)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception("Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1728. FontSettings.SetFontsFolders no funciona o Aspose.PSD utiliza una fuente incorrecta**

{{< highlight csharp >}}
string src = "1728_Untitled-1.psd";
string fontsDir = "Fonts";
string outputPng = "1728_output.png";

FontSettings.SetFontsFolders(new string[] { fontsDir }, true);
using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            var textData = textLayer.TextData;
            textData.UpdateLayerData();
        }
    }

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1739. Regresión. Corregir excepción de referencia nula al guardar PsdImage con capa de forma**

{{< highlight csharp >}}
string archivoFuente = "ShapeInternalSolid.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(archivoFuente))
{
    // Debería cargarse sin excepciones

    ShapeLayer capaForma = (ShapeLayer)im.Layers[1];

    if (capaForma.RawDataSettings == null)
    {
        throw new Exception("RawDataSettings no deber