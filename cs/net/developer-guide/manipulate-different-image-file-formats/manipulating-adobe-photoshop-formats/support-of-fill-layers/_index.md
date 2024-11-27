---
title: Podpora vrstev s plněním
type: docs
weight: 90
url: /cs/podpora-vrstev-s-plnenim/
---

## **Vrstvy s plněním vzorem**
Tento článek ukazuje, jak vyplnit vrstvu [PSD](https://wiki.fileformat.com/image/psd/) vzorem. Vzor* *je obrázek, barva, stín nebo čára, která se používá k vyplnění oblasti obrázku. Použijte třídu Aspose.PSD.FileFormats.Psd.Layers.FillLayer k přidání vzoru do vrstvy PSD. Následující části kódu načtou soubor PSD, přistoupí k třídě [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) a nastaví vzor pomocí vlastností [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



Zde je další příklad, který ukazuje, jak [Aspose.PSD](https://products.aspose.com/psd/net) vykresluje vzor pomocí tříd [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) a [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Vrstvy s plněním přechodem**
Tento článek ukazuje použití přechodného plnění k vyplnění vrstvy PSD. Aspose.PSD API poskytují efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD vystavil třídy [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) a [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) pro přidání efektu přechodu do vrstvy.

`Postup pro vyplnění vrstvy PSD přechodným plněním je jednoduchý:

- Načtěte soubor PSD jako obrázek pomocí tovární metody [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) vystavené třídou [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Nastavte vlastnosti nastavení objektu [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Vytvořte seznam [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) s požadovanými barvami a pozicemi barev.
- Vytvořte seznam bodů průhlednosti s požadovanou průhledností a pozicí bodu průhlednosti.
- Zavolejte metodu [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Uložte výsledky.



Následující úryvek kódu vám ukazuje, jak přidat přechodné plnění do vrstvy PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Zde je další příklad, který používá vlastnost [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** pro vyplnění vrstvy PSD přechodným plněním. Aspose.PSD podporuje následující typy přechodů pomocí enumerace GradientType:

- **GradientType.Linear:**       V lineárním přechodném plnění barvy přecházejí od počátečního odstínu ke konci ve svislé linii.
- **GradientType.Radial:**       V radiálním přechodném plnění barvy vyzařují od počátečního bodu ve formě kruhového vzoru.
- **GradientType.Angle:**         Při úhlovém přechodném plnění se barvy pohybují proti směru hodinových ručiček kolem počátečního bodu.
- **GradientType.Reflected:** V odraženém přechodném plnění je barva zrcadlena na obou stranách počátečního bodu.
- **GradientType.Diamond:**    Diamantové přechodné plnění vytváří tvar diamantu od počátečního bodu.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Podpora vlastnosti měřítka pro vrstvu s přechodným plněním**
Tento článek ukazuje, jak měnit měřítko FillLayer s přechodným plněním pomocí Aspose.PSD pro .NET. K tomuto účelu byla přidána nová vlastnost [**Měřítko**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) v [**GradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).

Níže je ukázka kódu, která ukazuje, jak použít vlastnost **Měřítko**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Vrstvy s plněním barevné plní**
Tento článek ukazuje, jak vyplnit vrstvu [PSD](https://wiki.fileformat.com/image/psd/) barvou. Použijte třídu [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) k přidání barvy do vrstvy PSD. Následující úryvek kódu načte soubor PSD, přistoupí k třídě Fill layer a nastaví barvu pomocí vlastností [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}

