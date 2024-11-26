---
title: Korzystanie z plików PSD jako szablonów do automatyzacji - Przypadek wizytówek
type: docs
weight: 10
url: /pl/korzystanie-z-plików-psd-jako-szablonów-do-automatyzacji-przypadek-wizytówek/
---

### **Przegląd**
Ten artykuł opisuje często stosowane przypadki, gdy konieczne jest aktualizowanie niektórych warstw w [pliku PSD](https://wiki.fileformat.com/image/psd/) programowo, gdzie plik PSD/PSB ma strukturę przypominającą szablon. Można to wykorzystać do tworzenia dużej ilości wizytówek dla różnych osób (Przypadek wizytówek). Lub gdy musisz przetłumaczyć plik PSD na różne języki z zamianą pewnych materiałów graficznych w nim.

Po przeczytaniu tego artykułu dowiesz się, jak to zrobić:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **Prosty przypadek**
Na przykład masz szablon PSD z znanymi nazwami warstw. Potrzebujesz więc zmienić, zaktualizować lub zamienić warstwę PSD za pomocą C#. Na początek musisz otworzyć plik szablonu za pomocą Aspose.PSD.

Jak otworzyć plik PSD za pomocą C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Następnie musimy znaleźć warstwę, którą chcemy zastąpić za jej nazwą. Oto prosty sposób implementacji tego.

Jak znaleźć warstwę w pliku PSD po jej nazwie

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}

Gdy znajdziemy warstwę, możemy ją zaktualizować w standardowy sposób, korzystając z [Grafiki](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Jak rysować na warstwie PSD Grafiki

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

W tym konkretnym przypadku rysujemy nowo załadowany [obraz PNG](https://wiki.fileformat.com/image/png/) na istniejącej warstwie PSD, dzięki czemu stare dane zostaną utracone w nowym pliku.

Ale co jeśli musimy także zaktualizować tekst? Proces będzie podobny. Znajdź [Warstwę Tekstu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) po jej nazwie, a następnie dokonaj programowej [aktualizacji Warstwy Tekstu w pliku Photoshopa](/psd/pl/net/render-text-with-different-colors-in-text-layer/) za pomocą C#.

Jak zaktualizować Warstwę Tekstu w Photoshopie za pomocą C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}

Na końcu musimy zapisać nasze zmiany:

Jak zapisać zmieniony plik PSD za pomocą [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}

Otrzymany obrazek:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **Skomplikowany przypadek z dodatkowymi funkcjami**
Powyżej pokazaliśmy najprostszy sposób zastąpienia obrazka w warstwie pliku PSD.

Ale Aspose.PSD może zaoferować bardziej złożone dodatkowe funkcje, takie jak dodawanie nowej warstwy, usuwanie starych warstw oraz aktualizacja warstwy tekstu z wykorzystaniem różnych stylów w tekście wieloliniowym.

Możemy znaleźć [Warstwę](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer), którą chcemy zastąpić, następnie znajdujemy jej indeks na liście Warstw, usuwamy ją i wstawiamy nową warstwę po jej stworzeniu z [Pliku Jpeg](https://wiki.fileformat.com/image/jpeg/) w to samo miejsce.

Utwórz nową warstwę z pliku i wstaw ją do obrazu PSD za pomocą [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}

Na końcu tego pliku ze snipetem kodu poprawiamy pozycję warstwy i zapisujemy nową tablicę warstw w obrazie PSD.

Jak skopiować właściwości warstwy [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}

I na koniec, musimy zaktualizować warstwy tekstowe w istniejącym obrazie PSD za pomocą C#. Aspose.PSD obsługuje [aktualizację Warstwy Tekstu po Częściach](/psd/pl/net/working-with-text-layers/). Każda [część tekstu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) ma unikalną kombinację stylu i właściwości akapitu.

Jak skopiować właściwości warstwy [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}

W rezultacie, zmieniliśmy szablon PSD za pomocą kodu, dodając nową warstwę z pliku Jpeg, Png, J2k, Bmp, Gif lub Tiff oraz wieloliniowy [tekst z różnymi stylami](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) w każdym wierszu.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
