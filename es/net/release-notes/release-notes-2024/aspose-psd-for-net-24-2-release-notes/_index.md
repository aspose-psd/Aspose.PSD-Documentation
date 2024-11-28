---
title: Notas de lanzamiento de Aspose.PSD for .NET 24.2
type: docs
weight: 110
url: /es/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento de [Aspose.PSD for .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                  | **Categoría** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1503 | Manejar la propiedad Angle en PatternFillSettings                              |   Funcionalidad   |
| PSDNET-1719 | Soporte de escala vertical y horizontal para TextLayer                       |     Funcionalidad     |
| PSDNET-1783 | [Formato AI] Implementar renderizado correcto del fondo en Formato AI basado en PDF |     Funcionalidad     |
| PSDNET-1611 | Cambiar mecanismo Distort en warp                                             |     Mejora     |
| PSDNET-1802 | Acelerar warp                                                                |     Mejora     |
| PSDNET-995  | Excepción "Error al cargar la imagen." al abrir el documento                         |     Error     |
| PSDNET-1491 | Corregir problemas al guardar archivos psd que tienen un Stroke Pattern                                   |     Error     |
| PSDNET-1642 | El estilo de texto es incorrecto en un objeto inteligente cuando se utiliza ReplaceContents    |     Error     |
| PSDNET-1884 | [Formato AI] Corregir el renderizado de Cubic Bezier en archivo AI                        |     Error     |

## **Cambios en la API pública**
# **APIs añadidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-1503. Manejar la propiedad Angle en PatternFillSettings**

{{< highlight csharp >}}
string archivoOrigen = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string archivoSalida = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage imagen = (PsdImage)Image.Load(archivoOrigen, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer capaRelleno = (FillLayer)imagen.Layers[1];
    PatternFillSettings ajustesRelleno = (PatternFillSettings)capaRelleno.FillSettings;
    ajustesRelleno.Angle = 70;
    capaRelleno.Update();
    imagen.Save(archivoSalida, new PsdOptions());
}

using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer capaRelleno = (FillLayer)imagen.Layers[1];
    PatternFillSettings ajustesRelleno = (PatternFillSettings)capaRelleno.FillSettings;

    Assert.AreEqual(70, ajustesRelleno.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Soporte de escala vertical y horizontal para TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var imagenPsd = (PsdImage)Image.Load(src))
{
    imagenPsd.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [Formato AI] Implementar renderizado correcto del fondo en formato AI basado en PDF**

{{< highlight csharp >}}
string archivoOrigen = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage imagen = (AiImage)Image.Load(archivoOrigen))
{
    imagen.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. Excepción "Error al cargar la imagen." al abrir el documento**

{{< highlight csharp >}}
string archivo1 = Path.Combine(baseFolder, "PRODUCT.ai");
string archivoSalida1 = Path.Combine(outputFolder, "PRODUCT.png");

using (AiImage imagen = (AiImage)Image.Load(archivo1))
{
    imagen.Save(archivoSalida1, new PngOptions());
}

string archivo2 = Path.Combine(baseFolder, "Dolota.ai");
string archivoSalida2 = Path.Combine(outputFolder, "Dolota.png");

using (AiImage imagen = (AiImage)Image.Load(archivo2))
{
    imagen.Save(archivoSalida2, new PngOptions());
}

string archivo3 = Path.Combine(baseFolder, "ARS_novelty_2108_out_01(1).ai");
string archivoSalida3 = Path.Combine(outputFolder, "ARS_novelty_2108_out_01(1).png");

using (AiImage imagen = (AiImage)Image.Load(archivo3))
{
    imagen.Save(archivoSalida3, new PngOptions());
}

string archivo4 = Path.Combine(baseFolder, "bit_gear.ai");
string archivoSalida4 = Path.Combine(outputFolder, "bit_gear.png");

using (AiImage imagen = (AiImage)Image.Load(archivo4))
{
    imagen.Save(archivoSalida4, new PngOptions());
}

string archivo5 = Path.Combine(baseFolder, "test.ai");
string archivoSalida5 = Path.Combine(outputFolder, "test.png");

using (AiImage imagen = (AiImage)Image.Load(archivo5))
{
    imagen.Save(archivoSalida5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. Corregir problemas al guardar archivos psd que tienen un Stroke Pattern**

{{< highlight csharp >}}
string archivoOrigen = Path.Combine(baseFolder, "StrokeShapePattern.psd");
string archivoSalida = Path.Combine(outputFolder, "StrokeShapePattern_output.psd");

Rectangle nuevosLimitesPatron = new Rectangle(0, 0, 4, 4);
Guid guid = Guid.NewGuid();
string nuevoNombrePatron = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
int[] nuevoPatron = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
};

using (PsdImage imagen = (PsdImage)Image.Load(archivoOrigen))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    PatternFillSettings ajustesRellenoInterno = (PatternFillSettings)capaForma.Fill;

    PattResource recursoPatt;
    foreach (var recursoGlobalCapa in imagen.GlobalLayerResources)
    {
        if (recursoGlobalCapa is PattResource)
        {
            recursoPatt = (PattResource)recursoGlobalCapa;
            PattResourceData itemPatron = recursoPatt.Patterns[0]; // Datos del patrón interno de trazo

            itemPatron.PatternId = guid.ToString();
            itemPatron.Name = nuevoNombrePatron;
            itemPatron.SetPattern(nuevoPatron, nuevosLimitesPatron);

            break;
        }
    }

    ajustesRellenoInterno.PatternName = nuevoNombrePatron;
    ajustesRellenoInterno.PatternId = guid.ToString() + "\0";

    capaForma.Update();

    imagen.Save(archivoSalida);
}

// Verificar los datos cambiados.
using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida))
{
    ShapeLayer capaForma = (ShapeLayer)imagen.Layers[1];
    PatternFillSettings ajustesRellenoInterno = (PatternFillSettings)capaForma.Fill;

    Assert.AreEqual(guid.ToString().ToUpper(), ajustesRellenoInterno.PatternId);
    Assert.AreEqual(nuevoNombrePatron, ajustesRellenoInterno.PatternName + "\0");
}
{{< /highlight >}}

**PSDNET-1642. El estilo de texto es incorrecto en un objeto inteligente cuando se utiliza ReplaceContents**

{{< highlight csharp >}}
string archivoEntrada = Path.Combine(baseFolder, "source.psd");
string salida2 = Path.Combine(outputFolder, "output.png");

PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
opcionesCargaPsd.LoadEffectsResource = true;

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoEntrada, opcionesCargaPsd))
{
    SmartObjectLayer objetoInteligente = (SmartObjectLayer)imagenPsd.Layers[1];

    using (PsdImage imagenObjetoInteligente = (PsdImage)objetoInteligente.LoadContents(opcionesCargaPsd))
    {
        objetoInteligente.ReplaceContents(imagenObjetoInteligente);
    }

    imagenPsd.Save(salida2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1884. [Formato AI] Corregir el renderizado de Cubic Bezier en archivo AI**

{{< highlight csharp >}}
string archivoOrigen = Path.Combine(baseFolder, "Typography.ai");
string outputFilePath = Path.Combine(outputFolder, "Typography.png");

using (AiImage imagen = (AiImage)Image.Load(archivoOrigen))
{
    imagen.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1611. Cambiar mecanismo Distort en warp**

{{< highlight csharp >}}
string archivoOrigen = Path.Combine(baseFolder, "crow_grid.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opciones = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(archivoOrigen, opciones))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1802. Acelerar warp**

{{< highlight csharp >}}
string archivoOrigen = Path.Combine(baseFolder, "output.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opciones = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

var sw = new Stopwatch();
sw.Start();

using (PsdImage img = (PsdImage)Image.Load(archivoOrigen, opciones))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}

sw.Stop();

// valor antiguo = 193300
// nuevo valor =  55500
int tiempoEnSeg = (int)sw.Elapsed.TotalMilliseconds;
if (tiempoEnSeg > 100000)
{
    throw new Exception("El tiempo de procesamiento es demasiado largo");
}
{{< /highlight >}}
