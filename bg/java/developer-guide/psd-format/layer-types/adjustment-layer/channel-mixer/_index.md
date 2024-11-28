---
title: Слой за настройка на канален миксер
type: docs
weight: 30
url: /bg/java/layer-types/adjustment-layer/channel-mixer/
---

# Работа със слоя за настройка на канален миксер в Photoshop в Java

Днес ще разгледаме как да смесваме цветовете на каналите в документи на Photoshop по програмен начин в Java. Понеже редакторът на Photoshop не поддържа скриптове на Java, ще използваме специална библиотека за манипулиране на формата на PSD файлове, наречена Aspose.PSD за Java.

Библиотеката съдържа **API за работа с цветовите канали**. Има няколко начина за смесване на цветовете, но в тази статия ще се съсредоточим върху слоя за настройка на канален миксер.

API-то на слоя за настройка на канален миксер **позволява да се играе с цветовите канали** за създаване на изображения с различни креативни цветови ефекти или дори за преобразуване на изображението в черно-бяло. След това ще разгледаме как да приложим слоя за настройка на канален миксер към съществуващ документ на Photoshop с помощта на Aspose.PSD за Java, но първо трябва да говорим за общите характеристики на API.

## Преглед на API-то

Няма нищо специално в създаването на слой за настройка на канален миксер. Той може да бъде добавен чрез [фабричния метод по подразбиране](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--), който връща инстанция на класа ChannelMixerLayer. Този клас съдържа общи функции като опцията за монохромен цвят и метод за получаване на изходен канал. Конкретният изходен канал може да бъде от два типа: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) или [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Типът на [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) зависи от [режима на цветовете](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) на изображението.

## Направете изображението монохромно

Сега да разгледаме пример за прилагане на слоя за настройка на канален миксер към съществуващ документ на Photoshop. Понеже този вид слой за настройка все още не поддържа предварително зададени опции, ние ще **възсъздадем настройката на Photoshop за черно и бяло инфрачервено (RGB)** (а). Тази настройка ще бъде приложена към изображението на цъфтящо дърво (b). Като резултат, искаме да постигнем ефекта на инфрачервена фотография (c).

![Пример за слой за настройка на канален миксер](channel-mixer-adjustment-psd-layer-figure-1.png) Първо, за да възсъздадем настройката на Photoshop за черно и бяло инфрачервено е необходимо да активираме флага за монохромен цвят и да зададем подходящи стойности за всеки цвят (червен, зелен и син) за изходния Gray канал:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

Изображението трябва да бъде в цветовия режим RGB, за да работи кодът (заради преобразуването към класа RgbMixerChannel). Също така, CMYK цветовият режим се поддържа, но само за изображения със съответния цветови режим.

Имайте предвид, че стойността на всеки цвят, както и константното свойство трябва да бъдат в интервала от -200 до 200.

## Заключение

В тази статия разгледахме как да работим с API на каналния миксер на Aspose.PSD за Java, за да променим цветовете в цветовите канали, както и да конвертираме изображението в черно-бяло.
