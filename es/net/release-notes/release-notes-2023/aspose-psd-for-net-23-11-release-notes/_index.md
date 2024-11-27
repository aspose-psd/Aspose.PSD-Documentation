---
title: Notas de la versión de Aspose.PSD para .NET 23.11
type: docs
weight: 20
url: /es/net/aspose-psd-para-net-23-11-notas-de-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión para [Aspose.PSD para .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                                                              | **Categoría** |
|:------------|:----------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-412  | Soporte de LMskResource                                                                                   | Funcionalidad |
| PSDNET-1669 | [Formato AI] Agregar capacidad para renderizar archivo AI basado en PDF con Aspose.PSD                     | Funcionalidad |
| PSDNET-1702 | [Formato AI] Agregar soporte para el operador PostScript "cm"                                               | Funcionalidad |
| PSDNET-1752 | Agregar nuevos tipos de deformaciones: onda, carcasa arriba, carcasa abajo                                  | Funcionalidad |
| PSDNET-1797 | Agregar soporte para deformaciones verticales                                                             | Funcionalidad |
| PSDNET-1756 | System.ArgumentNullException: 'El valor no puede ser nulo. (Parámetro 'clave')' al llamar a TextLayer.GetFonts() | Error |

## **Cambios en la API pública**
# **APIs agregadas:**

- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale

# **APIs eliminadas:**

- Ninguna

## **Ejemplos de uso:**
**PSDNET-412. Soporte de LMskResource**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "archivoFuente.psd");
string psdSalida = Path.Combine(outputFolder, "archivoFuente_salida.psd");

void AssertAreEqual(object esperado, object actual)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception("Los objetos no son iguales.");
    }
}

// Cargar imagen de 16 bits.
using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    // Encontrar LmskResource.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in imagen.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // Verificar propiedades de LmskResource.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // Cambiar propiedades de LmskResource.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // Guardar la imagen.
    imagen.Save(psdSalida);
}
{{< /highlight >}}

**PSDNET-1669. [Formato AI] Agregar capacidad para renderizar archivo AI basado en PDF con Aspose.PSD**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "ai_uno.ai");
string outputPng = Path.Combine(outputFolder, "ai_uno_salida.png");

// Cargar la imagen AI basada en PDF.
using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    // Guardar la imagen AI como una imagen PNG.
    imagen.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [Formato AI] Agregar soporte para el operador PostScript "cm"**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "ai_dos.ai");
string outputPng = Path.Combine(outputFolder, "ai_dos_salida.png");

// Cargar la imagen AI.
using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    // Guardar la imagen AI como una imagen PNG.
    imagen.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Agregar nuevos tipos de deformaciones: onda, carcasa arriba, carcasa abajo**

{{< highlight csharp >}}
var loadOptions = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var saveOptions = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string archivoPez = Path.Combine(baseFolder, "1752_deformacion_pez.psd");
string archivoSubida = Path.Combine(baseFolder, "1752_deformacion_subida.psd");
string archivoBajada = Path.Combine(baseFolder, "1752_deformacion_bajada.psd");

string archivoSalidaPez = Path.Combine(outputFolder, "1752_salida_pez.png");
string archivoSalidaSubida = Path.Combine(outputFolder, "1752_salida_subida.png");
string archivoSalidaBajada = Path.Combine(outputFolder, "1752_salida_bajada.png");

using (var imagenPsd = (PsdImage)Image.Load(archivoPez, loadOptions))
{
    imagenPsd.Save(archivoSalidaPez, saveOptions);
}

using (var imagenPsd = (PsdImage)Image.Load(archivoSubida, loadOptions))
{
    imagenPsd.Save(archivoSalidaSubida, saveOptions);
}

using (var imagenPsd = (PsdImage)Image.Load(archivoBajada, loadOptions))
{
    imagenPsd.Save(archivoSalidaBajada, saveOptions);
}
{{< /highlight >}}

**PSDNET-1756. System.ArgumentNullException: 'El valor no puede ser nulo. (Parámetro 'clave')' al llamar a TextLayer.GetFonts()**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "TextoSimple.psd");

FontSettings.RemoveFontCacheFile();

using (var psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Agregar soporte para deformaciones verticales**

{{< highlight csharp >}}
var loadOptions = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var saveOptions = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string archivoArcoAbajo = Path.Combine(baseFolder, "1797_deformacion_arco_abajo_v.psd");
string archivoArcoArriba = Path.Combine(baseFolder, "1797_deformacion_arco_arriba_v.psd");
string archivoArco = Path.Combine(baseFolder, "1797_deformacion_arco_v.psd");
string archivoProtuberancia = Path.Combine(baseFolder, "1797_deformacion_protuberancia_v.psd");
string archivoBandera = Path.Combine(baseFolder, "1797_deformacion_bandera_v.psd");
string archivoPez = Path.Combine(baseFolder, "1797_pez_deformacion_v.psd");
string archivoSubida = Path.Combine(baseFolder, "1797_salida_subida_v.psd");
string archivoOnda = Path.Combine(baseFolder, "1797_salida_onda_v.psd");

string archivoSalidaArcoAbajo = Path.Combine(outputFolder, "1797_salida_arco_abajo_v.png");
string archivoSalidaArcoArriba = Path.Combine(outputFolder, "1797_salida_arco_arriba_v.png");
string archivoSalidaArco = Path.Combine(outputFolder, "1797_deformacion_arco_v.png");
string archivoSalidaProtuberancia = Path.Combine(outputFolder, "1797_deformacion_protuberancia_v.png");
string archivoSalidaBandera = Path.Combine(outputFolder, "1797_deformacion_bandera_v.png");
string archivoSalidaPez = Path.Combine(outputFolder, "1797_salida_pez_v.png");
string archivoSalidaSubida = Path.Combine(outputFolder, "1797_salida_subida_v.png");
string archivoSalidaOnda = Path.Combine(outputFolder, "1797_salida_onda_v.png");

using (var psdImage = (PsdImage)Image.Load(archivoArcoAbajo, loadOptions)) { psdImage.Save(archivoSalidaArcoAbajo, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoArcoArriba, loadOptions)) { psdImage.Save(archivoSalidaArcoArriba, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoArco, loadOptions)) { psdImage.Save(archivoSalidaArco, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoProtuberancia, loadOptions)) { psdImage.Save(archivoSalidaProtuberancia, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoBandera, loadOptions)) { psdImage.Save(archivoSalidaBandera, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoPez, loadOptions)) { psdImage.Save(archivoSalidaPez, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoSubida, loadOptions)) { psdImage.Save(archivoSalidaSubida, saveOptions); }
using (var psdImage = (PsdImage)Image.Load(archivoOnda, loadOptions)) { psdImage.Save(archivoSalidaOnda, saveOptions); }
{{< /highlight >}}
