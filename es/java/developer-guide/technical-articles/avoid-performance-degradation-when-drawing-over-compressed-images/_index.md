---
title: Evitar la Degradación del Rendimiento al Dibujar sobre Imágenes Comprimidas
type: docs
weight: 40
url: /es/java/evitar-degradacion-rendimiento-dibujar-sobre-imagenes-comprimidas/
---

## **Evitar la Degradación del Rendimiento al Dibujar sobre Imágenes Comprimidas**
Hay momentos en los que se desea realizar operaciones gráficas extremadamente extensas en una imagen comprimida. Cuando Aspose.PSD tiene que comprimir y descomprimir imágenes sobre la marcha, puede haber una degradación del rendimiento. Dibujar sobre imágenes comprimidas también puede implicar una penalización en el rendimiento.
### **Solución**
Para evitar la degradación del rendimiento, recomendamos que convierta la imagen a un formato no comprimido, o en bruto, antes de realizar operaciones gráficas.
### **Usando la Ruta del Archivo**
En el siguiente ejemplo, se convierte una imagen PSD al formato en bruto (sin compresión) y se guarda en disco. La imagen sin comprimir se vuelve a cargar antes de realizar operaciones gráficas en ella. La misma técnica se aplica para archivos BMP y GIF.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Usando un Objeto de Flujo**
El siguiente fragmento de código le muestra cómo convertir una imagen PSD al formato en bruto (sin compresión) y guardarla en disco usando un flujo.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
