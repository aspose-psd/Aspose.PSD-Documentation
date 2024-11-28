---
title: Додавання водяного знаку до зображення
type: docs
weight: 30
url: /uk/net/adding-a-watermark-to-an-image/
---

## **Додавання водяного знаку до зображення**
Цей документ пояснює, як додати водяний знак до зображення за допомогою Aspose.PSD. Додавання водяного знаку до зображення є загальною вимогою для додатків обробки зображень. У цьому прикладі використовується клас Graphics для малювання рядка на поверхні зображення.
### **Додавання водяного знаку**
Для демонстрації операції ми завантажимо зображення BMP з диска і намалюємо рядок як водяний знак на поверхні зображення за допомогою методу DrawString класу Graphics. Ми збережемо зображення у форматі PNG, використовуючи клас PngOptions. Нижче наведений код прикладу, який демонструє, як додати водяний знак до зображення. Вихідний код прикладу був розбитий на частини для зручності відстеження. Крок за кроком приклади показують, як:

1. [Завантажити](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) зображення.
1. Створити та ініціалізувати об'єкт [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Створити та ініціалізувати об'єкти Font та [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Намалювати рядок як водяний знак за допомогою методу [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) класу Graphics.
1. Зберегти зображення у PNG.

Наступний фрагмент коду показує, як додати водяний знак на зображення.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Додавання діагонального водяного знаку**
Додавання діагонального водяного знаку до зображення схоже на додавання горизонтального водяного знаку, про яке йшлося вище, з деякими відмінностями. Для демонстрації операції ми завантажимо зображення JPG з диска, додамо трансформації за допомогою об'єкту [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) та намалюємо рядок як водяний знак на поверхні зображення за допомогою методу DrawString класу Graphics. Нижче наведений код прикладу, який демонструє, як додати діагональний водяний знак на зображення. Вихідний код прикладу був розбитий на частини для зручності відстеження. Крок за кроком приклади показують, як:

1. Завантажити зображення.
1. Створити та ініціалізувати об'єкт Graphics.
1. Створити та ініціалізувати об'єкти [Font](https://reference.aspose.com/psd/net/aspose.psd/font) та SolidBrush.
1. Отримати розмір зображення в об'єкті [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Створити екземпляр класу Matrix та здійснити комбіноване перетворення.
1. Призначити перетворення об'єкту Graphics.
1. Створити та ініціалізувати об'єкт [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Намалювати рядок як водяний знак за допомогою методу DrawString класу Graphics.
1. Зберегти результат зображення.

Наступний фрагмент коду показує, як додати діагональний водяний знак.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
