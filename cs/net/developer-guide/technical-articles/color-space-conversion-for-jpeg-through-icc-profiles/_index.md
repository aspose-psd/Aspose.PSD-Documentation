---
title: Převod prostoru barev pro JPEG pomocí ICC profilů
type: docs
weight: 60
url: /cs/net/prevod-prostoru-barev-pro-jpeg-pomoci-icc-profilu/
---

## **Správa barev pro formát JPEG**

Tento článek diskutuje o použití ICC profilů k provedení správy barev při zacházení s formátem JPEG pomocí API Aspose.PSD. Vnitřní barevný prostor JPEG je YCbCr, avšak tento [formát](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) může také zahrnout stupnice šedi, RGB, CMYK a YCCK barevné prostory k uložení metadat obrázku. API Aspose.PSD hlavně pracuje v prostoru RGB, proto musí API provádět konverzi mezi barevnými prostory tam a zpět, aby bylo možné správně zacházet s soubory ve formátu JPEG. Konverze ze stupnice šedi do RGB a z YCbCr do RGB mohou být provedeny pomocí matematických transformací, ale prostory CMYK a YCCK nelze snadno převést do prostoru RGB.

API Aspose.PSD musí provádět přímou transformaci barev z RGB do CMYK pro obrázky ve formátu JPEG s prostorem barev CMYK. Na druhé straně obrázky s prostorem barev YCCK vyžadují transformaci barev z RGB do CMYK do YCCK, kde pro transformaci z CMYK do YCCK se používá konverze [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) aplikovaná na první tři kanály a poslední kanál (k) zůstává nedotčený. Jinými slovy, API Aspose.PSD musí provádět vzájemnou konverzi mezi prostory RGB a CMYK pro oba obrázky s prostory CMYK a YCCK, a tyto transformace se provádějí pomocí ICC profilů, což jsou v podstatě tabulky popisující vlastnosti barvy a pomáhající při transformacích barev.

## **ICC Profily**

Mechanismus konverze ICC používá „Profily“, které zobrazují zdrojový barevný prostor na nezávislé zařízení CIELAB nebo CIEXYZ. Aspose.PSD může konvertovat data do barevného prostoru podle potřeby při použití těchto dvou barevných prostorů s dalšími profily. Proto musí uživatel pro konverzi ICC dodat dva profily - jeden RGB profil pro přechod do vnitřního barevného prostoru CIE a jeden CMYK profil pro získání charakteristik barev CMYK. Aby se dosáhlo konverze z CMYK do RGB, je nutné vyměnit profily, to znamená; použít CMYK profil jako zdrojový profil a RGB profil jako cílový profil.

## **Převod barev pro JPEG pomocí ICC profilů**

API Aspose.PSD skrývá detaily a poskytuje snadno použitelný mechanismus pro specifikaci ICC profilů prostřednictvím třídy [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Navíc Aspose.PSD používá vzorové profily SWOP, CMYK a sRGB vložené do svého jádra, proto ve většině běžných případů uživatel nepotřebuje hledat konkrétní profily. Existuje nevýhoda takových oprav, totiž; takové konverze barevných prostorů jsou nevratné, protože nelze očekávat stejnou barvu po konverzi z RGB do CMYK a zpět na RGB kvůli nekompatibilním barevným prostorům a různým barevným profilům. Následující ukázkový kód ukazuje použití Aspose.PSD pro .NET API k určení RGB a CMYK barevných profilů pro obrázek ve formátu YCCK JPEG. V následujícím příkladu jsou změněny RGB a CMYK barevné profily a obrázek je uložen ve formátu YCCK. Upozorňujeme, že tyto vlastnosti [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) a [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) budou fungovat pro změnu pixelových dat pro prostor YCCK. Pro všechny ostatní barevné prostory nejsou barevné profily načítány pro aktualizaci barevných dat.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Pokud nejsou nastaveny žádné profily, pak API Aspose.PSD pro .NET použije výchozí profily. Následující příklad používá vlastnosti cílových profilů, které mění cílový barevný prostor pro většinu obrázků ve formátu JPEG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
