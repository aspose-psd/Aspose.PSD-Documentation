---
title: Промяна на изображения
type: docs
weight: 50
url: /bg/net/modifying-images/
---

## **Dithering за растерни изображения**
Дитърингът е техника за създаване на илюзия за нови цветове и нюанси, като варира модела на точките, които наистина създават изображение. Това е най-честният начин за намаляване на цветовия обхват на изображенията до 256 (или по-малко) цвята. Aspose.PSD предоставя поддръжка на дитъринг за класа [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), като въвежда метода Dither, който приема два параметъра. Първият е от тип DitheringMethod, който да се приложи, с две възможни опции FloydSteinbergDithering и ThresholdDithering. Вторият параметър на метода [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) е BitCount в цяло число. BitCount дефинира размера на пробата за резултата от дитъринга. Стойността по подразбиране е 1, която представлява черно и бяло, докато позволените стойности са 1, 4, 8, генериращи палитри съответно от 2, 4 и 256 цвята.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}

## **Регулиране на яркостта, контраста и гамата**
Корекциите на цветовете в цифровите изображения са една от основните функции, които повечето библиотеки за обработка на изображения предоставят. Корекциите на цветовете могат да бъдат категоризирани по следния начин.

1. Яркостта се отнася до светлостта или тъмнотата на цвета. Увеличаването на яркостта на изображение оразглежда всички цветове, докато намаляването на яркостта затъмнява всички цветове.
1. Контрастът се отнася до правенето на обектите или детайлите в изображението по-очевидни. Увеличаването на контраста на изображението увеличава разликата между светлината и тъмните области, така че светлите области стават по-светли, а тъмните области стават по-тъмни. Намаляването на контраста ще запази светли и тъмни области приблизително същите, но цялото изображение става по-еднородно.
1. Гамата оптимизира контраста и яркостта на непосредствената светлина, която осветява обект в изображението.
## **Регулиране на яркостта**
Aspose.PSD за .NET API предоставя метода [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) за класа [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), който може да се използва за регулиране на яркостта на изображението, като се подаде цяло число като параметър. Най-високата стойност на параметъра означава по-светло изображение. Тук е оригиналното изображение и резултатното изображение за сравнение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}

## **Регулиране на контраста**
Методът [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast), изложен от класа [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), може да се използва за регулиране на контраста на изображение, като се подаде плаващо число като параметър.

Най-високата стойност на параметъра означава по-висок контраст в даденото изображение. Тук е оригиналното изображение и резултатното изображение за сравнение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}

## **Регулиране на гама**
Методът [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma), изложен от класа [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), има две версии. Едната от претоварените версии приема едно плаващо число и извършва корекция на гамата за коефициентите на червен, син и зелен канал. Докато другата претовареност приема три плаващи параметъра, представляващи всеки цвят коефициент поотделно. Следният пример на код демонстрира как да се регулира гамата на изображение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}

## **Размазване на изображение**
Тази статия демонстрира използването на Aspose.PSD за .NET за извършване на размазващ ефект върху изображение. Aspose.PSD APIs са изложили ефективни и лесни за използване методи за постигане на тази цел. Aspose.PSD за .NET е изложило класа [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions), за да се създаде размазващ ефект на живо. Класът [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) изисква стойности на радиуса и сигмата, за да създаде размазващ ефект върху изображението. Стъпките за извършване на преоразмеряване са толкова прости, както следва:

1. Заредете изображение чрез метода на фабриката Load, изложен от класа Image.
1. Преобразувайте изображението в [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Създайте екземпляр на класа [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) с конструктора по подразбиране или предоставете радиус и стойности на сигмата в конструктора.
1. Извикайте метода Filter на [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), като посочите правоъгълника като граници на изображението и екземпляра на класа [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd/imagefilters/filteroptions/gaussianblurfilteroptions).
1. Запазете резултатите.

Следният пример на код демонстрира как да се създаде размазващ ефект върху изображение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}

## **Проверка на прозрачността на изображението**
Тази статия демонстрира използването на Aspose.PSD за .NET за проверка на прозрачността на изображение. Стъпките за проверка на прозрачността на изображението са толкова прости, както следва:

1. Заредете изображение чрез метода на фабриката [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2), изложен от класа [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Проверете прозрачността на изображението, ако прозрачността е нула, изображението е прозрачно.
Следният пример на код демонстрира как да се провери дали изображението е прозрачно.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}

## **Използване на компресор за загуби в GIF формат**
С помощта на Aspose.PSD за .NET разработчиците могат да задават разлика в пикселите. Компресията на GIF се основава на "речник" от низове от пиксели. Нормалният кодер търси в речника най-дългия низ от пиксели, които точно съвпадат с пикселите в изображението. Кодерът за загуба избира най-дългия низ от пиксели, които са "достатъчно подобни" на пикселите в изображението. По-долу е кодовата демонстрация на посочената функционалност.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}

## **Изпълнение на бикубичен ресеймпър**
Ресеймпълването означава, че променяте пикселните размери на изображение. Когато намалявате, елиминирате пикселите и следователно изтривате информация и детайли от изображението си. Когато увеличавате, добавяте пиксели. Photoshop добавя тези пиксели, като използва интерполация. Тази статия демонстрира как можете да извършите бикубично ресеймпване, като използвате Aspose.PSD за .NET.

По-долу е кодовата демонстрация на посочената функционалност.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}

## **Слой за регулиране на баланса на цветовете**
Тази статия демонстрира използването на Aspose.PSD за .NET за извършване на **Слой за регулиране на баланса на цветовете** върху изображение. Слоят за регулиране на баланса на цветовете ви дава възможност да направите настройки на цветовете на своите изображения. Той представя трите цветни канала и техните съплементарни цветове и можете да регулирате баланса на тези двойки, за да промените външния вид на снимка.

По-долу е кодовата демонстрация на посочената функционалност.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}

## **Слой за обръщане на цветовете**
Тази статия демонстрира как можете да използвате **Слой за обръщане на цветовете** с помощта на Aspose.PSD за .NET. Слой за регулиране е специален вид слой, използван основно за цветна корекция. Вместо да има собствено съдържание, те регулират информацията на слоевете под тях. Слоят за обръщане прави фотография с негативен ефект, като обръща цветовете на изображението.

По-долу е кодовата демонстрация на посочената функционалност.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}