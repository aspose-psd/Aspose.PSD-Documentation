---
title: Edición de máscaras de capa de mapa de bits en archivo PSD a través de API
type: docs
weight: 20
url: /es/editar-mascaras-de-capa-de-mapa-de-bits-en-archivo-psd-a-traves-de-api/
---

## **Descripción general**
**Para automatizar la edición de formato PSD y cambiar archivos PSD sin Adobe® Photoshop®, puede utilizar la API de Aspose.PSD proporcionada a continuación. Hay fragmentos de código en C# y .NET que pueden ayudarlo a modificar archivos PSD.**

Utilizando máscaras de capa y máscaras vectoriales de PSD podemos ocultar y mostrar píxeles de capas sin eliminarlos permanentemente. Las máscaras de mapas de bits también se denominan máscara de capa o máscara de usuario. El acceso a las máscaras de mapa de bits y vectoriales en Aspose.PSD se proporciona a través de la propiedad de capa [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata), que puede ser una instancia de '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' y '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)', que son clases secundarias de la clase abstracta 'LayerMaskData'. Si una capa tiene tanto máscaras de mapa de bits como vectoriales, se proporciona una instancia [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). Si una capa tiene solo una máscara de mapa de bits o una vectorial, se proporciona una instancia [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort). Si la propiedad LayerMaskData es nula, entonces la capa no tiene máscaras o solo tiene una máscara vectorial deshabilitada.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Una máscara de mapa de bits y una máscara vectorial deshabilitada LayerMaskDataShort</p><p>Una máscara de mapa de bits deshabilitada LayerMaskDataShort</p><p>Una máscara de mapa de bits y una máscara vectorial LayerMaskDataFull</p><p>Una máscara de mapa de bits LayerMaskDataShort</p><p>Una máscara vectorial LayerMaskDataShort</p><p>Una máscara vectorial deshabilitada nula (Pero el recurso vectorial está presente)</p>|
| :- | :- |
## **¿Cómo obtener una máscara de mapa de bits de capa en el archivo PSD?**
En primer lugar, debemos averiguar si una capa tiene tanto máscaras vectoriales como de capa:

A continuación, se proporciona un código de ejemplo que demuestra cómo obtener una máscara de mapa de bits de capa.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-1.cs" >}}

De lo contrario, el tipo de la propiedad de capa LayerMaskData es LayerMaskDataShort. En este caso, verifiquemos si la capa tiene solo una máscara de mapa de bits comprobando la propiedad Flags. No debe contener [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).LinkedLayerMask flag, de lo contrario, la máscara es una caché de máscara vectorial.

Fragmento de código para obtener la máscara:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-2.cs" >}}

Si necesita **extraer una máscara de mapa de bits** como LayerMaskDataShort (para más manipulaciones) incluso cuando ambas máscaras están presentes, se debe extraer LayerMaskDataFull y convertirlo en LayerMaskDataShort. El siguiente código puede usarse para ambos casos:

Extrayendo una máscara de mapa de bits de PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-11.cs" >}}
## **¿Cómo verificar si una capa en el archivo PSD tiene una máscara de mapa de bits?**
El siguiente código C# puede ayudarlo a verificar si una capa tiene una máscara de mapa de bits:

Cómo saber si se aplica una máscara de mapa de bits a la [capa PSD](/psd/es/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-6.cs" >}}
## **¿Cómo eliminar / añadir / actualizar una máscara de mapa de bits de capa en el archivo PSD?**
Simplemente eliminar / añadir / actualizar LayerMaskData no es suficiente para una correcta salvaguarda porque los canales no se actualizan; aunque puede proporcionar una correcta representación. Esto no cambia los canales de la máscara:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-3.cs" >}}

Deberíamos usar el método AddLayerMask de la capa para eliminar / añadir / actualizar.

Esto agrega/actualiza tanto la máscara como los canales:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-4.cs" >}}

Esto quita tanto la máscara como los canales:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-5.cs" >}}
## **Eliminar una máscara de mapa de bits de capa en la imagen PSD**
En primer lugar, comprobamos si la máscara está en formato corto y si no es vectorial, simplemente podemos llamar al método AddLayerMask con nulo para eliminar la máscara de mapa de bits. Pero si está en formato completo, debemos convertirla a un formato corto, dejando así solo la máscara vectorial. Para eliminar una máscara de capa, se puede utilizar este siguiente fragmento de código en C# .NET:

Fragmento de código sobre cómo eliminar una máscara de capa del archivo PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-7.cs" >}}
## **Actualización de una máscara de mapa de bits de capa en la imagen PSD**
Esto es directo: si la máscara está en formato corto, debemos cambiar ImageData y MaskRectangle si es necesario, de lo contrario, [UserMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata) y [UserMaskRectangle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)se deben cambiar. El siguiente fragmento de código en C# .NET se puede utilizar para actualizar una máscara de capa:

Actualizar máscara de capa PSD con C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-7.cs" >}}

Aquí hay un ejemplo de posibles acciones que cambian una máscara de mapa de bits. Este invierte una máscara de usuario de capa:

Actualizar máscara de capa PSD con C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-12.cs" >}}
## **Actualización de una máscara vectorial en el archivo PSD cuando una máscara de mapa de bits de capa está presente**
Se supone que un usuario ya ha cambiado un recurso de ruta vectorial. Luego puede actualizar la máscara vectorial simplemente llamando al método de capa [AddLayerMask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask):

Actualizar [máscara vectorial de capa PSD](/psd/es/net/layer-vector-mask/) con C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-9.cs" >}}
## **Añadir una máscara de mapa de bits de capa en el archivo PSD**
Si una capa no tiene máscara, podemos añadir la máscara de mapa de bits dada simplemente llamando al método de capa AddLayerMask.

Si la máscara no tiene la bandera [UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags) entonces ya tiene una máscara de mapa de bits y debemos actualizarla como se describe arriba. De lo contrario, si esta máscara está en un formato corto, la convertimos a un formato completo. Si no, la usamos como está. Luego, actualizamos UserMaskData, UserMaskRectangle y otras propiedades con las propiedades de la máscara dada. El siguiente fragmento de código en C# .NET se puede utilizar para agregar (actualizar) una máscara de capa:

Agregar nueva máscara de capa a PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-10.cs" >}}

## **¿Cómo verificar si una máscara de capa está habilitada?**
Para averiguar el estado habilitado de la máscara de mapa de bits de la capa, podemos verificar el estado de la bandera LayerMaskFlags.Disabled en la propiedad Flags de LayerMaskDataShort o en RealFlags de LayerMaskDataFull. El siguiente fragmento de código en C# .NET se puede utilizar para obtener el estado habilitado de una máscara de capa:

Comprobar si una máscara está habilitada:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-13.cs" >}}

## **¿Cómo habilitar o deshabilitar una máscara de mapa de bits de capa?**
Para habilitar o deshabilitar una máscara de mapa de bits de capa, podemos cambiar el estado de la bandera LayerMaskFlags.Disabled en la propiedad Flags de LayerMaskDataShort o en RealFlags de LayerMaskDataFull. El siguiente fragmento de código en C# .NET se puede utilizar para cambiar el estado habilitado de una máscara de capa:

Habilitar o deshabilitar Máscara de Capa de Mapa de Bits:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-TrabajandoConMascarasDeMapaDeBits-Snippet-14.cs" >}}


