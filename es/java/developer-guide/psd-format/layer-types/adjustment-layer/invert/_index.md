---
title: Capa de ajuste de Inversión
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/invert/
---

# Trabajando con la capa de ajuste de Inversión en Photoshop en Java

En este artículo vamos a mostrar cómo convertir una imagen en un documento de Photoshop a negativo de manera programática en Java. Para este propósito, utilizaremos la biblioteca para la manipulación de formatos de archivo PSD llamada Aspose.PSD para Java.

La API de inversión de colores permite **agregar un efecto negativo a una imagen**. Es posible que ya hayas visto cómo [invertir los colores de una imagen usando la capa de ajuste de Curvas](/psd/es/java/layer-types/adjustment-layer/curves/). Sin embargo, hoy consideraremos una forma más rápida y sencilla de hacer el trabajo con la capa de ajuste de Inversión.

## Resumen de la API

**La API de la capa de ajuste de Inversión** consiste en la clase de la capa en sí misma que es [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Esta clase no tiene miembros públicos propios, ya que hereda todos los miembros públicos de la clase padre ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Este hecho simplifica su uso porque todo lo que necesitas hacer es agregarla a un archivo PSD y la imagen se convierte en negativa.

## Invertir colores de imagen

Entonces, aunque parezca obvio, permítenos demostrar por claridad cómo **aplicar la capa de ajuste de Inversión a la imagen** de un astronauta (a) para crear el efecto negativo en esa imagen (b).

![Ejemplo de capa de ajuste Invertir Antes y Después](invert-adjustment-layer-figure-1.png)

Para **invertir los colores de una imagen** solo agrega una capa de ajuste de Inversión en el PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

¡Eso es todo! No hay propiedades específicas que configurar para este tipo de capa de ajuste.

## Conclusión

En este artículo aprendimos acerca de la API de la capa de ajuste de Inversión de Aspose.PSD para Java. Es una herramienta sencilla para obtener imágenes en negativo debido a que la API de esta capa de ajuste no declara ningún miembro público.
