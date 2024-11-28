---
title: Использование PSD-файлов в качестве шаблонов для автоматизации - дело визиток
type: docs
weight: 10
url: /ru/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **Обзор**
Эта статья описывает часто используемые случаи, когда вам нужно программно обновить некоторые слои в [PSD-файле](https://wiki.fileformat.com/image/psd/), который имеет известную шаблонную структуру. Это может быть использовано для создания большого количества визиток для разных людей (дело визиток). Или вам может понадобиться перевести PSD-файл на разные языки с заменой некоторых графических материалов в нем.

После прочтения этой статьи вы узнаете, как сделать следующее:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **Простой случай**
Например, у вас есть PSD-шаблон с известными именами слоев. Поэтому вам нужно изменить, обновить или заменить PSD-слои с помощью C#. Сначала вам нужно открыть файл шаблона с помощью Aspose.PSD.

Как открыть PSD-файл с помощью C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Затем нам нужно найти слой, который мы хотим заменить по его имени. Вот простая реализация для этого.

Как найти слой в PSD-файле по его имени

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}


Когда слой найден, мы можем обновить его обычным способом, используя [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Как рисовать на слое PSD с помощью Graphics

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

В этом случае мы рисуем новое загруженное изображение [PNG](https://wiki.fileformat.com/image/png/) на существующем слое PSD, поэтому старые данные будут утеряны в новом файле.

Но что, если нам также нужно обновить текст? Процесс будет аналогичным. Найдите [текстовой слой](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) по его имени, затем мы программно [обновляем текстовой слой файла Photoshop](/psd/ru/net/render-text-with-different-colors-in-text-layer/).


Как обновить текстовой слой в Photoshop с помощью C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



В конце мы должны сохранить наши изменения:

Как сохранить измененный PSD-файл с использованием [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



Полученное изображение:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **Сложный случай с дополнительными функциями**
Выше мы показали самый простой способ замены изображения в слое PSD-файла.

Однако Aspose.PSD может предложить более сложные дополнительные функции, такие как добавление нового слоя, удаление старых слоев и обновление текстового слоя с разными стилями в многострочном тексте.

Мы можем найти [Слой](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer), который мы хотим заменить, затем найти его индекс в списке слоев, удалить его и вставить новый слой после его создания из [Jpeg-файла](https://wiki.fileformat.com/image/jpeg/) на то же место.

Создайте новый слой из файла и вставьте его в изображение PSD с использованием [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



В конце этого файлового отрывка кода мы корректируем позицию слоя и сохраняем новый массив слоев в изображении Psd.

Как скопировать свойства слоя [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



И в конце, нам нужно обновить текстовые слои в существующем изображении PSD с помощью C#. Aspose.PSD поддерживает [обновление TextLayer порциями](/psd/ru/net/working-with-text-layers/). Каждая [текстовая порция](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) имеет уникальное сочетание свойств стиля и абзаца.

Как скопировать свойства слоя [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



В результате мы изменили шаблон PSD с помощью кода с добавлением нового слоя из файлов Jpeg, Png, J2k, Bmp, Gif или Tiff и многострочным [текстом с разными стилями](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) в каждой строке.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
