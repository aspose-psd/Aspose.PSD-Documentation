---
title: Notas de la versión de Aspose.PSD para .NET 19.11
type: docs
weight: 20
url: /es/net/aspose-psd-for-net-19-11-notas-de-version/
---

{{% alert color="primary" %}} 

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-151|[Soporte de Efecto de Capa de Sombra Interna](/psd/es/net/efectos-de-sombra-en-photoshop/#efectosdesombraenphotoshop-efectodesombradentro)|Característica|
|PSDNET-135|[Implementar renderizado de Capa de Relleno: Patrón](/psd/es/net/soporte-de-capas-de-relleno/#soportedecapasderellenocapasconrellenodepatrón)|Característica|
|PSDNET-187|[Soporte de Imágenes Raster en Archivos AI](/psd/es/net/manipulación-de-formatos-de-adobe-illustrator/#manipulacióndeformatosdeadobeillustrator-imágenesrasterenillustrator)|Característica|
|PSDNET-225|[Obtener propiedades de formateo en línea de TextLayer](/psd/es/net/trabajando-con-capas-de-texto/#trabajandoconcapasdetextosobtenerpropiedadesdetextodeunacapa)|Característica|
|PSDNET-214|Exportación incorrecta de PSD a otros formatos si contiene Efectos de Capa y Capas de Ajuste|Error|

## **Cambios en la API Pública**
# **APIs Agregadas:**
- T:Aspose.PSD.FileFormats.Ai.AiSection
- M:Aspose.PSD.FileFormats.Ai.AiSection.GetData
- P:Aspose.PSD.FileFormats.Ai.AiImage.Layers
- M:Aspose.PSD.FileFormats.Ai.AiImage.AddLayer(Aspose.PSD.FileFormats.Ai.AiLayerSection)
- T:Aspose.PSD.FileFormats.Ai.AiLayerSection
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.RasterImages
- M:Aspose.PSD.FileFormats.Ai.AiLayerSection.AddRasterImage(Aspose.PSD.FileFormats.Ai.AiRasterImageSection)
- T:Aspose.PSD.FileFormats.Ai.AiRasterImageSection
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Pixels
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.OffsetX
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.OffsetY
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Width
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Angle
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.LeftBottomShift
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Height
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddInnerShadow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.UseGlobalLight
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Distance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.UseGlobalLight
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Distance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Noise
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.GetFonts
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.FontType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Script
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Synthetic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.PostScriptName
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.FamilyName
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Style
# **APIs Eliminadas:**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **Ejemplos de Uso:**
**PSDNET-151. Soporte de Efecto de Capa de Sombra Interna**

{{< highlight java >}}

            string sourceFile = "muestra.psd";

            string destName = "muestra_salida.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (var imagen = (PsdImage)Image.Load(sourceFile, loadOptions))

            {

                var capa = imagen.Layers[imagen.Layers.Length - 1];

                var efectoSombra = (IShadowEffect)capa.BlendingOptions.Effects[0];

                efectoSombra.Color = Color.Green;

                efectoSombra.Opacity = 128;

                efectoSombra.Distance = 1;

                efectoSombra.UseGlobalLight = false;

                efectoSombra.Size = 2;

                efectoSombra.Angle = 45;

                efectoSombra.Spread = 50;

                efectoSombra.Noise = 5;

                imagen.Save(destName, new PsdOptions(imagen));

            }

{{< /highlight >}}

**PSDNET-135. Implementar renderizado de Capa de Relleno: Patrón**

{{< highlight java >}}

            string sourceFile = "muestra.psd";

            string destName = "muestra_salida.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (var imagen = (PsdImage)Image.Load(sourceFile))

            {

                foreach (var capa in imagen.Layers)

                {

                    if (capa is FillLayer)

                    {

                        var capaRelleno = (FillLayer)capa;

                        var configuración = (IPatternFillSettings)capaRelleno.FillSettings;

                        configuración.HorizontalOffset = -5;

                        configuración.VerticalOffset = 12;

                        configuración.Scale = 300;

                        configuración.Linked = true;

                        configuración.PatternData = new int[]

                                                   {

                                                       Color.Black.ToArgb(), Color.Red.ToArgb(),

                                                       Color.Green.ToArgb(), Color.Blue.ToArgb(),

                                                       Color.White.ToArgb(), Color.AliceBlue.ToArgb(),

                                                       Color.Violet.ToArgb(), Color.Chocolate.ToArgb(),

                                                       Color.IndianRed.ToArgb(), Color.DarkOliveGreen.ToArgb(),

                                                       Color.CadetBlue.ToArgb(), Color.YellowGreen.ToArgb(),

                                                       Color.Black.ToArgb(), Color.Azure.ToArgb(),

                                                       Color.ForestGreen.ToArgb(), Color.Sienna.ToArgb(),

                                                   };

                        configuración.PatternHeight = 4;

                        configuración.PatternWidth = 4;

                        configuración.PatternName = "$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0";

                        configuración.PatternId = Guid.NewGuid().ToString() + "\0";

                        capaRelleno.Update();

                        break;

                    }

                }

                imagen.Save(destName, new PsdOptions(imagen));

            }

{{< /highlight >}}

**PSDNET-187. Soporte de Imágenes Raster en Archivos AI**

{{< highlight java >}}

            const double ToleranciaPredeterminada = 1e-6;

void AssertIsTrue(bool condición, string mensaje) {

 if (!condición) {

  throw new FormatException(mensaje);

 }

}

string archivoFuente = "muestra.ai";

using(AiImage imagen = (AiImage) Image.Load(archivoFuente)) {

 AiLayerSection capa = imagen.Layers[0];

 AssertIsTrue(capa.RasterImages != null, "La propiedad RasterImages no debería ser nula");

 AssertIsTrue(capa.RasterImages.Length == 1, "La propiedad RasterImages debería contener exactamente un ítem");

 AiRasterImageSection imagenRaster = capa.RasterImages[0];

 AssertIsTrue(imagenRaster.Pixels != null, "La propiedad rasterImage.Pixels no debería ser nula");

 AssertIsTrue(imagenRaster.Pixels.Length == 100, "La propiedad rasterImage.Pixels debería contener exactamente 100 ítems");

 AssertIsTrue((uint) imagenRaster.Pixels[99] == 0xFFB21616, "imagenRaster.Pixels[99] debería ser 0xFFB21616");

 AssertIsTrue((uint) imagenRaster.Pixels[19] == 0xFF00FF00, "imagenRaster.Pixels[19] debería ser 0xFF00FF00");

 AssertIsTrue((uint) imagenRaster.Pixels[10] == 0xFF01FD00, "imagenRaster.Pixels[10] debería ser 0xFF01FD00");

 AssertIsTrue((uint) imagenRaster.Pixels[0] == 0xFF0000FF, "imagenRaster.Pixels[0] debería ser 0xFF0000FF");

 AssertIsTrue(Math.Abs(0.999875 - imagenRaster.Width) < ToleranciaPredeterminada, "imagenRaster.Width debería ser 0.99987");

 AssertIsTrue(Math.Abs(0.999875 - imagenRaster.Height) < ToleranciaPredeterminada, "imagenRaster.Height debería ser 0.99987");

 AssertIsTrue(Math.Abs(387 - imagenRaster.OffsetX) < ToleranciaPredeterminada, "imagenRaster.OffsetX debería ser 387");

 AssertIsTrue(Math.Abs(379 - imagenRaster.OffsetY) < ToleranciaPredeterminada, "imagenRaster.OffsetY debería ser 379");

 AssertIsTrue(Math.Abs(0 - imagenRaster.Angle) < ToleranciaPredeterminada, "imagenRaster.Angle debería ser 0");

 AssertIsTrue(Math.Abs(0 - imagenRaster.LeftBottomShift) < ToleranciaPredeterminada, "imagenRaster.LeftBottomShift debería ser 0");

 AssertIsTrue(Math.Abs(0 - imagenRaster.ImageRectangle.X) < ToleranciaPredeterminada, "imagenRaster.ImageRectangle.X debería ser 0");

 AssertIsTrue(Math.Abs(0 - imagenRaster.ImageRectangle.Y) < ToleranciaPredeterminada, "imagenRaster.ImageRectangle.Y debería ser 0");

 AssertIsTrue(Math.Abs(10 - imagenRaster.ImageRectangle.Width) < ToleranciaPredeterminada, "imagenRaster.ImageRectangle.Width debería ser 10");

 AssertIsTrue(Math.Abs(10 - imagenRaster.ImageRectangle.Height) < ToleranciaPredeterminada, "imagenRaster.ImageRectangle.Height debería ser 10");

}

{{< /highlight >}}

**PSDNET-225. Obtener propiedades de formateo en línea de TextLayer**

{{< highlight java >}}

     using (var imagenPsd = (PsdImagen)Imagen.Cargar("formato_en_linea.psd"))

            {

                List<ITextPortion> textoRegular = new List<ITextPortion>();

                List<ITextPortion> textoNegrita = new List<ITextPortion>();

                List<ITextPortion> textoCursiva = new List<ITextPortion>();

                var capas = imagenPsd.Layers;

                for (int índice = 0; índice < capas.Longitud; índice++)

                {

                    var capa = capas[índice];

                    if (!(capa es TextLayer))

                    {

                        continuar;

                    }

                    var capaTexto = (TextLayer)capa;

                    // obtiene fuentes que contiene la capa de texto

                    var fuentes = capaTexto.GetFonts();

                    var porcionesTexto = capaTexto.TextData.Items;

                    foreach (var porciónTexto in porcionesTexto)

                    {

                        TextFontInfo fuente = fuentes[porciónTexto.Style.FontIndex];

                        if (fuente != null)

                        {

                            switch (fuente.Style)

                            {

                                case FontStyle.Regular:

                                    textoRegular.Agregar(porciónTexto);

                                    romper;

                                case FontStyle.Bold:

                                    textoNegrita.Agregar(porciónTexto);

                                    romper;

                                case FontStyle.Italic:

                                    textoCursiva.Agregar(porciónTexto);

                                    romper;

                                defecto:

                                    lanzar nuevo ArgumentOutOfRangeException();

                            }

                        }

                    }

                }

            }

{{< /highlight >}}



**PSDNET-214. Exportación incorrecta de PSD a otros formatos si contiene Efectos de Capa y Capas de Ajuste**

{{< highlight java >}}

     var opcionesCarga = new PsdLoadOptions();

   opcionesCarga.LoadEffectsResource = true;

   usando (var imagen = (PsdImagen)Imagen.Cargar("clip_shadow.psd", opcionesCarga))

   {

       imagen.Guardar("salida.png", new PngOptions());

   }

{{< /highlight >}}