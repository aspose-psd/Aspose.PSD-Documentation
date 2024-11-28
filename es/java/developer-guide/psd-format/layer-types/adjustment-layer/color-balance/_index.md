---
title: Capa de ajuste de equilibrio de color
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/color-balance/
---

# Trabajando con la capa de ajuste de equilibrio de color en Photoshop en Java

En este artículo vamos a **ajustar el equilibrio de color de la imagen** en formato de archivo PSD en Java. Utilizaremos una librería especial llamada Aspose.PSD para Java que es una caja de herramientas para la manipulación de documentos de Photoshop.

Dado que la librería trabaja con el formato de archivo PSD, contiene casi [todas las funciones](https://docs.aspose.com/psd/java/features/) disponibles en el editor de Photoshop y la **capa de ajuste de equilibrio de color**, que es absolutamente adecuada para esta tarea, no es una excepción.

La capa de ajuste de equilibrio de color hace posible cambiar el equilibrio entre colores primarios (RGB) y colores sustractivos (CMY) para sombras, medios tonos y luces de manera simple y rápida.

## Ajustar el equilibrio de color

Como se mencionó anteriormente, la capa de ajuste de equilibrio de color en Aspose.PSD para Java es simplemente **un equilibrador entre colores primarios y sustractivos**. Esto significa que hay tres escalas para cada par de colores (cian/rojo, magenta/verde, amarillo/azul). La intensidad de un color en particular del par aumentará si el valor se acerca a él y viceversa. Además, esos tres pares inherentes a cada área del rango tonal (sombras, medios tonos y luces) aumentan la flexibilidad de este tipo de ajuste.

Entonces, apliquemos este conocimiento en la práctica. Como ejemplo, elegimos una foto rojiza del rostro de una mujer (b). El rostro es demasiado rojizo y vamos a corregirlo **agregando una capa de ajuste de equilibrio de color** para disminuir el rojo y aumentar el cian básicamente (a) para obtener un rostro que luzca más natural (c). Nuevamente, hay mucho trabajo por hacer con esta imagen, pero dentro de este artículo es todo lo que haremos.

![Ejemplo de capa de ajuste de equilibrio de color](color-balance-adjustment-layer-example-figure-1.png) La API de la capa de ajuste de equilibrio de color tiene un diseño plano. Por lo tanto, la [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) clase es todo lo que necesitas. En primer lugar, conserva la luminosidad porque está desactivada de forma predeterminada. Luego, agrega un poco de verde y un poco más de amarillo para las sombras utilizando los métodos correspondientes (cuyos nombres consisten en el nombre de la zona del rango tonal particular y los nombres de los colores en el par de colores), luego agrega más cian y un poco de azul para los medios tonos, y finalmente agrega más cian además de un poco de magenta y azul:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

¡Ahora tenemos la imagen que queríamos! ¡Es tan simple, ¿no es cierto?

Presta atención que _el valor de cada par de colores debe estar en el rango de -100 a 100_ que son valores negativos para colores sustractivos y positivos para colores primarios respectivamente, al igual que en el editor de Photoshop.

Consulta nuestra referencia de API para conocer más detalles técnicos sobre la [capa de ajuste de equilibrio de color](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Conclusión

En este artículo hemos considerado cómo ajustar el equilibrio de color de la imagen de forma programática en Java utilizando la librería Aspose.PSD para Java. La librería contiene una API completamente funcional para trabajar con capas de ajuste de equilibrio de color en documentos de Photoshop.
