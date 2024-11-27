---
title: Capa de ajuste de exposición
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/exposure/
---

# Trabajando con la capa de ajuste de exposición de Photoshop en Java

En este artículo vamos a añadir una capa de ajuste de exposición a un documento de Adobe® Photoshop® utilizando Aspose.PSD para Java, una librería de manipulación de archivos PSD. La librería funciona sin necesidad de tener instalado el editor de Photoshop, ya que utiliza sus propios algoritmos de procesamiento de imágenes. También hemos aprendido algunos detalles relacionados con la API de ajuste de exposición de la librería.

## Visión general de la API

La capa de ajuste de exposición se configura a través de la clase [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) que contiene las siguientes propiedades para trabajar con el ajuste de exposición:

- Define cuánta luz tiene la foto al comprimir o estirar todo el histograma en relación con los negros, afectando principalmente a los puntos más claros.
- A diferencia del desplazamiento de exposición que afecta principalmente a las sombras.
- Corrección gamma. Corrige la luminancia de la imagen.

## Corrección de exposición

Corregir la exposición y propiedades relacionadas es tan simple como cambiar algunas propiedades de la clase. Vamos a aplicar algunos ajustes de exposición (a) a una foto subexpuesta de una biblioteca (b) para hacerla perceptible al ojo humano (c).

![Ejemplo de capa de ajuste de exposición](exposure-adjustment-layer-figure-1.png)

El ajuste se realiza principalmente utilizando la corrección gamma. Sin embargo, la exposición y el desplazamiento también se ajustan un poco. Todo lo que necesita hacer es establecer valores apropiados a las propiedades ya mencionadas:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Tenga en cuenta que la exposición debe estar en un rango de -20.0 a 20.0, el valor del desplazamiento debe estar en un rango de -0.5 a 0.5 y el valor de corrección gamma debe estar entre 9.99 y 0.01.

Consulte la [referencia de la API de la capa de ajuste de exposición](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) para más detalles.

## Conclusión

En este artículo hemos aprendido cómo añadir una capa de ajuste de exposición a un archivo PSD para iluminar la imagen, así como considerado algunos detalles de la API.
