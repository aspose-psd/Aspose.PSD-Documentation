---
title: Manipulace s formáty Adobe Photoshopu
type: docs
weight: 20
url: /cs/net/manipulace-s-formaty-adobe-photoshopu/
---

## **Sloučení vrstev PSD do jiných vrstev**

## **Exportování obrázku do formátu PSD**
PSD, PhotoShop dokument, je výchozím formátem souboru používaným programem Adobe Photoshop k práci s obrázky. Aspose.PSD vám umožňuje načíst, upravit a uložit soubory do formátu PSD, aby mohly být otevřeny a upraveny v programu Photoshop. Tento článek ukazuje, jak uložit soubor do formátu PSD pomocí Aspose.PSD a také diskutuje některá nastavení, která lze použít při ukládání do tohoto formátu. [Options - Psd](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) je specializovaná třída v prostoru názvů [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions), která se používá pro export obrázků do formátu PSD. Pro export do formátu PSD vytvořte instanci třídy Image, buď načtenou ze stávajícího obrázkového souboru (například miniatury) nebo vytvořenou od začátku. Tento článek vysvětluje, jak to udělat. V následujících příkladech je obrázek vytvořen od začátku. Jakmile je vytvořen a naplněna daty obrazových bodů, uložte obrázek pomocí metody Save třídy Image a jako druhý argument poskytněte objekt PsdOptions. Některá nastavení třídy PsdOptions lze nastavit pro pokročilou konverzi. Některá z vlastností jsou ColorMode, [Metoda Komprese](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) a Verze. Aspose.PSD podporuje následující metody komprese prostřednictvím výčtu CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Následující barevné režimy jsou podporovány prostřednictvím výčtu [Režim barev](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


Další zdroje mohou být přidány, například zdroje miniatur pro PSD verze 4.0, 5.0 a vyšší, nebo síťové a průvodcovské zdroje pro PSD verze 4.0 a vyšší. Následující kód vytváří soubor Image od začátku, naplní pixely a uloží jej do formátu PSD s kompresí RLE a režimem šedé. Následující kód ukazuje, jak exportovat obrázek do formátu PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-ExportObrázkuDoPSD-ExportObrázkuDoPSD.cs" >}}
## **Import obrázku do vrstvy PSD**
Tento článek ukazuje použití Aspose.PSD k přidání nebo importu obrázku do vrstvy PSD. API Aspose.PSD poskytuje efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD zpřístupnil metodu [VložitObrázek](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) třídy Layer k přidání/importování obrázku do souboru PSD. Metoda VložitObrázek vyžaduje umístění a hodnoty obrázku k přidání/importování obrázku do souboru PSD. Kroky k importu obrázku do vrstvy PSD jsou tak jednoduché, jak následují:

- Načtěte soubor PSD jako obrázek pomocí statické metody Load vystavené třídou Image.
- Vytvořte instanci třídy Layer ze streamu s Png, Jpeg, Tiff, Gif, Bmp, Psd nebo j2k souborem
- Přidejte vrstvu do Psd pomocí metody AddLayer.
- Uložte výsledky.


Kód níže vám ukazuje, jak importovat obrázek do vrstvy PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-Otevření-NačteníObrázkuZeStreamu-NačteníObrázkuZeStreamu.cs" >}}
## **Nahrazení barvy ve vrstvách PSD**
Tento článek ukazuje použití Aspose.PSD k přidání nebo importu obrázku do vrstvy PSD. API Aspose.PSD poskytuje efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD zpřístupnil metodu VložitObrázek třídy Layer k přidání/importování obrázku do souboru PSD. Metoda VložitObrázek vyžaduje umístění a hodnoty obrázku k přidání/importování obrázku do souboru PSD. Kroky k importu obrázku do vrstvy PSD jsou tak jednoduché, jak následují:

- Načtěte soubor PSD jako obrázek pomocí statické metody Load vystavené třídou Image.
- Vytvořte instanci třídy Layer a přiřaďte ji k obrázku vrstvy PSD.
- Načtěte obrázek, který má být přidán, nebo vytvořte nový od začátku.
- Zavolejte metodu Layer.VložitObrázek a zároveň určete umístění a instanci obrázku.
- Uložte výsledky.


Následující kódový úryvek ukazuje, jak importovat obrázek do vrstvy PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-NahrazeníBarvyVPSD-NahrazeníBarvyVPSD.cs" >}}
## **Vytvoření miniatur z souborů PSD**
PSD je nativním formátem dokumentu pro aplikaci Adobe Photoshop. Adobe Photoshop (verze 5.0 a novější) ukládá informace o miniaturách pro zobrazení náhledu v bloku zdroje obrázku, který se skládá z úvodní hlavičky 28 bajtů, do nějž může následovat miniatura JFIF ve standardním pořadí RGB (červená, zelená, modrá). API Aspose.PSD poskytuje snadný mechanismus k přístupu k zdrojům souboru PSD. Tyto zdroje zahrnují také zdroj miniatury, který lze zase načíst a uložit na disk podle potřeby aplikace. Následující kód vám ukazuje, jak vytvořit miniatury ze souborů PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-VytvořeníMiniaturekZeSouborůPSD-VytvořeníMiniaturekZeSouborůPSD.cs" >}}
## **Vytváření indexovaných souborů PSD**
API Aspose.PSD pro .NET umí vytvářet indexované soubory PSD od začátku. Tento článek ukazuje použití tříd PsdOptions a [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) k vytvoření indexovaného souboru PSD při kreslení některých tvarů na nově vytvořeném plátně. K vytvoření indexovaného souboru PSD jsou vyžadovány následující jednoduché kroky:

- Vytvořte instanci třídy PsdOptions a nastavte zdroj.
- Nastavte vlastnost ColorMode třídy PsdOptions na ColorModes.Indexed.
- Vytvořte novou paletu barev v RGB prostoru a nastavte ji jako vlastnost Palette třídy PsdOptions.
- Nastavte vlastnost CompressionMethod na požadovaný kompresní algoritmus.
- Vytvořte nový obraz PSD zavoláním metody [.Vytvořit](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) třídy PsdImage.
- Vykreslete grafiku nebo proveďte další operace podle potřeby.
- Zavolejte metodu Save třídy PsdImage k uložení všech změn.

Následující kódový úryvek ukazuje, jak vytvářet indexované soubory PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-VytvořeníIndexovanýchPSDSouborů-VytvořeníIndexovanýchPSDSouborů.cs" >}}
## **Export vrstvy PSD do rastrového obrázku**
Aspose.PSD pro .NET umožňuje exportovat vrstvy v souboru PSD do rastrových obrázků. Použijte metodu [Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) třídy Aspose.PSD.FileFormats.Psd.Layers.Layer k exportu vrstvy do obrázku. Následující ukázkový kód načte soubor PSD a exportuje každou z jeho vrstev do obrázku PNG pomocí metody Save třídy Aspose.PSD.FileFormats.Psd.Layers.Layer. Jakmile jsou všechny vrstvy exportovány do obrázků PNG, je lze otevřít pomocí vašeho oblíbeného prohlížeče obrázků. Následující kódový úryvek ukazuje, jak exportovat vrstvu PSD do rastrového obrázku.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-ExportovatPSDVrstvuDoRastra-ExportovatPSDVrstvuDoRastra.cs" >}}
## **Aktualizace textové vrstvy v souboru PSD**
Aspose.PSD pro .NET umožňuje manipulovat s textem ve textové vrstvě souboru PSD. Použijte třídu [TextováVrstva](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) třídy Aspose.PSD.FileFormats.Psd.Layers k aktualizaci textu ve vrstvě PSD. Následující kód načte soubor PSD, získá přístup ke textové vrstvě, aktualizuje text a uloží soubor PSD pod novým názvem pomocí metody [AktualizovatText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index) třídy Aspose.PSD.FileFormats.Psd.Layers.TextLayer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-AktualizaceTextovéVrstvyVeSouboruPSD-AktualizaceTextovéVrstvyVeSouboruPSD.cs" >}}
## **Detekce sloučených vrstev PSD**
Aspose.PSD pro .NET vám umožňuje zjistit, zda daný soubor PSD je sloučený nebo ne. Vlastnost IsFlatten byla představena v třídě Aspose.PSD.FileFormats.Psd.PsdImage pro dosažení této funkcionality. Následující kód načte soubor PSD, přistupuje k vlastnosti [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-ZjištěníSloučenéhoPSD-ZjištěníSloučenéhoPSD.cs" >}}
## **Sloučení vrstev PSD**
Tento článek ukazuje, jak sloučit vrstvy v souboru PSD při konverzi souboru PSD na JPG pomocí Aspose.PSD. V následujícím příkladu je existující soubor PSD načten tím, že se cesta k souboru předá metodu Load třídy Image. Jakmile je načten, konvertuje/získává se obrázek do PsdImage. Vytvořte instanci třídy JpegOptions a nastavte její různé vlastnosti. Nyní zavolejte metodu Save instance PsdImage. Následující kódový úryvek vám ukazuje, jak sloučit vrstvy PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Příklady-CSharp-Aspose-ModifikaceAKonverzeObrázků-PSD-SloučeníPSDvrstev-SloučeníPSDvrstev.cs" >}}
## **Podpora šedé s alfa kanálem pro PSD**
Tento článek ukazuje, jak podporovat šedou s alfa kanálem pro soubor PSD při konverzi souboru PSD na PNG s pomocí Aspose.PSD. V následujícím příkladu je existující soubor PSD načten tím, že se cesta k souboru předá metodu Load třídy Image. Jakmile je načten, konvertuje/získává se obrázek do PsdImage. Vytvořte instanci třídy PngOptions a nastavte její různé vlastnosti. Nastavte vlastnost [TypBarvy](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) na BarvaSPrůhledností. Nyní zavolejte metodu Save instance PngOptions. Následující kódový úryvek vám ukazuje, jak konvertovat do šedého