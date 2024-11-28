---
title: Шар PSD
type: документація
weight: 70
url: /uk/net/psd-layer/
---

## **Огляд**
Шар PSD в Adobe® Photoshop® - один з кращих концепцій обробки графіки. Шари містять інформацію про пікселі, можуть мати різну кількість каналів.

Однією з найважливіших частин шару в документі Photoshop є Ресурси шару. У нашій документації ви знайдете повний список підтримуваних [Ресурсів шару](/psd/uk/net/list-of-psd-layer-resources/) в PSD.

Ви можете знайти користувацький інтерфейс для маніпулювання шаром на наступному знімку екрану:

![todo:image_alt_text](psd-layer_1.png)

Але Aspose.PSD спеціалізується на програмних маніпуляціях PSD-шару через [C# ](/psd/uk/net/home/)та [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home).

Додаткову документацію можна знайти в цій статті: [Маніпулювання Зображеннями](/psd/uk/net/manipulating-images-html/). Усі маніпуляції можуть бути оброблені для Попереднього перегляду PSD та Шару, ви знайдете більше інформації в [Довідці API для Растрових Зображень Aspose.PSD](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).

## **Доступні API для Шару PSD**
- Ефекти шару
- Загальні властивості шарів
- Метадані шару

## **Приклади редагування шару через C#**
### **Додавання нового Шару**
Якщо ви хочете додати порожній Шар до відкритого [Файлу PSD](/psd/uk/net/psd-file/), ви можете використати наступний код.

Додаток нового Шару до файлу PSD за допомогою API

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}

### **Додавання нового Шару з файлів Jpeg, Png, Gif, Ai, Tiff, Bmp**
Файли будь-яких [підтримуваних форматів ](/psd/uk/net/supported-file-formats/) можна додати як новий шар до вашого зображення. Але ви не можете завантажити його безпосередньо.

Ви можете використовувати наведений нижче код, щоб додати новий шар PSD з файлу будь-якого підтримуваного формату з потоку

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

### **Об'єднати всі шари або групи шарів**
Це може бути корисним, якщо ви не хочете надавати вашим користувачам редагований файл PSD. Також ви можете ідентифікувати через API, чи був файл зрівняний.

Зрівнювання Шару файлу PSD:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
