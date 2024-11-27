---
title: Vyobrazení obrázků
type: docs
weight: 10
url: /cs/vyobrazeni-obrazku/
---

## **Kreslení čar**
Tento příklad používá třídu [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) k vykreslení tvarů čar na povrchu obrázku. Pro demonstraci operace vytvoří příklad nový obrázek a vykreslí čáry na povrchu obrázku pomocí metody [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) poskytované třídou Graphics. Nejprve vytvoříme obrázek PsdImage s určenou výškou a šířkou.

Jakmile je obrázek vytvořen, použijeme metodu Clear poskytovanou třídou Graphics k nastavení barvy pozadí. Metoda [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) je použita k vykreslení čáry na obrázku spojující dvě struktury bodů. Tato metoda má několik verzí přijímajících instanci třídy Pen a souřadnice párů bodů nebo struktur Point/PointF jako argumenty. Třída Pen definuje objekt používaný kreslení čar, křivek a tvarů. Třída Pen má několik přetížených konstruktorů pro kreslení čar s určenou barvou, šířkou a štětcem. Třída SolidBrush je použita ke kontinuálnímu kreslení s konkrétní barvou. Nakonec je obrázek exportován do formátu bmp. Následující úryvek kódu vám ukazuje, jak vykreslit tvary čar na povrchu obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **Kreslení elipsy**
Příklad kreslení elipsy je druhým článkem ve skupině kreslících tvarů. Použijeme třídu [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) k vykreslení tvaru elipsy na povrchu obrázku. Pro demonstraci operace vytvoří příklad nový obrázek a vykreslí elipsoidní tvar na povrchu obrázku pomocí metody DrawEllipse poskytované třídou [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Nejprve vytvoříme obrázek PsdImage s určenou výškou a šířkou.

Po vytvoření obrázku vytvoříme a inicializujeme objekt třídy Graphics a nastavíme barvu pozadí obrázku pomocí metody Clear třídy Graphics. Metoda DrawEllipse třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) je použita k vykreslení tvaru elipsy na povrchu obrázku specifikovaný obdélníkem. Tato metoda má několik verzí přijímajících instance tříd Pen a Rectangle/RectangleF nebo pár souřadnic, výšku a šířku jako argumenty. Třída Pen definuje objekt používaný kreslení čar, křivek a tvarů. Třída Pen má několik přetížených konstruktorů pro kreslení čar s určenou barvou, šířkou a štětcem. Třída Rectangle uchovává sadu čtyř celých čísel, která reprezentují umístění a velikost obdélníka. Třída Rectangle má několik přetížených konstruktorů pro kreslení obdélníkové struktury s určenou velikostí a umístěním. Třída SolidBrush je použita ke kontinuálnímu kreslení s konkrétní barvou. Nakonec je obrázek exportován do formátu bmp. Následující úryvek kódu vám ukazuje, jak vykreslit tvar elipsy na povrchu obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **Kreslení obdélníku**
V tomto příkladu nakreslíme tvar obdélníku na povrchu obrázku. Pro demonstraci operace vytvoří příklad nový obrázek a nakreslí obdélníkový tvar na povrchu obrázku pomocí metody DrawRectangle poskytované třídou [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Nejprve vytvoříme obrázek PsdImage s určenou výškou a šířkou. Poté nastavíme barvu pozadí obrázku pomocí metody Clear třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

Metoda DrawRectangle třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) je použita k vykreslení tvaru obdélníku na povrchu obrázku specifikovaný strukturou obdélníku. Tato metoda má několik verzí přijímajících instance tříd Pen a Rectangle/RectangleF nebo dvojici souřadnic, šířku a výšku jako argumenty. Třída Rectangle uchovává sadu čtyř celých čísel, která reprezentují umístění a velikost obdélníka. Třída Rectangle má několik přetížených konstruktorů pro kreslení obdélníkové struktury s určenou velikostí a umístěním. Nakonec je obrázek exportován do formátu bmp. Následující úryvek kódu vám ukazuje, jak nakreslit tvar obdélníku na povrchu obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **Kreslení oblouku**
V této části série kreslení tvarů nakreslíme tvar oblouku na povrchu obrázku. Budeme používat metodu DrawArc třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) k demonstraci operace na bmp obrázku. Nejprve vytvoříme obrázek PsdImage s určenou výškou a šířkou. Jakmile je obrázek vytvořen, použijeme metodu Clear poskytovanou třídou [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) k nastavení barvy pozadí.

Metoda DrawArc třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) je použita k vytvoření tvaru oblouku na povrchu obrázku. DrawArc reprezentuje část elipsy specifikované strukturou obdélníku nebo dvojicí souřadnic. Tato metoda má několik verzí přijímajících instance tříd Pen a Rectangle/RectangleF nebo dvojici souřadnic, šířku a výšku jako argumenty. Nakonec je obrázek exportován do formátu bmp. Následující úryvek kódu vám ukazuje, jak nakreslit tvar oblouku na povrchu obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **Kreslení Bézierovy křivky**
Tento příklad používá třídu [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) k vykreslení tvaru Bézier na povrchu obrázku. Pro demonstraci operace vytvoří příklad nový obrázek a nakreslí tvar Bézier na povrchu obrázku pomocí metody DrawBezier poskytované třídou [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Nejprve vytvoříme obrázek PsdImage s určenou výškou a šířkou. Jakmile je obrázek vytvořen, použijeme metodu Clear poskytovanou třídou [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) k nastavení barvy pozadí.

Metoda DrawBezier třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) je použita k vykreslení tvaru Bézier spline na povrchu obrázku definovaný čtyřmi strukturami Point. Tato metoda má několik verzí přijímajících instance třídy Pen a čtyři uspořádané páry souřadnic nebo čtyři struktury Point/PointF nebo pole struktur Point/PointF. Třída Pen definuje objekt používaný kreslení čar, křivek a tvarů. Třída Pen má několik přetížených konstruktorů pro kreslení čar s určenou barvou, šířkou a štětcem. Nakonec je obrázek exportován do formátu bmp. Následující úryvek kódu vám ukazuje, jak nakreslit tvar Bézier na povrchu obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **Kreslení obrázků pomocí základní funkcionality jádra**
Aspose.PSD je knihovna, která nabízí mnoho cenných funkcí, včetně vytváření obrázků od základu. Kreslete pomocí základní funkcionality jako manipulace s bitmapovými informacemi obrázku nebo využijte pokročilé funkce jako třídy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) a [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) kreslit tvary na povrchu obrázku s pomocí různých štětců a per. Pomocí třídy RasterImage Aspose.PSD můžete získat informace o pixelech oblasti obrázku a manipulovat s nimi. Třída RasterImage obsahuje veškerou základní kreslící funkčnost, jako získání a nastavení pixelů a další metody pro manipulaci s obrázkem. Vytvořte nový obrázek pomocí libovolné z metod popsaných vytváření souborů a přiřaďte ho instanci třídy RasterImage. Použijte metodu LoadPixels třídy RasterImage k získání informací o pixelech dané oblasti obrázku. Jakmile máte pole pixelů, můžete je manipulovat, například změnit barvu každého pixelu. Po manipulaci s informacemi o pixelech je možné je vrátit zpět na stanovenou oblast v obrázku pomocí metody SavePixels třídy RasterImage. Následující úryvek kódu vám ukazuje, jak kreslit obrázky pomocí základní funkcionality jádra.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
