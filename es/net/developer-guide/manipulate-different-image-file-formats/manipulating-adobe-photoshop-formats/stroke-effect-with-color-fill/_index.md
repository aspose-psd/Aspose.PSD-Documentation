---
title: Efecto de trazo con relleno de color
type: docs
weight: 60
url: /es/net/stroke-effect-with-color-fill/
---

## **Efecto de trazo con relleno de color**
Este artículo demuestra cómo renderizar el efecto de trazo con relleno de color. El efecto de trazo se utiliza para agregar trazos y bordes a capas y formas. Se puede utilizar para crear líneas de color sólido, degradados coloridos, así como bordes con patrones.

Los pasos para renderizar el efecto de trazo con relleno de color son tan simples como se muestra a continuación:

- Establecer la propiedad [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource).
- Cargar un archivo PSD como imagen utilizando el método de fábrica Load expuesto por la clase de Image y definir [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions).
- Establecer las propiedades de configuración de [**ColorFillSetting**.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- Guardar los resultados.

El siguiente fragmento de código te muestra cómo renderizar el efecto de trazo con relleno de color.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
