---
title: Ořezání, Otočení a Změna Velikosti Obrázků
type: docs
weight: 40
url: /cs/net/crop-rotate-and-resize-images/
---

## **Ořezání Obrázků**
Ořezání obrázku obvykle znamená odstranění vnějších částí obrázku k zlepšení ořezu. Ořezání lze také použít k vystřižení části obrázku a zvýšení zaměření na určitou oblast. API Aspose.PSD podporuje dvě různé přístupy k ořezání obrázků: pomocí posunů a obdélníku.
### **Ořezání pomocí Posunů**
Třída [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) poskytuje přetíženou verzi metody Crop, která přijímá 4 celočíselné hodnoty označující Levý, Pravý, Horní a Dolní okraj. Na základě těchto čtyř hodnot metoda Crop posouvá okraje obrázku směrem ke středu obrázku a zahazuje vnější část. Ukázkový kód níže ukazuje, jak oříznout obrázek pomocí posunů.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Ořezání pomocí Obdélníku**
Třída [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) poskytuje další přetíženou verzi metody Crop, která přijímá instanci třídy Rectangle. Můžete vyříznout libovolnou část obrázku poskytnutím požadovaných hranic objektu Rectangle. Ukázkový kód níže ukazuje, jak oříznout libovolný obrázek pomocí obdélníku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Otočení a Překlopení Obrázku**
Aspose.PSD pro .NET je snadno použitelná knihovna, protože poskytuje jednoduché metody k provádění složitých operací. Například Aspose.PSD pro .NET poskytuje metodu RotateFlip pro svou základní třídu Image, pokud aplikace vyžaduje otočení obrázku. Bez ohledu na formát obrázku může knihovna provádět specifickou Rotaci a Překlopení na něm.
### **Otočení Obrázku**
Metodu Image.RotateFlip lze použít k otočení obrázku o 90/180/270 stupňů a zrcadlení obrázku vodorovně nebo svisle. Metoda Image.RotateFlip přijímá parametr RotateFlipType, který určuje typ rotace a překlopení, které se má aplikovat na obrázek. Kroky k provedení Rotace & Překlopení jsou následující,

1. Načtěte obrázek pomocí metody Load poskytované třídou Image.
1. Zavolejte metodu Image.RotateFlip a specifikujte odpovídající RotateFlipType.
1. Uložte výsledky.

Následující ukázkový kód demonstruje nastavení vlastnosti RotateFlip obrázku a výčet RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Otočení Obrázku na Konkrétní Úhel**
API Aspose.PSD pro .NET poskytuje metodu [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate, která umožňuje uživatelům otočit obrázek na konkrétní úhel. Na rozdíl od metody [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip metoda [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate přijímá tři parametry:

1. Úhel rotace: Parametr typu float určující úhel rotace, do kterého má být obrázek otočen. Kladná hodnota otáčí obrázek ve směru hodinových ručiček; záporná hodnota provádí rotaci proti směru hodinových ručiček.
1. Poměrně změnit: Parametr typu Boolean určuje, zda má být změněna velikost obrázku podle projekcí otočeného obdélníku (rohové body). Pokud je nastaveno na false, rozměry obrázku zůstanou nedotčeny a pouze se otočí vnitřní obsah obrázku.
1. Barva pozadí: Parametr typu Color určuje barvu, která má být vyplněna do pozadí otočeného obrázku.

Následující ukázkový kód demonstruje použití metody [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Změna Velikosti Obrázků**
Tento článek demonstruje použití Aspose.PSD pro .NET ke změně velikosti obrázku. API Aspose.PSD poskytuje efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD pro .NET poskytuje metodu Resize pro třídu Image, která může být použita k dynamické změně velikosti existujících obrázků. Existují dvě přetížení metody Resize, aby vyhovovaly potřebám aplikace.
### **Jednoduché Změny Velikosti**
Kroky k provedení změny velikosti jsou následující:

1. Načtěte obrázek pomocí metody Load poskytované třídou Image.
1. Zavolejte metodu Image.Resize a specifikujte novou výšku a šířku.
1. Uložte výsledky.

Následující ukázkový kód demonstruje, jak změnit velikost obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Změna Velikosti s Výčtem ResizeType**
API Aspose.PSD poskytuje výčet ResizeType, který lze použít s metodou Image.Resize k dosažení požadovaných výsledků. Níže poskytnutá ukázka kódu ukazuje použití výčtu ResizeType, zatímco podrobnosti o členech výčtu ResizeType lze nalézt na konci této stránky.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



Pokud si přejete získat kvalitní výsledek po aplikaci změny velikosti, je doporučeno vždy používat ResizeType.LanczosResample, protože vytvoří vysoce kvalitní výsledky, ale může pracovat pomaleji než ResizeType.NearestNeighbourResample. Na druhou stranu algoritmus ResizeType.NearestNeighbourResample je speciálně používán pro rychlou změnu velikosti s kompromisem v kvalitě obrázku. Tato metoda může být užitečná pro generování náhledů v reálném čase nebo podobné procesy, kde je vyžadována výkonová efektivita.
## **Změna Velikosti Obrázku Proportionalitně**
Obrázky lze změnit velikostí předáváním nových výškových a šířkových hodnot jako parametry metody Image.Resize, ale v tomto případě musíte spočítat poměr stran sami. To je způsobeno tím, že když je změněna šířka nebo výška obrázku, obrázek je buď zvětšen nebo zmenšen tak, aby vyplnil novou velikost. Pokud nejsou změny šířky a výšky obrázku v poměru, může to vést k roztaženému a zkreslenému výsledku. Tento článek demonstruje použití Aspose.PSD pro .NET API k změně velikosti obrázků předáním buď nové výšky nebo šířky a umožnění API automaticky vypočítat druhou proporcionální hodnotu.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Výčet ResizeType**
ResizeType určuje typ změny velikosti obrázku založenou na vybraném filtru.

Členové Výčtu [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Jméno Člena**|**Hodnota**|**Popis**|
| :- | :- | :- |
|LevýHorníNaLevýHorní|0|Levý horní bod nového obrázku bude souhlasit s levým horním bodem původního obrázku. Případně dojde ke zkrácení.|
|PravýHorníNaPravýHorní|1|Pravý horní bod nového obrázku bude souhlasit s pravým horním bodem původního obrázku. Případně dojde ke zkrácení.|
|PravýDolníNaPravýDolní|2|Pravý dolní bod nového obrázku bude souhlasit s pravým dolním bodem původního obrázku. Případně dojde ke zkrácení.|
|LevýDolníNaLevýDolní|3|Levý dolní bod nového obrázku bude souhlasit s levým dolním bodem původního obrázku. Případně dojde ke zkrácení.|
|StředNaStřed|4|Střed nového obrázku bude souhlasit s středem původního obrázku. Případně dojde ke zkrácení.|
|LanczosResample|5|Převzorkování pomocí Lanczosova algoritmu s maskou 7x7.|
|NejbližšíSousedResample|6|Převzorkování pomocí algoritmu nejbližšího souseda.|
