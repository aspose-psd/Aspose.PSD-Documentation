---
title: Agregar una Marca de Agua a una Imagen
type: docs
weight: 30
url: /es/net/agregar-una-marca-de-agua-a-una-imagen/
---

## **Agregar una Marca de Agua a una Imagen**
Este documento explica cómo agregar una marca de agua a una imagen usando Aspose.PSD. Agregar una marca de agua a una imagen es un requisito común para aplicaciones de procesamiento de imágenes. Este ejemplo utiliza la clase Graphics para dibujar una cadena en la superficie de la imagen.
### **Agregar una Marca de Agua**
Para demostrar la operación, cargaremos una imagen BMP desde el disco y dibujaremos una cadena como la marca de agua en la superficie de la imagen usando el método DrawString de la clase Graphics. Guardaremos la imagen en formato PNG utilizando la clase PngOptions. A continuación se muestra un ejemplo de código que muestra cómo agregar una marca de agua a una imagen. El código de ejemplo se ha dividido en partes para facilitar su seguimiento. Paso a paso, los ejemplos muestran cómo:

1. [Cargar](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) una imagen.
1. Crear e inicializar un objeto [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Crear e inicializar objetos Font y [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Dibujar una cadena como marca de agua usando el método [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) de la clase Graphics.
1. Guardar la imagen en PNG.

El siguiente fragmento de código le muestra cómo agregar una marca de agua a la imagen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Agregar una Marca de Agua Diagonal**
Agregar una marca de agua diagonal a una imagen es similar a agregar una marca de agua horizontal como se discutió anteriormente, con algunas diferencias. Para demostrar la operación, cargaremos una imagen JPG desde el disco, agregaremos transformaciones usando un objeto de la clase [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) y dibujaremos una cadena como la marca de agua en la superficie de la imagen utilizando el método DrawString de la clase Graphics. A continuación se muestra un ejemplo de código que muestra cómo agregar una marca de agua diagonal a una imagen. El código de ejemplo se ha dividido en partes para facilitar su seguimiento. Paso a paso, los ejemplos muestran cómo:

1. Cargar una imagen.
1. Crear e inicializar un objeto Graphics.
1. Crear e inicializar objetos [Font](https://reference.aspose.com/psd/net/aspose.psd/font) y SolidBrush.
1. Obtener el tamaño de la imagen en un objeto [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Crear una instancia de la clase Matrix y realizar una transformación compuesta.
1. Asignar la transformación al objeto Graphics.
1. Crear e inicializar un objeto [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Dibujar una cadena como marca de agua usando el método DrawString de la clase Graphics.
1. Guardar la imagen resultante.

El siguiente fragmento de código le muestra cómo agregar una marca de agua diagonal.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
