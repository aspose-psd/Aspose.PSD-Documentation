---
title: Creación, Apertura y Guardado de Imágenes
type: docs
weight: 30
url: /es/net/creacion-apertura-y-guardado-de-imagenes/
---

## **Creación de Archivos de Imagen**
Aspose.PSD para .NET permite a los desarrolladores crear sus propias imágenes. Utilice el método estático Create expuesto por la clase Image para crear nuevas imágenes. Todo lo que necesita hacer es proporcionar el objeto apropiado de una de las clases del espacio de nombres ImageOptions para el formato de imagen de salida deseado. Para crear un archivo de imagen, primero cree una instancia de una de las clases del espacio de nombres ImageOptions. Estas clases determinan el formato de imagen de salida. A continuación se muestran algunas clases del espacio de nombres ImageOptions (tenga en cuenta que actualmente solo se admiten formatos de archivo PSD):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) configura las opciones para crear un archivo PSD. Los archivos de imagen se pueden crear estableciendo una ruta de salida o configurando un flujo.
### **Creación mediante Configuración de Ruta**
Cree PsdOptions desde el espacio de nombres [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) y configure las diferentes propiedades. La propiedad más importante para establecer es la propiedad Source. Esta propiedad especifica dónde residen los datos de la imagen (en un archivo o un flujo). En el siguiente ejemplo, la fuente es un archivo. Después de configurar las propiedades, pase el objeto a uno de los métodos estáticos [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) junto con los parámetros de ancho y alto. El ancho y alto están definidos en píxeles.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Creación Usando un Flujo**
El proceso para crear una imagen utilizando un flujo es el mismo que al usar una ruta. La única diferencia es que necesita crear una instancia de [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) pasando un objeto Stream a su constructor y asignándolo a la propiedad Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Apertura de Archivos de Imagen**
Los desarrolladores pueden utilizar la API de Aspose.PSD para .NET para abrir archivos de imagen PSD existentes para diferentes propósitos, como agregar efectos a la imagen o convertir un archivo existente a otro formato. Sea cual sea el propósito, Aspose.PSD proporciona dos formas estándar de abrir archivos existentes: desde un archivo o desde un flujo.
### **Apertura desde Disco**
Abra un archivo de imagen pasando la ruta y el nombre del archivo como parámetro al método estático Load expuesto por la clase Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Apertura usando un Flujo**
A veces, la imagen que necesitamos abrir se almacena como un flujo. En esos casos, utilice la versión sobrecargada del método Load. Este acepta un objeto Stream como argumento para abrir la imagen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Cargar Imagen como Capa**
Este artículo demuestra el uso de Aspose.PSD para cargar una imagen como capa. Aspose.PSD ha expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto el método AddLayer de la clase PsdImage para agregar una imagen a un archivo PSD como capa.

Los pasos para cargar una imagen en PSD como capa son tan simples como los siguientes:

- Cree una instancia de una imagen usando la clase PsdImage con un ancho y alto específicos.
- Cargue un archivo PSD como una imagen utilizando el método de fábrica Load expuesto por la clase Image.
- Cree una instancia de la clase Layer y asígnele la capa de imagen PSD.
- Agregue la capa creada utilizando el método AddLayer expuesto por la clase PsdImage.
- Guarde los resultados.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Cargar Imagen como Capa desde un Flujo**
Este artículo demuestra el uso de Aspose.PSD para cargar una imagen como capa desde un flujo. Para cargar una imagen desde un flujo, simplemente pase un objeto Stream que contenga una imagen al constructor de la clase Layer. Agregue la capa creada utilizando el método AddLayer expuesto por la clase PsdImage y guarde los resultados.


Aquí está el código de muestra.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Guardado de Archivos de Imagen**
Aspose.PSD le permite crear archivos de imagen desde cero. También proporciona los medios para editar archivos de imagen existentes. Una vez que la imagen ha sido creada o modificada, el archivo suele guardarse en disco. Aspose.PSD le proporciona métodos para guardar imágenes en disco especificando una ruta o utilizando un objeto Stream.
### **Guardado en Disco**
La clase Image representa un objeto de imagen, por lo que esta clase proporciona todas las herramientas necesarias para crear, cargar y guardar un archivo de imagen. Utilice el método Save de la clase Image para guardar imágenes. Una versión sobrecargada del método Save acepta la ubicación del archivo como una cadena.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Guardado en un Flujo**
Otra versión sobrecargada del método Save acepta un objeto Stream como argumento y guarda el archivo de imagen en el flujo.

Si la imagen se crea especificando cualquiera de las CreateOptions en el constructor de Image, la imagen se guardará automáticamente en la ruta o en el flujo suministrado durante la inicialización de la clase Image llamando al método Save que no acepta ningún parámetro.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Configuración para Reemplazar Fuentes Faltantes**
Los desarrolladores pueden utilizar la API de Aspose.PSD para .NET para cargar archivos de imagen PSD existentes para diferentes propósitos, por ejemplo, establecer el nombre de fuente predeterminado al guardar documentos PSD como una imagen de mapa de bits (en formatos PNG, JPG y BMP). Esta fuente predeterminada debe usarse como reemplazo para todas las fuentes faltantes (fuentes que no se encuentran en el sistema operativo actual). Una vez que la imagen ha sido modificada, el archivo se guardará en disco.
 

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
