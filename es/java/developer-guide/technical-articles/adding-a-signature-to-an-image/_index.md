---
title: Agregar una Firma a una Imagen
type: docs
weight: 10
url: /es/java/agregar-una-firma-a-una-imagen/
---

## **Agregar una Firma**

Agregar una firma a una imagen a veces es necesario para firmar digitalmente las imágenes y evitar la falsificación. Otra idea podría ser tratar la imagen como si estuviera siendo mostrada en una galería. Sea cual sea la razón, las APIs de Aspose.PSD proporcionan la característica de agregar una firma a una imagen utilizando el mecanismo más simple como se explica a continuación. Tenga en cuenta que este ejemplo utiliza la clase Graphics para dibujar otra imagen con la firma en la superficie de la imagen original. Para demostrar la operación, cargaremos una imagen PSD desde el disco y dibujaremos otra imagen como firma en la superficie de la imagen original utilizando el método DrawImage de la clase Graphics. Guardaremos la imagen resultante en formato PNG utilizando la clase PngOptions. A continuación se muestra un ejemplo de código que demuestra cómo agregar una firma a una imagen. El código de ejemplo se ha dividido en partes para facilitar su seguimiento. Paso a paso, el ejemplo muestra cómo:

- Cargar las imágenes primaria y secundaria (firma).
- Crear e inicializar un objeto Graphics.
- Dibujar la imagen utilizando el método DrawImage de la clase Graphics.
- Guardar el resultado en formato PNG.
### **Ejemplos de Programas**
#### **Cargando Imágenes**
Primero, crear instancias de la clase Image para cargar las imágenes de muestra desde el disco.
#### **Creando e Inicializando un Objeto Gráfico**
Después de cargar las imágenes, crear e inicializar un objeto de la clase Graphics utilizando el objeto de la imagen primaria.
#### **Dibujando la Imagen Secundaria sobre la Imagen Primaria**
Luego, utilizando el método DrawImage de la clase Graphics, añadir la imagen secundaria a la imagen primaria. Hay varias sobrecargas del método DrawImage que aceptan un objeto de la clase Image como primer parámetro, mientras que todos los demás parámetros corresponden a la ubicación donde la imagen debe ser dibujada. Para demostración, el siguiente código utiliza la versión de sobrecarga de DrawImage que acepta un objeto de la clase Point como segundo parámetro e intenta dibujar la firma en la esquina inferior derecha de la imagen primaria.
#### **Guardando la Imagen**
Por último, guardar la imagen de nuevo en el disco local como un archivo PNG utilizando la clase PngOptions.
#### **Fuente Completa**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}
