---
title: Kreslení obrázků pomocí grafiky
type: docs
weight: 20
url: /cs/net/kresleni-obrazku-pomoci-grafiky/
---

## **Kreslení obrázků pomocí grafiky**
S knihovnou Aspose.PSD můžete kreslit jednoduché tvary jako jsou čáry, obdélníky a kružnice, stejně jako složité tvary jako jsou polygon, křivky, oblouky a tvarové křivky Bézier. Knihovna Aspose.PSD vytváří tyto tvary pomocí třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), která se nachází v jmenném prostoru Aspose.PSD. Objekty grafiky jsou zodpovědné za provádění různých kreslicích operací na obrázku, které mění povrch obrázku. Třída [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) využívá různé pomocné objekty k vylepšení tvarů:

·         Tužky, pro kreslení čar, obrysů tvarů nebo vykreslování jiných geometrických reprezentací.

·         Kartáče, pro definování, jak jsou oblasti vyplněny.

·         Písma, pro definování tvaru písmen textu.
### **Kreslení s třídou Graphics**
Níže je uveden příklad kódu demonstující použití třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Zdrojový kód příkladu byl rozdělen do několika částí, aby byl jednoduchý a snadno sledovatelný. Krok za krokem ukazují příklady, jak:

1. Vytvořit obrázek.
1. Vytvořit a inicializovat objekt grafiky.
1. Vymazat povrch.
1. Kreslit elipsu.
1. Nakreslete vyplněný polygon a uložte obrázek.
### **Vzorové programování**
#### **Vytvoření obrázku**
Začněte vytvářením obrázku pomocí jedné z metod popsaných v Sekci vytváření souborů.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Vytvoření a inicializace objektu Graphics**
Poté vytvořte a inicializujte objekt grafiky předáním objektu Image do jeho konstruktoru.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Vyčištění povrchu**
Vymažte povrch grafiky zavoláním metody Clear třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) a předejte barvu jako parametr. Tato metoda vyplní povrch grafiky barvou předanou jako argument.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Kreslení elipsy**
Můžete si všimnout, že třída [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) má vystaveno spoustu metod pro kreslení a vyplňování tvarů. Kompletní seznam metod naleznete v referenční příručce API Aspose.PSD pro .NET. Třída Graphics má několik přetížených verzí metody DrawEllipse. Všechny tyto metody přijímají objekt Pen jako svůj první argument. Pozdější parametry jsou předány k definici ohraničujícího obdélníku kolem elipsy. Pro potřeby tohoto příkladu použijte verzi metody přijímající objekt Rectangle jako druhý parametr pro nakreslení elipsy použitím objektu Pen ve vaší požadované barvě.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Kreslení vyplněného polygonu**
Poté nakreslete polygon pomocí objektu LinearGradientBrush a pole bodů. Třída Graphics má vystaveno několik přetížených verzí metody FillPolygon(). Všechny tyto přijímají objekt Brush jako svůj první argument, který definuje vlastnosti vyplnění. Druhým parametrem je pole bodů. Upozorňujeme, že každé dva po sobě jdoucí body v poli určují stranu polygonu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Kreslení obrázků pomocí grafiky: Úplný zdroj**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Všechny třídy, které implementují IDisposable a přistupují k neupraveným prostředkům, jsou vytvořeny ve výroku Using, aby bylo zajištěno, že jsou správně zlikvidovány.

