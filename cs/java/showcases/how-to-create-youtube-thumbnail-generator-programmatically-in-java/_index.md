---
title: Jak programově vytvořit generátor náhledů YouTube thumbnail v Javě
type: docs
weight: 10
url: /cs/java/jak-programove-vytvorit-youtube-thumbnail-generator-programova-v-java/
---

## **Úvod**
Účelem tohoto dokumentu je demonstrovat použití API některých složených nástrojů z [Aspose.PSD pro Javu](https://products.aspose.com/psd/java) na reálném příkladu. V tomto článku bude napsán a objasněn **jednoduchý Java program, který generuje náhledy YouTube** pro kanál [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q). Tento kanál byl vybrán z reálného světa, protože jeho náhledy jsou dost standardní a ilustrují použití několika populárních složených nástrojů Aspose.PSD pro Javu (např. efekt [stínu](/psd/cs/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), radiální gradientní vyplnění, kreslení textu a tvarů):

![todo:image_alt_text](jak-vytvorit-thumbnail-youtube-programově-v-javě_1.png)

## **Jak to funguje v kostce**
Jednoduchý Java program přijímá jako vstup dva argumenty: popisek a obrázek. Z tohoto vstupu je **vytvořen paměťový dokument Photoshopu (PSD)** pomocí Aspose.PSD pro Javu. Poté program **převede dokument z formátu PSD na PNG** soubor, aby získal náhled YouTube o velikosti 1280x720 pixelů. Výstupní obrázek vypadá podobně jako následující:

![todo:image_alt_text](jak-vytvorit-thumbnail-youtube-programově-v-javě_2.png)

## **Technické požadavky**
Pro úspěšné spuštění kódu tohoto článku jsou vyžadovány následující technologie:

- Java 6+
- [Aspose.PSD pro Javu](/psd/cs/java/installation/) (nejnovější)

## **Začínáme**
Jak již bylo zmíněno, program využívá pro generování náhledu paměťový formát PSD. Takže začněme **vytvořením dokumentu PSD**:

```java
PsdImage psdImage = new PsdImage(1280, 720);
```

Pokud se podíváte pozorněji na výše uvedený náhled YouTube, můžete si všimnout, že **se skládá ze několika komponent**:

1. pozadí (vytisknutá maska)
2. radiální gradientní vyplnění (zdůrazňuje oblast v pravém horním rohu)
3. logotyp s efektem stínu
4. popisek a jednoduché kreslení (modrý obdélník)

Ponořme se hlouběji, jak implementovat každou z těchto komponent pomocí Aspose.PSD pro Javu v dalších sekcích.

## **1. Přidání pozadí**
Pořadí vrstev je důležité. Proto je nezbytné nejprve přidat pozadí, aby nedocházelo k překrytí jiných vrstev. Všimněte si, že v současné době jsou podporovány pouze [rastrové souborové formáty](/psd/cs/java/supported-file-formats/).

### **1.1. Přidejte pozadí do vrstvy Photoshopu**
Pro **přidání rastrového obrázku do PSD** musí být při konstrukci vrstvy předán vstupní proud (viz více [příklady načítání rastrových obrázků](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

1.2. Přizpůsobení rastrového obrázku plátnu

Následující 2 akce (změna velikosti, pozicování) jsou užitečné pro případy, kdy **velikost obrázku se liší od velikosti plátna**, ačkoli v tomto článku má obrázek stejnou velikost jako plátno (předpokládejte, že to ne vždy bude).

Ujistěte se, že načtený obrázek **zapadá** do **velikosti plátna** (viz více [příklady změny velikosti](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

Po změně velikosti je změněna i pozice obrázku. Proto, **pro resetování pozice obrázku**, přesuňte změněný obrázek do pravého horního rohu:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. Přidání radiálního gradientu**
Existují **dva způsoby přidání radiálního gradientu**, pomocí:

- efektu [nastavení přechodu](/psd/cs/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) na existující vrstvu (účinek přechodu, který je vázán na aktuální vrstvu a aplikuje se na její obsah)
- nové [vrstvy plnění přechodem](/psd/cs/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (samostatná vrstva, která uchovává samostatnou konfiguraci přechodu)

Pro tento příklad postačí použít efekt vrstvy přechodu. Nicméně, aby byl tento článek zajímavější a užitečnější, **je použita vrstva plnění přechodem**, protože všechny efekty vrstvy se aplikují podobně a další efekt vrstvy bude použit v následující sekci.

### **2.1. Přidejte vrstvu plnění radiálním gradientem**
Proces přidání nové vrstvy plnění gradientem se skládá ze dvou kroků:

1. Je **nutné deklarovat nastavení plnění gradientem**, protože nejsou k dispozici předdefinované. Minimálně vyžadovaná konfigurace vypadá následovně (znamená to, že jsou požadovány vlastnosti typu gradientu, měřítko, barva a průhlednostní body):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

Uvedená konfigurace deklaruje radiální gradient, který je na okrajích průhledný a tmavě modrý uprostřed. Poloha gradientu je ve výchozím nastavení uprostřed plátna.

Pro obrácení plnění gradientu a jemné posunutí jej na pravý horní roh použijte příslušné nepovinné vlastnosti:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

2. Jakmile je konfigurace dokončena, přidejte vrstvu plnění gradientem spolu s jejími nastaveními do PSD:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **Přidání logotypu se stínem**
**Stín** je efekt, který umožňuje přidat vlastní stín podél obrysu objektu (obrázku, textu atd.).

### **3.1. Přidejte logotyp do vrstvy Photoshopu**
Stejný přístup jako v sekci 1.1. lze použít k **přidání logotypu do PSD**:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. Pozicování logotypu**
Načtený obrázek je výchozím nastavením těsně přilepen ke levému hornímu rohu. Nicméně, je třeba přidat **okraje**, aby vypadal jako originální náhled YouTube na kanálu. Proto by měla být pozice obrázku posunuta od okrajů vrstvy:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. Přidejte efekt stínu k logotypu**
Logotyp může být neviditelný, pokud je použit světlý obrázek pozadí. Proto je žádoucí k logotypu **přidat efekt stínu** prostřednictvím vlastnosti vrstevních efektů (viz více [příklady stínování](/psd/cs/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}
```

Efekt stínu nemá požadované vlastnosti kvůli výchozí konfiguraci (vypadá jako ten v Photoshopu). Nicméně, výše uvedený stín je upraven, aby vypadal jako průhledný okraj rozostřený na okrajích.

## **4. Přidání kreslení textu a tvaru**
### **4.1. Vytvořte grafickou vrstvu**
Kreslení není podporováno přímo pomocí běžné vrstvy. Proto je vedle vrstvy použit grafický engine, aby **poskytl API pro kreslení** (viz více [příklady kreslení](/psd/cs/java/drawing-images-using-graphics/)):

```java
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **4.2. Nakreslete víceřádkový text**
Odborný čtenář se může ptát: proč nepoužít textovou vrstvu k přidání textu? No, existuje několik důvodů: úprava textu v tomto případě není nutná, protože PSD je vytvářen od základu pokaždé; přizpůsobení písma není podporováno [textovým API](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) ještě (verze 20.6 v době psaní).

Je snadné **nakreslit nějaký text s přizpůsobeným písmem** stačí jen instancovat požadované písmo a zavolat příslušnou metodu z grafického enginu. Nicméně, vytvořit obdélník (viz podrobnosti v další sekci), který automaticky mění svoji výšku na základě počtu řádků textu, je trochu náročnější. Nejprve je třeba spočítat přesnou výšku všech řádků:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}
```

Kde 1.15 je výška řádku, 3 je odsazení textu.

### **4.3. Nakreslete obdélník**
Je také snadné nakreslit obdélník i s gradientovým štětcem (stačí nastavit oblast k nakreslení a barevný rozsah). Když je známa výška textu, vypočte se velikost a pozice obdélníku. Pro **nakreslení vyplněného obdélníku** **v psd** (nejen rám) zavolejte příslušnou metodu z grafického enginu s tímto vším:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}
```

Kde 40, 15, 25 jsou odsazení.

## **Výsledek**
Takže tvarování náhledu je dokončeno. Je tedy čas **exportovat náhled do rastrového souborového formátu** (např. PNG) pro další distribuci:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
```

## **Závěr**
V tomto článku jsme vytvořili generátor náhledů YouTube pro kanál DW Documentary a vysvětlili, jak použít některé z nejpopulárnějších složených nástrojů, jako jsou efekt stínu, radiální gradientní vyplnění, kreslení textu a tvarů.

## **Celý příklad**
Můžete si [stáhnout Aspose.PSD SDK](https://products.aspose.com/psd/net)

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
``````java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
```