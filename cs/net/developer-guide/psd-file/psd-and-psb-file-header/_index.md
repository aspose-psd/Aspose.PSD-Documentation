---
title: Hlavička souboru PSD a PSB
type: docs
weight: 40
url: /cs/net/psd-and-psb-file-header/
---

## **Popis**
Hlavička souboru Adobe Photoshop obsahuje informace o verzi souboru (1 pro PSD a 2 pro PSB), počet kanálů, barevný režim a hloubku bitů.

Kombinace barevného režimu a hloubky bitů podporované Aspose.PSD můžete zjistit z příslušného článku.


Hlavička souboru obsahuje základní vlastnosti obrazu.

|**Délka**|**Popis**|
| :- | :- |
|4|Podpis: vždy rovno *"8BPS"*|
|2|[Verze PSD](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): vždy rovno 1 pro soubory PSD a 2 pro soubory PSB. Aspose.PSD dokáže rozpoznat verzi formátu souboru a správně ji číst.|
|6|Vyhrazeno: musí být nula.|
|2|Počet kanálů v obraze, včetně případných alfa kanálů. Podporovaný rozsah je 1 až 56.|
|4|Výška obrazu v pixelech. Podporovaný rozsah je 1 až 30 000. Soubor PSB podporuje výšku až 300 000 pixelů. PSB soubory jsou také podporovány Aspose.PSD.|
|4|Šířka obrazu v pixelech. Podporovaný rozsah je 1 až 30 000. Soubor PSB podporuje šířku až 300 000 pixelů. Dávkové zpracování velkých souborů PSD/PSB je také podporováno Aspose.PSD.|
|2|Hloubka: počet bitů na kanál. Podporované hodnoty jsou 1, 8, 16 a 32. Ale ne každý barevný režim funguje s každou hloubkou.|
|2|[Barevný režim PSD](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) souboru. Podporované hodnoty jsou: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.|
Můžete zkontrolovat naši [PSD API referenci](https://reference.aspose.com/psd) pro to.
