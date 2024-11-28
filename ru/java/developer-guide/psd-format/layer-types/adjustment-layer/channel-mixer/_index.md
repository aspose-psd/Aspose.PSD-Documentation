---
title: Регулировка слоя микшера каналов
type: docs
weight: 30
url: /ru/java/layer-types/adjustment-layer/channel-mixer/
---

# Работа с регулятором слоя микшера каналов Photoshop в Java

Сегодня мы рассмотрим, как программно смешивать цветовые каналы в документах Photoshop с помощью Java. Поскольку редактор Photoshop не поддерживает сценарии Java, мы будем использовать специальную библиотеку манипуляции форматом файла PSD, называемую Aspose.PSD для Java.

В библиотеке есть **API для работы с цветовыми каналами**. Существует несколько способов смешивания цветов, но, в этой статье, мы сосредоточимся на регуляторе слоя микшера каналов.

API регулятора слоя микшера каналов **позволяет играть с цветовыми каналами** для создания насыщенных изображений, создания различных творческих цветовых эффектов или даже преобразования изображения в черно-белое. Далее мы рассмотрим, как применить регулятор слоя микшера каналов к существующему документу Photoshop с помощью Aspose.PSD для Java, но сначала нам нужно поговорить о общих функциях API.

## Обзор API

Нет ничего особенного в создании слоя микшера каналов. Его можно добавить через [метод фабрики по умолчанию](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) , который возвращает экземпляр класса ChannelMixerLayer. Этот класс содержит общую функциональность, такую как параметр Монохромный и метод для получения выходного канала. Особый выходной канал может быть одним из двух типов: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) или [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Тип [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) зависит от [режима цвета](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) изображения.

## Преобразование изображения в монохромное

Теперь давайте рассмотрим пример применения регулятора слоя микшера каналов к существующему документу Photoshop. Поскольку этот тип регулировки слоя пока не поддерживает предустановки, мы **воссоздадим предустановку Черно-белое инфракрасное (RGB) Photoshop** (a). Эта предустановка будет применена к изображению цветущего дерева (b). В результате мы хотим добиться эффекта инфракрасной фотографии (c).

![Пример регулятора слоя микшера каналов](channel-mixer-adjustment-psd-layer-figure-1.png) Сначала, чтобы воссоздать предустановку Черно-белое инфракрасное (RGB) Photoshop, необходимо включить флаг монохрома и установить соответствующие сырые значения для каждого цвета (красный, зеленый и синий) для выходного канала Gray:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

Изображение должно быть в режиме цвета RGB, чтобы код работал (из-за приведения к классу RgbMixerChannel). Режим цвета CMYK также поддерживается, но только для изображений с соответствующим режимом цвета.

Помните, что значение каждого цвета, а также свойство `Constant`, должны быть в диапазоне от -200 до 200.

## Вывод

В этой статье мы рассмотрели, как работать с API регулятора слоя микшера каналов Aspose.PSD для Java для настройки цветов в цветовых каналах, а также преобразования изображения в черно-белое.
