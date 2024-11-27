---
title: Notas de la versión de Aspose.PSD para .NET 19.3
type: docs
weight: 100
url: /es/net/aspose-psd-para-net-19-3-notas-de-lanzamiento/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de Aspose.PSD para .NET 19.3

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-104|Renderizado de capas de texto rotadas por TransformMatrix|Característica|
|PSDNET-96|Implementar renderizado de efecto de trazo con color de relleno para exportación|Característica|
|PSDNET-112|Los transformadores de InnerData corrompen algunas capas con máscaras vectoriales|Error|
|PSDNET-113|Actualizar capa de texto para imagen PSD arroja un error al abrir en Photoshop|Error|

## **Cambios en la API pública**
# **APIs añadidas:**
- Ninguna
# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**
**PSDNET-104. Renderizado de capas de texto rotadas por TransformMatrix**

{{< highlight java >}}

 string nombreArchivoOrigen = "TextoTransformado.psd";

string rutaExportacion = "ExportacionTextoTransformado.psd";

string rutaExportacionPng = "ExportacionTextoTransformado.png";

var imagenPSD = (PsdImage) Image.Load(nombreArchivoOrigen);

using(imagenPSD) {

 imagenPSD.Save(rutaExportacion);

 imagenPSD.Save(rutaExportacionPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Implementar renderizado de efecto de trazo con color de relleno para exportación**

{{< highlight java >}}

  // Implementar renderizado de efecto de trazo con color de relleno para exportación

 string nombreArchivoOrigen = "TrazoComplejo.psd";

 string rutaExportacion = "RenderizadoTrazoComplejo.psd";

 string rutaExportacionPng = "RenderizadoTrazoComplejo.png";

 var opcionesCarga = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var imagenPSD = (PsdImage) Image.Load(nombreArchivoOrigen, opcionesCarga)) {

  for (int i = 0; i < imagenPSD.Layers.Length; i++) {

   var efecto = (StrokeEffect) imagenPSD.Layers[i].BlendingOptions.Effects[0];

   var ajustes = (ColorFillSettings) efecto.FillSettings;

   ajustes.Color = Color.DeepPink;

  }

  // Guardar PSD

  imagenPSD.Save(rutaExportacion, new PsdOptions());

  // Guardar PNG

  imagenPSD.Save(rutaExportacionPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Los transformadores de InnerData corrompen algunas capas con máscaras vectoriales**

{{< highlight java >}}

 // Los transformadores de InnerData corrompen algunas capas con máscaras vectoriales

var archivoFuente = "1.psd";

var rutaPNG = "PruebaRotarVoltear2617.png";

var rutaPSD = "PruebaRotarVoltear2617.psd";

var tipoVolteo = RotateFlipType.Rotate270FlipXY;

using(var imagenPSD = (PsdImage)(Image.Load(archivoFuente))) {

 imagenPSD.RotateFlip(tipoVolteo);

 imagenPSD.Save(rutaPNG, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 imagenPSD.Save(rutaPSD);

}

{{< /highlight >}}

**PSDNET-113. Actualizar capa de texto para imagen PSD arroja un error al abrir en Photoshop**

{{< highlight java >}}

 string nombreArchivoOrigen = "Prueba.psd";

string rutaExportacion = "Resultado.psd";

using(Image imagen = Image.Load(nombreArchivoOrigen)) {

 if (!(imagen is PsdImage)) {

  return;

 }

 PsdImage imagenPSD = (PsdImage) imagen;

 Layer[] capas = imagenPSD.Layers;

 for (int indice = capas.Length - 1; indice >= 0; indice--) {

  Layer capa = capas[indice];

  if (!(capa is TextLayer)) {

   continue;

  }

  TextLayer capaTexto = (TextLayer) capa;

  capaTexto.UpdateText("\\()");

 }

 PsdOptions opcionesImagen = new PsdOptions(imagenPSD);

 imagenPSD.Save(rutaExportacion, opcionesImagen);

}

// El archivo debe abrirse sin excepciones y ser legible para Photoshop

using(Image imagen = Image.Load(rutaExportacion)) {}

{{< /highlight >}}
