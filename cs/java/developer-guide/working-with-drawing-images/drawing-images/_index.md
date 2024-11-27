---
title: Kreslení obrázků
type: docs
weight: 10
url: /cs/java/kresleni-obrazku/
---

## **Kreslení čar**
Tento příklad používá třídu Graphics kreslit tvar čar na povrchu obrázku. Pro demonstrování operace vytváří příklad nový obrázek a kreslí čáry na povrch obrázku pomocí metody DrawLine, kterou poskytuje třída Graphics. Nejprve vytvoříme objekt PsdImage a specifikujeme jeho výšku a šířku.

Jakmile je obrázek vytvořen, použijeme metodu Clear, kterou poskytuje třída Graphics, k nastavení barvy pozadí. Metoda DrawLine třídy Graphics je použita k nakreslení čáry na obrázku spojující dvě struktury bodů. Tato metoda má několik přetížení, která přijímají instanci třídy Pen a dvojice souřadnic nebo struktury Point/PointF jako argumenty. Třída Pen definuje objekt používaný kreslení linií, křivek a tvarů. Třída Pen má několik přetížených konstruktorů pro kreslení linií s určenou barvou, šířkou a štětcem. Třída SolidBrush se používá k nepřetržitému kreslení s konkrétní barvou. Nakonec se obrázek exportuje do formátu souboru BMP. Následující kódový úryvek ukazuje, jak nakreslit tvary čar na povrch obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **Kreslení elipsy**
Příklad kreslení elipsy je druhým článkem v sérii kreslení tvarů. Budeme používat třídu Graphics k nakreslení tvaru elipsy na povrchu obrázku. Pro demonstrování operace vytváří příklad nový obrázek a kreslí tvar elipsy na povrch obrázku pomocí metody DrawEllipse, kterou poskytuje třída Graphics. Nejprve vytvoříme objekt PsdImage a specifikujeme jeho výšku a šířku.

Po vytvoření obrázku vytvoříme a inicializujeme objekt třídy Graphics a nastavíme pozadí obrázku pomocí metody Clear třídy Graphics. Metoda DrawEllipse třídy Graphics je použita k nakreslení tvaru elipsy na povrch obrázku specifikovaným strukturou ohraničujícího obdélníku. Tato metoda má několik přetížení, která přijímají instance tříd Pen a Rectangle/RectangleF nebo dvojici souřadnic, výšku a šířku jako argumenty. Třída Pen definuje objekt používaný kreslení linií, křivek a tvarů. Třída Pen má několik přetížených konstruktorů pro kreslení linií s určenou barvou, šířkou a štětcem. Třída Rectangle uchovává soubor čtyř celých čísel, která reprezentují umístění a velikost obdélníku. Třída Rectangle má několik přetížených konstruktorů pro kreslení struktury obdélníku s určenou velikostí a umístěním. Třída SolidBrush se používá k nepřetržitému kreslení s konkrétní barvou. Nakonec se obrázek exportuje do formátu souboru BMP. Následující kódový úryvek ukazuje, jak nakreslit tvar elipsy na povrch obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **Kreslení obdélníku**
V tomto příkladu nakreslíme tvar obdélníku na povrchu obrázku. Pro demonstrování operace vytváří příklad nový obrázek a nakreslí tvar obdélníku na povrch obrázku pomocí metody DrawRectangle, kterou poskytuje třída Graphics. Nejprve vytvoříme objekt PsdImage a specifikujeme jeho výšku a šířku. Poté nastavíme barvu pozadí obrázku pomocí metody Clear třídy Graphics.

Metoda DrawRectangle třídy Graphics je použita k nakreslení tvaru obdélníku na povrchu obrázku specifikovaným strukturou obdélníku. Tato metoda má několik přetížení, která přijímají instance tříd Pen a Rectangle/RectangleF nebo dvojice souřadnic, šířku a výšku jako argumenty. Třída Rectangle uchovává soubor čtyř celých čísel, která reprezentují umístění a velikost obdélníku. Třída Rectangle má několik přetížených konstruktorů pro kreslení struktury obdélníku s určenou velikostí a umístěním. Nakonec se obrázek exportuje do formátu souboru BMP. Následující kódový úryvek ukazuje, jak nakreslit tvar obdélníku na povrch obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **Kreslení oblouku**
Při této části série kreslení tvarů nakreslíme tvar oblouku na povrchu obrázku. Budeme používat metodu DrawArc třídy Graphics k demonstrování operace na obrázku BMP. Nejprve vytvoříme objekt PsdImage a specifikujeme jeho výšku a šířku. Jakmile je obrázek vytvořen, použijeme metodu Clear, kterou poskytuje třída Graphics, k nastavení barvy pozadí.

Metoda DrawArc třídy Graphics je použita k nakreslení tvaru oblouku na obrázkovém povrchu. DrawArc reprezentuje část elipsy specifikovanou strukturou obdélníku nebo dvojicí souřadnic. Tato metoda má několik přetížení, která přijímají instance tříd Pen a Rectangle/RectangleF nebo dvojice souřadnic, šířku a výšku jako argumenty. Nakonec se obrázek exportuje do formátu souboru BMP. Následující kódový úryvek ukazuje, jak nakreslit tvar oblouku na povrch obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **Kreslení Bézierovy křivky**
Tento příklad používá třídu Graphics kreslit tvar Bézierovy křivky na povrchu obrázku. Pro demonstrování operace vytváří příklad nový obrázek a nakreslí tvar Bézierovy křivky na povrch obrázku pomocí metody DrawBezier, kterou poskytuje třída Graphics. Nejprve vytvoříme objekt PsdImage a specifikujeme jeho výšku a šířku. Jakmile je obrázek vytvořen, použijeme metodu Clear, kterou poskytuje třída Graphics, k nastavení barvy pozadí.

Metoda DrawBezier třídy Graphics je použita k nakreslení tvaru Bézierovy křivky na obrázku definovaný čtyřmi strukturami Point. Tato metoda má několik přetížení, která přijímají instance třídy Pen a čtyři uspořádané páry souřadnic nebo čtyři struktury Point/PointF nebo pole struktur Point/PointF jako argumenty. Třída Pen definuje objekt používaný kreslení linií, křivek a tvarů. Třída Pen má několik přetížených konstruktorů pro kreslení linií s určenou barvou, šířkou a štětcem. Nakonec se obrázek exportuje do formátu souboru BMP. Následující kódový úryvek ukazuje, jak nakreslit tvar Bézierovy křivky na povrch obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **Kreslení obrázků pomocí hlavní funkcionality**
Aspose.PSD je knihovna, která nabízí mnoho cenných funkcí, včetně vytváření obrázků od základů. Kreslete pomocí hlavní funkcionality, jako je manipulace s bitmapovými informacemi obrázku, nebo používejte pokročilé funkce jako Graphics a GraphicsPath kreslit tvary na povrchu obrázku s pomocí různých štětců a per. Pomocí třídy RasterImage z Aspose.PSD můžete získat informace o pixelech oblasti obrázku a manipulovat s nimi. Třída RasterImage obsahuje celou hlavní kreslící funkčnost, jako získávání a nastavování pixelů a další metody pro manipulaci s obrázkem. Vytvořte nový obrázek pomocí kterékoli z metod popsaných vytváření souborů a přiřaďte jej k instanci třídy RasterImage. Použijte metodu LoadPixels třídy RasterImage k získání informací o pixelu části obrazu. Jakmile máte pole pixelů, můžete s ním manipulovat, například změnit barvu každého pixelu. Po manipulaci s informacemi o pixelech je vrátíte na požadovanou oblast obrázku pomocí metody SavePixels třídy RasterImage. Následující kódový úryvek ukazuje, jak kreslit obrázky pomocí hlavní funkcionality.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}

