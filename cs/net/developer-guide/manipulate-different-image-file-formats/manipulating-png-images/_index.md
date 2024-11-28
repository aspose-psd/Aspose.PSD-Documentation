---
title: Manipulace s PNG obrázky
type: docs
weight: 40
url: /cs/net/manipulace-s-png-obrazky/
---

## **Určování průhlednosti pro PNG obrázky**
Jednou z výhod ukládání obrázků ve formátu PNG je možnost mít průhledné pozadí. Aspose.PSD pro .NET poskytuje funkci určování průhlednosti pro PNG obrázky a rastrární obrázky, jak je ukázáno v následující části. Aspose.PSD pro .NET API může být použito k nastavení jakékoliv barvy jako průhledné při vytváření nových PNG obrázků nebo při konverzi existujících obrázků do formátu PNG. Pro tyto účely má Aspose.PSD pro .NET API vystavenu vlastnost [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) a výčet [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype), které lze nastavit k určení libovolné barvy, která bude ve vykreslena jako průhledná v PNG obrázku. Následující ukázkový kód demonstruje, jak převést existující obrázek PSD na obrázek PNG s určením požadované barvy jako průhledné.

## **Nastavení rozlišení pro PNG obrázky**
Aspose.PSD pro .NET vystavuje třídu ResolutionSetting, která může být použita k nastavení rozlišení pro všechny formáty obrázků včetně PNG. Tento článek demonstruje použití Aspose.PSD pro .NET API k nastavení horizontálních a vertikálních parametrů rozlišení pro formát PNG. Následující ukázkový kód načte existující obrázek PSD a konvertuje ho do formátu PNG, přičemž také mění rozlišení.

## **Komprese PNG souborů**
Portable Network Graphic (PNG) je bezeztrátový kompresní formát pro přenos bitmapy po sítích. Když uložíte obrázek jako soubor PNG v jakémkoli programu, můžete být požádáni, abyste vybrali úroveň komprese v rozsahu od 0 do maximální úrovně. Nastavení tohoto hodnoty ve skutečnosti komprimuje velikost souboru a neovlivňuje kvalitu obrázku. Tento článek popisuje, jak Aspose.PSD API umožňuje ovládat velikost PNG souboru. Aspose.PSD API lze použít k nastavení úrovní komprese pro formát PNG s použitím třídy PngOptions, která obsahuje vlastnost celočíselného typu [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). Tato vlastnost přijímá hodnotu od 0 do 9, kde 9 představuje maximální kompresi. Následující ukázkový kód demonstruje, jak nastavit úrovně komprese pomocí Aspose.PSD pro .NET API.

## **Určování hloubky bitů pro PNG obrázky**
Hloubka bitů v obrazovkách je počet bitů použitých k označení barvy jediného pixelu v bitmapovém obrázku. Stejně jako ve všech ostatních formátech bitmap, je hloubka barev PNG také vyjádřena v bitech, jako například 1 bit (2 barvy), 2 bity (4 barvy), 4 bity (16 barev) a 8 bitů (256 barev). Aspose.PSD pro .NET API lze použít k nastavení hloubky bitů pro PNG obrázky pomocí vlastnosti [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth), kterou vystavuje třída PngOptions. V současné době lze vlastnost BitDepth nastavit na 1, 2, 4 nebo 8 bitů pro stupnice šedé a indexované barvy. Pro všechny ostatní typy barev jsou podporovány pouze 8 bitů. Následující ukázkový kód demonstruje, jak nastavit hloubku bitů pro PNG obrázek.

## **Aplikace filtrací na PNG obrázky**
Hloubka bitů v obrazovkách je počet bitů použitých k označení barvy jediného pixelu v bitmapovém obrázku. Stejně jako ve všech ostatních formátech bitmap, je hloubka barev PNG také vyjádřena v bitech, jako například 1 bit (2 barvy), 2 bity (4 barvy), 4 bity (16 barev) a 8 bitů (256 barev). Aspose.PSD pro .NET API lze použít k nastavení hloubky bitů pro PNG obrázky pomocí vlastnosti BitDepth vystavované třídou PngOptions. V současné době lze vlastnost BitDepth nastavit na 1, 2, 4 nebo 8 bitů pro stupnice šedé a indexované barvy. Pro všechny ostatní typy barev jsou podporovány pouze 8 bitů. Následující ukázkový kód demonstruje, jak nastavit hloubku bitů pro PNG obrázek.

## **Změna pozadí transparentního PNG obrázku**
Obrázky ve formátu PNG mohou mít transparentní pozadí. Aspose.PSD pro .NET poskytuje možnost změnit barvu pozadí PNG obrázku, která má transparentní pozadí. Aspose.PSD pro .NET API lze použít k nastavení/změně barvy transparentního PNG obrázku. Následující ukázkový kód demonstruje, jak nastavit/změnit barvu pozadí transparentního PNG obrázku.
