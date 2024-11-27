---
title: Conversión del Espacio de Color para JPEG a través de Perfiles ICC
type: docs
weight: 60
url: /es/net/conversion-del-espacio-de-color-para-jpeg-a-traves-de-perfiles-icc/
---

## **Gestión del Color para el Formato JPEG**


Este artículo discute el uso de perfiles ICC para realizar la gestión del espacio de color al manejar el formato JPEG con las API de Aspose.PSD. El espacio de color interno de JPEG es YCbCr, sin embargo, este [formato](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) también puede acomodar espacios de color Grayscale, RGB, CMYK y YCCK para almacenar los metadatos de la imagen. Las API de Aspose.PSD operan principalmente en el espacio RGB, por lo tanto, la API tiene que realizar conversiones de y hacia el espacio de color para poder manejar correctamente los archivos JPEG. Las conversiones de Grayscale a RGB y de YCbCr a RGB se pueden realizar con transformaciones matemáticas, pero los espacios CMYK y YCCK no se pueden convertir fácilmente al espacio RGB.

Las API de Aspose.PSD tienen que realizar una transformación directa del color RGB a CMYK para las imágenes JPEG que tienen espacio de color CMYK. Por otro lado, las imágenes que tienen espacio de color YCCK requieren una transformación de color RGB a CMYK a YCCK, donde la transformación de CMYK a YCCK utiliza la conversión [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) aplicada a los tres primeros canales, dejando el canal k sin cambios. En resumen, las API de Aspose.PSD tienen que realizar la interconversión de los espacios de color RGB y CMYK para ambas imágenes CMYK e YCCK, y estas transformaciones se realizan con la ayuda de perfiles ICC que son básicamente tablas de búsqueda que describen las propiedades de un color y ayudan en las transformaciones de color.


## **Perfiles ICC**
El mecanismo de conversión ICC utiliza "Perfiles" que mapean el espacio de color fuente a espacios de color CIELAB o CIEXYZ independientes del dispositivo. Aspose.PSD puede convertir los datos en el espacio de color según sea necesario al usar estos dos espacios de color con perfiles adicionales. Por lo tanto, para la conversión ICC, el usuario debe suministrar dos perfiles: un perfil RGB para llegar al espacio de color interno CIE y un perfil CMYK para obtener las características de color CMYK. Para lograr la conversión de CMYK a RGB, es necesario intercambiar los perfiles, es decir; usar el perfil CMYK como perfil fuente y el perfil RGB como perfil de destino.
## **Conversión de Color para JPEG a través de Perfiles ICC**
Las API de Aspose.PSD ocultan los detalles, proporcionando un mecanismo fácil de usar para especificar perfiles ICC a través de la clase [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Además, Aspose.PSD utiliza los perfiles de muestra de SWOP, CMYK y sRGB incrustados en su núcleo, por lo tanto, en la mayoría de los casos de uso comunes, el usuario no necesita buscar perfiles específicos. Hay un inconveniente en tales correcciones, es decir; tales conversiones de espacio de color son irreversibles porque no podemos esperar obtener el mismo color después de la conversión de RGB a CMYK a RGB debido a espacios de color incompatibles y perfiles de color diferentes. El siguiente fragmento de código muestra el uso de Aspose.PSD para la API de .NET para especificar perfiles de color RGB y CMYK para la imagen JPEG YCCK. En el ejemplo a continuación, los perfiles de color RGB y CMYK son cambiados y la imagen se guarda en el espacio de color YCCK. Tenga en cuenta que esas propiedades [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) y [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) funcionarán para cambiar los datos de píxeles para el espacio de color YCCK. Todos los otros espacios de color no obtendrán los perfiles de color para actualizar los datos de color.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


Si no se establecen perfiles, entonces Aspose.PSD para la API de .NET utilizará los perfiles predeterminados. El ejemplo a continuación utiliza las propiedades de perfiles de destino que cambian el espacio de color de destino para la mayoría de las imágenes JPEG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
