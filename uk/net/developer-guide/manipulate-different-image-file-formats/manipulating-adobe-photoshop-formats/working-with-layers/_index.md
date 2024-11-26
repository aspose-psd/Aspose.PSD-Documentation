---
title: Робота з шарами
type: docs
weight: 150
url: /uk/net/робота-з-шарами/
---

## **Створення групи шарів**
Група шарів складається з одного або кількох шарів та допомагає організувати схожі або пов'язані шари. Використовуючи Aspose.PSD для .NET, ви можете створювати групу шарів. Для цього в клас **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** був доданий новий метод **[AddLayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)**, що додає групу шарів. 

Кроки для створення групи шарів настільки прості, як наведено нижче:

- Створити екземпляр зображення за допомогою класу PsdImage з вказаними шириною, висотою та параметрами зображення.
- Створити [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup)з вказаним індексом та назвою групи.
- Створити екземпляр класу Layer та призначити йому зображення PSD.
- Додати створений шар до групи шарів за допомогою методу AddLayer, який надається класом LayerGroup.
- Зберегти результати.

У наведеному нижче фрагменті коду показано, як створити групу шарів.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Перейменування шару**
Ви можете використовувати будь-яку назву, яку захочете, але типовою практикою є використання загального опису об'єкта або елемента, який знаходиться на тому шарі. Ця стаття демонструє, як ви можете змінити назву шару, використовуючи Aspose.PSD для .NET. Для цього в клас Layer було додано новий властивість [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) для відображення назви шару належним чином. Було помічено, що коли Photoshop зберігає назву шару за допомогою властивості [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), то корейські символи зберігаються як байт 63 '?' у системі ASCII. Тому, якщо ви хочете належним чином відобразити назву шару, використовуйте властивість **DisplayName**, оскільки властивість **Name** не підтримує корейських символів.

У наведеному нижче зразку коду показано, як ви можете перейменувати шар.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **Підтримка зв'язаних шарів**
Зв'язування шарів подібне до групування шарів. Якщо ви зв'язуєте два або більше шарів, то ви зможете робити певні зміни у всіх зв'язаних шарах. Наприклад, якщо ви застосовуєте трансформації до одного шару, то вони будуть застосовуватися до всіх інших зв'язаних шарів. Ця стаття демонструє, як ви можете отримувати та роз'єднувати зв'язані шари за допомогою [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
