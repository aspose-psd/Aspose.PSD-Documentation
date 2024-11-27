---
title: Notas de la versión de Aspose.PSD para .NET 24.6
type: docs
weight: 70
url: /es/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                         | **Categoría** |
|:------------|:-------------------------------------------------------------------------------------|:--------------|
| PSDNET-1450 | Implementar soporte de capa de mapa de degradado                                      | Feature       |
| PSDNET-1670 | [Formato AI] Agregar soporte de metadatos de paquete XPacket al formato AI           | Feature       |
| PSDNET-1831 | Implementar tipos de deformación Inflate, Squeeze y Twist                             | Feature       |
| PSDNET-1653 | Los modos Rgb y Lab no pueden contener menos de 3 canales o más de 4 canales en el archivo con capas de ArtBoard | Bug |
| PSDNET-1775 | El área de procesamiento superior debe ser positiva. (Parámetro 'areaToProcess') en el procesamiento de archivos específicos | Bug |
| PSDNET-2052 | La imagen ampliada sobre el lienzo se recorta después de guardar. Los datos se pierden pero la vista previa se ve correctamente | Bug |

## **Cambios en la API Pública**
# **APIs Agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-1450. Implementar soporte de capa de mapa de degradado**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "gradiente_mapa_src.psd");
string archivoSalida = Path.Combine(outputFolder, "gradiente_mapa_src_output.psd");

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    // Agregar capa de ajuste de mapa de degradado.
    GradientMapLayer capa = imagen.AddGradientMapAdjustmentLayer();
    capa.GradientSettings.Reverse = true;

    imagen.Save(archivoSalida);
}

// Verificar cambios guardados
using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida))
{
    GradientMapLayer capaMapaDegradado = imagen.Layers[1] as GradientMapLayer;
    GradientFillSettings ajustesDegradado = (GradientFillSettings)capaMapaDegradado.GradientSettings;

    AssertAreEqual(0.0, ajustesDegradado.Angle);
    AssertAreEqual((short)4096, ajustesDegradado.Interpolation);
    AssertAreEqual(true, ajustesDegradado.Reverse);
    AssertAreEqual(false, ajustesDegradado.AlignWithLayer);
    AssertAreEqual(false, ajustesDegradado.Dither);
    AssertAreEqual(GradientType.Linear, ajustesDegradado.GradientType);
    AssertAreEqual(100, ajustesDegradado.Scale);
    AssertAreEqual(0.0, ajustesDegradado.HorizontalOffset);
    AssertAreEqual(0.0, ajustesDegradado.VerticalOffset);
    AssertAreEqual("Personalizado", ajustesDegradado.GradientName);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Formato AI] Agregar soporte de metadatos de paquete XPacket al formato AI**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "ai_uno.ai");

void AssertAreEqual(object esperado, object actual)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception("Los objetos no son iguales.");
    }
}

void AssertIsNotNull(object objetoPrueba)
{
    if (objetoPrueba == null)
    {
        throw new Exception("El objeto de prueba es nulo.");
    }
}

string claveHerramientaCreador = ":HerramientaCreador";
string claveNPaginas = "xmpTPg:NPaginas";
string claveUnidad = "stDim:unidad";
string claveAltura = "stDim:h";
string claveAncho = "stDim:w";

string herramientaCreadorEsperada = "Adobe Illustrator CC 22.1 (Windows)";
string nPaginasEsperadas = "1";
string unidadEsperada = "Píxeles";
double alturaEsperada = 768;
double anchoEsperado = 1366;

using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    // Se agregó metadatos Xmp.
    var metadatosXmp = imagen.XmpData;

    AssertIsNotNull(metadatosXmp);

    // Ahora podemos acceder a los paquetes Xmp de los archivos AI.
    var paqueteBasico = metadatosXmp.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var paquete = metadatosXmp.Packages[4];

    // Y tenemos acceso al contenido de estos paquetes.
    var herramientaCreador = paqueteBasico[claveHerramientaCreador].ToString();
    var nPaginas = paquete[claveNPaginas];
    var unidad = paquete[claveUnidad];
    var altura = double.Parse(paquete[claveAltura].ToString(), CultureInfo.InvariantCulture);
    var ancho = double.Parse(paquete[claveAncho].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(herramientaCreador, herramientaCreadorEsperada);
    AssertAreEqual(nPaginas, nPaginasEsperadas);
    AssertAreEqual(unidad, unidadEsperada);
    AssertAreEqual(altura, alturaEsperada);
    AssertAreEqual(ancho, anchoEsperado);
}
{{< /highlight >}}

**PSDNET-1831. Implementar tipos de deformación Inflate, Squeeze y Twist**

{{< highlight csharp >}}
string[] archivos = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefijo in archivos)
{
    string archivoFuente = Path.Combine(baseFolder, prefijo + ".psd");
    string archivoSalida = Path.Combine(outputFolder, prefijo + "_export.png");

    using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        imagenPsd.Save(archivoSalida, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Los modos Rgb y Lab no pueden contener menos de 3 canales o más de 4 canales en el archivo con capas de ArtBoard**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "Rgb5Canales.psb");
string archivoSalida = Path.Combine(outputFolder, "Rgb5Canales_output.psd");

using (PsdImage imagen = (PsdImage)Aspose.PSD.Image.Load(archivoFuente))
{
    // Aquí no debería haber excepción
    imagen.Save(archivoSalida);
}
{{< /highlight >}}

**PSDNET-1775. El área de procesamiento superior debe ser positiva. (Parámetro 'areaToProcess') en el procesamiento de archivos específicos**

{{< highlight csharp >}}
string archivoFuente = @"BANNERS_2_Intel-Gamer_psak.psd";
string archivoSalida = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
opcionesCargaPsd.LoadEffectsResource = true;
opcionesCargaPsd.AllowWarpRepaint = true;
using (PsdImage imagen = (PsdImage)PsdImage.Load(archivoFuente, opcionesCargaPsd))
{
    imagen.Save(archivoSalida);
    // No debería haber excepción
}
{{< /highlight >}}

**PSDNET-2052. La imagen ampliada sobre el lienzo se recorta después de guardar. Los datos se pierden pero la vista previa se ve correctamente**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "archivo_grande.psd");

string archivoSalida = Path.Combine(outputFolder, "archivo_grande_output.psd");
string imagenSalida = Path.Combine(outputFolder, "archivo_grande.png");

PsdLoadOptions opcionesCarga = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, opcionesCarga))
{
    // No debería haber error aquí
    imagenPsd.Save(archivoSalida, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var imagenPsd = (PsdImage)Image.Load(archivoSalida, opcionesCarga))
{
    imagenPsd.Resize(imagenPsd.Width / 10, imagenPsd.Height / 10);

    // No debería haber error aquí
    imagenPsd.Save(imagenSalida, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
