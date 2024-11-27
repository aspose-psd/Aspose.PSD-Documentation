---
title: Renderización de Capas de Texto Rotadas
type: docs
weight: 40
url: /es/renderizacion-de-capas-de-texto-rotadas/
---

## **Renderización de Capas de Texto Rotadas**
Aspose.PSD proporciona la función de renderización de capas de texto rotadas. En el siguiente ejemplo, se carga un archivo PSD existente pasando la ruta del archivo al método estático Load de la clase Image. Ahora llame al método [Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) de la instancia [PsdImage](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage).

El siguiente fragmento de código le muestra cómo renderizar [capas de texto](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer) rotadas.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.cs" >}}
## **Rotar Máscaras Vectoriales y Capas de Texto**
Aspose.PSD proporciona la función para rotar máscaras vectoriales y capas de texto. Aspose.PSD ha expuesto el método RotateFlip para rotar máscaras vectoriales y capas de texto. Los pasos para rotar las capas son tan simples como se muestra a continuación:

- Cargar un archivo PSD como una imagen utilizando el método de fábrica Load expuesto por la clase Image.
- Establecer el [RotateFlipType](https://reference.aspose.com/psd/net/aspose.psd/rotatefliptype) requerido.
- Llamar al método [RotateFlip](https://reference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip)
- Guardar los resultados.

El siguiente fragmento de código le muestra cómo rotar máscaras vectoriales y capas de texto.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.cs" >}}
