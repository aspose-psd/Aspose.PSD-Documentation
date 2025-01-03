---
title: Създаване, Отваряне и Запазване на Изображения
type: docs
weight: 30
url: /bg/java/creating-opening-and-saving-images/
---

## **Създаване на Изображения**
Aspose.PSD за Java позволява на разработчиците да създават свои собствени изображения. Използвайте статичния метод Create, който е изложен от класа Image, за да създадете нови изображения. Всичко, което трябва да направите, е да предоставите подходящ обект от един от класовете от пространството на имена ImageOptions за желания формат на изходното изображение. За да създадете файл с изображение, първо създайте инстанция на един от класовете от пространството на имена ImageOptions. Тези класове определят формата на изходното изображение. По-долу са избрани някои класове от пространството на имена ImageOptions (забележете, че в момента се поддържат само семействата от файлови формати на PSD):

PsdOptions задава опциите за създаване на файл PSD. Изображенията могат да бъдат създадени с настройка на пътя за изход или чрез задаване на поток.
### **Създаване чрез Задаване на Път**
Създайте PsdOptions от пространството на имена ImageOptions и задайте различните свойства. Най-важното свойство за задаване е Source свойството. Това свойство посочва къде се намира информацията за изображението (във файл или поток). В примера по-долу източникът е файл. След задаване на свойствата, предайте обекта на един от статичните методи Create заедно с параметър за широчина и височина. Широчината и височината се определят в пиксели.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Създаване с Използване на Поток**
Процедурата за създаване на изображение с използване на поток е същата като при използване на пътя. Единствената разлика е, че трябва да създадете инстанция на StreamSource, като предадете обект Stream на конструктора му и го зададете като свойство на Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Отваряне на Изображения**
Разработчиците могат да използват Aspose.PSD за Java API, за да отворят съществуващи файлове с изображения във формат PSD за различни цели, като добавяне на ефекти към изображението или конвертиране на съществуващ файл в друг формат. Независимо от целта, Aspose.PSD предоставя два стандартни начина за отваряне на съществуващи файлове: чрез файл или чрез поток.
### **Отваряне от Диск**
Отворете файл с изображение, като предадете пътя и името на файла като параметър на статичния метод Load, който е изложен от класа Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Отваряне с Използване на Поток**
Понякога изображението, което трябва да отворите, се съхранява като поток. В такива случаи използвайте претоварената версия на метода Load. Той приема обект Stream като аргумент, за да отвори изображението.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Зареждане на изображение като слой**
Тази статия демонстрира използването на Aspose.PSD за зареждане на изображение като слой. Aspose.PSD API-тата изложиха ефикасни и лесни за използване методи за постигане на тази цел. Aspose.PSD е изложил метода AddLayer на класа PsdImage, за да добави изображение като слой във файл PSD.

Стъпките за зареждане на изображение във PSD като слой са толкова прости, както по-долу:

- Създайте инстанция на изображение с класа PsdImage с определени широчина и височина.
- Заредете файл PSD като изображение с помощта на фабричния метод Load, който е изложен от Image класа.
- Създайте инстанция на класа Layer и присвоете слоя на PSD изображението на него.
- Добавете създадения слой, като използвате метода AddLayer, изложен от PsdImage класа.
- Запазете резултатите.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Запазване на изображения**
Aspose.PSD ви позволява да създавате файлове с изображения от нулата. Той също така предоставя средства за редактиране на съществуващи файлове с изображения. След като изображението е създадено или променено, обикновено файлът се запазва на диск. Aspose.PSD ви предоставя методи за запазване на изображения на диск, като посочите път или използвате обект Stream.
### **Запазване на Диск**
Класът Image представя обект с изображение, така че този клас предоставя всички необходими инструменти за създаване, зареждане и запазване на файл с изображение. Използвайте метода Save на класа Image, за да запазите изображения. Една претоварена версия на метода Save приема местоположението на файла като низ.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Запазване в Поток**
Друга претоварена версия на метода Save приема обект Stream като аргумент и запазва файлът с изображението в потока.

Ако изображението е създадено, като са посочени някакви от CreateOptions в конструктора на Image, то изображението автоматично се запазва на пътя или потока, предоставени по време на инициализацията на класа Image, като се извика методът Save, който не приема параметър.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Задаване за Заместване на Липсващи Шрифтове**
Разработчиците могат да използват Aspose.PSD за Java API, за да зареждат съществуващи файлове с изображения във формат PSD за различни цели, например за задаване на име на шрифт по подразбиране при запазване на PSD документи като растерно изображение (в PNG, JPG и BMP формати). Този шрифт по подразбиране трябва да се използва за замяна на всички липсващи шрифтове (шрифтове, които не се намират в текущата операционна система). След като изображението е променено, файла ще бъде запазен на диск.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}
