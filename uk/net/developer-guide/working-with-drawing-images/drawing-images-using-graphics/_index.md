---
title: Малювання зображень за допомогою графіки
type: docs
weight: 20
url: /uk/net/drawing-images-using-graphics/
---

## **Малювання зображень за допомогою графіки**
З бібліотекою Aspose.PSD можна малювати прості форми, такі як лінії, прямокутники і кола, а також складні форми, такі як багатокутники, криві, дуги та фігури Без'є. Бібліотека Aspose.PSD створює такі форми, використовуючи клас [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), який знаходиться в просторі імен Aspose.PSD. Об'єкти Graphics відповідальні за виконання різних операцій малювання на зображенні, змінюючи поверхню зображення. Клас [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) використовує ряд допоміжних об'єктів для покращення форм:

- Ручки для малювання ліній, обводок форм або відтворення інших геометричних представлень.
- Кисті для визначення того, як заповнюються області.
- Шрифти для визначення форми символів тексту.

### **Малювання за допомогою класу Graphics**
Нижче наведено приклад коду, демонструючий використання класу [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Джерелний код прикладу було розділено на кілька частин, щоб зробити його простішим та легким для розуміння. Крок за кроком приклади показують, як:

1. Створити зображення.
1. Створити та ініціювати об'єкт Graphics.
1. Очистити поверхню.
1. Намалювати еліпс.
1. Намалювати заповнений багатокутник та зберегти зображення.

### **Приклади програмування**
#### **Створення зображення**
Почніть зі створення зображення за допомогою будь-якого з методів, що описані в розділі "Створення файлів".

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Створення та Ініціалізація об'єкта Graphics**
Потім створіть та ініціалізуйте об'єкт Graphics, передаючи об'єкт Image до його конструктора.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Очищення Поверхні**
Очистіть поверхню Graphics, викликавши метод Clear класу [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) та передавши колір як параметр. Цей метод заповнює поверхню Graphics переданим кольором.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Намалювати Еліпс**
Ви можете помітити, що клас [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) виклав безліч методів для малювання та заповнення форм. Ви знайдете повний список методів у довідці API Aspose.PSD для .NET. Клас Graphics виклав декілька версій методу DrawEllipse. Усі ці методи приймають об'єкт Pen як свій перший аргумент. Подальші параметри передаються для визначення описуючого прямокутника навколо еліпса. Для прикладу використайте версію, яка приймає об'єкт Rectangle в якості другого параметра, щоб намалювати еліпс за допомогою об'єкта Pen у вибраному вами кольорі.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Намалювати Заповнений Багатокутник**
Далі намалюйте багатокутник, використовуючи LinearGradientBrush та масив точок. Клас Graphics виклав декілька перегружених версій метода FillPolygon(). Всі вони приймають об'єкт Brush як перший аргумент, що визначає характеристики заливки. Другий параметр - це масив точок. Зверніть увагу, що кожні дві послідовні точки у масиві вказують на сторону багатокутника.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Малювання зображень за допомогою графіки : Повний код**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Всі класи, які реалізують IDisposable та мають доступ до некерованих ресурсів, створюються в операторі Using, щоб гарантувати їх правильне видалення.
