---
title: Aspose.PSD для .NET 20.8 - Примітки до випуску
type: docs
weight: 50
url: /uk/net/aspose-psd-for-net-20-8-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску для [Aspose.PSD для .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDNET-390|Підтримка PlLdResource (ресурс розміщеного шару для Шару об'єктів Smart)|Функція|
|PSDNET-400|Підтримка SoLdResource (ресурс даних шару об'єктів Smart)|Функція|
|PSDNET-693|Додайте підтримку структур масиву об'єктів та масиву одиниць: ObAr / UnFl signatures|Функція|
|PSDNET-600|Виправлення збереження зміненого зображення PSD з режимом кольору CMYK 16 біт на канал|Помилка|
|PSDNET-664|Підкреслення та перекреслення загублені після фокусування на тексті у файлі, збереженому за допомогою Aspose.PSD|Помилка|
|PSDNET-710|Регресія: Aspose.PSD 20.7.0 руйнує розміри шрифтів для старіших файлів|Помилка|

## **Зміни в публічному API**
# **Додані API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Structures
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitTypes,System.Double[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.UnitType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Values
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.ValueCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- ...

## **Приклади використання:**
**PSDNET-390. Підтримка PlLdResource (ресурс розміщеного шару для Шару об'єктів Smart)**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-400. Підтримка SoLdResource (ресурс даних шару об'єктів Smart)**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-693. Додайте підтримку структур масиву об'єктів та масиву одиниць: ObAr / UnFl signatures**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-600. Виправлення збереження зміненого зображення PSD з режимом кольору CMYK 16 біт на канал**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-664. Підкреслення та перекреслення загублені після фокусування на тексті у файлі, збереженому за допомогою Aspose.PSD**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-710. Регресія: Aspose.PSD 20.7.0 руйнує розміри шрифтів для старіших файлів**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}```
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-600. Виправлення збереження зміненого зображення PSD з режимом кольору CMYK 16 біт на канал**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-664. Підкреслення та перекреслення загублені після фокусування на тексті у файлі, збереженому за допомогою Aspose.PSD**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
**PSDNET-710. Регресія: Aspose.PSD 20.7.0 руйнує розміри шрифтів для старіших файлів**
{{< highlight csharp >}}
        // Код прикладу
{{< /highlight >}}
```