---
title: Vykreslování obrázků pomocí GraphicsPath
type: docs
weight: 30
url: /cs/vykreslovani-obrazku-pomoci-graphicspath/
---

## **Vykreslování obrázků pomocí GraphicsPath**
Třída GraphicsPath je zodpovědná za vytváření a udržování grafické cesty. GraphicsPath nemá odkaz na obrázek a nemění samotný obrázek, místo toho může být považován za objekt, který obsahuje metadata popisující cesty, které může třída Graphics vykreslit. Třída GraphicsPath používá figury; každá figura je složena buď z řady propojených linií a křivek, nebo z geometrického tvaru primitiva. Každý tvar může být rozdělen na tvarové segmenty. Do objektu GraphicsPath můžete přidávat, odebírat a měnit různé figury nebo tvary. Jakmile je GraphicsPath plně popsán, použijte příslušné metody třídy Graphics (DrawPath a Fill Paths) k vykreslení nebo vyplnění cest. Třída Graphics vezme každý tvarový segment a vykreslí ho pro vytvoření finálního obrázku.
### **Vykreslování pomocí třídy GraphicsPath**
Níže je příklad, který ukazuje použití třídy GraphicsPath. Zdrojový kód příkladu je rozdělen do několika částí, aby byl jednoduchý a snadno sledovatelný. Postupně vám příklady ukazují, jak:

- Vytvořit obrázek.
- Inicializovat objekt Graphics.
- Vyčistit plochu.
- Vytvořit instanci GraphicsPath.
- Vytvořit figuru.
- Přidat tvary k figuře.
- Vytvořit pole Figur.
- Vykreslit cesty.
- Vyplnit cesty.

### **Vykreslování obrázků pomocí GraphicsPath: Programové vzorky**
#### **GraphicsPath : Vytvoření obrázku**
Začněte vytvořením obrázku pomocí kterékoli z metod popsaných v sekci Vytváření souborů.
#### **GraphicsPath : Inicializace objektů Graphics**
Vytvořte a inicializujte objekt Graphics předáním objektu Image do jeho konstruktoru.
#### **GraphicsPath : Vyčištění plochy**
Vyčistěte grafickou plochu zavoláním metody Clear třídy Graphics a předejte barvu jako parametr. Tato metoda vyplní grafickou plochu barvou předanou jako argument.
#### **GraphicsPath : Vytvoření instance GraphicsPathu**
Vytvořte instanci GraphicsPath s nastavením GraphicsPathu jako výchozího na Alternate. Tento režim určuje, jak vyplnit interiér uzavřené figury. Další možnou hodnotou GraphicsPath je Winding.
#### **GraphicsPath : Vytvoření figury**
Vytvořte instanci třídy Figure. Jak bylo již zmíněno, Figure může obsahovat tvary a tvary se nacházejí v oboru Shapes třídy Aspose.PSD.Shapes.
#### **GraphicsPath : Přidání tvarů k figuře**
Metoda Add Shapes vystavená třídou Figure vám umožňuje přidávat tvary k figuře. V níže uvedených příkladech kódu je několik tvarů přidáno do objektu Figure.
#### **GraphicsPath : Přidání figur do pole**
Do objektu GraphicsPath mohou být přidány více figur pomocí metody AddFigures vystavené třídou GraphicsPath. Tato metoda přijímá pole figur jako parametr.
#### **GraphicsPath : Vykreslení cest**
Vykreslete GraphicsPath pomocí metody DrawPath u třídy Graphics. Metoda přijímá dva parametry. Prvním parametrem je objekt třídy Pen, který určuje barvu, šířku a styl cesty. Druhým parametrem je objekt třídy GraphicsPath, který představuje samotnou cestu.
#### **GraphicsPath : Vyplnění cest**


Cestu můžete vyplnit předáním objektu GraphicsPath metodě Fill Paths vystavené třídou Graphics. Metoda Fill Paths vyplní cestu podle aktuálně nastaveného režimu výplně (alternate nebo winding) pro danou cestu. Pokud cesta obsahuje jakékoli otevřené figury, cesta je vyplněna, jako by tyto figury byly uzavřeny.

Metoda Fill Paths přijímá dva parametry. Prvním parametrem je objekt jakékoliv třídy štětce z oboru Aspose.PSD.Brushes. Druhým parametrem je cesta sama. Pro tento příklad použijte HatchBrush, což je obdélníkový štětec s vzorovým stylem, přední barvou a pozadím. Před předáním objektu HatchBrush metodě Fill Paths nastavte jeho vlastnosti.
### **GraphicsPath : Úplný zdroj**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Všechny třídy, které implementují IDisposable, jsou instanciovány ve Using prohlášení, aby bylo zajištěno, že jsou korektně uvolněny.

