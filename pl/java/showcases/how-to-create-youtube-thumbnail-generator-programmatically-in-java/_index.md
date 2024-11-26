---
title: Jak programowo stworzyć generator miniatury YouTube w języku Java
type: docs
weight: 10
url: /pl/java/jak-stworzyc-generator-miniatury-youtube-programowo-w-jezyku-java/
---

## **Wprowadzenie**
Celem tego dokumentu jest przedstawienie korzystania z interfejsu API niektórych złożonych narzędzi [Aspose.PSD dla Javy](https://products.aspose.com/psd/java) na przykładzie prawdziwego przypadku. W tym artykule będzie opisany i wyjaśniony **prosty program w języku Java, który generuje miniatury YouTube** dla kanału [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q). Ten kanał został wybrany ze świata rzeczywistego, ponieważ jego miniatury są dość standardowe i ilustrują użycie kilku popularnych złożonych narzędzi Aspose.PSD dla Javy (np. efekt [cienia](/psd/pl/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), wypełnienie gradientowe radialne, rysowanie tekstu i kształtów):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Jak to działa w skrócie**
Prosty program w języku Java przyjmuje jako wejście dwa argumenty: podpis i obraz. Z wejścia tego generowany jest **plik wewnętrzny dokumentu Photoshop (PSD)** za pomocą Aspose.PSD dla Javy. Następnie program **konwertuje dokument z PSD do formatu pliku PNG**, aby uzyskać miniaturę YouTube o rozmiarze 1280x720 pikseli. Wygenerowany obraz wygląda podobnie jak poniżej:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Wymagania techniczne**
Aby pomyślnie uruchomić kod tego artykułu, wymagane są następujące technologie:

- Java 6+
- [Aspose.PSD dla Javy](/psd/pl/java/installation/) (najnowsza wersja)

## **Rozpoczęcie**
Jak już wspomniano, program używa wewnętrznej PSD do generowania miniatury. Rozpoczniemy od **utworzenia dokumentu w formacie PSD**:

```java
PsdImage psdImage = new PsdImage(1280, 720);
```

Jeśli przyjrzysz się uważnie miniaturze YouTube powyżej, możesz zauważyć, że **składa się z kilku elementów**:

1. obrazu tła (maski drukowanej)
1. gradientu radialnego PSD (podświetla obszar w prawym górnym rogu)
1. logotypu z efektem cienia
1. podpisu i prostego rysunku (niebieski prostokąt)

Zanurzmy się głębiej, aby zobaczyć, jak zaimplementować każdy z tych elementów, korzystając z Aspose.PSD dla Javy, w kolejnych sekcjach.

## **1. Dodanie obrazu tła**
Kolejność warstw jest ważna. Dlatego obraz tła musi zostać dodany jako pierwszy, aby nie nakładać się na inne warstwy. Zwróć uwagę, że obecnie obsługiwane są tylko [formaty plików rastrowych](/psd/pl/java/supported-file-formats/).

### **1.1. Dodanie obrazu tła do warstwy Photoshopa**
Aby **dodać obraz rastrowy do PSD**, jako argument podczas tworzenia warstwy należy przekazać strumień wejściowy (zobacz więcej [przykłady ładowania obrazów rastrowych](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

1.2. Dopasuj obraz tła do kanwy

Następujące 2 działania (zmiana rozmiaru, pozycjonowanie) są przydatne w przypadkach, gdy **rozmiar obrazu różni się od rozmiaru kanwy**, chociaż obraz w tym artykule ma taki sam rozmiar jak kanwa (załóżmy, że nie zawsze będzie tak samo).

Upewnij się, że załadowany obraz **odpowiada rozmiarowi kanwy** (zobacz więcej [przykłady zmiany rozmiaru](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

Po zmianie rozmiaru obrazu zmienia się jego pozycja. Dlatego, aby **zresetować pozycję obrazu**, przenieś zmieniony obraz w lewy górny róg:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. Dodanie gradientu radialnego**
Istnieją **dwa sposoby dodania gradientu radialnego**, korzystając z:

- efektu nakładania gradientu ([gradient overlay effect](/psd/pl/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163)) na istniejącą warstwę (efekt gradientu, który łączy się z bieżącą warstwą i stosuje się do jej zawartości)
- nową [warstwę wypełnienia gradientem](/psd/pl/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (odrębną warstwę, która zachowuje samodzielnie konfigurację gradientu)

Wystarczy użyć efektu nakładania gradientu dla tego przykładu. Jednak, aby uczynić ten artykuł bardziej interesującym i użytecznym, **używana jest warstwa wypełnienia gradientem radialnym**, ponieważ wszystkie efekty warstwy są stosowane w podobny sposób, a inny efekt warstwy zostanie użyty w następnej sekcji.

### **2.1. Dodanie warstwy wypełnienia gradientem radialnym**
Proces dodania nowej warstwy wypełnienia gradientem składa się z następujących 2 kroków:

1. Konieczne jest **zadeklarowanie ustawień wypełnienia gradientowego**, ponieważ nie ma predefiniowanych. Minimalna wymagana konfiguracja wygląda następująco (oznacza to, że właściwości wymagane to typ gradientu, skala, kolor i punkty przezroczystości):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

Konfiguracja powyżej deklaruje gradient radialny, który jest transparentny na brzegach i ciemnoniebieski w centrum. Punkt gradientu znajduje się domyślnie w środku kanwy.

Aby odwrócić wypełnienie gradientu i delikatnie przesunąć go w prawy górny róg, użyj odpowiednich opcjonalnych właściwości:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

2. Gdy konfiguracja zostanie ukończona, dodaj warstwę wypełnienia gradientem wraz z jej ustawieniami do PSD:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **Dodanie logotypu z cieniem**
**Efekt cienia** to efekt, który pozwala dodać niestandardowy cień wzdłuż konturu obiektu (obraz, tekst itp.).

### **3.1. Dodanie logotypu do warstwy Photoshopa**
Można użyć tego samego podejścia co w sekcji 1.1. do **dodania logotypu do PSD**:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. Pozycjonowanie logotypu**
Załadowany obraz jest domyślnie przylegający do lewego górnego rogu. Jednakże, aby uzyskać efekt podobny do oryginalnej miniatury YouTube na kanale, należy dodać **marginesy** aby obraz wyglądał jak oryginalny. Dlatego pozycja obrazu powinna być przesunięta od krawędzi warstwy:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. Dodanie efektu cienia do logotypu**
Logotyp może być niewidoczny, jeśli używany jest jasny obraz tła. Dlatego warto **dodać efekt cienia** do logotypu za pomocą właściwości opcji mieszania (zobacz więcej [przykłady cieniowania](/psd/pl/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}
```

Efekt cienia nie ma wymaganych właściwości ze względu na domyślną konfigurację (wygląda jak w Photoshopie). Jednakże, przedstawiony cień jest zmodyfikowany tak, aby wyglądał jak przezroczysta krawędź rozmyta na brzegach.

## **4. Dodanie rysunku tekstu i kształtu**
### **3.1. Utworzenie warstwy graficznej**
Rysowanie nie jest obsługiwane bezpośrednio przez zwykłą warstwę. Dlatego obok warstwy stosowany jest silnik graficzny, aby **dostarczyć interfejs API do rysowania** (zobacz więcej [przykłady rysowania](/psd/pl/java/drawing-images-using-graphics/)):

```java
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **3.2. Narysowanie tekstu wielowierszowego**
Bywalczy czytelnik może zapytać: dlaczego nie użyć warstwy tekstowej do dodania tekstu? Cóż, jest kilka powodów: edycja tekstu nie jest wymagana w tym przypadku, ponieważ PSD jest generowany od nowa za każdym razem; personalizacja czcionki nie jest obsługiwana przez [API tekstu](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) (w wersji 20.6 w chwili pisania).

Łatwo jest **narysować tekst z dostosowaną czcionką**, wystarczy zainicjować pożądaną czcionkę i wywołać odpowiednią metodę z silnika graficznego. Jednak, aby stworzyć prostokąt (zobacz szczegóły w następnej sekcji), który zmienia swoją wysokość automatycznie w zależności od ilości linii tekstu, jest trochę trudniej. Najpierw należy obliczyć dokładną wysokość wszystkich linii:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}
```

Gdzie 1.15 to wysokość linii, a 3 to marginesy tekstu.

### **3.3. Narysowanie prostokąta**
Rysowanie prostokąta jest również proste, nawet z pędzlem gradientowym (ustaw po prostu obszar rysowania i zakres koloru). Gdy znana jest wysokość tekstu, obliczane są rozmiar i pozycja prostokąta. Aby **narysować wypełniony prostokąt** **w psd** (nie tylko rysunek obramowania), należy wywołać odpowiednią metodę z silnika graficznego z wymaganymi parametrami:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}
```

Gdzie 40, 15, 25 to wcięcia.

## **Wynik**
Tak więc, kształtowanie miniatury zostało zakończone. Dlatego nadszedł czas **wyeksportować miniaturę do formatu pliku rastrowego** (na przykład PNG) w celu dalszego rozpowszechniania:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
```

## **Podsumowanie**
W tym artykule stworzyliśmy generator miniatury YouTube dla kanału DW Documentary i wyjaśniliśmy, jak korzystać z niektórych najpopularniejszych narzędzi złożonych, takich jak efekt cienia, wypełnienie gradientowe radialne, rysowanie tekstu i kształtów.

## **Pełny przykład**
Możesz [pobrać SDK Aspose.PSD](https://products.aspose.com/psd/net)

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
```