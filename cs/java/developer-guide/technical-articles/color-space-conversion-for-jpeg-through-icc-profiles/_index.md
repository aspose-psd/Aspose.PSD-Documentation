---
title: Konverze barevného prostoru pro JPEG pomocí ICC profilů
type: docs
weight: 50
url: /cs/java/konverze-barevneho-prostoru-pro-jpeg-pomoci-icc-krofili/
---

## **Správa barev pro formát JPEG**

Tento článek diskutuje o použití ICC profilů k provádění správy barevného prostoru při práci s formátem JPEG pomocí API Aspose.PSD. Vnitřní barevný prostor JPEG je YCbCr, ale tento formát může také pojmout odstíny šedi, RGB, CMYK a YCCK barevné prostory k ukládání metadat obrázku. API Aspose.PSD převážně pracuje v barevném prostoru RGB, proto API musí provádět konverzi mezi barevnými prostory do a z RGB pro správné zpracování souborů JPEG. Konverze odstínů šedi na RGB a YCbCr na RGB lze provést pomocí matematických transformací, ale prostory CMYK a YCCK nelze snadno převést do barevného prostoru RGB.

API Aspose.PSD musí provádět přímou transformaci barev z RGB do CMYK pro obrazy JPEG s barevným prostorem CMYK. Na druhé straně obrázky s barevným prostorem YCCK vyžadují transformaci barev z RGB do CMYK do YCCK, přičemž transformace CMYK na YCCK používá konverzi ITU-R BT.601 aplikovanou na první tři kanály a ponechává kanál k nedotčenýmu. Jinými slovy, API Aspose.PSD musí provádět vzájemnou konverzi barevných prostorů RGB a CMYK pro obrazy s oběma prostory CMYK a YCCK, a tyto transformace se provádějí pomocí ICC profilů, které jsou v podstatě tabulky vyhledávání popisující vlastnosti barvy a pomáhající při barevných transformacích.

## **ICC Profily**

Mechanismus konverze ICC používá „Profily“, které mapují zdrojový barevný prostor na zařízením nezávislé barevné prostory CIELAB nebo CIEXYZ. Aspose.PSD může konvertovat data do požadovaného barevného prostoru při použití těchto dvou barevných prostorů s dodatečnými profily. Proto pro ICC konverzi musí uživatel dodat dva profily – jeden RGB profil k dosažení vnitřního barevného prostoru CIE a jeden CMYK profil k získání vlastností barev CMYK. Aby bylo dosaženo konverze z CMYK na RGB, je nutné prohození profilů, tj. použití CMYK profilu jako zdrojového profilu a RGB profilu jako cílového profilu.

## **Konverze barev pro JPEG pomocí ICC profilů**

API Aspose.PSD skrývá podrobnosti a poskytuje snadno použitelný mechanismus k určení ICC profilů prostřednictvím třídy JpegOptions. Navíc Aspose.PSD používá vzorové profily SWOP CMYK a sRGB vložené do svého jádra, takže ve většině běžných případů uživatel nepotřebuje hledat žádné konkrétní profily. Existuje nevýhoda takových korekcí, a to je; takové konverze barevného prostoru jsou nevratné, protože nemůžeme očekávat stejnou barvu po konverzi z RGB do CMYK do RGB kvůli nekompatibilním barevným prostorům a odlišným barevným profilům. Následující část kódu demonstatuje použití Aspose.PSD pro Java API k nastavení RGB a CMYK barevných profilů pro obraz YCCK ve formátu JPEG. V následujícím příkladu jsou změněny RGB a CMYK barevné profily a obrázek je uložen ve barevném prostoru YCCK. Zaznamenejte, že tyto vlastnosti RgbColorProfile a CmykColorProfile budou fungovat pro změnu pixelových dat pro barevný prostor YCCK. Všechny ostatní barevné prostory nezískají barevné profily k aktualizaci barevných dat.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}

Pokud nejsou žádné profily nastaveny, pak Aspose.PSD pro Java API použije výchozí profily. Následující příklad používá vlastnosti cílových profilů, které mění cílový barevný prostor pro většinu JpegImages.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}
