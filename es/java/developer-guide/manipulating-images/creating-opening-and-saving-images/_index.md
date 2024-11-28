---
title: Creación, apertura y guardado de imágenes
type: docs
weight: 30
url: /es/java/creacion-apertura-y-guardado-de-imagenes/
---

## **Creación de archivos de imagen**
Aspose.PSD para Java permite a los desarrolladores crear sus propias imágenes. Utiliza el método estático Create expuesto por la clase Image para crear nuevas imágenes. Todo lo que necesitas hacer es proporcionar el objeto apropiado de una de las clases del espacio de nombres ImageOptions para el formato de imagen de salida deseado. Para crear un archivo de imagen, primero crea una instancia de una de las clases del espacio de nombres ImageOptions. Estas clases determinan el formato de imagen de salida. A continuación se muestran algunas clases del espacio de nombres ImageOptions (nota que actualmente solo se admiten la familia de formatos de archivo PSD para la creación):

PsdOptions establece las opciones para crear un archivo PSD. Los archivos de imagen se pueden crear configurando una ruta de salida o configurando un flujo.
### **Creación configurando la ruta**
Crea PsdOptions desde el espacio de nombres ImageOptions y configura las diversas propiedades. La propiedad más importante a configurar es la propiedad Source. Esta propiedad especifica dónde residen los datos de la imagen (en un archivo o un flujo). En el ejemplo a continuación, la fuente es un archivo. Después de configurar las propiedades, pasa el objeto a uno de los métodos estáticos Create junto con los parámetros de ancho y alto. El ancho y alto están definidos en píxeles.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Creación utilizando un flujo**
El proceso para crear una imagen utilizando un flujo es el mismo que el de utilizar una ruta. La única diferencia es que necesitas crear una instancia de StreamSource pasando un objeto Stream a su constructor y asignándolo a la propiedad Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Apertura de archivos de imagen**
Los desarrolladores pueden utilizar la API de Aspose.PSD para Java para abrir archivos de imagen PSD existentes para diferentes propósitos, como agregar efectos a la imagen o convertir un archivo existente a otro formato. Sea cual sea el propósito, Aspose.PSD proporciona dos formas estándar de abrir archivos existentes: desde archivo o desde un flujo.
### **Apertura desde disco**
Abre un archivo de imagen pasando la ruta y el nombre del archivo como parámetro al método estático Load expuesto por la clase Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Apertura utilizando un flujo**
A veces la imagen que necesitamos abrir está almacenada como un flujo. En tales casos, utiliza la versión sobrecargada del método Load. Este acepta un objeto Stream como argumento para abrir la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Cargar imagen como capa**
Este artículo demuestra el uso de Aspose.PSD para cargar una imagen como capa. Aspose.PSD APIs ha expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto el método AddLayer de la clase PsdImage para agregar una imagen a un archivo PSD como una capa.

Los pasos para cargar una imagen en PSD como capa son tan simples como se muestran a continuación:

- Crea una instancia de imagen utilizando la clase PsdImage con el ancho y alto especificados.
- Carga un archivo PSD como una imagen utilizando el método de fábrica Load expuesto por la clase Image.
- Crea una instancia de la clase Layer y asigna la capa de imagen PSD a ella.
- Agrega la capa creada utilizando el método AddLayer expuesto por la clase PsdImage.
- Guarda los resultados.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Guardado de archivos de imagen**
Aspose.PSD te permite crear archivos de imagen desde cero. También proporciona los medios para editar archivos de imagen existentes. Una vez que la imagen ha sido creada o modificada, el archivo se guarda generalmente en el disco. Aspose.PSD te proporciona métodos para guardar imágenes en un disco especificando una ruta o utilizando un objeto Stream.
### **Guardado en disco**
La clase Image representa un objeto de imagen, por lo que esta clase proporciona todas las herramientas necesarias para crear, cargar y guardar un archivo de imagen. Utiliza el método Save de la clase Image para guardar imágenes. Una versión sobrecargada del método Save acepta la ubicación del archivo como una cadena.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Guardado en un flujo**
Otra versión sobrecargada del método Save acepta un objeto Stream como argumento y guarda el archivo de imagen en el flujo.

Si la imagen se crea especificando cualquiera de las CreateOptions en el constructor de la clase Image, la imagen se guarda automáticamente en la ruta o flujo suministrado durante la inicialización de la clase Image llamando al método Save que no acepta ningún parámetro.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Configuración para reemplazar fuentes faltantes**
Los desarrolladores pueden utilizar la API de Aspose.PSD para Java para cargar archivos de imagen PSD existentes para diferentes propósitos, por ejemplo, para establecer el nombre de fuente predeterminado al guardar documentos PSD como imagen de mapa de bits (en formatos PNG, JPG y BMP). Esta fuente predeterminada se debe utilizar como reemplazo para todas las fuentes faltantes (fuentes que no se encuentran en el Sistema Operativo actual). Una vez que la imagen ha sido modificada, el archivo se guardará en el disco.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}

