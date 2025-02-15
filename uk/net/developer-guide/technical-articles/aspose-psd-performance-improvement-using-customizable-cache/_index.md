---
title: Покращення продуктивності Aspose.PSD за допомогою налаштованого кешу
type: docs
weight: 20
url: /uk/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Покращення продуктивності за допомогою налаштованого кешу**
[Aspose.PSD](https://products.aspose.com/psd/family) використовує кешування для тимчасового збереження даних. Механізм простий у використанні, налаштовується та прозорий. Він гарантує відсутність проблем з продуктивністю під час обробки зображень. У цій статті пояснено, як налаштувати кеш за допомогою API Aspose.PSD для .NET.
### **Налаштування кешу**
Коли процесу потрібне тимчасове зберігання даних, це зберігання виділяється в кеші. Кеш може бути простором у пам'яті або на диску та налаштовується користувачем. Якщо тимчасові дані більше не потрібні, простір звільняється. Статистику виділеного простору можна переглянути у будь-який час. Те, як Aspose.PSD виділяє та використовує кеші, може бути налаштовано. Цей розділ описує різні налаштування та їх значення за замовчуванням, а наведені нижче фрагменти коду показують, як їх можна використовувати.
### **Встановлення місця виділення кешу**
Щоб настроїти, як виділяється простір кешу, встановіть властивість [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). За замовчуванням кеш виділяється в пам'яті, а коли в пам'яті немає достатньо місця, він виділяється на диск. Ця поведінка захоплюється автоматичним режимом. Автоматичний режим гнучкий та максимізує продуктивність. Існують й інші режими:

- режим CacheOnDiskOnly: виділення лише на диск.
- режим CacheInMemoryOnly: виділення лише в пам'ять.

Вибір режиму CacheOnDiskOnly може призвести до поганої продуктивності.
### **Встановлення розміру кешу**
Встановіть максимальний простір (у байтах), який може бути виділений на диск чи в пам'ять, встановивши властивості [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) та [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) відповідно. За замовчуванням обидва значення встановлені ​​на 0, що означає, що верхньої межі немає.
### **Керування перерозподілом кешу**
Якщо в пам'яті недостатньо місця (як вказано у властивості MaxMemoryForCache) під час виділення нового кешу, кеш виділяється на диск. Якщо на диску недостатньо місця, виникає виняток. Процес виділення кешів переходить з пам'яті на диск, але не навпаки. Властивість [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) використовується для керування перерозподілом пам'яті. Перерозподіл імовірніше відбувається для передвідведених кешів. Це може траплятися, коли система вирішує, що виділеного простору буде недостатньо. Якщо ExactReallocateOnly встановлено ​​на значення за замовчуванням, False, простір перерозподіляється на ту саму середу. Якщо встановлено ​​на True, перерозподіл не може перевищувати максимально вказаний простір. У цьому випадку існуючий кеш у пам'яті (який потребує перерозподілу) звільняється, а розширений простір виділяється на диск.
### **Приклади програмного коду**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
