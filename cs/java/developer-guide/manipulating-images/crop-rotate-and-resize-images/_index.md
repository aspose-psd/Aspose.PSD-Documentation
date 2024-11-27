---
title: Ořezávání, Otočení a Změna Velikosti Obrázků
type: docs
weight: 40
url: /cs/java/ořezávání-otočení-a-změna-velikosti-obrázků/
---

## **Ořezávání Obrázků**
Ořezávání obrázků obvykle znamená odstranění vnějších částí obrázku k zlepšení rámečku. Ořezávání může být také použito k vystřižení určité části obrázku a zvýraznění konkrétní oblasti. Aspose.PSD API podporuje dva různé přístupy k ořezávání obrázků: pomocí posunů a obdélníku.
### **Ořezávání podle Posunů**
Třída RasterImage poskytuje přetíženou verzi metody Crop, která přijímá 4 celočíselné hodnoty označující Levý, Pravý, Horní a Dolní okraj. Na základě těchto čtyř hodnot metoda Crop posune hranice obrázku směrem k jeho středu a zahodí vnější část. Následující ukázka kódu ukazuje, jak oříznout obrázek pomocí posunů.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
```
### **Ořezávání Obdélníkem**
Třída RasterImage poskytuje další přetíženou verzi metody Crop, která přijímá instanci třídy Rectangle. Můžete vystřihnout libovolnou část obrázku poskytnutím požadovaných hranic objektu Rectangle. Následující ukázka kódu ukazuje, jak oříznout libovolný obrázek obdélníkem.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
```

## **Otočení a Překlopení Obrázku**
Aspose.PSD pro Java je snadno použitelná knihovna, protože poskytuje jednoduché metody k provádění složitých operací. Například Aspose.PSD pro Java poskytuje metodu RotateFlip pro svou základní třídu Image, pokud aplikace vyžaduje otočení obrázku. Bez ohledu na formát obrázku může knihovna provést konkrétní postup Rotate & Flip.

### **Otočení Obrázku**
Metodu Image.RotateFlip lze použít k otáčení obrázku o 90/180/270 stupňů a k překlopení obrázku horizontálně nebo vertikálně. Metoda Image.RotateFlip přijímá parametr RotateFlipType, který určuje typ rotace a překlopení, které se mají na obrázek aplikovat. Kroky k provedení Otočení a Překlopení jsou následující:

1. Načtení obrázku pomocí tovární metody Load vystavenou třídou Image.
1. Volání metody Image.RotateFlip s určením vhodného RotateFlipType.
1. Uložení výsledků.

Následující příklad kódu ukazuje, jak nastavit vlastnost RotateFlip obrázku a enumeraci RotateFlipType.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
```

## **Otočení Obrázku Podle Specifického Úhlu**
Aspose.PSD pro Java API poskytuje metodu RasterImage.Rotate, která usnadňuje uživatelům otočení obrázku podle konkrétního úhlu. Na rozdíl od metody RasterImage.RotateFlip přijímá metoda RasterImage.Rotate tři parametry:

1. Úhel otočení: Parametr typu float, který určuje úhel otočení, podle kterého má být obrázek otočen. Kladná hodnota otočí obrázek ve směru hodinových ručiček; záporná hodnota provede otočení obrázku proti směru hodinových ručiček.
1. Zachování příměru: Parametr typu Boolean určuje, zda má být velikost obrázku změněna podle projekcí otočeného obdélníku (rohové body). Pokud je nastaveno na false, rozměry obrázku zůstanou nezměněny a otočeny budou pouze vnitřní obsahy obrázku.
1. Pozadí barvy: Parametr typu Barva určuje barvu, kterou má být vyplněno pozadí otočeného obrázku.

Následující ukázka kódu ukazuje použití metody RasterImage.Rotate.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
```

## **Změna Velikosti Obrázků**
Tento článek demonstuje použití Aspose.PSD pro Java k provedení operace Resize na obrázku. API Aspose.PSD poskytuje efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD pro Java poskytuje metodu Resize pro třídu Image, kterou lze použít k změně velikosti existujících obrázků „na letu“. Existuje dvě verze přetížení metody Resize, které vyhovují potřebám aplikace.
### **Jednoduchá Změna Velikosti**
Kroky pro provedení změny velikosti jsou následující:

1. Načtení obrázku pomocí tovární metody Load vystavenou třídou Image.
1. Volání metody Image.Resize s určením nové Výšky a Šířky.
1. Uložení výsledků.

Následující ukázka kódu ukazuje, jak změnit velikost obrázku.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
```

### **Změna Velikosti s Enumerací ResizeType**
Aspose.PSD API zavedla enumeraci ResizeType, která lze použít s metodou Image.Resize k dosažení požadovaných výsledků. Níže uvedená ukázka kódu ukazuje použití enumerace ResizeType, zatímco podrobnosti o prvcích enumerace ResizeType lze najít na konci této stránky.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}
```

Pokud si přejete získat kvalitní výsledek po použití změny velikosti, doporučuje se vždy použít ResizeType.LanczosResample, protože poskytne velmi kvalitní výsledky, ale může pracovat pomaleji než ResizeType.NearestNeighbourResample. Na druhou stranu algoritmus ResizeType.NearestNeighbourResample je speciálně používán pro rychlou změnu velikosti s kompromisem na kvalitu obrázku. Tato metoda může být užitečná pro generování náhledů v reálném čase nebo podobné procesy, kde je vyžadována výkonová rychlost.

## **Změna Velikosti Obrázku Proportionalně**
Můžete změnit velikost obrázků předáním nových hodnot výšky a šířky jako parametrů metody Image.Resize, ale v tomto případě si musíte spočítat poměr stran sami. To je způsobeno tím, že když je změněna šířka nebo výška obrázku, obrázek se buď změní nebo smrští, aby vyplnil novou velikost. Pokud změny šířky a výšky obrázku nejsou v poměru, může to vést k mazání a deformovanému výsledku. Tento článek demonstruje použití Aspose.PSD pro Java API k změně velikosti obrázků předáním nové výšky nebo šířky a umožnění API automaticky spočítat druhou proporcionální hodnotu.

```cs
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
```

### **Enumerace ResizeType**
ResizeType určuje typ změny velikosti, který se má provést na obrázku podle vybraného filtru.

Členové Enumerace ResizeType

|**Název Člena**|**Hodnota**|**Popis**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Levý horní bod nového obrázku bude spadat s levým horním bodem původního obrázku. Pokud je požadováno, dojde k oříznutí.|
|RightTopToRightTop|1|Pravý horní bod nového obrázku bude spadat s pravým horním bodem původního obrázku. Pokud je požadováno, dojde k oříznutí.|
|RightBottomToRightBottom|2|Pravý spodní bod nového obrázku bude spadat s pravým spodním bodem původního obrázku. Pokud je požadováno, dojde k oříznutí.|
|LeftBottomToLeftBottom|3|Levý spodní bod nového obrázku bude spadat s levým spodním bodem původního obrázku. Pokud je požadováno, dojde k oříznutí.|
|CenterToCenter|4|Střed nového obrázku bude spadat s centrem původního obrázku. Pokud je požadováno, dojde k oříznutí.|
|LanczosResample|5|Převzorkování pomocí Lanczosova algoritmu s maskou 7x7.|
|NearestNeighbourResample|6|Převzorkování pomocí algoritmu nejbližšího souseda.|

