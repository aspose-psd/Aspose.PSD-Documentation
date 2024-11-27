---
title: Soporte de capas de relleno
type: docs
weight: 50
url: /es/java/soporte-de-capas-de-relleno/
---

## **Soporte de capas de relleno con relleno de color**
Este artículo demuestra cómo rellenar una capa PSD con color. Por favor, utilice FillLayer de Aspose.PSD.FileFormats.Psd.Layers para añadir color en la capa PSD. Los siguientes fragmentos de código cargan un archivo PSD, acceden a la clase Filllayer y establecen el color usando la propiedad FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImágenes-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Soporte de capas de relleno con relleno de degradado**
Este artículo demuestra el uso de relleno de degradado para llenar una capa PSD. Aspose.PSD APIs han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto las clases GradientColorPoint y GradientTransparencyPoint para agregar efecto de degradado a una capa.

Los pasos para llenar una capa PSD con relleno de degradado son tan simples como los siguientes:

- Cargar un archivo PSD como una imagen utilizando el método Load expuesto por la clase Image.
- Establecer las propiedades de configuración del objeto FillLayer.
- Crear una lista de ColorPoints con los colores requeridos y la posición del color.
- Crear una lista de TransparencyPoints con la opacidad requerida y la posición del punto de transparencia.
- Llamar al método FillLayer.Update.
- Guardar los resultados.

El siguiente fragmento de código le muestra cómo añadir un relleno de degradado para llenar una capa PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImágenes-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Efecto de trazo con relleno de color**
Este artículo demuestra cómo renderizar el efecto de trazo con relleno de color. El efecto de trazo se utiliza para añadir trazos y bordes a capas y formas. Se puede utilizar para crear líneas de color sólido, degradados coloridos, así como bordes con patrones.

Los pasos para renderizar el efecto de trazo con relleno de color son tan simples como los siguientes:

- Establecer la propiedad de **LoadEffectsResource**.
- Cargar un archivo PSD como una imagen utilizando el método Load expuesto por la clase Image y definir **PsdLoadOptions**.
- Establecer las propiedades de configuración de **ColorFillSetting.**
- Guardar los resultados.

El siguiente fragmento de código le muestra cómo renderizar el efecto de trazo con relleno de color.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImágenes-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}



