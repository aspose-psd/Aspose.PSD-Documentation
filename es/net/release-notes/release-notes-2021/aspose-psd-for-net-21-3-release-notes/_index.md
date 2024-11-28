---
title: Aspose.PSD para .NET 21.3 - Notas de la Versión
type: docs
weight: 100
url: /es/net/aspose-psd-para-net-21-3-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-823|Añadir la capa SectionDividerLayer para mejorar la experiencia con grupos de capas|Mejora|
|PSDNET-694|Al leer PattResource, el ancho y el alto estaban intercambiados|Error|
|PSDNET-789|Mezcla incorrecta de más de un efecto de capa|Error|
|PSDNET-805|Orden y lógica de mezcla incorrectos cuando hay más de un efecto de capa|Error|
|PSDNET-842|Propiedades de efecto de trazo no se guardan en el archivo PSD|Error|

## **Cambios en la API Pública**
# **APIs Añadidas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de Uso:**

**PSDNET-694. Al leer PattResource, el ancho y el alto estaban intercambiados**

{{< highlight csharp >}}
            string archivoFuente = "Untitled-1.psd";
            string archivoSalida = "salida.png";

            using (var imagen = (PsdImage)Image.Load(archivoFuente))
            {
                var capaRelleno = (FillLayer)imagen.Layers[1];
                capaRelleno.Update(); // invocar renderizado de patrón

                imagen.Save(archivoSalida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Mezcla incorrecta de más de un efecto de capa**

{{< highlight csharp >}}
            string archivoFuente = "fuente_789.psd";
            string rutaSmartObjectSalida = "salida789.png";
            string archivoSalida = "salida789.psd";

            using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var longitud = imagen.Layers.Length;
                for (int i = 0; i < longitud; i++)
                {
                    var smart = imagen.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var flujo = new MemoryStream(smart.Contents))
                        {
                            flujo.Position = 0;
                            using (var imagenEnSmart = (PsdImage)Image.Load(flujo))
                            {
                                for (int j = 0; j < imagenEnSmart.Layers.Length; j++)
                                {
                                    // Buscar Capa de Texto
                                    var capaTexto = imagenEnSmart.Layers[j] as TextLayer;
                                    if (capaTexto != null)
                                    {
                                        var datosTexto = capaTexto.TextData;

                                        datosTexto.Items[0].Texto = "Mejor";
                                        datosTexto.Items[0].Estilo.TamañoFuente = 170;
                                    }
                                }

                                smart.ReplaceContents(imagenEnSmart);
                            }
                        }

                        break;
                    }
                }
                // De esta manera estamos guardando el archivo PSD modificado
                imagen.Save(rutaSmartObjectSalida, new PngOptions() { TipoColor = PngColorType.TruecolorWithAlpha });
                imagen.Save(archivoSalida);
            }
{{< /highlight >}}

**PSDNET-805. Orden y lógica de mezcla incorrectos cuando hay más de un efecto de capa**

{{< highlight csharp >}}
            string archivoFuente = "1_200x200.psd";
            string archivoContenido = "NumerosMejor.png";

            string archivoSalidaPng = "salida.png";
            string archivoSalidaPsd = "salida.psd";

            using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var longitud = imagen.Layers.Length;
                for (int i = 0; i < longitud; i++)
                {
                    var smart = imagen.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(archivoContenido);
                        break;
                    }
                }

                //De esta manera estamos guardando el archivo PSD modificado
                imagen.Save(archivoSalidaPng, new PngOptions() { TipoColor = PngColorType.TruecolorWithAlpha });
                imagen.Save(archivoSalidaPsd);
            }
{{< /highlight >}}

**PSDNET-823. Añadir la capa SectionDividerLayer para mejorar la experiencia con grupos de capas**

{{< highlight csharp >}}
            // El siguiente código demuestra las capas SectionDividerLayer y cómo obtener el Grupo de capa relacionado.

            // Jerarquía de capas
            //    [0]: '</Grupo de capa>' SectionDividerLayer para Grupo 1
            //    [1]: 'Capa 1' Capa Regular
            //    [2]: '</Grupo de capa>' SectionDividerLayer para Grupo 2
            //    [3]: '</Grupo de capa>' SectionDividerLayer para Grupo 3
            //    [4]: 'Grupo 3' Grupo de Capa
            //    [5]: 'Grupo 2' Grupo de Capa
            //    [6]: 'Grupo 1' Grupo de Capa

            void AssertAreEqual(object esperado, object actual, string mensaje = null)
            {
                if (!object.Equals(esperado, actual))
                {
                    throw new FormatException(mensaje ?? "Los objetos no son iguales.");
                }
            }

            using (var imagen = new PsdImage(100, 100))
            {
                // Creando jerarquía de capas
                // Añadir el Grupo de Capa 'Grupo 1'
                LayerGroup grupo1 = imagen.AddLayerGroup("Grupo 1", 0, true);
                // Añadir capa regular
                Layer capa1 = new Layer();
                capa1.DisplayName = "Capa 1";
                grupo1.AddLayer(capa1);
                // Añadir el Grupo de Capa 'Grupo 2'
                LayerGroup grupo2 = grupo1.AddLayerGroup("Grupo 2", 1);
                // Añadir el Grupo de Capa 'Grupo 3'
                LayerGroup grupo3 = grupo2.AddLayerGroup("Grupo 3", 0);

                // Obtener los SectionDividerLayer
                SectionDividerLayer separador1 = (SectionDividerLayer)imagen.Layers[0];
                SectionDividerLayer separador2 = (SectionDividerLayer)imagen.Layers[2];
                SectionDividerLayer separador3 = (SectionDividerLayer)imagen.Layers[3];

                // mediante el método SectionDividerLayer.GetRelatedLayerGroup(), se obtiene la instancia de LayerGroup relacionada.
                AssertAreEqual(grupo1.DisplayName, separador1.GetRelatedLayerGroup().DisplayName); // el mismo Grupo de Capa
                AssertAreEqual(grupo2.DisplayName, separador2.GetRelatedLayerGroup().DisplayName); // el mismo Grupo de Capa
                AssertAreEqual(grupo3.DisplayName, separador3.GetRelatedLayerGroup().DisplayName); // el mismo Grupo de Capa

                LayerGroup carpeta1 = separador1.GetRelatedLayerGroup();
                AssertAreEqual(5, carpeta1.Layers.Length); // 'Grupo 1' contiene 5 capas
            }
{{< /highlight >}}

**PSDNET-842. Propiedades de efecto de trazo no se guardan en el archivo PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object esperado, object actual, string mensaje = null)
            {
                if (!object.Equals(esperado, actual))
                {
                    throw new FormatException(mensaje ?? "Los objetos no son iguales.");
                }
            }

            string archivoFuente = "malaCapaDeTrazo.psd";
            string salida = "salida.psd";

            using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var capa1 = new Layer();
                imagen.AddLayer(capa1);
                capa1.BlendingOptions.AddStroke(FillType.Color); // No lanzará ArgumentNullException

                StrokeEffect efectoTrazo = imagen.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                efectoTrazo.Size = 10;
                efectoTrazo.Position = StrokePosition.Outside;
                efectoTrazo.Overprint = true;

                imagen.Save(salida);
            }

            // Comprobar los valores guardados
            using (var imagen = (PsdImage)Image.Load(salida, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect efectoTrazo = (StrokeEffect)imagen.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, efectoTrazo.Size);
                AssertAreEqual(StrokePosition.Outside, efectoTrazo.Position);
                AssertAreEqual(true, efectoTrazo.Overprint);
            }
{{< /highlight >}}
