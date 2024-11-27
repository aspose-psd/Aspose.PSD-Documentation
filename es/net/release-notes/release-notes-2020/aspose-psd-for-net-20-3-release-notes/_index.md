---
title: Notas de la versión de Aspose.PSD para .NET 20.3
type: docs
weight: 100
url: /es/net/aspose-psd-para-net-20-3-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión para [Aspose.PSD para .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-188|Soporte de .Net Core|Característica|
|PSDNET-523|Convertir archivos de Adobe Illustrator en PDF|Característica|
|PSDNET-212|Agregar capacidad para representar diferentes estilos en una capa de texto|Característica|
|PSDNET-144|Soporte de Capa de Ajuste en Blanco y Negro|Característica|
|PSDNET-233|Agregar soporte para exportar formato AI (Versión 8) a otros formatos|Característica|
|PSDNET-540|Soporte de Modo de Mezcla de Pase de Procesamiento (Utilizado solo para Grupos de Capas).|Característica|
|PSDNET-539|Excepción: Falla al cargar imagen con Nombres Alfa Unicode vacíos|Error|
|PSDNET-541|Salida incorrecta después de cambiar la visibilidad de un Grupo de Capas|Error|
|PSDNET-516|Excepción al cargar imagen PSD: La sección de color (Recurso de Sombra) debe contener 3 componentes de color para RGB o 4 componentes de color para CMYK|Error|
|PSDNET-536|Excepción al intentar dibujar en una capa recién creada si se usa la versión simple del Constructor|Error|

## **Cambios en la API pública**
# **APIs añadidas:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**
**PSDNET-523. Convertir archivos de Adobe Illustrator en PDFs**

{{< highlight java >}}

 string archivoFuente = "rect2_color.ai";

using (var imagenAI = (AiImage)Image.Load(archivoFuente))

{

    imagenAI.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Agregar capacidad para representar diferentes estilos en una capa de texto**

{{< highlight java >}}

 string archivoFuente = "text212.psd";

string archivoEthalon = "Ethalon_text212.psd";

string archivoSalida = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(archivoFuente))

{

    TextLayer capaTexto = (TextLayer)img.Layers[1];

    IText datosTexto = capaTexto.TextData;

    ITextStyle estiloPredeterminado = datosTexto.ProducePortion().Style;

    ITextParagraph parrafoPredeterminado = datosTexto.ProducePortion().Paragraph;

    estiloPredeterminado.FillColor = Color.DimGray;

    estiloPredeterminado.FontSize = 51;

    datosTexto.Items[1].Style.Strikethrough = true;

    ITextPortion[] nuevasPorciones = datosTexto.ProducePortions(new string[] { "E=mc",  "2\r",  "Negrita",  "Cursiva\r",  "Texto en minúsculas" }, estiloPredeterminado, parrafoPredeterminado);

    nuevasPorciones[0].Style.Underline = true; // editar estilo de texto "E=mc"

    nuevasPorciones[1].Style.FontBaseline = FontBaseline.Superscript; // editar estilo de texto "2\r"

    nuevasPorciones[2].Style.FauxBold = true; // editar estilo de texto "Negrita"

    nuevasPorciones[3].Style.FauxItalic = true; // editar estilo de texto "Cursiva\r"

    nuevasPorciones[3].Style.BaselineShift = -25; // editar estilo de texto "Cursiva\r"

    nuevasPorciones[4].Style.FontCaps = FontCaps.SmallCaps; // editar estilo de texto "Texto en minúsculas"

    foreach (var nuevaPorcion in nuevasPorciones)

    {

        datosTexto.AddPortion(nuevaPorcion);

    }

    datosTexto.UpdateLayerData();

    img.Save(archivoSalida);

}

{{< /highlight >}}

**PSDNET-233. Agregar soporte para exportar AI formato (Versión 8) a otros formatos**

{{< highlight java >}}

 // Ejemplo de exportar archivo AI a formato PSD y PNG

string nombreArchivoFuente = "form_8.ai";

string nombreArchivoSalida = "form_8_export";

using (AiImage imagen = (AiImage)Image.Load(nombreArchivoFuente))

{

    imagen.Save(nombreArchivoSalida + ".psd", new PsdOptions());

    imagen.Save(nombreArchivoSalida + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Soporte de Procesamiento de Modo de Mezcla de Pase (Utilizado solo para Grupos de Capas).**

{{< highlight java >}}

 void AssertIsTrue(bool condicion, string mensaje)

{

    if (!condicion)

    {

        throw new FormatException(mensaje);

    }

}

string nombreArchivoFuente = "Apple.psd";

string nombreArchivoSalida = "Salida" + nombreArchivoFuente;

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))

{

    AssertIsTrue(imagen.Layers.Length >= 23, "No hay una 23ra capa.");

    var capa = imagen.Layers[23] as LayerGroup;

    AssertIsTrue(capa != null, "La 23ra capa no es un grupo de capas.");

    AssertIsTrue(capa.Name == "GrupoAjuste", "El nombre de la 23ra capa no es 'GrupoAjuste'.");

    AssertIsTrue(capa.BlendModeKey == BlendMode.PassThrough, "La capa de GrupoAjuste debería tener un modo de mezcla 'pase por'.");

    imagen.Save(nombreArchivoSalida, new PsdOptions());

    imagen.Save("SalidaApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    capa.BlendModeKey = BlendMode.Normal;

    imagen.Save("Normal" + nombreArchivoSalida, new PsdOptions());

    imagen.Save("NormalSalidaApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Actualizar texto de capa de texto lanza una excepción**

{{< highlight java >}}

 // Actualizar texto de capa de texto lanza una excepción

string rutaArchivo = "FlipVertical.psd";

string rutaSalida = "FlipVertical_cambiado.psd";

var nuevoTexto = "Prueba";

using (var imagen = Image.Load(rutaArchivo))

{

    var imagenPSD = imagen as PsdImage;

    if (imagen == null)

    {

        return;

    }

    var capas = imagenPSD.Layers;

    for (var indice = capas.Length - 1; indice >= 0; indice--)

    {

        var capa = capas[indice] as TextLayer;

        if (capa == null)

        {

            continue;

        }

        capa.UpdateText(nuevoTexto);

    }

    var opcionesImagen = new PsdOptions(imagenPSD);

    imagenPSD.Save(rutaSalida, opcionesImagen);

}

{{< /highlight >}}

**PSDNET-182. Guardar imagen PSD después de la operación RotateFlip produce un archivo corrupto que no se puede abrir.**

{{< highlight java >}}

 string nombreArchivoFuente = "1.psd";

RotateFlipType tipoFlip = RotateFlipType.Rotate270FlipXY;

string nombreArchivoSalidaPsd = "RotateFlipTest2617.psd";

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))

{

    imagen.RotateFlip(tipoFlip);

    imagen.Save(nombreArchivoSalidaPsd);

}

// Debería ejecutarse sin excepciones

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoSalidaPsd)) 

{

    // No hacer nada

}

{{< /highlight >}}

**PSDNET-539. Excepción: Fallo al cargar imagen con Recurso de Nombres Alfa Unicode vacíos**

{{< highlight java >}}

 string rutaArchivo = "apple.psd";

using (var imagenPSD = (PsdImage)Image.Load(rutaArchivo)) // Aquí no deberíamos obtener excepciones

{

    // no hacer nada

}

{{< /highlight >}}

**PSDNET-541. Salida incorrecta después de cambiar la visibilidad de un Grupo de Capas**

{{< highlight java >}}

 string archivoFuente = "input.psd";

string archivoSalida = "output.psd";

// realizar cambios en los nombres de las capas y guardarlo

using (var imagen = (PsdImage)Image.Load(archivoFuente))

{

    for (int i = 0; i < imagen.Layers.Length; i++)

    {

        var capa = imagen.Layers[i];

        // Apagar todo dentro de un grupo

        if (capa is LayerGroup)

        {

            capa.IsVisible = false;

        }

    }

    imagen.Save(archivoSalida);

}

{{< /highlight >}}

**PSDNET-516. Excepción al cargar imagen PSD: La sección de color (Recurso de Sombra) debe contener 3 componentes de color para RGB o 4 componentes de color para CMYK**

{{< highlight java >}}

 string archivoFuente = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(archivoFuente)) // Aquí no deberíamos obtener excepciones

{

    // no hacer nada

}

{{< /highlight >}}

**PSDNET-536. Excepción si se intenta dibujar en una capa recién creada si se usa la versión simple del Constructor**

{{< highlight java >}}

 string archivoSalida = "output.psd";

int ancho = 100;

int alto = 100;

using (var imagen = new PsdImage(ancho, alto))

{

    var capa = new Layer();

    capa.Bottom = alto;

    capa.Right = ancho;

    imagen.AddLayer(capa);

    Graphics grafico = new Graphics(capa);

    grafico.Clear(Color.Yellow);

    // dibujar un rectángulo con la herramienta de Pluma

    grafico.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // dibujar otro rectángulo con Brocha Sólida en color Azul

    grafico.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    imagen.Save(archivoSalida);

}

{{< /highlight >}}
