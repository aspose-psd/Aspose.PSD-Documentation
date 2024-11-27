---
title: Notas de la versión de Aspose.PSD para .NET 22.8
type: docs
weight: 50
url: /es/net/aspose-psd-para-net-22-8-notas-de-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD for .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1225|Investigar y corregir los problemas en el instalador|Mejora|
|PSDNET-800|Soporte de Línea de Tiempo de Fotogramas desde Archivo PSD|Característica|
|PSDNET-1219|Soporte de recurso 'mlst' que contiene en ShmdResource como un sub-recurso|Característica|
|PSDNET-814|Cambio del Hash de Capa al llamar a layer.BlendingOptions.Effects|Error|

## **Cambios en la API Pública**
# **APIs Añadidas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Delay
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.LayerStates
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.DisposalMethod
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Automatic
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.DoNotDispose
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Dispose
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.HorizontalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.VerticalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.FillOpacity
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.DescriptorVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.SubResourcesx

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-800. Soporte de Línea de Tiempo de Fotogramas desde Archivo PSD**

{{< highlight csharp >}}
string archivoOrigen = "imagen1219.psd";
string psdSalida = "imagen800_salida.psd";

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoOrigen))
{
    TimeLine lineaDeTiempo = TimeLine.InitializeFrom(imagenPsd);

    // Cambiar método de disposición del fotograma 1
    lineaDeTiempo.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // Cambiar retardo del fotograma 2
    lineaDeTiempo.Frames[1].Delay = 15;

    // Cambiar opacidad de 'Capa 1' en el fotograma 2
    LayerState estadoCapa11 = lineaDeTiempo.Frames[1].LayerStates[lineaDeTiempo.LayerIds[1]];
    estadoCapa11.Opacity = 50;

    // Mover 'Capa 1' a la esquina inferior izquierda en el fotograma 3
    LayerState estadoCapa21 = lineaDeTiempo.Frames[2].LayerStates[lineaDeTiempo.LayerIds[1]];
    estadoCapa21.Offset = new Point(-50, 230);

    // Agregar nuevo fotograma
    List<Frame> fotogramas = new List<Frame>(lineaDeTiempo.Frames);
    fotogramas.Add(new Frame(lineaDeTiempo));
    lineaDeTiempo.Frames = fotogramas.ToArray();

    // Cambiar modo de fusión de 'Capa 1' en el fotograma 4
    LayerState estadoCapa31 = lineaDeTiempo.Frames[3].LayerStates[lineaDeTiempo.LayerIds[1]];
    estadoCapa31.BlendMode = BlendMode.Dissolve;

    // Aplicar cambios de nuevo a la instancia de PsdImage
    lineaDeTiempo.ApplyTo(imagenPsd);
    imagenPsd.Save(psdSalida);
}
{{< /highlight >}}

**PSDNET-814. Hash de Capa cambia si llamamos a layer.BlendingOptions.Effects**

{{< highlight csharp >}}
string archivoOrigen = "AllTypesLayerPsd.psd";

using (var imagen = (PsdImage)Image.Load(archivoOrigen))
{
    var capa = imagen.Layers[0];
    var hashInicial = capa.GetHashCode();
    var efectos = capa.BlendingOptions.Effects;
    var hashFinal = capa.GetHashCode();

    if (hashInicial != hashFinal)
    {
        throw new Exception("El hash no debe haber cambiado");
    }
}
{{< /highlight >}}

**PSDNET-1219. Soporte de recurso 'mlst' que contiene en ShmdResource como un sub-recurso**

{{< highlight csharp >}}
string archivoOrigen = "imagen1219.psd";
string psdSalida = "imagen1219_salida.psd";

using (PsdImage imagen = (PsdImage)Image.Load(archivoOrigen))
{
    Layer capa1 = imagen.Layers[1];
    ShmdResource recursoShmd = (ShmdResource)capa1.Resources[8];
    MlstResource recursoMlst = (MlstResource)recursoShmd.SubResources[0];

    ListStructure listaEstadosCapa = (ListStructure)recursoMlst.Items[1];
    DescriptorStructure estadosCapasEnFrame1 = (DescriptorStructure)listaEstadosCapa.Types[1];
    BooleanStructure capaHabilitada = (BooleanStructure)estadosCapasEnFrame1.Structures[0];

    // Deshabilitar capa 1 en el fotograma 1
    capaHabilitada.Value = false;

    imagen.Save(psdSalida);
}
{{< /highlight >}}
