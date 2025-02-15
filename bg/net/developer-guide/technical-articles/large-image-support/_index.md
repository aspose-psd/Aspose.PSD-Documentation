---
title: Голяма поддръжка на изображения
type: docs
weight: 40
url: /bg/net/large-image-support/
---

## **Голяма поддръжка на изображения**
Тъй като стандартната библиотека .NET има някои ограничения по отношение на размера на изображението, което може да обработи, въведохме нов механизъм за поддръжка на големи изображения. Новият подход преодолява ограниченията, но поради ограниченията на размера на данните максималните поддържани размери за създаване и зареждане са 2 147 483 647 x 2 147 483 647 пиксела.
### **Работа с големи изображения**
Aspose.PSD предлага подобрена производителност и поддръжка за големи изображения. Изображенията, които са на стотици мегабайти в размер, вече не представляват проблем, така че можете да създавате, зареждате и рисувате върху тези изображения. Въпреки това, поради частичната обработка и обработката на изключенията OutOfMemoryException, производителността може да бъде много ниска при много големите изображения. Това е поради факта, че Aspose.PSD се опитва да преразпредели по-малко количество данни за обработка и всеки стъпка за преразпределение е много скъпа. Предимствата на новата архитектура са очевидни:

- Няма ограничение за размера на изображението.
- Не ви е забранено от паметта, налична на вашия компютър.

Ако изпитвате бавно обработване, се препоръчва да увеличите общото количество RAM, за да поберете всичките си пиксели в паметта. Ако не, обработката е възможна, но е по-бавна. Подходът е следният:

- Извикайте метода [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) с желаното правоъгълник и делегат за приемане на заредените указани пиксели.

Aspose.PSD се опитва да зареди целия правоъгълник.

- Ако има достатъчно памет, за да побере всичките пиксели, тогава всички пиксели се връщат просто към извикващия.
- Ако няма достатъчно памет, извикващият получава подмножество от пиксели от вътрешно определения правоъгълник. След като тези пиксели са обработени, извикващият получава следващия правоъгълник. Обработката приключва, когато целият правоъгълник е обработен.

Aspose.PSD се опитва да извлече колкото е възможно повече линии. Ако няма достатъчно памет, за да побере един ред пиксели, тогава един ред се разделя на части, съобразени с правоъгълници с височина 1. Можете също да рисувате върху големи изображения. Процесът на рисуване се опитва да засегне целия желан правоъгълник. Ако няма достатъчно памет, рисуването се извършва върху частични правоъгълници, докато не се нарисува цялата област. Освен това, Aspose.PSD поддържа запазването и експортирането на големи изображения. Запазването на изходното изображение на диск или експортирането му в друг файлов формат се извършва чрез частични правоъгълници, ако е необходимо. 
### **Поддържани формати на изображения**
За обработка на големи изображения се поддържат следните формати:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Гореспоменатите формати могат да се обработват безопасно чрез създаване, модифициране, прилагане на рисуване, запазване на диск или експортиране във всеки случай без значение от размера на изображението.
