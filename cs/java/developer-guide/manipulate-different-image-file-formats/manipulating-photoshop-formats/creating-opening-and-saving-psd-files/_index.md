---
title: Vytváření, Otevírání a Ukládání souborů PSD
type: docs
weight: 10
url: /cs/vytváření-otevírání-a-ukládání-souborů-psd/
---

## **Exportování obrázku do formátu PSD**
PSD, PhotoShop dokument, je výchozí formát souboru používaný programem Adobe PhotoShop pro práci s obrázky. Aspose.PSD vám umožňuje načíst, upravit a uložit soubory do formátu PSD, aby mohly být otevřeny a upraveny v programu PhotoShop. Tento článek ukazuje, jak uložit soubor do formátu PSD s Aspose.PSD a také diskutuje některá nastavení, která lze použít při ukládání do tohoto formátu. PsdOptions je specializovaná třída v prostoru názvů ImageOptions používaná k exportu obrázků do formátu PSD. Chcete-li exportovat do formátu PSD, vytvořte instanci třídy Image, buď načtenou z existujícího obrázkového souboru (například náhledů) nebo vytvořenou základě ze začátku. Tento článek vysvětluje jak. V následujících příkladech je obrázek vytvořen od základu. Jakmile je vytvořen a pixelová data jsou naplněna, uložte obrázek pomocí metody Save třídy Image a jako druhý argument zadejte objekt PsdOptions. Některé vlastnosti třídy PsdOptions lze nastavit pro pokročilou konverzi. Některé z vlastností jsou ColorMode, CompressionMethod a Version. Aspose.PSD podporuje následující metody komprese pomocí enumerace CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Následné barevné módy jsou podporovány pomocí enumerace ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


K tomu se dají přidat další zdroje, jako jsou náhledové zdroje pro PSD verze 4.0, 5.0 a vyšší, nebo mřížková a průvodcovská rozhraní zdrojů pro PSD verze 4.0 a vyšší. Kód níže vytvoří soubor BMP od základu, naplní pixely a uloží jej do formátu PSD s kompresní metodou RLE a módem šedé stupnice. Následující kódový úryvek vám ukazuje, jak exportovat obrázek do formátu PSD.


## **Importování obrázku na vrstvu PSD**
Tento článek ukazuje použití Aspose.PSD k přidání nebo importování obrázku na vrstvu PSD. API Aspose.PSD vystavily efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD vystavil metodu DrawImage třídy Layer k přidání/importování obrázku do souboru PSD. Metoda DrawImage potřebuje umístění a hodnoty obrázku pro přidání/importování obrázku do souboru PSD. Kroky k importu obrázku do vrstvy PSD jsou jednoduché následujícím způsobem:

- Načtěte soubor PSD jako obrázek pomocí tovární metody Load vystavené třídou Image.
- Vytvořte instanci třídy Layer a přiřaďte ji vrstvě obrázku PSD.
- Načtěte obrázek, který potřebuje být přidán, nebo vytvořte jeden od základu.
- Voláním metody Layer.DrawImage a specifikováním umístění a instance obrázku.
- Uložte výsledky.



Následující kódový úryvek vám ukazuje, jak importovat obrázek do vrstvy PSD.


## **Vytváření miniatur z souborů PSD**
PSD je národní formát dokumentu aplikace Adobe Photoshop. Adobe Photoshop (verze 5.0 a novější) ukládá informace o náhledech pro zobrazení náhledu v bloku zdrojů obrázku skládajícím se z úvodní záhlaví o 28 bytech, následovaného JFIF náhledem ve stejném pořadí RGB (červená, zelená, modrá). API Aspose.PSD poskytuje snadný mechanismus pro přístup k zdrojům souboru PSD. Tyto zdroje zahrnují také náhledový zdroj, který lze následně získat a uložit na disk dle potřeby aplikace. Následující kódový úryvek vám ukazuje, jak vytvořit náhledy z souborů PSD.


## **Vytváření indexovaných souborů PSD**
API Aspose.PSD pro Java umožňuje vytvořit indexované soubory PSD od základu. Tento článek ukazuje použití tříd PsdOptions a PsdImage k vytvoření indexovaného souboru PSD při kreslení některých tvarů na nově vytvořené plátno. Následující jednoduché kroky jsou potřebné pro vytvoření indexovaného souboru PSD.

- Vytvoření instance třídy PsdOptions a nastavit její zdroje.
- Nastavte vlastnost ColorMode třídy PsdOptions na ColorModes.Indexed.
- Vytvořte novou paletu barev ze spektra RGB a nastavte ji jako vlastnost Palette třídy PsdOptions.
- Nastavte vlastnost CompressionMethod na požadovaný kompresní algoritmus.
- Vytvořte nový obrázek PSD voláním metody PsdImage.Create.
- Nakreslete grafiku nebo proveďte jiné operace podle potřeby.
- Zavolejte metodu PsdImage.Save k potvrzení všech změn.


Následující kódový úryvek vám ukazuje, jak vytvářet indexované soubory PSD.


## **Exportování vrstvy PSD do rástrového obrázku**
Aspose.PSD pro Java vám umožňuje exportovat vrstvy v souboru PSD do rástrovaných obrázků. Použijte prosím metodu Aspose.PSD.FileFormats.Psd.Layers.Layer.Save k exportu vrstvy do obrázku. Následující ukázkový kód načte soubor PSD a exportuje každou z jeho vrstev do obrázku PNG pomocí metody Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Jakmile jsou všechny vrstvy exportovány do obrázků PNG, můžete je otevřít pomocí vašeho oblíbeného prohlížeče obrázků. Následující kódový úryvek vám ukazuje, jak exportovat vrstvu PSD do rástrového obrázku.


