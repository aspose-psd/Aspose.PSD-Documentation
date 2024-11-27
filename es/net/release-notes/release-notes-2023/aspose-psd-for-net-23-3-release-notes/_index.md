---
title: Notas de la versión de Aspose.PSD para .NET 23.3
type: docs
weight: 100
url: /es/net/aspose-psd-for-net-23-3-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-146|Soporte de la capa de ajuste de Posterizar|Característica|
|PSDNET-1366|Implementar soporte de VscgResource|Característica|
|PSDNET-1437|Agregar soporte del recurso PostResource para datos de la capa de ajuste de Posterizar|Característica|
|PSDNET-931|Exportación incorrecta a capa PNG con ajuste de Curvas y modo de color CMYK|Error|
|PSDNET-1403|Se pierde el estilo de párrafo después de guardar y actualizar el archivo por PS|Error|
|PSDNET-1453|Renderizado incorrecto de efectos de resplandor y sombra en texto|Error|


## **Cambios en la API pública**
# **APIs añadidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-146. Soporte de la capa de ajuste de Posterizar**

{{< highlight csharp >}}
string archivoFuente = "zendeya_posterize.psd";
string archivoSalida = "zendeya_posterize_10.psd";

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions()))
{
    foreach (Layer capa in imagen.Layers)
    {
        if (capa is PosterizeLayer)
        {
            ((PosterizeLayer)capa).Levels = 10;
            imagen.Save(archivoSalida);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Exportación incorrecta a capa PNG con ajuste de Curvas y modo de color CMYK**

{{< highlight csharp >}}
string archivoSrc = "input_LevelsLayerWithLayerMaskCmyk.psd";
string archivoSalida = "output_LevelsLayerWithLayerMaskCmykTest.png";
string archivoPsdSalida = "output.psd";

var opcionesCargaPsd = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage imagen = (PsdImage)Image.Load(archivoSrc, opcionesCargaPsd))
{
    imagen.Save(archivoPsdSalida, new PsdOptions()); // la parte ', new PsdOptions()' provoca un error.
    imagen.Save(archivoSalida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Implementar soporte de VscgResource**

{{< highlight csharp >}}
string archivoFuente = "StrokeInternalFill_src.psd";
string archivoSalida = "StrokeInternalFill_res.psd";

void SonIguales(double esperado, double actual, double tolerancia = 0.1)
{
    if (Math.Abs(esperado - actual) > tolerancia)
    {
        throw new Exception(
        $"Los valores no son iguales.\nEsperado: {esperado}\nResultado: {actual}\nDiferencia: {esperado - actual}");
    }
}

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    VscgResource vscgResource = (VscgResource)imagen.Layers[1].Resources[0];
    DescriptorStructure estructuraColorRgb = (DescriptorStructure)vscgResource.Items[0];

    SonIguales(89.8, ((DoubleStructure)estructuraColorRgb.Structures[0]).Value);
    SonIguales(219.6, ((DoubleStructure)estructuraColorRgb.Structures[1]).Value);
    SonIguales(34.2, ((DoubleStructure)estructuraColorRgb.Structures[2]).Value);

    ((DoubleStructure)estructuraColorRgb.Structures[0]).Value = 255d; // Rojo
    ((DoubleStructure)estructuraColorRgb.Structures[1]).Value = 0d; // Verde
    ((DoubleStructure)estructuraColorRgb.Structures[2]).Value = 0d; // Azul

    imagen.Save(archivoSalida);
}

// comprobando cambios
using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida))
{
    VscgResource vscgResource = (VscgResource)imagen.Layers[1].Resources[0];
    DescriptorStructure estructuraColorRgb = (DescriptorStructure)vscgResource.Items[0];

    SonIguales(255, ((DoubleStructure)estructuraColorRgb.Structures[0]).Value);
    SonIguales(0, ((DoubleStructure)estructuraColorRgb.Structures[1]).Value);
    SonIguales(0, ((DoubleStructure)estructuraColorRgb.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Estilo de párrafo faltante después de guardar el archivo y actualizarlo por PS**

{{< highlight csharp >}}
string archivoFuente = "PSDTest3.psd";
string archivoSalida = "output.psd";

string[] nuevoTexto = new string[]
{
    "Título \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage imagen = (PsdImage)Aspose.PSD.Image.Load(archivoFuente))
{
    TextLayer capaTexto = imagen.AddTextLayer("Nueva capa", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var datosTexto = capaTexto.TextData;

    ITextStyle estiloPorDefecto = datosTexto.ProducePortion().Style;

    ITextParagraph párrafoPorDefecto = datosTexto.ProducePortion().Paragraph;
    ITextPortion[] nuevasPorcionesTexto = datosTexto.ProducePortions(nuevoTexto, estiloPorDefecto, párrafoPorDefecto);

    nuevasPorcionesTexto[0].Style.FontSize = 14;
    nuevasPorcionesTexto[0].Style.FontName = "TwCenMT-Bold";

    nuevasPorcionesTexto[1].Style.Leading = 20;
    nuevasPorcionesTexto[1].Style.FontSize = 10;
    nuevasPorcionesTexto[1].Style.FontName = "TwCenMT-Bold";

    // Eliminar el texto anterior
    datosTexto.RemovePortion(0);

    // Agregar nuevas porciones de texto
    foreach (var nuevaPorción in nuevasPorcionesTexto)
    {
        datosTexto.AddPortion(nuevaPorción);
    }

    datosTexto.UpdateLayerData();

    imagen.Save(archivoSalida);
}

using (PsdImage imagenPsd = (PsdImage)Aspose.PSD.Image.Load(archivoSalida))
{
    Txt2Resource recursoTxt2 = (Txt2Resource)imagenPsd.GlobalLayerResources[1];
    byte[] bytes = recursoTxt2.Data;
    string datosTxt2 = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        datosTxt2 += (char)bytes[i];
    }

    string clave0 = @" >> /6 0 >> >> /1 "; // prefijo de longitud del párrafo 0
    string clave1 = @" >> /6 1 >> >> /1 "; // prefijo de longitud del párrafo 1
    int índice0 = datosTxt2.IndexOf(clave0);
    int índice1 = datosTxt2.IndexOf(clave1);

    string longPar0 = datosTxt2.Substring(índice0 + clave0.Length, 1);
    string longPar1 = datosTxt2.Substring(índice1 + clave1.Length, 3);

    string esperado0 = nuevoTexto[0].Length.ToString();
    string esperado1 = (nuevoTexto[1].Length + 1).ToString();

    if (longPar0 != esperado0 || longPar1 != esperado1)
    {
        throw new Exception(
            $"La longitud de los párrafos es incorrecta.\nEsperado: {esperado0} y {esperado1}\nResultado: {longPar0} y {longPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Agregar soporte del recurso PostResource para datos de la capa de ajuste de Posterizar**

{{< highlight csharp >}}
string archivoFuente = "zendeya_posterize.psd";
string archivoSalida = "zendeya_posterize_10.psd";

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions()))
{
    Layer capa = imagen.Layers[1];

    foreach (LayerResource recurso in capa.Resources)
    {
        if (recurso is PostResource)
        {
            ((PostResource)recurso).Levels = 10;
            imagen.Save(archivoSalida);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Renderizado incorrecto de efectos de resplandor y sombra en texto**

{{< highlight csharp >}}
string archivoPsdSalida = "effect_bug.psd";
string archivoPngSalida = "effect_bug.png";

using (var imagenPsd = new PsdImage(500, 500))
{
    // Agregar capas de texto
    Aspose.PSD.Rectangle áreaTexto1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle áreaTexto2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle áreaTexto3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer capaTexto1 = imagenPsd.AddTextLayer("Texto con Efectos", áreaTexto1);
    TextLayer capaTexto2 = imagenPsd.AddTextLayer("Texto con Efectos", áreaTexto2);
    TextLayer capaTexto3 = imagenPsd.AddTextLayer("Texto con Efectos", áreaTexto3);

    // Modificar capas de texto
    capaTexto1.TextData.Items[0].Style.FontSize = 150;
    capaTexto1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    capaTexto1.TextData.UpdateLayerData();

    capaTexto2.TextData.Items[0].Style.FontSize = 150;
    capaTexto2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    capaTexto2.TextData.UpdateLayerData();

    capaTexto3.TextData.Items[0].Style.FontSize = 150;
    capaTexto3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    capaTexto3.TextData.UpdateLayerData();

    // Agregar efectos
    OuterGlowEffect resplandorExterno = capaTexto1.BlendingOptions.AddOuterGlow(); // romper
    resplandorExterno.Spread = 15;
    ((ColorFillSettings)resplandorExterno.FillColor).Color = Color.Red;

    var sombra = capaTexto2.BlendingOptions.AddDropShadow(); // romper con texto largo
    sombra.Distance = 25;
    sombra.Color = Color.DarkBlue;

    var sombraInterior = capaTexto3.BlendingOptions.AddInnerShadow(); // romper con texto largo
    sombraInterior.UseGlobalLight = false;
    sombraInterior.Angle = -179;
    sombraInterior.Distance = 10;
    sombraInterior.Size = 8;
    sombraInterior.Color = Color.HotPink;

    // exportar
    imagenPsd.Save(archivoPsdSalida);
    imagenPsd.Save(archivoPngSalida, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}