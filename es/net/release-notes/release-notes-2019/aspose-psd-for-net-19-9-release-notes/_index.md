---
title: Aspose.PSD para .NET 19.9 - Notas de la versión
type: docs
weight: 40
url: /es/net/aspose-psd-para-net-19-9-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-160|Nombre de capa incorrecto extraído|Característica|
|PSDNET-175|Obtención de propiedades de texto de una porción diferente de texto dentro de TextLayer PSD|Característica|
|PSDNET-190|Soporte para Agregar grupo de capas|Característica|
|PSDNET-192|Soporte de Propiedad de Escala para Capa de Relleno de Degradado|Característica|
|PSDNET-162|Ajuste de Brillo|Mejora|
|PSDNET-174|IndexOutOfRangeException al guardar la imagen PSD como JPEG|Error|
|PSDNET-180|Actualizar texto de capa de texto lanza una excepción|Error|
|PSDNET-182|Guardar imagen PSD después de la operación RotateFlip produce un archivo corrupto que no se puede abrir|Error|

## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**
**PSDNET-160. Nombre de capa incorrecto extraído**

Para mostrar correctamente el nombre de la capa, utilice la propiedad **DisplayName**. Ahora se ha añadido un setter para esta propiedad y la misma se puede modificar. Cuando Photoshop guarda el nombre de la capa utilizando la propiedad Name, los caracteres coreanos se almacenan como byte 63'?' en ASCII. Utilice la propiedad **DisplayName** porque la propiedad Name no admite caracteres coreanos.

{{< highlight java >}}

             // realizar cambios en los nombres de las capas y guardarlos

            using (var image = (PsdImage)Image.Load("capas con nombres.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var capa = image.Layers[i];

                    // establecer nuevo valor en la propiedad DisplayName

                    capa.DisplayName += "_modificado";

                }

                image.Save("salida.psd");

            }

{{< /highlight >}}

**PSDNET-175. Obtención de propiedades de texto de una porción diferente de texto dentro de TextLayer PSD**

{{< highlight java >}}

            const double Tolerancia = 0.0001;

            var rutaArchivo = "TresParrafosColores.psd";

            var rutaSalida = "TresParrafosColores_salida.psd";

            using (var im = (PsdImage)Image.Load(rutaArchivo))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var capa = im.Layers[i] as TextLayer;

                    if (capa != null)

                    {

                        var porciones = capa.TextData.Items;

                        if (porciones.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Comprobando texto de cada porción

                        if (porciones[0].Text != "Antiguo " ||

                            porciones[1].Text != "color" ||

                            porciones[2].Text != " texto\r" ||

                            porciones[3].Text != "Segundo párrafo\r")

                        {

                            throw new Exception();

                        }

                        // Comprobando datos de párrafos

                        // Los párrafos tienen diferentes justificaciones

                        if (

                            porciones[0].Paragraph.Justification != 0 ||

                            porciones[1].Paragraph.Justification != 0 ||

                            porciones[2].Paragraph.Justification != 0 ||

                            porciones[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Todas las demás propiedades del primer y segundo párrafo son iguales

                        for (int j = 0; j < porciones.Length; j++)

                        {

                            var parrafo = porciones[j].Paragraph;

                            if (Math.Abs(parrafo.AutoLeading - 1.2) > Tolerancia ||

                                parrafo.AutoHyphenate != false ||

                                parrafo.Burasagari != false ||

                                parrafo.ConsecutiveHyphens != 8 ||

                                Math.Abs(parrafo.StartIndent) > Tolerancia ||

                                Math.Abs(parrafo.EndIndent) > Tolerancia ||

                                parrafo.EveryLineComposer != false ||

                                Math.Abs(parrafo.FirstLineIndent) > Tolerancia ||

                                parrafo.GlyphSpacing.Length != 3 ||

                                Math.Abs(parrafo.GlyphSpacing[0] - 1) > Tolerancia ||

                                Math.Abs(parrafo.GlyphSpacing[1] - 1) > Tolerancia ||

                                Math.Abs(parrafo.GlyphSpacing[2] - 1) > Tolerancia ||

                                parrafo.Hanging != false ||

                                parrafo.HyphenatedWordSize != 6 ||

                                parrafo.KinsokuOrder != 0 ||

                                parrafo.LetterSpacing.Length != 3 ||

                                Math.Abs(parrafo.LetterSpacing[0]) > Tolerancia ||

                                Math.Abs(parrafo.LetterSpacing[1]) > Tolerancia ||

                                Math.Abs(parrafo.LetterSpacing[2]) > Tolerancia ||

                                parrafo.LeadingType != LeadingMode.Auto ||

                                parrafo.PreHyphen != 2 ||

                                parrafo.PostHyphen != 2 ||

                                Math.Abs(parrafo.SpaceBefore) > Tolerancia ||

                                Math.Abs(parrafo.SpaceAfter) > Tolerancia ||

                                parrafo.WordSpacing.Length != 3 ||

                                Math.Abs(parrafo.WordSpacing[0] - 0.8) > Tolerancia ||

                                Math.Abs(parrafo.WordSpacing[1] - 1.0) > Tolerancia ||

                                Math.Abs(parrafo.WordSpacing[2] - 1.33) > Tolerancia ||

                                Math.Abs(parrafo.Zone - 36.0) > Tolerancia)

                            {

                                throw new Exception();

                            }

                        }

                        // Comprobando datos de estilo

                        // Los estilos tienen diferentes colores y tamaño de fuente

                        if (Math.Abs(porciones[0].Style.FontSize - 12) > Tolerancia ||

                            Math.Abs(porciones[1].Style.FontSize - 12) > Tolerancia ||

                            Math.Abs(porciones[2].Style.FontSize - 12) > Tolerancia ||

                            Math.Abs(porciones[3].Style.FontSize - 10) > Tolerancia)

                        {

                            throw new Exception();

                        }

                        if (porciones[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            porciones[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            porciones[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            porciones[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < porciones.Length; j++)

                        {

                            var estilo = porciones[j].Style;

                            if (estilo.AutoLeading != false ||

                                estilo.HindiNumbers != false ||

                                estilo.Kerning != 0 ||

                                estilo.Leading != 0 ||

                                estilo.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                estilo.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Ejemplo de edición de texto

                        porciones[0].Text = "Hola ";

                        porciones[1].Text = "Mundo";

                        // Ejemplo de eliminación de porciones de texto

                        capa.TextData.RemovePortion(3);

                        capa.TextData.RemovePortion(2);

                        // Ejemplo de agregar nueva porción de texto

                        var porcionCreada = capa.TextData.ProducePortion();

                        porcionCreada.Text = "!!!\r";

                        capa.TextData.AddPortion(porcionCreada);

                        porciones = capa.TextData.Items;

                        // Ejemplo de edición de párrafo y estilo para porciones

                        // Establecer justificación derecha

                        porciones[0].Paragraph.Justification = 1;

                        porciones[1].Paragraph.Justification = 1;

                        porciones[2].Paragraph.Justification = 1;

                        // Colores diferentes para cada estilo. Serán cambiados, pero la renderización no está completamente soportada

                        porciones[0].Style.FillColor = Color.Aquamarina;

                        porciones[1].Style.FillColor = Color.Violeta;

                        porciones[2].Style.FillColor = Color.AzulClaro;

                        // Fuente diferente. Será cambiada, pero la renderización no está completamente soportada

                        porciones[0].Style.FontSize = 6;

                        porciones[1].Style.FontSize = 8;

                        porciones[2].Style.FontSize = 10;

                        capa.TextData.UpdateLayerData();

                        im.Save(rutaSalida, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Soporte para Agregar grupo de capas**

{{< highlight java >}}

             // -Grupo 1

            // --Capa 1

            // --Grupo 2

            // ---Capa 2

            // ---Capa 3

            // --Capa 4

            string rutaDatos = "prueba_psdnet190.psd";

            var opcionesCreacion = new PsdOptions();

            opcionesCreacion.Source = new FileCreateSource(rutaDatos, false);

            opcionesCreacion.Palette = new PsdColorPalette(new Color[] { Color.Verde });

            using (var imagenPsd = (PsdImage)Image.Create(opcionesCreacion, 500, 500))

            {

                LayerGroup grupo1 = imagenPsd.AddLayerGroup("Grupo 1", 0, true);

                Layer capa1 = new Layer(imagenPsd);

                capa1.Name = "Capa 1";

                grupo1.AddLayer(capa1);

                LayerGroup grupo2 = grupo1.AddLayerGroup("Grupo 2", 1);

                Layer capa2 = new Layer(imagenPsd);

                capa2.Name = "Capa 2";

                grupo2.AddLayer(capa2);

                Layer capa3 = new Layer(imagenPsd);

                capa3.Name = "Capa 3";

                grupo2.AddLayer(capa3);

                Layer capa4 = new Layer(imagenPsd);

                capa4.Name = "Capa 4";

                grupo1.AddLayer(capa4);

                imagenPsd.Save();

            }

{{< /highlight >}}

**PSDNET-192. Soporte de Propiedad de Escala para Capa de Relleno de Degradado**

{{< highlight java >}}

            using (var imagen = (PsdImage)Image.Load("CapaRellenoDegradado.psd"))

            {

                // obteniendo una capa de relleno

                FillLayer capaRelleno = null;

                foreach (var capa in imagen.Layers)

                {

                    capaRelleno = capa as FillLayer;

                    if (capaRelleno != null)

                    {

                        break;

                    }

                }

                var ajustes = capaRelleno.FillSettings as IGradientFillSettings;

                // actualizar valor de escala

                ajustes.Scale = 200;

                capaRelleno.Update(); // Actualiza los datos de píxeles

                imagen.Save("imagenEscala.png", new PngOptions() { TipoColor = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-174. IndexOutOfRangeException al guardar la imagen PSD como JPEG**

{{< highlight java >}}

          using (var imagen = Aspose.PSD.Image.Load("EjemploPSD.psd"))

        {

            imagen.Save("ejemploJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. Actualizar el texto de capa de texto lanza una excepción**

{{< highlight java >}}

           // Actualizar el texto de capa de texto lanza una excepción

            string rutaArchivo = "VoltearVertical.psd";

           