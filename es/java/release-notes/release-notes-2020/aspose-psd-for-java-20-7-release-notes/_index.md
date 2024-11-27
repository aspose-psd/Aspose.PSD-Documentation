---
title: Notas de la versión de Aspose.PSD para Java 20.7
type: docs
weight: 50
url: /es/java/aspose-psd-para-java-20-7-notas-de-lanzamiento/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento para [Aspose.PSD para Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-231|Soporte de la adición de Efecto de Contorno en tiempo de ejecución|Característica|
|PSDJAVA-249|Soporte de Recursos lnk2 / lnk3 (Recursos de Capa de Objeto Inteligente)|Característica|
|PSDJAVA-247|Cambiar el Mensaje de Excepción al intentar abrir formatos no compatibles como imagen|Mejora|
|PSDJAVA-235|Si guardamos el archivo PSD después de la creación de un nuevo Grupo de Capas, obtenemos una advertencia de Photoshop al abrir el archivo.|Error|
|PSDJAVA-236|Error al guardar la Máscara de Capa|Error|
|PSDJAVA-237|Máscara de recorte no se aplica al grupo|Error|
|PSDJAVA-238|No se puede abrir el archivo con Aspose.PSD para Java|Error|
|PSDJAVA-239|Excepción al guardar la imagen al convertir el PSD a PDF|Error|
|PSDJAVA-240|Operación de Recorte hace que la Ruta de Recorte sea inválida en la imagen PSD|Error|
|PSDJAVA-241|Excepción NullReference al intentar guardar un archivo PSD específico con el Efecto de Sombra|Error|
|PSDJAVA-243|Aspose.PSD devuelve verdadero en Image.CanLoad(pdfStream)|Error|
|PSDJAVA-244|Las capas no se renderizan en el PNG generado|Error|
|PSDJAVA-245|Excepción al acceder a TextoDatos|Error|
|PSDJAVA-246|Excepción al guardar la PSD|Error|

# **Cambios en la API Pública**
# **APIs Agregadas:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- ...

## **APIs Eliminadas:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])

# **Ejemplos de Uso:**

**PSDJAVA-231. Soporte de la adición de Efecto de Contorno en tiempo de ejecución**
{{< highlight java >}}
// Este ejemplo muestra cómo agregar un efecto de contorno (borde) a las capas existentes de un archivo PSD en Java.
// Hay tres tipos de contornos: color, degradado y patrón. Cada tipo tiene
// tres formas (posiciones) en las que se renderiza el contorno: dentro, centro y fuera.
// Este ejemplo demuestra el uso de todos estos casos.
...
{{< /highlight >}}

**PSDJAVA-249. Soporte de Recursos lnk2 / lnk3 (Recursos de Capa de Objeto Inteligente)**
...

**PSDJAVA-247. Cambiar el Mensaje de Excepción al intentar abrir formatos no compatibles como imagen**
...

**PSDJAVA-235. Si guardamos el archivo PSD después de la creación de un nuevo Grupo de Capas, obtenemos una advertencia de Photoshop al abrir el archivo.**
...

**PSDJAVA-236. Error al guardar la Máscara de Capa**
...

**PSDJAVA-237. Máscara de recorte no se aplica al grupo**
...

**PSDJAVA-238. No se puede abrir el archivo con Aspose.PSD para Java**
...

**PSDJAVA-239. Excepción al guardar la imagen al convertir el PSD a PDF**
...

**PSDJAVA-240. Operación de Recorte hace que la Ruta de Recorte sea inválida en la imagen PSD**
...

**PSDJAVA-241. Excepción NullReference al intentar guardar un archivo PSD específico con el Efecto de Sombra**
...

**PSDJAVA-243. Aspose.PSD devuelve verdadero en Image.CanLoad(pdfStream)**
...

**PSDJAVA-244. Las capas no se renderizan en el PNG generado**
...

**PSDJAVA-245. Excepción al acceder a TextoDatos**
...

**PSDJAVA-246. Excepción al guardar la PSD**
...**PSDJAVA-235. If we save PSD file after the creation of new Layer Group we get Photoshop warning on the file opening.**
{{< highlight java >}}
// This example demonstrates that there is no exception on saving a generated PSD file
// that contains inner layer groups.
...
{{< /highlight >}}

**PSDJAVA-236. Failed to save LayerMask**
{{< highlight java >}}
// This example demonstrates the ability of saving and rendering Layer Masks for
// Layer Groups when layers are added from another PSD image.
...
{{< /highlight >}}

**PSDJAVA-237. Clipping mask not applying to the folder**
{{< highlight java >}}
// This example verifies that clipping masks that are bound to layer groups are exported
// properly for a predefined PSD file.
...
{{< /highlight >}}

**PSDJAVA-238. Cannot open file with Aspose.PSD for Java**
{{< highlight java >}}
// This example loads and saves a particular PSD file without throwing exception.
...
{{< /highlight >}}

**PSDJAVA-239. Image saving failed exception when converting PSD to PDF**
{{< highlight java >}}
// This example exports a particular PSD file to PDF file format with the read only mode is
// turned on and off to make sure that no error is throwing and the output file is correct.
...
{{< /highlight >}}

**PSDJAVA-240. Crop operation makes Clipping path invalid in PSD image**
{{< highlight java >}}
// This example demonstrates that the crop operation does not make a clipping path invalid.
...
{{< /highlight >}}

**PSDJAVA-241. NullReference Exception when trying to save Specific PSD file with the Shadow Effect**
{{< highlight java >}}
// This example demonstrates that there is no exception on saving a particular PSD file.
...
{{< /highlight >}}

**PSDJAVA-243. Aspose.PSD returns true on Image.CanLoad(pdfStream)**
{{< highlight java >}}
// This example verifies that Image.canLoad property was fixed and returns "false" for
// unsupported files. The program just loops through a list of predefined un/supported files.
...
{{< /highlight >}}

**PSDJAVA-244. Layers failed to render in generated PNG**
{{< highlight java >}}
// This examples verifies that a particular PSD file is exported correctly after flattening.
...
{{< /highlight >}}

**PSDJAVA-245. Exception on accessing TextData**
{{< highlight java >}}
// This examples verifies that there is no exception on accessing particular text data.
...
{{< /highlight >}}

**PSDJAVA-246. ImageSaveException on saving the PSD**
{{< highlight java >}}
// This example verifies that there is no exception on saving particular PSD file.
...
{{< /highlight >}}