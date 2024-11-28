---
title: Capa de ajuste de brillo y contraste
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/brightness-contrast/
---

# Trabajando con la capa de ajuste de brillo/contraste de Photoshop en Java

En este artículo aplicaremos un ajuste de brillo/contraste a un documento de Adobe® Photoshop® utilizando la biblioteca Aspose.PSD for Java®. Además, aprenderemos más sobre las características de la biblioteca relacionadas con este tipo de capa de ajuste a lo largo del camino.

Pero primero un poco de teoría.

La capa de ajuste de brillo/contraste cambia el brillo y contraste de la imagen. Pero espera un minuto, ¿qué significa realmente? Aumentar el brillo aclara el valor del color hasta blanco y disminuir el brillo oscurece el valor del color hasta negro. Aumentar el contraste a su vez aumentará la diferencia entre los colores claros y oscuros, y disminuir el contraste disminuirá esa diferencia respectivamente; lo que significa que los colores claros se vuelven más claros y los oscuros más oscuros.

## El soporte del modo de color

La biblioteca permite agregar una capa de ajuste de brillo/contraste a imágenes en modo de color RGB, CMYK o Lab.

## El comportamiento actual y heredado

La implementación actual de la biblioteca (v20.6 en el momento de la escritura) utiliza el algoritmo predeterminado de Photoshop que conserva el rango tonal completo desde las sombras hasta los reflejos, pero aún no soporta el comportamiento heredado. Esto significa que la biblioteca admite la capa de ajuste de brillo/contraste en documentos creados en las últimas versiones de Photoshop (CS4 y superior). Sin embargo, puedes [solicitar la implementación heredada de la capa de ajuste de brillo/contraste](https://forum.aspose.com/c/psd) en nuestro foro si lo necesitas.

## Ajustar brillo y contraste

Ahora describamos cómo funciona la API de alto nivel de la capa de ajuste de brillo/contraste (anticipando, la API es sencilla). La clase PsdImage contiene un método de fábrica (addBrightnessContrastAdjustmentLayer) para instanciar la clase BrightnessContrastLayer que es la puerta de entrada para el ajuste de brillo y contraste. La clase BrightnessContrastLayer solo contiene un par de métodos de obtención y establecimiento para acceder a las propiedades de brillo y contraste, así como para cambiar sus valores.

![|Ejemplo de capa de ajuste de brillo/contraste en PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Entonces, tomemos una imagen de un perro (b), por ejemplo, para ajustar su brillo1 y contraste2 (a), utilizando únicamente el método de fábrica con los argumentos correspondientes, para eventualmente obtener una imagen (c) que luzca más vívida:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Notas:

1. El valor de brillo debe estar en el rango de -150 a 150.
2. El valor de contraste debe estar en el rango de -50 a 100.

Consulta la documentación de [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) para más detalles.

## Conclusión

En este artículo hemos obtenido una rápida visión general de la capa de ajuste de brillo/contraste y aprendido cómo ajustar el brillo y el contraste de la imagen utilizando el método de fábrica.

Consulta nuestra serie de [artículos sobre las APIs de capa de ajuste](/psd/es/java/layer-types/adjustment-layer/) de Aspose.PSD para Java para obtener más información.
