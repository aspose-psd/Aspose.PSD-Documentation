---
title: Soporte de capas de relleno
type: docs
weight: 90
url: /es/net/soporte-de-capas-de-relleno/
---

## **Capas de relleno con relleno de patrón**
Este artículo demuestra cómo rellenar la capa de [PSD](https://wiki.fileformat.com/image/psd/) con el relleno de patrón. Un patrón es una imagen, color, sombra o línea que se utiliza para rellenar un área de una imagen. Utilice Aspose.PSD.FileFormats.Psd.Layers.FillLayer para agregar un patrón en la capa PSD. Los fragmentos de código siguientes cargan un archivo PSD, acceden a la clase [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) y establecen el patrón utilizando las propiedades [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificaryConvertirImágenes-PSD-CapaRellenoDePatrón-CapaRellenoDePatrón.cs" >}}

Aquí hay otro ejemplo que demuestra cómo [Aspose.PSD](https://products.aspose.com/psd/net) renderiza el patrón utilizando [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) e [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificaryConvertirImágenes-PSD-ImplementarCapaRellenoDePatrón-ImplementarCapaRellenoDePatrón.cs" >}}

## **Capas de relleno con relleno de degradado**
Este artículo demuestra el uso del relleno de degradado para llenar la capa PSD. Aspose.PSD APIs han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto las clases [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) y [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) para agregar un efecto de degradado en una capa.

Los pasos para llenar la capa de PSD con un relleno de degradado son tan simples como los siguientes:

- Cargue un archivo PSD como una imagen utilizando el método de fábrica [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) expuesto por la clase [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Establezca las propiedades de configuración del objeto [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Cree una lista de [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) con los colores requeridos y las posiciones de color.
- Cree una lista de puntos de transparencia con la opacidad requerida y la posición del punto de transparencia.
- Llame al método [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Guarde los resultados.

El siguiente fragmento de código le muestra cómo agregar un relleno de degradado para llenar la capa de PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificaryConvertirImágenes-PSD-CapaRellenoDeDegradado-CapaRellenoDeDegradado.cs" >}}

Aquí hay otro ejemplo que utiliza una propiedad de **GradientFillSettings.GradientType** para llenar la capa de PSD con un relleno de degradado. Aspose.PSD admite los siguientes tipos de degradado a través de la enumeración GradientType:

- **GradientType.Linear:** En un degradado lineal, la transición de color va desde el tono inicial al final en línea recta.
- **GradientType.Radial:** En un degradado radial, los colores se despliegan desde el punto de inicio en un patrón circular.
- **GradientType.Angle:** En un degradado angular, el degradado se mueve en sentido antihorario alrededor del punto de inicio.
- **GradientType.Reflected:** En un degradado reflejado, el color se refleja en ambos lados del punto de inicio.
- **GradientType.Diamond:** El degradado de diamante crea una forma de diamante a partir del punto de inicio.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificaryConvertirImágenes-PSD-CapasRellenoDeDegradado-CapasRellenoDeDegradado.cs" >}}

## **Soporte de propiedad de escala para capa de relleno de degradado**
Este artículo demuestra cómo escalar FillLayer con relleno de degradado utilizando Aspose.PSD para .NET. Para este propósito, se ha agregado una nueva propiedad [Scale](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) en [IGradientFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).

A continuación se muestra la demostración del código que muestra cómo utilizar la propiedad de **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificaryConvertirImágenes-PSD-SoporteDePropiedadDeEscala-SoporteDePropiedadDeEscala.cs" >}}

## **Capas de relleno con relleno de color**
Este artículo demuestra cómo llenar la capa de [PSD](https://wiki.fileformat.com/image/psd/) con color. Por favor, utilice la clase [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) para añadir color en la capa PSD. El siguiente fragmento de código carga un archivo PSD, accede a la clase de capa de relleno y establece el color utilizando la propiedad [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificaryConvertirImágenes-PSD-CapaRellenoDeColor-CapaRellenoDeColor.cs" >}}

