---
title: Podpora vrstev vyplňování
type: docs
weight: 50
url: /cs/podpora-vrstev-vyplnovani/
---


## **Podpora vrstev vyplňování barvou**
Tento článek ukazuje, jak vyplnit vrstvu PSD barvou. Použijte třídu Aspose.PSD.FileFormats.Psd.Layers.FillLayer pro přidání barvy do vrstvy PSD. Následující ukázky kódu načtou soubor PSD, přistoupí k třídě Filllayer a nastaví barvu pomocí vlastnosti FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Podpora vrstev vyplňování přechodem**
Tento článek ukazuje použití přechodové výplně k vyplnění vrstvy PSD. Aspose.PSD API nabízí efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD zpřístupnil třídy GradientColorPoint a GradientTransparencyPoint pro přidání přechodového efektu do vrstvy.

Kroky k vyplnění vrstvy PSD pomocí přechodové výplně jsou následující:

- Načtěte soubor PSD jako obrázek pomocí metody Load, kterou poskytuje třída Image.
- Nastavte vlastnosti nastavení objektu FillLayer.
- Vytvořte seznam ColorPoints s požadovanými barvami a pozicí barvy.
- Vytvořte seznam transparencyPoints s požadovanou průhledností a pozicí průhlednostního bodu.
- Zavolejte metodu FillLayer.Update.
- Uložte výsledky.

Následující ukázka kódu vám ukazuje, jak přidat přechodovou výplň k vyplnění vrstvy PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Efekt obrysu s vyplněním barvou**
Tento článek ukazuje, jak vykreslit efekt obrysu s vyplněním barvou. Efekt obrysu se používá k přidání čar a ohraničení vrstev a tvarů. Může být použit k vytváření linií jedné barvy, pestrých přechodů a vzorovaných ohraničení.

Kroky k vykreslení efektu obrysu s vyplněním barvou jsou následující:

- Nastavte vlastnost **LoadEffectsResource**.
- Načtěte soubor PSD jako obrázek pomocí metody Load, kterou poskytuje třída Image a definujte **PsdLoadOptions**.
- Nastavte vlastnosti nastavení **ColorFillSetting.**
- Uložte výsledky.

Následující ukázka kódu vám ukazuje, jak vykreslit efekt obrysu s vyplněním barvou.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}


