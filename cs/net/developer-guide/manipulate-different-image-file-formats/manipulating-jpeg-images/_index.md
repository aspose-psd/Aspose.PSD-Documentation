---
title: Manipulace s obrázky ve formátu JPEG
type: docs
weight: 30
url: /cs/net/manipulace-s-obrazky-ve-formatu-jpeg/
---

## **Použití třídy ExifData k čtení a úpravám EXIF značek ve formátu JPEG**
Téměř všechny digitální fotoaparáty (včetně chytrých telefonů), skenery a další systémy pracující s obrazem ukládají obrázky s EXIF (Exchangeable Image File) informacemi. Fotoaparát do souboru obrazu zaznamenává nastavení fotoaparátu a informace o scéně. EXIF data zahrnují také čas závěrky, datum a čas pořízení fotografie, ohniskovou vzdálenost, kompenzaci expozice, vzorek metrující oblasti a informaci o použití blesku. API služby Aspose.Imaging umožňuje extrahovat EXIF informace z daného obrázku velmi snadným a jednoduchým způsobem. Vývojáři mohou také zapisovat EXIF data do obrázků nebo upravovat existující informace podle svých potřeb. Aspose.PSD poskytuje třídu [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) pro čtení, zápis a úpravy EXIF dat, zatímco jmenný prostor [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) obsahuje relevantní enumerace používané v procesu.
### **Čtení EXIF dat**
Aspose.PSD API poskytuje prostředky pro čtení EXIF dat z daného obrázku. Níže uvedené kroky ilustrují použití třídy ExifData k čtení EXIF informací z obrázku.

- Načtěte obraz PSD pomocí tovární metody Load.
- Najděte miniaturu JPEG mezi zdroji PSD.
- Extrahujte instanci třídy ExifData.

Získejte požadované informace a zapište je do konzole.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Alternativně mohou vývojáři získat konkrétní informace pomocí následující části kódu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Zápis a úpravy EXIF dat**
Pomocí API Aspose.PSD mohou vývojáři zapisovat nové EXIF informace a upravovat existující EXIF data obrázku. Oba procesy (Zápis a Úprava) vyžadují načtení obrazu a získání EXIF dat do instance třídy ExifData. Poté můžete přistupovat k vlastnostem vystaveným třídou ExifData a nastavit je podle potřeby. Pamatujte, že obrázky pro úpravy by měly být v formátu Jpeg nebo Tiff, které jsou obvykle miniaturami PSD. Ukázkový kód pro demonstrování použití je následující:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Extrakce miniatur z prostředků PSD**
Miniatury jsou zmenšené verze obrázků, které slouží k zobrazení významné části obrázku namísto celého rámce. Některé obrazové soubory (zejména ty pořízené digitálními fotoaparáty) obsahují vložený miniatury obrázku v souboru. API Aspose.PSD vám umožňuje extrahovat miniatury prostředků PSD a uložit je samostatně na disk. Prostředky miniatur obsahují vlastnost ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail), která může získat data miniatury. Následující kódová ukázka demonstruje, jak ji používat.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Použijte výše popsaný postup k uložení miniatury do jiných podporovaných formátů souborů. Pokud chcete exportovat data miniatury do jiných obrázkových formátů, jako jsou BMP a PNG, použijte jiné možnosti exportu obrázků.


### **Extrakce miniatur z segmentů JFIF**
Je také možné extrahovat miniatury z JFIF segmentů nebo ExifData segmentů prostředků miniatur PSD. Následující kód ukazuje, jak provést extrakci dat miniatury z JFIF nebo ExifData segmentu:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Použijte výše popsaný postup k uložení miniatury do jiných podporovaných formátů souborů. Pokud chcete exportovat data miniatury do jiných obrázkových formátů, jako jsou BMP a PNG, použijte jiné možnosti exportu obrázků.
### **Přidání miniatury do segmentu JFIF**
Následující kódová ukázka ukazuje, jak použít vlastnost JFIF.Thumbnail k přidání miniatury do segmentu JFIF načteného obrazu PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Obrázky miniatur s jinými daty segmentu nesmí obsahovat více než 65 545 bytů kvůli specifikacím formátu JPEG. V případě, že budou odeslány velké obrázky jako miniatury, může nastat výjimka.
### **Přidání miniatury do segmentu EXIF**
Následující kódová ukázka ukazuje, jak použít vlastnost ExifData.Thumbnail k přidání miniatury do segmentu EXIF načteného obrazu PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


V tomto případě API Aspose.PSD nemůže odhadnout velikost miniatury, ale může zkontrolovat velikost celého segmentu EXIF dat. Tato velikost nemůže být větší než 65 535 bytů.
## **Použití třídy JpegExifData k čtení a úpravám EXIF značek ve formátech Jpeg**
API Aspose.PSD poskytuje třídu[JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata), která je výlučná pro formáty obrázků Jpeg k získání a aktualizaci EXIF informací. Tento článek demonstruje použití třídy JpegExifData k dosažení toho samého. Třída Aspose.PSD.Exif.JpegExifData slouží jako kontejner EXIF dat pro obrázky Jpeg a poskytuje prostředky k získání standardních EXIF značek Jpeg, jak je ukázáno níže:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Kompletní seznam EXIF značek**
Výše uvedená část kódu čte několik EXIF značek pomocí vlastností nabízených třídou Aspose.PSD.Exif.JpegExifData. Kompletní seznam těchto vlastností je k dispozici zde. Následující kód přečte všechny EXIF značky pomocí třídy [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Automatická korekce orientace obrázků ve formátu JPEG**


Fotografie mohou být pořízeny fotoaparátem otočeným o 90°, 180°, 270° nebo žádným způsobem (normální orientace). Většina digitálních fotoaparátů ukládá informace o orientaci spolu s obrazovými daty jako EXIF značkami obrázků ve formátu JPEG. Tyto informace lze použít k automatickému otočení obrázků a k opravě orientace. API Aspose.PSD poskytuje metodu AutoRotate pro třídu JpegImage k automatické korekci orientace obrázků ve formátu JPEG. Zde je, jak můžete použít metodu AutoRotate s API Aspose.PSD pro .NET.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Podpora pro JPEG-LS s CMYK a YCCK**


API Aspose.PSD pro .NET poskytuje podporu pro barevné modely CMYK a YCCK s formátem JPEG-LS. Následující část kódu demonstruje, jak tuto podporu pro JPEG-LS použít.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Podpora pro 2-7 bitů na vzorek v obrazech JPEG-LS**


API Aspose.PSD pro .NET poskytuje podporu pro obrázky JPEG-LS s 2 až 7 bity na vzorek. Následující část kódu demonstruje, jak tuto podporu pro JPEG-LS použít.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Nastavení ColorType a CompressionType pro obrázky ve formátu JPEG**




API Aspose.PSD pro .NET poskytuje podporu pro typ barvy a typ komprese a nastavuje je jako stupně šedi a postupný pro obrázky ve formátu JPEG. Následující část kódu demonstruje, jak tuto podporu použít.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}


Následující část kódu ukazuje, jak použít vlastnost ExifData.Thumbnail k přidání miniatury do segmentu EXIF načteného obrázku PSD.



{{< gist "aspose-com-gists" "8a4d34ce76d165c2fc7c0ce9174154" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

V tomto případě API Aspose.PSD nemůže odhadnout velikost miniatury, ale může zkontrolovat velikost celého segmentu EXIF dat. Tato velikost nemůže být větší než 65 535 bytů.
