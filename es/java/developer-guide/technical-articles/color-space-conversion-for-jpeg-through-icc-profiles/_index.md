---
title: Conversión del espacio de color para JPEG a través de perfiles ICC
type: docs
weight: 50
url: /es/java/conversion-del-espacio-de-color-para-jpeg-a-traves-de-perfiles-icc/
---

## **Gestión de color para formato JPEG**

Este artículo discute el uso de perfiles ICC para realizar la gestión del espacio de color mientras se maneja el formato JPEG con las APIs de Aspose.PSD. El espacio de color interno de JPEG es YCbCr, sin embargo, este formato también puede acomodar espacios de color Escala de grises, RGB, CMYK y YCCK para almacenar los metadatos de la imagen. Las APIs de Aspose.PSD operan principalmente en el espacio RGB, por lo tanto, la API tiene que realizar conversiones de espacio de color hacia y desde RGB para manejar correctamente los archivos JPEG. Las conversiones de Escala de grises a RGB y de YCbCr a RGB se pueden realizar con transformaciones matemáticas, pero los espacios CMYK y YCCK no se pueden convertir fácilmente al espacio RGB.

Las APIs de Aspose.PSD tienen que realizar una transformación de color directa de RGB a CMYK para imágenes JPEG que tienen espacio de color CMYK. Por otro lado, las imágenes con espacio de color YCCK requieren una transformación de color de RGB a CMYK a YCCK, donde la transformación de CMYK a YCCK utiliza la conversión ITU-R BT.601 aplicada a los tres primeros canales, dejando el canal k sin modificar. En resumen, las APIs de Aspose.PSD tienen que realizar la interconversión de los espacios de color RGB y CMYK para ambas imágenes CMYK y YCCK, y dichas transformaciones se realizan con la ayuda de perfiles ICC que básicamente son tablas de búsqueda que describen las propiedades de un color y ayudan en las transformaciones de color.

## **Perfiles ICC**

El mecanismo de conversión ICC utiliza "Perfiles" que mapean el espacio de color fuente a los espacios de color CIELAB o CIEXYZ independientes del dispositivo. Aspose.PSD puede convertir datos en el espacio de color requerido mientras se usan estos dos espacios de color con perfiles adicionales. Por lo tanto, para la conversión ICC, el usuario necesita suministrar dos perfiles: un perfil RGB para llegar al espacio de color interno CIE y un perfil CMYK para obtener las características de color CMYK. Para lograr la conversión de CMYK a RGB, es necesario intercambiar perfiles, es decir, utilizar el perfil CMYK como perfil de origen y el perfil RGB como perfil de destino.

## **Conversión de color para JPEG a través de perfiles ICC**

Las APIs de Aspose.PSD ocultan los detalles, proporcionando un mecanismo fácil de usar para especificar perfiles ICC a través de la clase JpegOptions. Además, Aspose.PSD utiliza los perfiles de muestra de SWOP CMYK y sRGB incrustados en su núcleo, por lo tanto en la mayoría de los casos de uso comunes, el usuario no necesita buscar perfiles específicos. Existe una desventaja en tales correcciones, es decir, las conversiones de espacios de color son irreversibles porque no se puede esperar obtener el mismo color después de la conversión de RGB a CMYK a RGB debido a espacios de color incompatibles y perfiles de color diferentes. El fragmento de código siguiente muestra el uso de Aspose.PSD para la API de Java para especificar perfiles de color RGB y CMYK para imágenes JPEG en YCCK. En el ejemplo a continuación, los perfiles de color RGB y CMYK se cambian y la imagen se guarda en el espacio de color YCCK. Tenga en cuenta que esas propiedades RgbColorProfile y CmykColorProfile funcionarán para cambiar los datos de píxeles para el espacio de color YCCK. Todos los otros espacios de color no obtienen los perfiles de color para actualizar los datos de color.

Si no se establecen perfiles, entonces Aspose.PSD para la API de Java usará los perfiles predeterminados. El siguiente ejemplo utiliza las propiedades de perfiles de destino que cambian el espacio de color de destino para la mayoría de las JpegImages.

