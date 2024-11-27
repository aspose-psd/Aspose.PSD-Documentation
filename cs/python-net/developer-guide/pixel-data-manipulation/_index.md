---
title: Manipulace s pixelovými daty pomocí Aspose.PSD pro Python
weight: 100
type: docs
description: Příklad, jak přímo a rychle upravovat surová pixelová data pomocí API PSD pro Python
keywords: [upravit pixely, upravit psd, upravit vrstvu, manipulace se surovými daty, upravit psd data, psd api, python, ukázkový kód]
url: cs/python-net/manipulace-s-pixelovymi-datami/
---

## **Úvod**
Aspose.PSD je mocná knihovna, která vám umožňuje pracovat soubory Adobe Photoshop (PSD) v Pythonu. V tomto článku se podíváme na to, jak manipulovat pixelová data v souboru PSD pomocí Aspose.PSD.

## **Přehled**
Poskytnutý kód ukazuje, jak vytvořit soubor PSD, přidat novou vrstvu a pak přímo manipulovat pixelová data a uložit upravený obrázek.

Import potřebných modulů: Prvním krokem je importovat potřebné moduly. Importujeme modul BytesIO z knihovny io a třídy PsdImage a Layer z modulů aspose.psd.fileformats.psd a aspose.psd.fileformats.psd.layers.

Poté definujeme vstupní a výstupní cesty k souborům. 

Otevření vstupního souboru jako streamu: Otevřeme vstupní soubor jako stream pomocí funkce open a režimu "rb". Argument buffer je nastaven na 0 pro vypnutí vyrovnávání. Obsah souboru je načten do streamu BytesIO a stream je nastaven na začátek pomocí stream.seek(0).

Vytvoříme objekt vrstvy PSD předáním streamu konstruktoru třídy Layer.

Vytvoříme nový obrázek PSD pomocí konstruktoru třídy PsdImage a poskytneme šířku a výšku vrstvy jako argumenty.

Přiřadíme vrstvu k vlastnosti layers obrázku PSD pomocí operátoru přiřazení (=).

Pro manipulaci s pixelovými daty nejprve načteme pixely ARGB32 z vrstvy pomocí metody load_argb_32_pixels. Výsledek uložíme do proměnné pixels.

Následně definujeme rozsah indexů (pixelsRange) na základě délky pole pixels. Procházíme indexy a kontrolujeme, zda je index dělitelný pěti. V takovém případě nastavíme hodnotu pixelu na tomto indexu na 500000. Chceme vytvořit prostě nějaký opakující se vzor. Pixely můžete měnit podle svého uvážení.

Poté uložíme upravená pixelová data zpět do vrstvy pomocí metody save_argb_32_pixels.

Nakonec uložíme obrázek PSD do výstupního souboru pomocí metody save.

V tomto článku jsme prozkoumali, jak manipulovat pixelová data v souboru PSD pomocí Aspose.PSD pro Python. Porozuměním poskytnutého kódu můžete provádět různé operace na úrovni pixelů, například modifikovat pixely na základě určitých podmínek. Aspose.PSD poskytuje komplexní sadu funkcí pro práci se soubory PSD programově, což ho činí cenným nástrojem pro úkoly manipulace s obrázky v Pythonu.

Upozorňujeme, že poskytnutý kód předpokládá, že již máte nainstalovanou knihovnu Aspose.PSD a její závislosti. Další informace o instalaci a používání Aspose.PSD pro Python naleznete v oficiální dokumentaci.

Zkontrolujte prosím kompletní příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentace-Python-Aspose-manipulace-s-pixelovymi-datami.py" >}}
