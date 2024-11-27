---
title: Evitar la Degradación del Rendimiento al Dibujar sobre Imágenes Comprimidas
type: docs
weight: 10
url: /es/net/evitar-degradacion-rendimiento-dibujar-sobre-imagenes-comprimidas/
---

## **Evitar la Degradación del Rendimiento al Dibujar sobre Imágenes Comprimidas**
Hay momentos en los que se desean realizar operaciones gráficas extremadamente extensas en una imagen comprimida. Cuando Aspose.PSD tiene que comprimir y descomprimir imágenes sobre la marcha, puede producirse una degradación del rendimiento. Dibujar sobre imágenes comprimidas también puede acarrear una penalización en el rendimiento.
### **Solución**
Para evitar la degradación del rendimiento, recomendamos que convierta la imagen a un formato sin comprimir, o en bruto, antes de realizar operaciones gráficas.
### **Usando la Ruta del Archivo**
En el ejemplo que sigue, una imagen PSD se convierte a formato bruto (sin compresión) y se guarda en disco. La imagen sin comprimir luego se carga antes de realizar operaciones gráficas en ella. La misma técnica se aplica para los archivos BMP y GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingYConvertingImages-PSD-ImagenSinCompresionUsandoArchivo-ImagenSinCompresionUsandoArchivo.cs" >}}
### **Usando un Objeto Stream**
El siguiente fragmento de código le muestra cómo se convierte una imagen PSD a formato bruto (sin compresión) y se guarda en disco usando MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingYConvertingImages-PSD-ImagenSinCompresionObjetoStream-ImagenSinCompresionObjetoStream.cs" >}}
