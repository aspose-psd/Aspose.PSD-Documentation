---
title: Използване на PSD файлове като шаблони за автоматизация - Случай с визитни картички
type: docs
weight: 10
url: /bg/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **Преглед**
Тази статия описва често срещани случаи, когато трябва да актуализирате някои слоеве в [PSD файл](https://wiki.fileformat.com/image/psd/) програмно, където PSD/PSB файла има известна структура подобна на шаблон. Това може да се използва за създаване на голямо количество визитни картички за различни хора (Случай с визитни картички) или за превеждане на PSD файла на различни езици с замяна на някои графични материали в него.

След като прочетете тази статия, ще знаете как можете да направите това:

![todo:текст_на_изображението](using-psd-files-as-templates-for-automation-business-cards-case_1.png)

## **Прост случай**
Например, имате PSD шаблон с познати имена на слоеве. Така че имате нужда да промените, актуализирате или замените PSD слой чрез C#. Първоначално трябва да отворите шаблонния файл с Aspose.PSD.

Как да отворите PSD файл чрез C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:текст_на_изображението](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

След това трябва да намерим слой, който искаме да заместим по неговото име. Ето една проста имплементация за това.

Как да намерите слоя в PSD файла по неговото име

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}

Когато слоят бъде намерен, можем да го актуализираме по обичаен начин, използвайки [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Как да рисувате върху графиката на PSD слоя

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

В този случай рисуваме ново заредено [PNG изображение](https://wiki.fileformat.com/image/png/) върху съществуващия PSD слой, така че старите данни ще бъдат загубени в новия файл.

Но какво ако също така трябва да актуализирате текста? Процесът ще бъде подобен. Намираме [Текстов слой](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) по неговото име, след което програмно [актуализираме Текстов слой на Photoshop файл](/psd/bg/net/render-text-with-different-colors-in-text-layer/) чрез C#.

Как да актуализирате Текстов слой в Photoshop с помощта на C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}

В края ще трябва да запазим промените си:

Как да запазите променения PSD файл чрез [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}

Полученият образ:

![todo:текст_на_изображението](using-psd-files-as-templates-for-automation-business-cards-case_3.png)

## **Сложен случай с допълнителни функции**
Показваме най-простия начин за замяна на изображение в слой на PSD файл.

Но Aspose.PSD може да предложи по-сложни допълнителни функции като добавяне на нов слой, премахване на стари слоеве и актуализиране на текстов слой с различни стилове в текст с множество редове.

Можем да намерим [Слой](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer), който искаме да заместим, след това да намерим неговия индекс в Списъка със слоеве, да го премахнем и вмъкнем нов слой след създаването му от [Jpeg файл](https://wiki.fileformat.com/image/jpeg/) на същото място.

Създайте нов слой от файл и го вметнете в PSD изображение с помощта на [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}

В края на този файл с кодов фрагмент, коригираме позицията на слоя и запазваме новия масив от слоеве на PSD изображението.

Как да копирате свойствата на слоя на [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}

И след всичко това, трябва да актуализираме текстовите слоеве в съществуващото PSD изображение с помощта на C#. Aspose.PSD поддържа [актуализирането на Текстов слой чрез Порции](/psd/bg/net/working-with-text-layers/). Всяка [текстова порция](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) има уникална комбинация от Стил и Параграфни свойства.

Как да копирате свойствата на слоя на [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}

Като резултат, променихме PSD шаблона чрез код с нов слой от Jpeg, Png, J2k, Bmp, Gif или Tiff файл и многоредов [текст с различни стилове](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) във всяка редица.

![todo:текст_на_изображението](using-psd-files-as-templates-for-automation-business-cards-case_4.png)