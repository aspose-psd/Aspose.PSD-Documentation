---
title: Notas de Lanzamiento de Aspose.PSD para .NET 22.3
type: docs
weight: 100
url: /es/net/aspose-psd-para-net-22-3-notas-de-lanzamiento/
---

{{% alert color="primary" %}}

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-210|Agregar propiedad IsOpen para Grupo de Capas|Característica|
|PSDNET-643|La imagen PSD con máscaras de capa de ráster descarta las máscaras al guardar en una imagen PSD de 16 bits|Error|
|PSDNET-899|El modo de mezcla Dissolve no se aplica a la carpeta con máscara|Error|
|PSDNET-1047|Un archivo específico no se puede abrir con Photoshop después de guardar en Aspose.PSD 21.11|Error|
|PSDNET-1068|Representación incorrecta de la capa con modo de mezcla Linear Dodge (Añadir)|Error|
|PSDNET-1069|La capa de Relleno de Patrón lanza una excepción al actualizarse después de cargarse|Error|


## **Cambios en la API pública**
# **APIs Agregadas:**

- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **APIs Eliminadas:**

- Ninguna


## **Ejemplos de uso:**

**PSDNET-210. Agregar propiedad IsOpen para Grupo de Capas**

{{< highlight csharp >}}
// Ejemplo de lectura y escritura de la propiedad IsOpen en tiempo de ejecución.
string nombreArchivoOrigen = "AbrirCerrarGrupoCapas.psd";
string nombreArchivoSalida = "Salida" + nombreArchivoOrigen;

using (var imagen = (PsdImage)Image.Load(nombreArchivoOrigen))
{
    foreach (var capa in imagen.Layers)
    {
        if (capa is LayerGroup && capa.Name == "Grupo 1")
        {
            bool estaAbiertoGrupo1 = ((LayerGroup)capa).IsOpen;
            ((LayerGroup)capa).IsOpen = !estaAbiertoGrupo1;
        }

        if (capa is LayerGroup && capa.Name == "Grupo 2")
        {
            bool estaAbiertoGrupo2 = ((LayerGroup)capa).IsOpen;           
            ((LayerGroup)capa).IsOpen = !estaAbiertoGrupo2;
        }
    }

    imagen.Save(nombreArchivoSalida);
}
{{< /highlight >}}

**PSDNET-643. La imagen PSD con máscaras de capa de ráster descarta las máscaras al guardar en una imagen PSD de 16 bits**

{{< highlight csharp >}}
            string rutaArchivoOrigen = "UnaRegularYUnaRegularConMascara.psd";
            string rutaArchivoSalida = "out_UnaRegularYUnaRegularConMascara.psd";

            using (PsdImage imagen = (PsdImage)Image.Load(rutaArchivoOrigen))
            {
                imagen.Save(rutaArchivoSalida, new PsdOptions(imagen)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. El modo de mezcla Dissolve no se aplica a la carpeta con máscara**

{{< highlight csharp >}}
            string archivoFuente = "psdnet899.psd";
            string archivoSalidaPng = "out_psdnet899.png";

            using (PsdImage imagen = (PsdImage) Image.Load(archivoFuente))
            {
                imagen.Save(archivoSalidaPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Un archivo específico no se puede abrir con Photoshop después de guardar en Aspose.PSD 21.11**

{{< highlight csharp >}}
            string archivoFuente = "psdnet1047.psd";
            string archivoSalidaPsd = "out_psdnet1047.psd";

            using (PsdImage imagen = (PsdImage) Image.Load(archivoFuente))
            {
                imagen.Save(archivoSalidaPsd);
            }

            // Es necesario abrir manualmente el archivo PSD de salida con Photoshop.

            using (PsdImage imagen = (PsdImage) Image.Load(archivoSalidaPsd))
            {
                // Sin excepciones.
            }
{{< /highlight >}}

**PSDNET-1068. Representación incorrecta de la capa con modo de mezcla Linear Dodge (Añadir)**

{{< highlight csharp >}}
            string archivoFuente = "roto.psd";
            string archivoSalidaPng = "out_roto.psd.png";

            using (var imagenPsd = (PsdImage) Image.Load(archivoFuente))
            {
                imagenPsd.Save(archivoSalidaPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. La capa de Relleno de Patrón lanza una excepción al actualizarse después de cargarse**

{{< highlight csharp >}}
            string archivoFuente = "CapaPsdTodosTipos.psd";

            using (var imagen = (PsdImage) Image.Load(archivoFuente))
            {
                var capaRelleno = (FillLayer)imagen.Layers[9];
                capaRelleno.Update();
            }
{{< /highlight >}}
