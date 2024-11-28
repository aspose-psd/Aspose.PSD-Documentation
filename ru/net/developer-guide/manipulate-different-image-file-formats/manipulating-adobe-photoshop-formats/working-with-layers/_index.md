---
title: Работа с слоями
type: docs
weight: 150
url: /ru/net/working-with-layers/
---

## **Создание группы слоев**
Группа слоев состоит из одного или нескольких слоев и помогает организовать похожие или связанные слои. С помощью Aspose.PSD для .NET вы можете создать группу слоев. Для этого в класс **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** добавлен новый метод **[**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)** для добавления группы слоев.

Шаги для создания групп слоев просты:

- Создать экземпляр изображения, используя класс PsdImage с указанными шириной, высотой и параметрами изображения.
- Создать [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) с указанным именем группы и индексом.
- Создать экземпляр класса Layer и присвоить ему изображение PSD.
- Добавить созданный слой в группу слоев, используя метод AddLayer, доступный в классе LayerGroup
- Сохранить результаты.

В следующем фрагменте кода показано, как создать группу слоев.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Переименование слоя**
Вы можете использовать любое имя, которое вам нравится, но типичной практикой является использование общего описания объекта или элемента, находящегося на этом слое. В этой статье показано, как вы можете изменить имя слоя с использованием Aspose.PSD для .NET. Для этого в класс Layer было добавлено новое свойство [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) для корректного отображения имени слоя. Было замечено, что при сохранении Photoshop имени слоя с помощью свойства [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), корейские символы сохраняются как байт 63'?' в ASCII. Итак, если вы хотите правильно отображать имя слоя, то используйте свойство **DisplayName**, поскольку свойство **Name** не поддерживает корейские символы.

В следующем образце кода показано, как вы можете переименовать слой.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **Поддержка связанных слоев**
Связывание слоев аналогично группировке слоев. Если вы связываете два или более слоев, то это позволит вносить определенные изменения во все связанные слои. Например, если вы применяете преобразования к одному слою, то они будут применены ко всем остальным связанным слоям. В этой статье демонстрируется, как получать и разрывать связанные слои с помощью [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
