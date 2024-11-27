---
title: Seznam podporovaných globálních obrazových prostředků formátu PSD
type: docs
weight: 30
url: /cs/seznám-podporovaných-globálních-obrazových-prostředků-psd/
---

## **Aspose.PSD podporuje nízkoúrovňovou úpravu obrazových prostředků.**
Seznam plně podporovaných obrazových prostředků naleznete v Aspose.PSD .Net [Odkaz na API referenci](https://reference.aspose.com/psd/net)

Podle specifikace formátu Adobe® Photoshop®: Obrazové prostředky používají několik standardních čísel ID, jak je uvedeno v tabulce s ID obrazových prostředků. Ne všechny formáty souborů používají všechna ID. Některé informace mohou být uloženy v jiných sekcích souboru.

Pro tyto identifikátory zdrojů, které byly přidány od Photoshopu 3.0, záznam označuje verzi, ve které byly představeny, např. (*Photoshop 6.0).*

ID obrazových prostředků.

|**ID**|**Popis**|
| :- | :- |
|**Desítkové**||
|1000|*(Zastaralé - pouze Photoshop 2.0)* Počet kanálů, řádků, sloupců, hloubky a režimu|
|1001|Záznam informací tiskového správce Macintosh|
|1002|Informace o formátování stránky Macintoshu. Není již čteno Photoshopem. *(Zastaralé)*|
|1003|*(Zastaralé - pouze Photoshop 2.0)* Indexovaná barevná tabulka|
|1005|[Struktura ResolutionInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource).|
|1006|Názvy alfa kanálů jako řada Pascalových řetězců.|
|1007|*(Zastaralé) Viz ID 1077 Struktura* DisplayInfo*.*|
|1008|Titulek jako Pascalův řetězec.|
|1009|[Informace o ohraničení.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) Obsahuje pevné číslo (2 bajty skutečné, 2 bajty zlomek) pro šířku ohranice a 2 bajty pro jednotky ohranice (1 = palce, 2 = cm, 3 = body, 4 = koule, 5 = sloupce).|
|1010|[Barva pozadí. ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Tiskové příznaky. Řada jednobytových logických hodnot: návěští, řezné značky, barevné pruhy, registrační značky, negativní, přefotit, interpolovat, titulek, tiskové příznaky.|
|1012|Informace o konverzi do stupňů šedi a vícekanálové konverzní tabulky|
|1013|[Informace o konverzi barevých stupňů](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Informace o konverzi duotonových stupňů|
|1015|Konverzní funkce do stupňů šedi a vícekanálová|
|1016|[Funkce převedení barev](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Převodní funkce duotonů|
|1018|Informace o duotonovém obrázku|
|1019|Dva bajty pro efektivní černé a bílé hodnoty pro rozsah bodů|
|1020|*(Zastaralé)*|
|1021|Volby EPS|
|1022|[Informace o rychlém výběrovém rohu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). ID rychlé masky; 1- bajtová hodnota boolean, zda byla maska původně prázdná.|
|1023|*(Zastaralé)*|
|1024|[Informace o stavu vrstvy](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Pracovní cesta (není uložena). Formát zdroje cesty.|
|1026|[Informace o skupinách vrstev](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 bajty na vrstvu obsahující identifikátor skupiny pro přetažení skupin. Vrstvy ve skupině mají stejné ID skupiny.|
|1027|*(Zastaralé)*|
|1028|Záznam IPTC-NAA. Obsahuje informace *File Info...*.|
|1029|Režim obrazu pro soubory v raw formátu|
|1030|Kvalita JPEG. Privátní.|
|1032|*(Photoshop 4.0) [Informace o mřížce a vodítkách.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0)*(   )[Náhledový zdroj](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[pro Photoshop 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* pouze|
|1034|*(Photoshop 4.0)* Copyrightová vlajka. Boolean, indikující, zda je obrázek chráněn autorským právem.|
|1035|*(Photoshop 4.0)* URL. Odkaz na textový řetězec s jednotným umístěním zdroje.*.*|
|1036|*(Photoshop 5.0)[Náhledový zdroj](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (nahrazuje zdroj 1033).|
|1037|*(Photoshop 5.0) [Globální úhel](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 bajty obsahující celé číslo mezi 0 a 359, které je globálním úhlem osvětlení pro vrstvu efektů. Pokud není přítomen, předpokládá se 30.|
|1038|*(Zastaralé) Viz ID 1073 níže. (Photoshop 5.0)* Barevné vzorkovací zdroje.|
|1039|*(Photoshop 5.0) [Profil ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Hrubé bajty profilu formátu ICC (International Color Consortium).*  |
|1040|*(Photoshop 5.0) [Vodoznak](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [Profil ICC bez značek](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 bajt, který zakazuje jakékoli předpokládané zacházení s profilem při otevření souboru. 1 = záměrně neoznačeno.|
|1042|*(Photoshop 5.0)* Viditelné efekty. 1bajtová globální vlajka pro zobrazení/skrytí všech vrstev efektů. Přítomno pouze, pokud jsou skryty.|
|1043|*(Photoshop 5.0)* Spotové zrnítko. 4 bajty pro verzi, 4 bajty pro délku a proměnná délka dat.|
|1044|*(Photoshop 5.0)[Specifické ID dokumentu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* počáteční číslo. 4 bajty: Základní hodnota, od které bude generováno ID vrstev (nebo vyšší hodnota, pokud již existující ID překračují). Jeho účelem je zabránit případu, kdy přidáme vrstvy, zploštíme, uložíme, otevřeme a pak přidáme další vrstvy, které skončí s týmiž ID jako první sada.|
|1045|*(Photoshop 5.0) [Unicode alfa názvy](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Počet indexovaných barev tabulky. 2 bajty pro počet barevních tónů definovaných ve stolu|
|1047|*(Photoshop 6.0)* [Průhlednostní index](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Globální nadmořská výška.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Řezy.|
|1051|*(Photoshop 6.0)* URL pracovního postupu.|
|1052|*(Photoshop 6.0)* Skok na XPEP. 2 bajty hlavní verze, 2 bajty vedlejší verze, 4 bajty počet. Následuje opakování pro počet: 4 bajty velikost bloku, 4 bajty klíč, pokud je klíč *'jtDd'* , potom následuje boolean pro příznak špinavého zaškrtávání; jinak je to 4bajtový vstup pro modifikaci data.|
|1053|*(Photoshop 6.0)* Alfa identifikátory.|
|1054|*(Photoshop 6.0)[Seznam URL](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* [Informace o verzi](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource).|
|1058|*(Photoshop 7.0)* EXIF data 1.|
|1059|*(Photoshop 7.0)* EXIF data 3*.*|
|1060|*(Photoshop 7.0)* [XMP metadata](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Informace o souboru jako popis v XML.|
|1061|*(Photoshop 7.0)[Ověřovací souhrn](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 bajtů: RSA Data Security, algoritmus MD5 pro zprávu o stravitelnosti|
|1062|*(Photoshop 7.0)[Informace o tiskovém měřítku](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = středové, 1 = velikost pro přizpůsobení, 2 = uživatelem definované). 4 bajty x poloha (desetinné číslo). 4 bajty y poloha (desetinné číslo). 4 bajty měřítko (desetinné číslo)|
|1064|*(Photoshop CS)* [Poměr stran pixelů](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Vrstevné scény.|
|1066|*(Photoshop CS)* Ostatní duotonové barvy. Tento prostředek není čten nebo použit Photoshopem.|
|1067|*(Photoshop CS)* Ostatní spotové barvy. Tento prostředek není čten nebo použit Photoshopem.|
|1069|*(Photoshop CS2)* [Identifikátor(y) výběru vrstvy](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource). 2 bajty počet, následuje opakování pro každý počet: 4 bajty ID vrstvy|
|1070|*(Photoshop CS2)* Informace o HDR zesílení|
|1071|*(Photoshop CS2)* Tiskové informace|
|1072|*(Photoshop CS2)* [Identifikátor povolených skupin vrstev](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 bajt pro každou vrstvu v dokumentu, opakováno podle délky zdroje. POZNÁMKA: Skupiny vrstev mají značky začátku a konce|
|1073|*(Photoshop CS3)* Barevné vzorkovací zdroje. Viz také ID 1038 pro starý formát.|
|1074|*(Photoshop CS3)* Měřítko měření.|
|1075|*(Photoshop CS3)* Informace o časové ose.|
|1076|*(Photoshop CS3)* Zobrazení listu.|
|1077|*(Photoshop CS3) Struktura* DisplayInfo* pro podporu plovoucích bodových barev. Viz také ID 1007.|
|1078|*(Photoshop CS3)* Cibuloviny.|
|1080|*(Photoshop CS4)* Informace o počtu.|
|1082|*(Photoshop CS5)* Informace o tisku.|
|1083|*(Photoshop CS5)* Styl tisku. Tiskařské značky, návěští, ozdoby atd.|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo. Variabilní informace specifické pro OS pro Macintosh.|
|1085|*(Photoshop CS5)* Windows DEVMODE. Variabilní informace specifické pro OS pro Windows.|
|1086|*(Photoshop CS6)* Cesta k automatickému uložení souboru.|
|1087|*(Photoshop CS6)* Formát automatického uložení. |
|1088|*(Photoshop CC)* Stav výběru cesty.|
|2000-2997|Informace o cestě (uložené cesty).|
|2999|Název ořezové cesty.|
|3000|*(Photoshop CC)* Informace o původu cesty|
|4000-4999|Zásuvné prostředky. Prostředky přidané zásuvným modulem.|
|7000|Proměnné Image Ready. XML reprezentace definice proměnných|
|7001|Datasety Image Ready|
|7002|Výchozí vybraný stav Image Ready|
|7003|Rozšířený stav při najetí Image Ready 7|
|7004|Rozšířený stav při najetí Image Ready|
|7005|Uložená nastavení vrstvy v Image Ready|
|7006|Verze Image Ready|
|8000|*(Photoshop CS3)* Řízení práce v Lightroomu, pokud je přít