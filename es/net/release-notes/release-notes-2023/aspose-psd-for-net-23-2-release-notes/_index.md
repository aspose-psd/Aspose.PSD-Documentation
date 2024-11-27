---
title: Notas de lanzamiento Aspose.PSD para .NET 23.2
type: docs
weight: 110
url: /es/net/aspose-psd-para-net-23-2-notas-de-lanzamiento/
---

{{% alert color="primary" %}}

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1359|Reelaboración de la renderización de texto para mejorar el posicionamiento, renderización y soporte del texto|Mejora|
|PSDNET-1270|Agregar capacidad para procesar el Efecto Warp a través de la API pública|Función|
|PSDNET-1391|Agregar soporte para modos de interlineado de abajo hacia abajo y de arriba hacia arriba desde la configuración de párrafo|Función|
|PSDNET-912|Cambio de fuente y color para TextLayer PSD|Error|
|PSDNET-1022|Exportación incorrecta de texto en las pruebas TextUpdateTests, falta texto|Error|
|PSDNET-1221|Falta texto extra pequeño después de redimensionar la imagen PSD más grande|Error|
|PSDNET-1301|Aspose.Psd para .NET textLayer.UpdateText() imprime '-' (guion) como guion bajo de manera aleatoria para diferentes conjuntos de datos|Error|
|PSDNET-1379|Los ResolutionSettings no se aplican en la exportación de PSD a PDF|Error|


## **Cambios en la API pública**
# **APIs Agregadas:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **APIs Eliminadas:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Ejemplos de uso:**

**PSDNET-912. Cambiar fuente y color para TextLayer PSD**

{{< highlight csharp >}}
string carpetaFuentes = "Fuentes";
string archivoSrc = "M1PDTT26052021001.psd";
string psdSalida = "resultado.psd";
string pngSalida = "resultado.png";

FontSettings.SetFontsFolder(carpetaFuentes);

using (var imagen = (PsdImage)Image.Load(archivoSrc))
{
    TextLayer capaNombre = (TextLayer)imagen.Layers[9];
    var porciónTexto = capaNombre.TextData.Items[0];

    porciónTexto.Text = "MODESTO SR";
    porciónTexto.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    porciónTexto.Style.FillColor = Color.Red;

    capaNombre.TextData.UpdateLayerData();

    imagen.Save(psdSalida);
    imagen.Save(pngSalida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Exportación incorrecta de texto en las pruebas TextUpdateTests, falta texto**

{{< highlight csharp >}}
string archivoSrc = "ComplexKerningExample.psd";
string psdSalida = "TextUpdateComplexKerningExample_.psd";
string pngSalida = "TextUpdateComplexKerningExample_.png";

using (var imagen = (PsdImage)Image.Load(archivoSrc))
{
    for (int i = 0; i < imagen.Layers.Length; i++)
    {
        var capa = imagen.Layers[i] as TextLayer;

        if (capa != null)
        {
            capa.UpdateText("El texto ha sido actualizado");
        }
    }

    imagen.Save(psdSalida);
    imagen.Save(pngSalida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Falta texto extra pequeño después de redimensionar la imagen PSD más grande**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Agregar capacidad para procesar el Efecto Warp a través de la API pública**

{{< highlight csharp >}}
string archivoFuente = "source.psd";
string pngExportadoWarp = "warped.png";
string psdExportadoWarp = "warpFile.psd";

var opcionesCargaWarp = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var imagen = (PsdImage)Image.Load(archivoFuente, opcionesCargaWarp))
{
    imagen.Save(pngExportadoWarp, new PngOptions());
    imagen.Save(psdExportadoWarp, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd para .NET textLayer.UpdateText() imprime '-' (guion) como guion bajo de manera aleatoria para diferentes conjuntos de datos**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var capa in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (capa is TextLayer)
        {
            TextLayer capaTexto = capa as TextLayer;
            switch (capa.Name.Trim().ToUpper())
            {
                case "NOMBRE":
                    capaTexto.UpdateText("MR. JACK SMITH");
                    break;
                case "IDNO":
                    capaTexto.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNACIÓN":
                    capaTexto.UpdateText("OFICIAL-001");
                    break;
                case "GRUPOSANGUÍNEO":
                    capaTexto.UpdateText("AB-");
                    break;
                case "DIRECCIÓN":
                    capaTexto.UpdateText("BLOQUE-A, CALLE-7, APPT Nº - 047, SECTOR-024");
                    break;
                case "DIRECCIÓNPERM":
                    capaTexto.UpdateText("CASA Nº - 42, CALLE -025, VISTA DE PALMERAS, SECTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. Los ResolutionSettings no se aplican en la exportación de PSD a PDF**

{{< highlight csharp >}}
string entrada = "Datensatz 1.psd";
string salida = "Datensatz 1.pdf";

using (var imagen = Image.Load(entrada, new PsdLoadOptions()))
{
    ResolutionSetting configuraciónResolución = new ResolutionSetting(300, 300);

    imagen.Save(salida, new PdfOptions()
    {
        ResolutionSettings = configuraciónResolución
    });
}
{{< /highlight >}}

**PSDNET-1391. Agregar soporte para modos de interlineado de abajo hacia abajo y de arriba hacia arriba desde la configuración de párrafo**

{{< highlight csharp >}}
string entrada = "leadingMode.psd";
string salida = "output_leadingMode.png";

using (var imagenPsd = (PsdImage)Image.Load(entrada, new PsdLoadOptions()))
{
    IText texto1 = ((TextLayer)imagenPsd.Layers[1]).TextData;
    foreach (var porciónTexto in texto1.Items)
    {
        porciónTexto.Paragraph.LeadingType = LeadingType.TopToTop; // Cambiar el valor de LeadingType   
    }
    texto1.Items[8].Text = "TopToTop";
    texto1.Items[8].Style.FillColor = Color.ForestGreen;
    texto1.UpdateLayerData();

    IText texto2 = ((TextLayer)imagenPsd.Layers[2]).TextData;
    foreach (var porciónTexto in texto2.Items)
    {
        porciónTexto.Paragraph.LeadingType = LeadingType.BottomToBottom; // Cambiar el valor de LeadingType   
    }
    texto2.Items[8].Text = "BottomToBottom";
    texto2.Items[8].Style.FillColor = Color.ForestGreen;
    texto2.UpdateLayerData();

    imagenPsd.Save(salida, new PngOptions());
}
{{< /highlight >}}
