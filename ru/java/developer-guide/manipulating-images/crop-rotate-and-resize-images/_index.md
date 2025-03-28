---
title: Обрезка, Поворот и Изменение размера изображений
type: docs
weight: 40
url: /ru/java/crop-rotate-and-resize-images/
---

## **Обрезка изображений**
Обрезка изображения обычно означает удаление внешних частей изображения для улучшения кадрирования. Обрезка также может использоваться для вырезания определенной части изображения и увеличения акцента на конкретной области. API Aspose.PSD поддерживает два различных подхода к обрезке изображения: сдвигом и прямоугольником.
### **Обрезка по сдвигам**
Класс RasterImage предоставляет перегруженную версию метода Crop, который принимает 4 целочисленных значения, обозначающих Лево, Право, Верх и Низ. На основе этих четырех значений метод Crop перемещает границы изображения к центру изображения, отбрасывая внешнюю часть. Нижеприведенный фрагмент кода демонстрирует, как обрезать изображение с помощью сдвигов.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Обрезка прямоугольником**
Класс RasterImage предоставляет другую перегруженную версию метода Crop, которая принимает экземпляр класса Rectangle. Вы можете вырезать любую часть изображения, указав желаемые границы объекта Rectangle. Нижеприведенный фрагмент кода демонстрирует, как обрезать любое изображение прямоугольником.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Поворот и Отражение изображения**
Aspose.PSD для Java - это простая в использовании библиотека, поскольку она предоставляет простые методы для выполнения сложных операций. Например, Aspose.PSD для Java предоставляет метод RotateFlip для своего базового класса Image, если приложение требует поворота изображения. Независимо от формата изображения, библиотека может выполнить специальную процедуру Rotate & Flip на нем.
### **Поворот изображения**
Метод Image.RotateFlip может использоваться для поворота изображения на 90/180/270 градусов и отражения изображения горизонтально или вертикально. Метод Image.RotateFlip принимает параметр RotateFlipType, который определяет тип поворота и отражения, применяемого к изображению. Шаги для выполнения поворота и отражения просты, как показано ниже:

1. Загрузите изображение с помощью фабричного метода Load, предоставленного классом Image.
1. Вызовите метод Image.RotateFlip, указав соответствующий параметр RotateFlipType.
1. Сохраните результаты.

Нижеприведенный пример кода демонстрирует, как установить свойство RotateFlip изображения и перечисление RotateFlipType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Поворот изображения на определенный угол**
API Aspose.PSD для Java предоставляет метод RasterImage.Rotate для пользователей, которые хотят повернуть изображение на определенный угол. В отличие от метода RasterImage.RotateFlip, метод RasterImage.Rotate принимает три параметра:

1. Угол поворота: Параметр типа float, указывающий угол поворота, на который изображение должно быть повернуто. Положительное значение поворачивает изображение по часовой стрелке; отрицательное значение выполняет вращение против часовой стрелки.
1. Пропорциональное изменение размера: Параметр типа Boolean указывает, должны ли изменяться размеры изображения в соответствии с проекциями повернутого прямоугольника (угловые точки). Если установлено значение false, размеры изображения останутся без изменений, и будут повернуты только внутренние содержимое изображения.
1. Цвет фона: Параметр типа Color указывает цвет, который будет заполнен в фон повернутого изображения.

Строковый фрагмент ниже демонстрирует использование метода RasterImage.Rotate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Изменение размера изображения**
Эта статья демонстрирует использование Aspose.PSD для Java для выполнения операции изменения размера изображения. API Aspose.PSD предоставляет эффективные и простые в использовании методы для достижения этой цели. Aspose.PSD для Java предоставляет метод Resize для класса Image, который можно использовать для изменения размера существующих изображений на лету. Есть две перегрузки метода Resize, чтобы соответствовать потребностям приложения.
### **Простое изменение размера**
Шаги для выполнения изменения размера просты, как показано ниже:

1. Загрузите изображение с помощью фабричного метода Load, предоставленного классом Image.
1. Вызовите метод Image.Resize, указав новую высоту и ширину.
1. Сохраните результаты.

Нижеприведенный пример кода демонстрирует, как изменить размер изображения.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Изменение размера с использованием перечисления ResizeType**
API Aspose.PSD предоставляет перечисление ResizeType, которое можно использовать с методом Image.Resize для достижения желаемых результатов. Приведенный ниже фрагмент кода демонстрирует использование перечисления ResizeType, а подробности членов перечисления ResizeType могут быть найдены в нижней части этой страницы.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Если вы хотите получить качественный результат после применения изменения размера, рекомендуется всегда использовать ResizeType.LanczosResample, потому что он будет выдавать высококачественные результаты, но может работать медленнее, чем ResizeType.NearestNeighbourResample. С другой стороны, алгоритм ResizeType.NearestNeighbourResample используется специально для быстрого изменения размера, при этом компрометируется качество изображения. Этот метод может быть полезен для генерации миниатюр в реальном времени или аналогичных процессов, где требуется высокая производительность.
## **Изменение размера изображения пропорционально**
Вы можете изменить размеры изображений, передав новые значения высоты и ширины в качестве параметров метода Image.Resize, но в этом случае вам придется самостоятельно рассчитать соотношение сторон. Это потому, что при изменении ширины или высоты изображения изображение либо масштабируется, либо уменьшается до заполнения нового размера. Если изменения ширины и высоты изображения не пропорциональны, это может привести к растянутому и искаженному результату. В этой статье демонстрируется использование API Aspose.PSD для Java для изменения размера изображений, передавая либо новую высоту, либо ширину, позволяя API автоматически рассчитать другое пропорциональное значение.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Перечисление ResizeType**
ResizeType определяет тип изменения размера, который должен быть выполнен на изображении на основе выбранного фильтра.

Члены перечисления ResizeType

|**Имя члена**|**Значение**|**Описание**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Левая верхняя точка нового изображения совпадет с левой верхней точкой оригинального изображения. Произойдет обрезка, если это необходимо.|
|RightTopToRightTop|1|Правая верхняя точка нового изображения совпадет с правой верхней точкой оригинального изображения. Произойдет обрезка, если это необходимо.|
|RightBottomToRightBottom|2|Правая нижняя точка нового изображения совпадет с правой нижней точкой оригинального изображения. Произойдет обрезка, если это необходимо.|
|LeftBottomToLeftBottom|3|Левая нижняя точка нового изображения совпадет с левой нижней точкой оригинального изображения. Произойдет обрезка, если это необходимо.|
|CenterToCenter|4|Центр нового изображения совпадет с центром оригинального изображения. Произойдет обрезка, если это необходимо.|
|LanczosResample|5|Переменный калибровочный фильтр по алгоритму Ланцош с использованием 7x7 маски.|
|NearestNeighbourResample|6|Переменный калибровочный фильтр с использованием алгоритма ближайших соседей.|

