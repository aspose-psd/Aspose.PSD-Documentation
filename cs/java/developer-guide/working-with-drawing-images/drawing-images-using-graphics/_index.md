---
title: Kreslení obrázků pomocí grafiky
type: docs
weight: 20
url: /cs/java/kresleni-obrazku-pomoci-grafiky/
---

## **Kreslení obrázků pomocí grafiky**

S knihovnou Aspose.PSD můžete kreslit jednoduché tvary jako jsou čáry, obdélníky a kruhy, stejně jako složité tvary jako jsou mnohoúhelníky, křivky, oblouky a Bezierovy tvary. Knihovna Aspose.PSD vytváří takové tvary pomocí třídy Graphics, která se nachází v oboru Aspose.PSD. Objekty Graphics jsou zodpovědné za provádění různých kreslicích operací na obrázku, změnou povrchu obrázku. Třída Graphics využívá různé pomocné objekty k vylepšení tvarů:

- Plnicí pero (Pens), pro kreslení čar, obrysů tvarů nebo vykreslování jiných geometrických reprezentací.
- Štětce (Brushes), pro definování způsobu vyplňování ploch.
- Písma (Fonts), pro definování tvaru znaků textu.
### **Kreslení s třídou Graphics**
Níže je kódový příklad demonstující využití třídy Graphics. Zdrojový kód příkladu byl rozdělen do několika částí, aby byl jednoduchý a snadno sledovatelný. Postupně ukazují příklady, jak:

1. Vytvořit obrázek.
1. Vytvořit a inicializovat objekt Graphics.
1. Vyčistit povrch.
1. Nakreslit elipsu.
1. Nakreslit vyplněný mnohoúhelník a uložit obrázek.
### **Programové ukázky**
#### **Vytvoření obrázku**
Začněte vytvořením obrázku pomocí kterékoli z metod popsaných v sekci Vytváření souborů.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Vytvoření a inicializace objektu Graphics**
Poté vytvořte a inicializujte objekt Graphics předáním objektu Image konstruktoru.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Vyčištění povrchu**
Vyčistěte povrch grafiky zavoláním metody Clear třídy Graphics a předejte barvu jako parametr. Tato metoda vyplní grafický povrch barvou předanou jako argument.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Nakreslení elipsy**
Můžete si všimnout, že třída Graphics má k dispozici spoustu metod pro kreslení a vyplňování tvarů. Úplný seznam metod najdete v referenční dokumentaci API Aspose.PSD pro Java. Třída Graphics má několik přetížených verzí metody DrawEllipse. Všechny tyto metody přijímají jako první argument objekt Pen. Další parametry jsou předány k definování ohraničujícího obdélníku kolem elipsy. Pro tento příklad použijte verzi, která přijímá objekt Rectangle jako druhý parametr pro nakreslení elipsy pomocí objektu Pen ve zvolené barvě.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Nakreslení vyplněného mnohoúhelníku**
Nakreslete následně mnohoúhelník pomocí metody FillPolygon a předaného objektu LinearGradientBrush a pole bodů. Třída Graphics má k dispozici několik přetížených verzí metody FillPolygon. Všechny tyto přijímají jako první argument objekt Brush, který definuje charakteristiky vyplnění. Druhým parametrem je pole bodů. Upozorňujeme, že každé dva po sobě následující body v poli určují stranu mnohoúhelníku.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Kreslení obrázků pomocí grafiky: Úplný zdroj**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Všechny třídy, které implementují rozhraní IDisposable a mají přístup k nezpravovaným prostředkům, jsou instancovány ve výrazu Using, aby bylo zajištěno, že jsou správně uvolněny.
