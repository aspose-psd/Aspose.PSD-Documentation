---
title: Manipulace s obrázky ve formátu JPEG
type: docs
weight: 20
url: /cs/java/manipulace-s-obrazky-ve-formatu-jpeg/
---

## **Použití třídy ExifData k čtení a modifikaci EXIF značek JPEG**

Téměř všechny digitální fotoaparáty (včetně chytrých telefonů), skenery a další systémy pro manipulaci s obrázky ukládají obrázky s informacemi EXIF (Exchangeable Image File). Fotoaparát zaznamenává do souboru s obrazem informace o nastavení kamery a scéně. EXIF data také zahrnují časy závěrky, datum a čas pořízení fotografie, ohniskovou vzdálenost, kompenzaci expozice, vzor měření a informaci o použití blesku. API Aspose.Imaging umožňuje extrahovat informace EXIF ze zadaného obrázku velmi snadným a jednoduchým způsobem. Vývojáři mohou také zapisovat EXIF data do obrázků nebo upravovat existující informace podle svých potřeb. Aspose.Imaging poskytuje třídu ExifData pro čtení, zápis a modifikaci EXIF dat, zatímco obor názvů Aspose.PSD.Exif.Enums obsahuje relevantní výčty používané v procesu.
### **Čtení EXIF dat**
API Aspose.PSD poskytuje způsoby, jak číst EXIF data ze zadaného obrázku. Níže uvedené kroky ilustrují použití třídy ExifData pro čtení informací EXIF z obrázku.

- Načtěte obrázek PSD pomocí metody Load.
- Najděte náhled v JPEG mezi zdroji PSD.
- Extrahujte instanci třídy ExifData.

Získejte požadované informace a zapište je na konzoli.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Alternativně mohou vývojáři získat konkrétní informace pomocí následujícího kódu.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Zapisování a modifikace EXIF dat**
Pomocí API Aspose.PSD mohou vývojáři zapisovat nové informace EXIF a modifikovat existující EXIF data obrázku. Obě procesy (Zapisování a Modifikace) vyžadují načtení obrázku a získání EXIF dat do instance třídy ExifData. Poté můžete přistupovat k vlastnostem zpřístupněným třídou ExifData ke správnému nastavení. Všimněte si, že obrázky určené k manipulaci by měly být obrázky ve formátu JPEG nebo TIFF, které jsou obvykle náhledy PSD. Ukázkový kód pro demonstraci použití je následující:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Extrakce náhledů ze zdrojů PSD**
Náhledy jsou zmenšené verze obrázků, které slouží k zobrazení významné části obrázku místo celého snímku. Některé obrazové soubory (zejména ty pořízené digitálním fotoaparátem) obsahují vložený náhled obrazu ve souboru. API Aspose.PSD vám umožňuje extrahovat náhledy zdrojů PSD a ukládat je samostatně na disk. Zdroje náhledů obsahují vlastnost ExifData.Thumbnail, která může získat data náhledu. Následující kódová ukázka demonstruje, jak to provést.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Použijte výše diskutovaný přístup ke zpřístupnění náhledu v jiných podporovaných formátech souborů. Pokud chcete exportovat data náhledu do jiných formátů obrázků jako BMP a PNG, použijte jiné možnosti exportu obrázků.
### **Extrakce náhledů z segmentů JFIF**
Je také možné extrahovat náhledy z segmentů ExifData nebo JFIF v zdrojích náhledů PSD. Následující kód ukazuje, jak provést extrakci dat náhledu z segmentu JFIF nebo ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Použijte výše diskutovaný přístup ke zpracování náhledu v jiných podporovaných formátech souborů. Pokud chcete exportovat data náhledu do jiných formátů obrázků jako BMP a PNG, použijte jiné možnosti exportu obrázků.
### **Přidání náhledu do segmentu JFIF**
Následující kódová ukázka ukazuje, jak použít vlastnost JFIF.Thumbnail k přidání náhledového obrázku do segmentu JFIF načteného obrázku PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Náhledové obrázky s jinými segmentovými daty nesmějí obsahovat více než 65 545 bajtů kvůli specifikacím formátu JPEG. V případech, kdy jsou velké obrázky určeny k použití jako náhled, může vzniknout výjimka.
### **Přidání náhledu do segmentu EXIF**
Název následujícího kódu ukazuje, jak použít vlastnost ExifData.Thumbnail k přidání náhledového obrázku do segmentu EXIF načteného obrázku PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

V tomto případě API Aspose.PSD nemůže odhadnout velikost náhledového obrázku, ale může zkontrolovat velikost celého segmentu dat EXIF. Tato velikost nemůže být větší než 65 535 bajtů.
## **Použití třídy JpegExifData k čtení a modifikaci EXIF značek JPEG**
API Aspose.PSD poskytuje třídu JpegExifData, která je exkluzivní pro formáty obrázků ve formátu JPEG k získání a aktualizaci informací EXIF. Tento článek demonstruje použití třídy JpegExifData k dosažení stejného cíle. Třída Aspose.PSD.Exif.JpegExifData slouží jako kontejner EXIF dat pro obrázky ve formátu JPEG a poskytuje způsob, jak získat standardní EXIF značky JPEG, jak je uvedeno níže:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Kompletní seznam EXIF značek**
Výše uvedený kód čte několik EXIF značek pomocí vlastností nabízených třídou Aspose.PSD.Exif.JpegExifData. Kompletní seznam těchto vlastností je k dispozici zde. Následující kód přečte všechny EXIF značky pomocí třídy System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Automatická korekce orientace obrázků ve formátu JPEG**
Fotografie mohou být pořízeny fotoaparátem otočeným o 90°, 180°, 270° nebo žádným směrem (normální orientace). Většina digitálních fotoaparátů ukládá informace o orientaci spolu s daty obrázku jako EXIF značky obrázků ve formátu JPEG. Tyto informace lze použít k automatickému otáčení obrázků k opravě orientace. API Aspose.PSD poskytuje metodu AutoRotate pro třídu JpegImage k automatické korekci orientace obrázků ve formátu JPEG. Zde je příklad, jak můžete použít metodu AutoRotate s API Aspose.PSD pro Java.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Podpora pro JPEG-LS s modely barev CMYK a YCCK**


API Aspose.PSD pro jazyk Java poskytuje podporu pro modely barev CMYK a YCCK s formátem JPEG-LS. Následující kódová ukázka ukazuje, jak tuto podporu pro JPEG-LS použít.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Podpora pro JPEG-LS s 2-7 bity na vzorek**


API Aspose.PSD pro jazyk Java poskytuje podporu pro JPEG-LS obrázky s 2-7 bity na vzorek. Následující kódová ukázka ukazuje, jak tuto podporu pro JPEG-LS použít.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Nastavení typu barvy a typu komprese pro obrázky ve formátu JPEG**




API Aspose.PSD pro jazyk Java poskytuje podporu pro typ barvy a typ komprese a nastavuje je jako stupně šedi a progresivní pro obrázky ve formátu JPEG. Následující kódová ukázka ukazuje, jak tuto podporu použít.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}


