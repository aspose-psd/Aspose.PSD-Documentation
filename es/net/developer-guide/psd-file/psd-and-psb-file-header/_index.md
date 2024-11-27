---
title: Encabezado de archivo PSD y PSB
type: docs
weight: 40
url: /es/net/psd-y-psb-encabezado-de-archivo/
---

## **Descripción**
El encabezado del archivo Adobe Photoshop contiene información sobre la versión del archivo (1 para PSD y 2 para PSB), el recuento de canales, el modo de color y la profundidad de bits.

Puede aprender sobre las combinaciones de modo de color y profundidad de bits admitidas por Aspose.PSD en el artículo relacionado.


El encabezado del archivo contiene las propiedades básicas de la imagen.

|**Longitud**|**Descripción**|
| :- | :- |
|4|Firma: siempre igual a *"8BPS"*|
|2|[Versión de PSD](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): siempre igual a 1 para archivos PSD y 2 para archivos PSB. Aspose.PSD puede detectar una versión del formato de archivo y leerlo correctamente.|
|6|Reservado: debe ser cero.|
|2|El número de canales en la imagen, incluidos los canales alfa. El rango admitido es de 1 a 56.|
|4|La altura de la imagen en píxeles. El rango admitido es de 1 a 30,000. El archivo PSB admite una altura de hasta 300,000 píxeles. Los archivos PSB también son compatibles con Aspose.PSD.|
|4|El ancho de la imagen en píxeles. El rango admitido es de 1 a 30,000. El archivo PSB admite un ancho de hasta 300,000 píxeles. El procesamiento por lotes de grandes archivos PSD/PSB también es compatible con Aspose.PSD.|
|2|Profundidad: el número de bits por canal. Los valores admitidos son 1, 8, 16 y 32. Pero no todos los modos de color funcionan con todas las profundidades.|
|2|El [modo de color PSD](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) del archivo. Los valores admitidos son: Mapa de bits = 0; Escala de grises = 1; Indexado = 2; RGB = 3; CMYK = 4; Multicanal = 7; Duotono = 8; Lab = 9.|
Puede consultar nuestra [Referencia de API de PSD](https://reference.aspose.com/psd) para obtener más información.
