---
title: Capa de ajuste blanco y negro
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/levels/
---

## Trabajando con la capa de ajuste de niveles en Java

En este artículo aprenderemos cómo ajustar el rango tonal y el equilibrio de color de una foto en formato de archivo PSD de forma programática en Java. No utilizamos el editor de fotos Adobe® Photoshop® en sí. En cambio, utilizamos la biblioteca Aspose.PSD para Java que funciona de forma independiente para manipular el documento de Photoshop.

Aunque Aspose.PSD para Java admite más que suficientes [herramientas para editar la foto](/psd/es/java/manipulating-images/) como queremos, vamos a **utilizar la API de la capa de ajuste de niveles** que es una de las formas más simples y rápidas de hacer el trabajo.

## Resumen de la API

La implementación actual (20.6 en el momento de la escritura) de la API de la capa de ajuste de niveles **admite todas las características básicas de los niveles de Photoshop**, es decir, ajustar los niveles de entrada y salida para el canal compuesto (RGB) así como para cada canal de color primario (rojo, verde y azul).

La API de la capa de ajuste de niveles es directa. La clase [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) es un punto de entrada para el ajuste de niveles. Contiene un par de métodos para acceder a los canales de color: getMasterChannel y getChannel(int). Ambos métodos devuelven [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) que tiene propiedades correspondientes para la manipulación de los niveles de entrada y salida. La diferencia es que getMasterChannel sirve para ajustar el canal de color compuesto (RGB) mientras que getChannel accede a un canal de color particular (rojo, verde o azul) por su índice.

## Compatibilidad con modos de color

Vale la pena añadir que la capa de ajuste de niveles **es compatible con la gran mayoría de modos de color** según los niveles de Photoshop. Por lo tanto, es posible ajustar los niveles para imágenes en Escala de grises (canal de gris), RGB (canales RGB, rojo, verde y azul), CMYK (canales CMYK, cian, magenta, amarillo y negro), Duotono (canal monocromo) y LAB (luminosidad, canales a y b) modos de color.

## Ajustar rango tonal

En resumen, la corrección tonal se aplica a una imagen para remapear las sombras y los reflejos para una mejor distribución de los tonos medio. Generalmente, **hace que la imagen parezca más contrastada** , si se hace correctamente. Por ejemplo, tomemos una foto de un perro (b) y ajustemos su rango tonal (a – la captura de pantalla está tomada de la ventana de niveles de Photoshop para mayor claridad) para que la foto parezca más contrastada (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Figura de Capa de Ajuste de Niveles 1](levels-adjustment-figure-1.png)|

Para **ajustar el rango tonal general** de una imagen, los niveles de entrada del canal maestro deben estar configurados:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

Es necesario tener en cuenta que los niveles de entrada deben estar en un rango de 0 a 253 para las sombras, de 9,99 a 0,01 para los medios tonos y de 2 a 255 para los reflejos. El rango de los niveles de salida deben estar entre 0 y 255.

¿Necesitas más ejemplos? Puedes encontrarlos en [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) y en la [base de conocimientos](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Conclusión

Para resumir, Aspose.PSD para Java tiene una API práctica y sencilla para cambiar el rango tonal y el equilibrio de color de una imagen que es compatible con casi todos los modos de color. La API de la capa de ajuste de niveles de la biblioteca se parece a los niveles de Photoshop, por lo tanto, es fácil comenzar incluso si nunca has trabajado con la biblioteca antes.
