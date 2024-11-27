---
title: Capa de ajuste del mezclador de canales
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/channel-mixer/
---

# Trabajando con la capa de ajuste del mezclador de canales de Photoshop en Java

Hoy veremos cómo mezclar colores de canales en documentos de Photoshop programáticamente en Java. Dado que el editor de Photoshop no admite scripts de Java, utilizaremos una biblioteca especial de manipulación de formatos de archivo PSD llamada Aspose.PSD para Java.

La biblioteca contiene una **API para trabajar con canales de color**. Hay varias formas de mezclar colores, pero en este artículo nos centraremos en la capa de ajuste del mezclador de canales.

La API de la capa de ajuste del mezclador de canales **permite jugar con los canales de color** para hacer imágenes tenidas, crear diferentes efectos de color creativos o incluso convertir la imagen en una en blanco y negro. A continuación, consideraremos cómo aplicar la capa de ajuste del mezclador de canales a un documento de Photoshop existente utilizando Aspose.PSD para Java, pero primero necesitamos hablar sobre las características generales de la API.

## Resumen de la API

No hay nada especial en la creación de la capa de ajuste del mezclador de canales. Se puede agregar a través del [método de fábrica predeterminado](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) que devuelve una instancia de la clase ChannelMixerLayer. Esta clase contiene funcionalidades generales como la opción de Monocromo y un método para obtener un canal de salida. Un canal de salida particular puede ser uno de dos tipos: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) o [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). El tipo de [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) depende del [modo de color](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) de la imagen.

## Hacer la imagen monocromática

Ahora, consideremos un ejemplo de aplicación de la capa de ajuste del mezclador de canales a un documento de Photoshop existente. Dado que este tipo de capa de ajuste aún no admite preajustes, recrearemos el preajuste de Photoshop de Fotografía infrarroja en blanco y negro (RGB) (a). El preajuste se aplicará a la imagen de un árbol en flor (b). Como resultado, queremos lograr el efecto de la fotografía infrarroja (c).

![Ejemplo de Capa de Ajuste del Mezclador de Canales](channel-mixer-adjustment-psd-layer-figure-1.png) Primero, para recrear el preajuste de Photoshop de Fotografía infrarroja en blanco y negro (RGB) es necesario activar la bandera de monocromo y establecer valores en bruto adecuados para cada color (rojo, verde y azul) en el canal de salida Gris:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome(**true**);
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed((**short**)-70);
    grayOutputChannel.setGreen((**short**)200);
    grayOutputChannel.setBlue((**short**)-30);

La imagen debe estar en modo de color RGB para que el código funcione (debido a la conversión a la clase RgbMixerChannel). El modo de color CMYK también es compatible, pero solo para imágenes con el modo de color correspondiente.

Ten en cuenta que el valor de cada color, así como la propiedad Constant, deben estar en el rango de -200 a 200.

## Conclusión

En este artículo consideramos cómo trabajar con la API del mezclador de canales de Aspose.PSD para Java para ajustar colores en los canales de color, así como convertir la imagen en blanco y negro.
