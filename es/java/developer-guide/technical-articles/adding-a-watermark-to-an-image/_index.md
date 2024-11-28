---
title: Agregar una marca de agua a una imagen
type: docs
weight: 20
url: /es/java/agregar-una-marca-de-agua-a-una-imagen/
---

## **Agregar una marca de agua a una imagen**
Este documento explica cómo agregar una marca de agua a una imagen utilizando Aspose.PSD. Agregar una marca de agua a una imagen es un requisito común en aplicaciones de procesamiento de imágenes. Este ejemplo utiliza la clase Graphics para dibujar una cadena en la superficie de la imagen.
### **Agregando una marca de agua**
Para demostrar la operación, cargaremos una imagen BMP desde el disco y dibujaremos una cadena como marca de agua en la superficie de la imagen utilizando el método DrawString de la clase Graphics. Guardaremos la imagen en formato PNG utilizando la clase PngOptions. A continuación se muestra un ejemplo de código que demuestra cómo agregar una marca de agua a una imagen. El código de ejemplo se ha dividido en partes para que sea fácil de seguir. Paso a paso, los ejemplos muestran cómo:

1. Cargar una imagen.
1. Crear e inicializar un objeto Graphics.
1. Crear e inicializar objetos Font y SolidBrush.
1. Dibujar una cadena como marca de agua utilizando el método DrawString de la clase Graphics.
1. Guardar la imagen en formato PNG.

El siguiente fragmento de código le muestra cómo agregar una marca de agua a la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Agregando una marca de agua diagonal**
Agregar una marca de agua diagonal a una imagen es similar a agregar una marca de agua horizontal como se discutió anteriormente, con algunas diferencias. Para demostrar la operación, cargaremos una imagen JPG desde el disco, añadiremos transformaciones utilizando un objeto de la clase Matrix y dibujaremos una cadena como marca de agua en la superficie de la imagen utilizando el método DrawString de la clase Graphics. A continuación se muestra un ejemplo de código que demuestra cómo agregar una marca de agua diagonal a una imagen. El código de ejemplo se ha dividido en partes para que sea fácil de seguir. Paso a paso, los ejemplos muestran cómo:

1. Cargar una imagen.
1. Crear e inicializar un objeto Graphics.
1. Crear e inicializar objetos Font y SolidBrush.
1. Obtener el tamaño de la imagen en un objeto SizeF.
1. Crear una instancia de la clase Matrix y realizar una transformación compuesta.
1. Asignar la transformación al objeto Graphics.
1. Crear e inicializar un objeto StringFormat.
1. Dibujar una cadena como marca de agua utilizando el método DrawString de la clase Graphics.
1. Guardar la imagen resultante.

El siguiente fragmento de código le muestra cómo agregar una marca de agua diagonal.





{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
