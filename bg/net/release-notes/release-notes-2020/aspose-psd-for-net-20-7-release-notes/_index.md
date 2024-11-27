---
title: Aspose.PSD за .NET 20.7 - Бележки за изданието
type: docs
weight: 60
url: /bg/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-673|Поддръжка на LnkE ресурс|Функционалност|
|PSDNET-392|Поддръжка на britResource (Ресурс за яркост/контраст на слоя за корекция)|Функционалност|
|PSDNET-629|Промяна на съобщението за грешка при опит за отваряне на несъпортовани формати като изображение|Подобрение|
|PSDNET-594|Неуспешно запазване на LayerMask|Проблем|
|PSDNET-597|При запазване на PSD файл след създаването на нова Група на слоеве се получава предупреждение в Photoshop при отваряне на файла|Проблем|
|PSDNET-618|Clipping маската не се прилага към папката|Проблем|
|PSDNET-625|Невъзможност за отваряне на файл с Aspose.PSD за .NET|Проблем|
|PSDNET-650|Изключение за неуспешно запазване на изображение при конвертиране на PSD в PDF|Проблем|
|PSDNET-655|rop операцията прави Clipping пътя невалиден в PSD изображение|Проблем|
|PSDNET-662|NullReference Изключение при опит за запазване на конкретен PSD файл с ефект на сянка|Проблем|
|PSDNET-666|Aspose.PSD връща true при Image.CanLoad(pdfStream)|Проблем|
|PSDNET-676|Слоевете не се визуализират в генерирания PNG|Проблем|
|PSDNET-677|Изключение при достъп до TextData|Проблем|
|PSDNET-679|ImageSaveException при запазване на PSD|Проблем|

## **Промени в публичния API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **Премахнати API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Примери за използване:**
**PSDNET-606. Поддръжка на LnkE ресурс**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(actual, expected))
    {
        throw new FormatException(string.Format("Фактическата стойност {0} не съвпада с очакваната {1}.", actual, expected));
    }
    
}

// Следват примерни случаи за поддръжка на Lnk2Resource
...

{{< /highlight >}}