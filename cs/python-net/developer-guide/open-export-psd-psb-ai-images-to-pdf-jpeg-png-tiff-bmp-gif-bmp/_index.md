---
title: Otevřete soubory PSD, PSB a AI a exportujte je do formátů PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Ukázkový export souborů PSD, PSB a AI do jiných formátů
keywords: [otevřít psd, otevřít ai, otevřít psb, exportovat do png, exportovat do pdf, exportovat do jpeg, exportovat do tiff, psd api, python, ukázkový kód]
url: cs/python-net/open-export-psd-psb-ai-obrázků-do-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Přehled**
Pro převod souborů PSD, PSB a AI do různých formátů můžete použít knihovnu Aspose.PSD v jazyce Python. Tato knihovna poskytuje různé možnosti a nastavení pro přizpůsobení procesu konverze.

Nejprve je nutné importovat potřebné třídy a moduly z knihovny Aspose.PSD. Ujistěte se, že jste knihovnu nainstalovali před spuštěním kódu.

V tomto kódu definujeme různé možnosti pro různé formáty, jako jsou PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB a PSD. Tyto možnosti vám umožňují přizpůsobit výstupní soubor vašim požadavkům.

Dále definujeme slovník `formáty`, který mapuje přípony souborů na odpovídající možnosti ukládání.

Pro převod souboru PSD do jiných formátů musíte načíst soubor PSD pomocí metody PsdImage.load() a následně projít slovníkem formátů. Pro každý formát určete název výstupního souboru a uložte obrázek pomocí metody image.save().

Podobně, pro převod souboru AI do jiných formátů načtěte soubor AI pomocí metody AiImage.load() a projděte slovník formátů. Určete název výstupního souboru a uložte obrázek pomocí metody image.save().

Ujistěte se, že poskytnete správné cesty k zdrojovým souborům PSD a AI.

To je vše! Nyní můžete použít tento kód k převodu souborů PSD, PSB a AI do různých formátů pomocí Aspose.PSD pro Python.

Zkontrolujte celý příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentace-Python-Aspose-Psd-otevření-exportování-psd-psb-ai-obrázků-do-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
