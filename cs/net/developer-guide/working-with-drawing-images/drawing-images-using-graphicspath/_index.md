---
title: Kreslení obrázků pomocí GraphicsPath
type: docs
weight: 30
url: /cs/net/kresleni-obrazku-pomoci-graphicspath/
---

## **Kreslení obrázků pomocí GraphicsPath**
Třída [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) je zodpovědná za vytváření a udržování grafické cesty. GraphicsPath nemá žádný odkaz na obrázek a samotný obrázek nemění, spíše se může považovat za objekt, který obsahuje metadata popisující cesty, které třída Graphics může kreslit. Třída GraphicsPath používá tvary; každý tvar je buď složen z posloupnosti propojených linií a křivek, nebo z geometrického tvaru prvku. Každý tvar lze rozdělit na tvarované segmenty. Do objektu GraphicsPath můžete přidávat, odebírat a měnit různé tvary nebo útvary. Když je GraphicsPath plně popsaný, použijte odpovídající metody třídy Graphics (DrawPath a Fill Paths), abyste mohli překreslit nebo vyplnit cesty. Třída Graphics vezme každý tvarový segment a nakreslí jej, aby vytvořila finální obrázek.
### **Kreslení pomocí třídy GraphicsPath**
Níže je příklad demonstrující použití třídy [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). Zdrojový kód příkladu byl rozdělen do několika částí, aby byl jednoduchý a snadno sledovatelný. Postupně vám příklady ukazují, jak:

- Vytvořit obrázek.
- Inicializovat objekt Graphics.
- Vymazat plochu.
- Vytvořit instanci třídy [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Vytvořit tvar.
- Přidat tvary do tvaru.
- Vytvořit pole útvarů.
- Nakreslit cesty.
- Vyplnit cesty.


### **Kreslení obrázků pomocí třídy GraphicsPath: Programové vzorky**
#### **GraphicsPath: Vytvoření obrázku**
Začněte vytvořením obrázku pomocí kterékoliv z metod popsaných v sekci Vytváření souborů.
#### **GraphicsPath: Inicializace objektů Graphics**
Vytvořte a inicializujte objekt Graphics předáním objektu Image do jeho konstruktoru.
#### **GraphicsPath: Vymazání plochy**
Vymažte grafickou plochu zavoláním metody Clear třídy Graphics a předejte barvu jako parametr. Tato metoda vyplní grafickou plochu barvou předanou jako argument.
#### **GraphicsPath: Vytvoření instance třídy GraphicsPath**
Vytvořte instanci GraphicsPath s výchozím nastavením GraphicsPath na Alternate. Tento režim určuje, jak vyplnit interiér uzavřeného tvaru. Další možná hodnota GraphicsPath je Winding.
#### **GraphicsPath: Vytvoření tvaru**
Vytvořte instanci třídy Figure. Jak bylo dříve diskutováno, Figure může obsahovat tvary a tvary jsou uloženy v prostoru názvů Aspose.PSD.Shapes.
#### **GraphicsPath: Přidání tvarů do tvaru**
Metoda Add Shapes, kterou objekt Figure třídy zveřejňuje, vám umožní přidat tvary do tvaru. V kódových příkladech níže jsou do objektu Figure přidány různé tvary.
#### **GraphicsPath: Přidání tvarů do pole**
Do objektu GraphicsPath může být přidáno několik tvarů pomocí metody AddFigures, kterou třída GraphicsPath zveřejňuje. Tato metoda přijímá jako parametr pole tvarů.
#### **GraphicsPath: Nakreslení cest**
Nakreslete GraphicsPath pomocí metody DrawPath zveřejněné třídou Graphics. Metoda přijímá dva parametry. První parametr je objekt třídy Pen, který určuje barvu, šířku a styl cesty. Druhým parametrem je objekt třídy GraphicsPath představující samotnou cestu.
#### **GraphicsPath: Vyplnění cest**


Cestu můžete vyplnit předáním objektu GraphicsPath metodě Fill Paths zveřejněné třídou Graphics. Metoda Fill Paths vyplní cestu podle aktuálně nastaveného režimu vyplnění (alternativní nebo obíhání). Pokud cesta obsahuje otevřené tvary, vyplní se cesta, jako by tyto tvary byly uzavřeny.

Metoda Fill Paths přijímá dva parametry. Prvním parametrem je objekt jakékoliv třídy štětce z prostoru názvů Aspose.PSD.Brushes. Druhým parametrem je sama cesta. Pro tento příklad použijte HatchBrush, což je obdélníkový štětec s výplňovým stylem, barvou popředí a barvou pozadí. Před předáním objektu HatchBrush metodě Fill Paths nastavte jeho vlastnosti.
### **GraphicsPath: Úplný zdroj**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Všechny třídy, které implementují IDisposable, jsou instancovány ve výroku Using, aby bylo zajištěno, že budou správně uvolněny.
