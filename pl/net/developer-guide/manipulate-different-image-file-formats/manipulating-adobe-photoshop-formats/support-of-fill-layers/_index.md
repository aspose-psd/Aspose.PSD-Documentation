---
title: Wsparcie warstw wypełnienia
type: docs
weight: 90
url: /pl/net/support-of-fill-layers/
---


## **Warstwy wypełnienia wzorem**
Ten artykuł demonstruje, jak wypełnić warstwę [PSD ](https://wiki.fileformat.com/image/psd/) wzorem. Wzór jest obrazem, kolorem, cieniem lub linią używaną do wypełnienia obszaru obrazu. W celu dodania wzoru do warstwy PSD należy skorzystać z klasy Aspose.PSD.FileFormats.Psd.Layers.FillLayer. Poniższy fragment kodu wczytuje plik PSD, uzyskuje dostęp do klasy [Filllayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)oraz ustawia wzór za pomocą właściwości [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



Oto kolejny przykład, który demonstruje, jak [Aspose.PSD](https://products.aspose.com/psd/net) renderuje wzór, korzystając z klas [FillLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)oraz [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Warstwy wypełnienia gradientem**
Ten artykuł demonstruje użycie wypełnienia gradientowego do wypełnienia warstwy PSD. Interfejsy API Aspose.PSD udostępniają efektywne i łatwe w użyciu metody, aby osiągnąć ten cel. Aspose.PSD udostępnia klasy [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) oraz [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) do dodawania efektu gradientu do warstwy.

`Kroki do wypełnienia warstwy PSD gradientowym wypełnieniem są takie proste, jak poniżej:

- Wczytaj plik PSD jako obraz, korzystając z metody fabrycznej [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) udostępnianej przez klasę [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Skonfiguruj właściwości ustawień obiektu [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Utwórz listę [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) z wymaganymi kolorami i pozycjami kolorów.
- Utwórz listę punktów transparentności z wymaganą przezroczystością i pozycją punktu transparentności.
- Wywołaj metodę [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Zapisz wyniki.



Poniższy fragment kodu pokazuje, jak dodać wypełnienie gradientowe do warstwy PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Oto kolejny przykład, który wykorzystuje właściwość [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** do wypełnienia warstwy PSD gradientowym wypełnieniem. Aspose.PSD obsługuje następujące typy gradientu poprzez wyliczenie GradientType:

- **GradientType.Linear:**   W linearnym gradientzie przejście kolorów odbywa się prosto od początkowego odcienia do końca.
- **GradientType.Radial:**   W radialnym gradientzie kolory rozchodzą się od punktu początkowego w sposób okrężny.
- **GradientType.Angle:**   Gradient kątowy obraca się przeciwnie do ruchu wskazówek zegara wokół punktu początkowego.
- **GradientType.Reflected:**   W odbitym gradientcie kolor jest lustrzany po obu stronach punktu początkowego.
- **GradientType.Diamond:**   Gradient diamentowy tworzy kształt diamentu od punktu początkowego.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Wsparcie właściwości skalowania warstwy gradientowego wypełnienia**
Ten artykuł demonstruje, jak skalować warstwę FillLayer z wypełnieniem gradientowym przy użyciu Aspose.PSD dla .NET. W tym celu dodano nową właściwość [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) w [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)**.** 

Poniżej znajduje się demonstracja kodu pokazująca, jak korzystać z właściwości **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Warstwy wypełnione kolorem**
Ten artykuł demonstruje, jak wypełnić warstwę [PSD](https://wiki.fileformat.com/image/psd/) kolorem. Proszę skorzystać z klasy [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) do dodania koloru w warstwie PSD. Poniższy fragment kodu wczytuje plik PSD, uzyskuje dostęp do klasy Fill layer oraz ustawia kolor korzystając z właściwości [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}


