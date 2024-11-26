---
title: Редактирование растровых масок слоев в файле PSD через API
type: docs
weight: 20
url: /ru/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **Обзор**
**Чтобы автоматизировать редактирование формата PSD и изменять файл PSD без Adobe® Photoshop®, можно использовать предоставленный ниже API Aspose.PSD. Для изменения файлов PSD доступны фрагменты кода на C# и .NET.**

Используя маски слоев и векторные маски PSD, мы можем скрывать и отображать пиксели слоя без их окончательного удаления. Растровые маски также называются масками слоя или пользовательскими масками. Доступ к растровым и векторным маскам в Aspose.PSD предоставляется через свойство слоя [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata), которое может быть экземпляром классов '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' и '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)', являющихся дочерними классами абстрактного класса 'LayerMaskData'. Если у слоя есть как растровая, так и векторная маски, то предоставляется экземпляр [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). Если у слоя есть только растровая или векторная маска, то предоставляется экземпляр [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.p sd.fileformats.psd.layers/layermaskdatashort). Если свойство LayerMaskData равно null, то у слоя нет масок или только отключенная векторная маска.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Растровая маска и отключенная векторная маска LayerMaskDataShort</p><p>Отключенная растровая маска  LayerMaskDataShort</p><p>Растровая маска и векторная маска  LayerMaskDataFull</p><p>Растровая маска  LayerMaskDataShort</p><p>Векторная маска  LayerMaskDataShort</p><p>Отключенная векторная маска null (но ресурс вектора присутствует)</p>|
| :- | :- |

## **Как получить растровую маску слоя в файле PSD?**
Сначала нам нужно определить, есть ли у слоя как векторная, так и растровая маски:

Ниже приведен пример кода, демонстрирующий, как получить растровую маску слоя

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

В противном случае тип свойства слоя LayerMaskData - LayerMaskDataShort. В этом случае давайте проверим, есть ли у слоя только растровая маска, проверив флаг Flags. Он не должен содержать [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags). Флаг **UserMaskFromRenderingOtherData**, в противном случае маска - это векторная маска кэш **.**

Получение фрагмента кода маски:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Если вам нужно **извлечь растровую маску** как LayerMaskDataShort (для дальнейших манипуляций), даже если присутствуют обе маски, должен быть извлечен LayerMaskDataFull и преобразован в LayerMaskDataShort. Для обоих случаев можно использовать следующий код:

Извлечение растровой маски из PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **Как проверить, есть ли у слоя в файле PSD растровая маска?**
Следующий код на C# может помочь вам проверить, есть ли у слоя растровая маска:

Как узнать, применена ли к растровой маска к [слою PSD](/psd/ru/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **Как удалить / добавить / обновить растровую маску слоя в файле PSD?**
Просто удаление / добавление / обновление LayerMaskData недостаточно для правильного сохранения, потому что каналы не обновляются; хотя это может обеспечить правильное воспроизведение. Это не изменяет каналы маски:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Мы должны использовать метод AddLayerMask слоя для удаления / добавления / обновления.

Этот метод добавляет/обновляет как маску, так и каналы:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Этот метод удаляет как маску, так и каналы:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **Удаление растровой маски слоя в изображении PSD**
Сначала мы проверяем, в коротком формате ли маска, и если это не вектор, мы просто вызываем метод AddLayerMask со значением null, чтобы удалить растровую маску. Но если она в полном формате, мы должны преобразовать ее в короткий формат, оставив только векторную маску. Для удаления маски слоя можно использовать следующий фрагмент кода на C# .NET:

Фрагмент кода, как удалить маску слоя из файла PSD.

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **Обновление растровой маски слоя в изображении PSD**
Это просто: если маска в коротком формате, мы должны изменить ImageData и MaskRectangle при необходимости, в противном случае должны быть изменены [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)и [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle). Для обновления маски слоя можно использовать следующий фрагмент кода на C# .NET:

Обновление маски слоя PSD с помощью C#

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Вот пример возможных действий, изменяющих растровую маску. Этот инвертирует пользовательскую маску слоя:

Обновление маски слоя PSD с помощью C#

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **Обновление векторной маски в файле PSD, когда присутствует растровая маска слоя**
Предполагается, что пользователь уже изменил ресурс векторного пути. Затем можно обновить векторную маску просто, вызвав [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask)метод слоя:

Обновление [PSD Layer Vector Mask ](/psd/ru/net/layer-vector-mask/)с C#

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **Добавление растровой маски слоя в файл PSD**
Если у слоя нет маски, мы можем добавить данную растровую маску, просто вызвав метод слоя AddLayerMask.

Если у маски нет [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)флага, то у нее уже есть растровая маска, и мы должны обновить ее, как описано выше. В противном случае, если эта маска в коротком формате, мы преобразуем ее в полный формат. Если нет, мы используем ее как есть. Затем обновите UserMaskData, UserMaskRectangle и другие свойства соответствующими свойствами маски. Для добавления (обновления) маски слоя можно использовать следующий фрагмент кода на C# .NET:

Добавление новой маски слоя в PSD

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Как узнать, включена ли маска слоя?**
Для определения состояния включения растровой маски слоя мы можем проверить состояние флага LayerMaskFlags.Disabled в свойстве Flags для LayerMaskDataShort или в RealFlags для LayerMaskDataFull. Для получения состояния включения маски слоя можно использовать следующий фрагмент кода на C# .NET:

Проверить, включена ли маска:

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}

## **Как включить или отключить растровую маску слоя?**
Чтобы включить или выключить растровую маску слоя, мы можем изменить состояние флага LayerMaskFlags.Disabled в свойстве Flags для LayerMaskDataShort или в RealFlags для LayerMaskDataFull. Для изменения состояния включения маски слоя можно использовать следующий фрагмент кода на C# .NET:

Включить или отключить растровую маску слоя:

{{< gist "aspose-com-gists" "8d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
