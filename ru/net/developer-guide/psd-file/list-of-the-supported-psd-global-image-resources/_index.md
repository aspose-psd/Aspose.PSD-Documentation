---
title: Список поддерживаемых ресурсов глобальных изображений PSD
type: docs
weight: 30
url: /ru/net/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSD поддерживает низкоуровневое редактирование ресурсов изображений.**
Список полностью поддерживаемых ресурсов изображений можно найти в Aspose.PSD .Net [Справочном руководстве по API](https://reference.aspose.com/psd/net)

Согласно спецификации формата Adobe® Photoshop®: Изображения используют несколько стандартных номеров ID, как показано в Идентификаторах ресурсов изображений. Не все форматы файлов используют все ID. Некоторая информация может храниться в других разделах файла.

Для тех идентификаторов ресурсов, которые были добавлены с момента Photoshop 3.0, запись указывает версию, в которой они были введены, например (*Photoshop 6.0).*

Идентификатор ресурса изображения.

|**ID**|**Описание**|
| :- | :- |
|**Десятичный**||
|1000|*(Устарело--только в Photoshop 2.0*) Количество каналов, строк, столбцов, глубины и режима|
|1001|Запись информации о печати менеджера Macintosh|
|1002|Информация о формате страницы Macintosh. Больше не читается Photoshop. (*Устарело*)|
|1003|*(Устарело--только в Photoshop 2.0*) Таблица цветов с индексацией|
|1005|[Структура ResolutionInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource)|
|1006|Имена альфа-каналов в виде серии Pascal-строк.|
|1007|*(Устарело) См. ID 1077 структуру DisplayInfo*.|
|1008|Подпись в виде Pascal-строки.|
|1009|[Информация о границах.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) Содержит фиксированное число (2 байта на реальное, 2 байта на дробное) для ширины границы и 2 байта для единиц границы (1 = дюймы, 2 = см, 3 = пункты, 4 = пики, 5 = колонки)|
|1010|[Фоновый цвет.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Флаги печати. Серия однобайтных булевых значений: метки, обрезные метки, цветные бруски, регистрационные метки, отрицательный, перевернутый, интерполированный, подпись, флаги печати.|
|1012|Информация о полутоновании в оттенках серого и многоканальном режиме|
|1013|[Информация о полутоновании в цвете](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Информация о дуотоновом полутоне|
|1015|Функция переноса в оттенках серого и многоканальном режиме|
|1016|[Функции переноса цвета](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Функции переноса дуотон|
|1018|Информация об изображении дуотон|
|1019|Два байта для эффективных чёрных и белых значений для диапазона точек|
|1020|*(Устарело)*|
|1021|Параметры EPS|
|1022|[Информация о Quick Mask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). Идентификатор канала Quick Mask; 1-байтовый булевый индикатор, указывающий, была ли маска изначально пустой.|
|1023|*(Устарело)*|
|1024|[Информация о состоянии слоя](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Рабочий путь (не сохранён). Формат ресурса пути.|
|1026|[Информация о группах слоев](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 байта на каждый слой, содержащие идентификатор группы для групп перетаскивания. Слои в группе имеют тот же идентификатор группы.|
|1027|*(Устарело)*|
|1028|Запись IPTC-NAA. Содержит информацию *File Info...*.|
|1029|Режим изображения для файлов сырого формата|
|1030|Качество JPEG. Частное.|
|1032|*(Photoshop 4.0) [Информация о сетке и направляющих.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Ресурс миниатюры](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* только|
|1034|*(Photoshop 4.0)* Флаг авторского права. Булево значение, указывающее, защищено ли изображение авторским правом.|
|1035|*(Photoshop 4.0)* URL. Хэндл текстовой строки с единым адресом ресурса.*.*|
|1036|*(Photoshop 5.0) [Ресурс миниатюры](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (заменяет ресурс 1033).|
|1037|*(Photoshop 5.0) [Глобальный угол](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 байта, содержащие целое число от 0 до 359, который является глобальным углом освещения для слоя эффектов. Если отсутствует, предполагается, что это 30.|
|1038|*(Устарело) См. ID 1073 ниже. (Photoshop 5.0)* Ресурсы сэмплеров цвета.|
|1039|*(Photoshop 5.0) [ICC Профиль](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Сырые байты профиля формата ICC (Международного консорциума цвета).*  |
|1040|*(Photoshop 5.0) [Водяной знак](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [ICC Непомеченный профиль](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 байт, который отключает любую предполагаемую обработку профиля при открытии файла. 1 = намеренно без метки.|
|1042|*(Photoshop 5.0)* Видимость эффектов. Глобальный флаг в 1 байт для показа/скрытия всех слоёв эффектов. Присутствует только, когда они скрыты.|
|1043|*(Photoshop 5.0)* Пятно от полутонов. 4 байта для версии, 4 байта для длины и переменные данные длины.|
|1044|*(Photoshop 5.0)[Идентификаторы специфические для документа](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)*. Начальное значение base value, с которого будут генерироваться идентификаторы слоя (или более крупное значение, если существующие идентификаторы уже его превышают). Его цель - избежать ситуации, когда мы добавляем слои, выравниваем, сохраняем, открываем и затем добавляем еще слои, которые окажутся с теми же идентификаторами, что и первый набор.|
|1045|*(Photoshop 5.0) [Unicode имена альфа](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Количество цветов в индексированной таблице цветов. 2 байта для числа определенных цветов|
|1047|*(Photoshop 6.0)* [Индекс прозрачности](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Общая высота.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Срезы.|
|1051|*(Photoshop 6.0)* URL рабочего процесса.|
|1052|*(Photoshop 6.0)* Переход к XPEP. 2 байта для главной версии, 2 байта для дополнительной версии, 4 байта для числа. Далее следуют повторы для числа: 4 байта для размера блока, 4 байта для ключа, если ключ = *'jtDd'* , то далее - булево значение для флага грязности; в противном случае это 4-байтовая запись для даты модификации.|
|1053|*(Photoshop 6.0)* Идентификаторы альфа.|
|1054|*(Photoshop 6.0)[Список URL](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* [Информация о версии](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource).|
|1058|*(Photoshop 7.0)* Данные EXIF 1.|
|1059|*(Photoshop 7.0)* Данные EXIF 3*.*|
|1060|*(Photoshop 7.0)* [Метаданные XMP](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Информация о файле в виде XML-описания.|
|1061|*(Photoshop 7.0)[Caption digest](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 байт: алгоритм хэширования сообщений RSA Data Security, MD5|
|1062|*(Photoshop 7.0)[Масштаб печати](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = по центру, 1 = размер по размеру, 2 = пользовательский определенный). 4 байта x расположение (с плавающей запятой). 4 байта y расположение (с плавающей запятой). 4 байта масштаб (с плавающей запятой)|
|1064|*(Photoshop CS)* [Соотношение сторон пикселя](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Композиции слоёв.|
|1066|*(Photoshop CS)* Альтернативные цвета дуотона. Этот ресурс не читается или не используется Photoshop.|
|1067|*(Photoshop CS)* Альтернативные пятновые цвета. Этот ресурс не читается или не используется Photoshop.|
|1069|*(Photoshop CS2)* Идентификатор(ы) выбранного слоя. 2 байта счетчика, далее повторяется для каждого счетчика: 4 байта идентификатора слоя|
|1070|*(Photoshop CS2)* Информация о тонах HDR|
|1071|*(Photoshop CS2)* Информация о печати|
|1072|*(Photoshop CS2)* [Включенные идентификаторы слоя групп](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 байт для каждого слоя в документе, повторяется по длине ресурса. ЗАМЕЧАНИЕ: Группы слоев имеют маркеры начала и конца|
|1073|*(Photoshop CS3)* Ресурсы сэмплеров цвета. См. также ID 1038 для старого формата.|
|1074|*(Photoshop CS3)* Шкала измерений.|
|1075|*(Photoshop CS3)* Информация о временной шкале.|
|1076|*(Photoshop CS3)* Раскрытие листа.|
|1077|*(Photoshop CS3) Структура DisplayInfo* для поддержки чисел с плавающей точкой *. См. также ID 1007.|
|1078|*(Photoshop CS3)* Луковые кожи.|
|1080|*(Photoshop CS4)* Информация о счетчике.|
|1082|*(Photoshop CS5)* Информация о печати.|
|1083|*(Photoshop CS5)* Стиль печати. Печать меток, метки, украшения и т. д.|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo. переменная ОС-специфическая информация для Macintosh.|
|1085|*(Photoshop CS5)* Windows DEVMODE. переменная ОС-специфическая информация для Windows.|
|1086|*(Photoshop CS6)* Путь к файлу автосохранения.|
|1087|*(Photoshop CS6)* Формат автосохранения. |
|1088|*(Photoshop CC)* Состояние выбора пути.|
|2000-2997|Информация о пути (сохраненные пути).|
|2999|Имя обрезного пути.|
|3000|*(Photoshop CC)* Информация о начальном пути|
|4000-4999|Ресурс(ы) плагина. Ресурсы, добавленные