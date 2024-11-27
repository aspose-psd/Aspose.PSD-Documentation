---
title: Capa de ajuste de curvas
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/curves/
---

# Trabajando con la capa de ajuste de curvas en Photoshop

El objetivo de este artículo es demostrar las capacidades de la biblioteca Aspose.PSD para Java al **trabajar con capas de ajuste de curvas** en documentos de Adobe® Photoshop®. La biblioteca es completamente autónoma. Por lo tanto, funciona sin necesidad de instalar el editor de fotos de Photoshop. La [lista completa de características](https://docs.aspose.com/psd/java/features/) se puede encontrar en nuestra base de conocimientos. Bueno, ahora volvamos a las Curvas.

## Resumen de la API

La herramienta Curvas se puede representar como una línea diagonal en un gráfico con reflejos en la esquina superior derecha y sombras en la esquina inferior derecha.

La biblioteca proporciona una API para trabajar con la curva, a saber, la clase [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Sin embargo, esta clase tiene **dos enfoques completamente diferentes** para trabajar con la curva. Por lo tanto, se puede editar en uno de dos modos en un momento dado:

- Continuo (la curva representada como un camino con puntos en lugares de flexión)
- Discreto (la curva representada como una línea punteada)

Por lo tanto, la biblioteca tiene dos formas de modificar la curva utilizando el [gestor continuo](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) y [gestor discreto](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) respectivamente. A continuación, explicaremos cómo utilizar cada uno de ellos en un ejemplo específico.

## Ajustar color y tono usando el Gestor Continuo de Curvas

El [Gestor Continuo de Curvas](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **configura puntos de flexión de una curva continua** para el canal compuesto (RGB) así como para cada canal de color en particular. Con fines de demostración, se aplicará un ajuste de Curvas (a) a una imagen oscurecida de una orquesta (b) para obtener una imagen iluminada con colores más cálidos (c):

![Figura 1 de la capa de ajuste de curvas](curves-psd-adjustment-layer-figure-1.png)

Dado que hay dos gestores, es necesario seleccionar explícitamente uno (gestor continuo en este caso) antes de obtenerlo. Después, podemos añadir puntos de curva directamente en ciertas coordenadas para los canales de color deseados (RGB compuesto, rojo y azul respectivamente) para recrear la forma de la curva:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

El origen de las coordenadas está en la esquina inferior izquierda. El valor de la coordenada máxima de un punto está limitado al tipo de datos (byte) y es igual a 255 (127 para el tipo firmado).

También hay algunos [otros métodos](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) que se pueden utilizar.

## Ajustar el tono usando el Gestor Discreto de Curvas

El Gestor Discreto de Curvas también permite posicionar puntos de curva (cambiar color y tono en realidad), pero la diferencia es que lo hacen de manera diferente. Primero, la **curva consiste en puntos** o puntos (no una línea sólida). Segundo, este gestor **no coloca un punto en cualquier lugar** en el gráfico. En su lugar, **mueve el punto hacia arriba o hacia abajo** con un rango de valores entre 255 y 0 respectivamente. Por defecto, los valores de los puntos de la curva aumentan incrementalmente para moldear una curva que está en un ángulo de 45 grados.

Por lo tanto, teniendo esto en cuenta, es fácil recrear el ajuste preestablecido de Photoshop "Negativo (RBG)" (a) y aplicarlo a una imagen en escala de grises de un valle (b) para obtener al final una representación negativa del valle (c).

![Figura 2 de la capa de ajuste de curvas](curves-psd-adjustment-layer-figure-2.png) En primer lugar, no olvide seleccionar el gestor correspondiente para poder utilizarlo y luego establezca los valores de los puntos de la curva en orden descendente comenzando desde 255 hasta 0 para cada punto de la curva (255 en total):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

El gestor también proporciona algunos [otros métodos](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) para gestionar la curva.

## Conclusión

En este artículo hemos aprendido cómo trabajar con capas de ajuste de curvas en documentos de Photoshop utilizando Aspose.PSD para Java en dos formas completamente diferentes (gestores continuo y discreto).
