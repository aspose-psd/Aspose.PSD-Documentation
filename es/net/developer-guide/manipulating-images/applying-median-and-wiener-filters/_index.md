---
title: Aplicación de filtros de mediana y Wiener
type: docs
weight: 10
url: /es/aplicando-filtros-de-mediana-y-wiener/
---

## **Aplicación de filtros de mediana y Wiener**
El filtro de mediana es una técnica de filtrado digital no lineal, a menudo utilizado para eliminar ruido. Esta reducción de ruido es un paso de preprocesamiento típico para mejorar los resultados del procesamiento posterior. El filtro de Wiener es el filtro lineal estacionario óptimo de error cuadrático medio (MSE) para imágenes degradadas por ruido aditivo y desenfoque. Con Aspose.PSD para .NET, los desarrolladores de API pueden aplicar un filtro de mediana para reducir el ruido de la imagen y pueden aplicar un filtro Gauss Wiener en las imágenes. Este artículo demuestra cómo se pueden aplicar los filtros de mediana y Gauss Wiener a las imágenes.
### **Aplicación del filtro de mediana**
Aspose.PSD proporciona la clase [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) para aplicar un filtro en una [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). El fragmento de código proporcionado a continuación muestra cómo aplicar el filtro de mediana a una imagen de ráster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-Conversion-AplicarFiltrosMedianaYWiener-AplicarFiltrosMedianaYWiener.cs" >}}


### **Aplicación del filtro Gauss Wiener**
Aspose.PSD proporciona la clase [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) para aplicar un filtro en una [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). El fragmento de código proporcionado a continuación muestra cómo aplicar el filtro Gauss Wiener a una imagen de ráster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-Conversion-AplicarFiltrosGaussWiener-AplicarFiltrosGaussWiener.cs" >}}


### **Aplicación del filtro Gauss Wiener para imagen en color**
Aspose.PSD también proporciona [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) para imágenes en color. El fragmento de código proporcionado a continuación muestra cómo aplicar el filtro Gauss Wiener a una imagen en color.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-Conversion-AplicarFiltrosGaussWienerParaImagenColor-AplicarFiltrosGaussWienerParaImagenColor.cs" >}}


### **Aplicación del filtro Wiener de movimiento**
Aspose.PSD proporciona la clase [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) para aplicar un filtro en una [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). El fragmento de código proporcionado a continuación muestra cómo aplicar un filtro de Wiener de movimiento a una imagen de ráster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-Conversion-AplicarFiltrosWienerDeMovimiento-AplicarFiltrosWienerDeMovimiento.cs" >}}


## **Aplicación de filtro de corrección en una imagen**
Este artículo demuestra el uso de Aspose.PSD para .NET para realizar filtros de corrección en una imagen. Las APIs de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD para .NET ha expuesto las clases [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) y [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) para la filtración. La clase BilateralSmoothingFilterOptions necesita un entero como tamaño. Los pasos para realizar el cambio de tamaño son simples y se detallan a continuación:

1. Cargar una imagen utilizando el método de fábrica Load expuesto por la clase Image.
1. Convertir la imagen en RasterImage.
1. Crear una instancia de las clases BilateralSmoothingFilterOptions y SharpenFilterOptions.
1. Llamar al método [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) especificando el rectángulo como límites de la imagen e instancia de la clase BilateralSmoothingFilterOptions.
1. Llamar al método [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) especificando el rectángulo como límites de la imagen e instancia de la clase SharpenFilterOptions.
1. Ajustar el contraste.
1. Establecer el brillo.
1. Guardar los resultados.


## **Uso del algoritmo de umbral de Bradley**
La segmentación de imágenes se usa en aplicaciones gráficas. El objetivo de la segmentación de una imagen es clasificar los píxeles como "oscuros" o "claros". Aspose.PSD API le permite utilizar el umbral de Bradley al convertir imágenes. El siguiente fragmento de código le muestra cómo definir el valor de umbral y luego invocar el algoritmo de umbral de Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
