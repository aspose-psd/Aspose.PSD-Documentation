---
title: Notas de Lanzamiento de Aspose.PSD for .NET 22.5
type: docs
weight: 80
url: /es/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento para [Aspose.PSD for .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-952|Agregar propiedad EffectType a la interfaz ILayerEffect|Característica|
|PSDNET-1146|Refactorización de la Clase ChannelData|Mejora|
|PSDNET-657|Hacer que la propiedad de opacidad funcione para DropShadowEffect|Error|
|PSDNET-825|Dibujo incorrecto de la capa de ajuste a través de la capa transparente en un caso específico|Error|
|PSDNET-1168|Mejorar el método Colorize. Colorizar gris + configurar el color correcto cuando la saturación no es del 100%|Error|
|Artículo|[Cómo ejecutar Aspose.PSD en Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Documentación|


## **Cambios en la API Pública**
# **APIs Añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor(Aspose.PSD.FileFormats.Psd.CompressionMethod,System.Int32,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ILayerEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorOverlayEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.DropShadowEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.EfectoTipo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EfectoTipo
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.DropShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.OuterGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.PatternOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.GradientOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.ColorOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.Satin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.InnerGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.InnerShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.Stroke
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TiposDeEfectosDeCapa.BevelEmboss


# **APIs Eliminadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Ejemplos de Uso:**

**PSDNET-657. Hacer que la propiedad de opacidad funcione para DropShadowEffect**

{{< highlight csharp >}}
string archivoEntrada = "entrada.psd";
string imagenSalida20 = "imagenSalida20.png";
string imagenSalida200 = "imagenSalida200.png";

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoEntrada, new LoadOptions()))
{
    Capa capaTrabajo = imagenPsd.Layers[1];

    DropShadowEffect efectoSombra = capaTrabajo.BlendingOptions.AddDropShadow();
    efectoSombra.Distance = 0;
    efectoSombra.Size = 8;

    // Ejemplo con Opacidad = 20
    efectoSombra.Opacity = 20;
    imagenPsd.Save(imagenSalida20, new PngOptions());

    // Ejemplo con Opacidad = 200
    efectoSombra.Opacity = 200;
    imagenPsd.Save(imagenSalida200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Dibujo incorrecto de la capa de ajuste a través de la capa transparente en un caso específico**

{{< highlight csharp >}}
string archivoFuente = "entrada_825.psd";
string salidaPng = "salida_psdnet825.png";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    foreach (var item in imagenPsd.Layers)
    {
        item.IsVisible = false;
    }
    var capa = imagenPsd.Layers[3];
    imagenPsd.Layers[1].IsVisible = true;
    imagenPsd.Layers[3].IsVisible = true;
    imagenPsd.Layers[4].IsVisible = true;
    imagenPsd.Layers[7].IsVisible = true;

    var ancho = capa.Width;
    var alto = capa.Height;
    var límitesCapa = new Rectangle(capa.Izquierda, capa.Arriba, ancho, alto);
    var límites = new Rectangle(0, 0, ancho, alto);
    var imagen = new PsdImage(límites.Ancho, límites.Alto);

    imagen.SaveArgb32Pixels(límites, imagenPsd.LoadArgb32Pixels(límitesCapa));

    imagen.Save(salidaPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. Agregar propiedad EffectType a la interfaz ILayerEffect**

{{< highlight csharp >}}
string archivoEntrada = "entrada.psd";
string salidaSin = "salidaSin.png";
string salidaCon = "salidaCon.png";

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoEntrada, new LoadOptions()))
{
    imagenPsd.Save(salidaSin, new PngOptions());

    Capa capaTrabajo = imagenPsd.Layers[1];

    DropShadowEffect efectoSombra = capaTrabajo.BlendingOptions.AddDropShadow();
    efectoSombra.Distance = 0;
    efectoSombra.Size = 8;
    efectoSombra.Opacity = 20;

    foreach (ILayerEffect iEfecto in capaTrabajo.BlendingOptions.Effects)
    {
        if (iEfecto.EffectType == LayerEffectsTypes.DropShadow)
        {
            // lo atrapó
            imagenPsd.Save(salidaCon, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Mejorar el método Colorize. Colorizar gris + configurar el color correcto cuando la saturación no es del 100%**

{{< highlight csharp >}}
string archivoSrc = "Colorize.psd";            
string salidaSimple = "salida_simple.png";
string salidaColorize = "salida_colorize.png";

using (var imagenPsd = (PsdImage)Image.Load(archivoSrc))
{
    // Imagen sin la propiedad Colorize
    imagenPsd.Save(salidaSimple, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Establecer la propiedad Colorize
    foreach (Capa capa in imagenPsd.Layers)
    {
        if (capa is HueSaturationLayer)
        {
            HueSaturationLayer capaSaturaciónMatiz = (HueSaturationLayer)capa;
            capaSaturaciónMatiz.Colorize = true;
            break;
        }
    }
    
    // Imagen con la propiedad Colorize
    imagenPsd.Save(salidaColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
