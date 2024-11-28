---
title: Aplicación de Filtros de Mediana y Wiener
type: docs
weight: 10
url: /es/java/aplicando-filtros-de-mediana-y-wiener/
---

## **Aplicando Filtros de Mediana y Wiener**
El filtro de mediana es una técnica de filtrado digital no lineal, a menudo utilizado para eliminar ruido. Esta reducción de ruido es un paso predefinido típico para mejorar los resultados de procesamientos posteriores. El filtro de Wiener es el filtro lineal estacionario óptimo de error cuadrático medio (MSE) para imágenes degradadas por ruido aditivo y desenfoque. Utilizando Aspose.PSD para Java API, los desarrolladores pueden aplicar el filtro de mediana para reducir el ruido de la imagen y aplicar el filtro de Wiener de Gauss en imágenes. Este artículo demuestra cómo se pueden aplicar los filtros de mediana y Wiener de Gauss a imágenes.
### **Aplicando Filtro de Mediana**
Aspose.PSD proporciona la clase MedianFilterOptions para aplicar un filtro en una RasterImage. El fragmento de código proporcionado a continuación demuestra cómo aplicar un filtro de mediana a una imagen de ráster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Aplicando Filtro de Wiener de Gauss**
Aspose.PSD proporciona la clase GaussWienerFilterOptions para aplicar un filtro en una RasterImage. El fragmento de código proporcionado a continuación demuestra cómo aplicar el filtro de Wiener de Gauss a una imagen de ráster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Aplicando Filtro de Wiener de Gauss para Imagen a Color**
Aspose.PSD proporciona GaussWienerFilterOptions para imágenes a color también. El fragmento de código proporcionado a continuación demuestra cómo aplicar el filtro de Wiener de Gauss a una imagen a color.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Aplicando Filtro de Wiener de Movimiento**
Aspose.PSD proporciona la clase MotionWienerFilterOptions para aplicar un filtro en una RasterImage. El fragmento de código proporcionado a continuación muestra cómo aplicar el filtro de Wiener de movimiento a una imagen de ráster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Aplicar Filtros de Corrección en una Imagen**
Este artículo demuestra el uso de Aspose.PSD para Java para realizar filtros de corrección en una imagen. Las API de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD para Java ha expuesto las clases BilateralSmoothingFilterOptions y SharpenFilterOptions para la filtración. La clase BilateralSmoothingFilterOptions necesita un entero como tamaño. Los pasos para realizar el redimensionamiento son tan simples como los siguientes:

1. Cargar una imagen utilizando el método de fábrica Load expuesto por la clase Imagen.
1. Convertir la imagen en RasterImage.
1. Crear instancias de las clases BilateralSmoothingFilterOptions y SharpenFilterOptions.
1. Llamar al método RasterImage.Filter especificando el rectángulo como los límites de la imagen e instancia de la clase BilateralSmoothingFilterOptions.
1. Llamar al método RasterImage.Filter especificando el rectángulo como los límites de la imagen e instancia de la clase SharpenFilterOptions.
1. Ajustar el contraste
1. Establecer el brillo
1. Guardar los resultados.

El siguiente fragmento de código te muestra cómo aplicar el filtro de corrección.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Utilizar el algoritmo de umbral de Bradley**
La segmentación de imagen se utiliza en aplicaciones de gráficos. El objetivo de segmentar una imagen es clasificar los píxeles como "oscuros" o "claros". Aspose.PSD API te permite usar la segmentación de Bradley al convertir imágenes. El siguiente fragmento de código te muestra cómo definir el valor de umbral y luego invocar el algoritmo de umbral de Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
