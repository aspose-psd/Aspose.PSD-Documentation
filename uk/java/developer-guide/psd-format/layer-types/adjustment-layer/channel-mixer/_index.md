---
title: Канальний змішувач верхнього рівня
type: docs
weight: 30
url: /uk/java/layer-types/adjustment-layer/channel-mixer/
---

# Робота з канальним змішувачем верхнього рівня Photoshop в Java

Сьогодні ми розглянемо, як програмно змішувати кольори каналів в документах Photoshop за допомогою Java. Оскільки редактор Photoshop не підтримує сценарії Java, ми будемо використовувати спеціальну бібліотеку маніпулювання форматом файлів PSD під назвою Aspose.PSD для Java.

Бібліотека містить **API для роботи з кольоровими каналами**. Є кілька способів, як змішувати кольори, проте в цій статті ми зосередимося на канальному змішувачі верхнього рівня.

API канального змішувача верхнього рівня **дозволяє гратися з кольоровими каналами** для створення гострих зображень, творення різних творчих кольорових ефектів або навіть конвертації зображення в чорно-біле. Наступно, ми розглянемо, як застосувати канальний змішувач верхнього рівня до існуючого документа Photoshop за допомогою Aspose.PSD для Java, але спочатку ми повинні говорити про загальні функції API.

## Огляд API

Немає нічого особливого у створенні канального змішувача верхнього рівня. Його можна додати через [фабричний метод за замовчуванням](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) , який повертає екземпляр класу ChannelMixerLayer. Цей клас містить загальні функції, такі як опція Monochrome та метод для отримання вихідного каналу. Конкретний вихідний канал може бути одним з двох типів: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) або [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Тип [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) залежить від [режиму кольору](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) зображення.

## Зробити зображення монохромним

Тепер давайте розглянемо приклад застосування канального змішувача верхнього рівня до існуючого документа Photoshop. Оскільки цей тип регулювання ще не підтримує попередньо налаштовані значення, ми **перестворимо налаштування Photoshop для Чорно-білий інфрачервоний (RGB) (а)**. Це налаштування буде застосовано до зображення цвітущого дерева (b). Як результат, ми хочемо досягти ефекту інфрачервоної фотографії (c).

![Приклад канального змішувача верхнього рівня](channel-mixer-adjustment-psd-layer-figure-1.png) Спочатку, для відтворення налаштування Чорно-білий інфрачервоний (RGB) Photoshop необхідно увімкнути прапорець монохромний та встановити відповідні сирові значення для кожного кольору (червоного, зеленого та синього) для вихідного каналу Grey:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **короткий** )-70);
    grayOutputChannel.setGreen(( **короткий** )200);
    grayOutputChannel.setBlue(( **короткий** )-30);

Зображення повинно бути в режимі кольору RGB для коректної роботи коду (через перетворення на клас RgbMixerChannel). Режим кольорів CMYK також підтримується, але тільки для зображень з відповідним режимом кольору.

Пам'ятайте, що значення кожного кольору, а також властивість Constant повинні бути в діапазоні від -200 до 200.

## Висновок

У цій статті ми розглянули, як працювати з канальним змішувачем API Aspose.PSD для Java для коригування кольорів у кольорових каналах, а також для конвертації зображення в чорно-біле.
