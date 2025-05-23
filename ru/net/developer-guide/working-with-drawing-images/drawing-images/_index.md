---
title: Рисование изображений
type: docs
weight: 10
url: /ru/net/drawing-images/
---

## **Рисование Линий**
Этот пример использует класс [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) для рисования линий на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует линии на его поверхности, используя метод [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) класса Graphics. Сначала мы создадим PsdImage, указав его высоту и ширину.

После создания изображения мы будем использовать метод Clear, предоставляемый классом Graphics, чтобы установить цвет фона. Метод [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) используется для рисования линии на изображении, соединяющей две точки. Этот метод имеет несколько перегрузок, принимающих экземпляр класса Pen и пары координат точек или структуры Point/PointF в качестве аргументов. Класс Pen определяет объект, используемый для рисования линий, кривых и фигур. У класса Pen есть несколько конструкторов для рисования линий с заданным цветом, шириной и кистью. Класс SolidBrush используется для непрерывного рисования с определенным цветом. Наконец, изображение экспортируется в формат bmp. В следующем фрагменте кода показано, как рисовать линии на поверхности изображения.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **Рисование Эллипса**
Пример рисования эллипса является второй статьей в серии статей о рисовании форм. Мы будем использовать класс [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) для рисования формы эллипса на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует форму эллипса на его поверхности с использованием метода DrawEllipse, предоставляемого классом [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Сначала мы создадим PsdImage, указав его высоту и ширину.

После создания изображения мы создадим и инициализируем объект класса Graphics, установим цвет фона изображения с помощью метода Clear класса Graphics. Метод DrawEllipse класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) используется для рисования эллипса на поверхности изображения, заданной структурой ограничивающего прямоугольника. Этот метод имеет несколько перегрузок, принимающих экземпляры классов Pen и Rectangle/RectangleF или пару координат, высоту и ширину в качестве аргументов. Класс Pen определяет объект, используемый для рисования линий, кривых и фигур. Класс Pen имеет несколько перегруженных конструкторов для рисования линий с заданным цветом, шириной и кистью. Класс Rectangle хранит набор из четырех целых чисел, представляющих местоположение и размер прямоугольника. Класс Rectangle имеет несколько перегруженных конструкторов для рисования структуры прямоугольника с указанным размером и местоположением. Класс SolidBrush используется для непрерывного рисования с определенным цветом. Наконец, изображение экспортируется в формат bmp. В следующем фрагменте кода показано, как рисовать эллипс на поверхности изображения.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **Рисование Прямоугольника**
В этом примере мы нарисуем форму прямоугольника на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует форму прямоугольника на его поверхности с использованием метода DrawRectangle, предоставляемого классом [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Сначала мы создадим PsdImage, указав его высоту и ширину. Затем установим цвет фона изображения с помощью метода Clear класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

Метод DrawRectangle класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) используется для рисования формы прямоугольника на поверхности изображения, указанной структурой прямоугольника. Этот метод имеет несколько перегрузок, принимающих экземпляры классов Pen и Rectangle/RectangleF или пару координат, ширину и высоту в качестве аргументов. Класс Rectangle хранит набор из четырех целых чисел, представляющих местоположение и размер прямоугольника. Класс Rectangle имеет несколько перегруженных конструкторов для рисования структуры прямоугольника с указанным размером и местоположением. Наконец, изображение экспортируется в формат bmp. В следующем фрагменте кода показано, как рисовать прямоугольник на поверхности изображения.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **Рисование Дуги**
В этом разделе серии статей о формах рисования мы нарисуем форму дуги на поверхности изображения. Мы будем использовать метод DrawArc класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) для демонстрации операции на изображении BMP. Сначала мы создадим PsdImage, указав его высоту и ширину. После создания изображения, мы будем использовать метод Clear, предоставляемый классом [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), чтобы установить цвет фона.

Метод DrawArc класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) используется для рисования формы дуги на поверхности изображения. DrawArc представляет часть эллипса, указанного структурой прямоугольника или парой координат. Этот метод имеет несколько перегрузок, принимающих экземпляры классов Pen и Rectangle/RectangleF или пару координат, ширину и высоту в качестве аргументов. Наконец, изображение экспортируется в формат bmp. В следующем фрагменте кода показано, как рисовать форму дуги на поверхности изображения.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **Рисование Безье**
Этот пример использует класс [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) для рисования кривой Безье на поверхности изображения. Чтобы продемонстрировать операцию, пример создает новое изображение и рисует форму кривой Безье на его поверхности с использованием метода DrawBezier, предоставляемого классом [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Сначала мы создадим PsdImage, указав его высоту и ширину. После создания изображения, мы будем использовать метод Clear, предоставляемый классом [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), чтобы установить цвет фона.

Метод DrawBezier класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) используется для рисования кривой Безье на поверхности изображения, определенной четырьмя структурами Point. Этот метод имеет несколько перегрузок, принимающих экземпляры класса Pen и четыре упорядоченных пары координат или четыре структуры Point/PointF или массив структур Point/PointF в качестве аргументов. Класс Pen определяет объект, используемый для рисования линий, кривых и фигур. Класс Pen имеет несколько перегруженных конструкторов для рисования линий с заданным цветом, шириной и кистью. Наконец, изображение экспортируется в формат bmp. В следующем фрагменте кода показано, как рисовать кривую Безье на поверхности изображения.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **Рисование изображений с использованием Основных Функций**
Aspose.PSD - это библиотека, предлагающая множество ценных функций, в том числе создание изображений с нуля. Рисуйте с использованием основных функций, таких как манипулирование информацией о битмапе изображения или использование продвинутых функций, таких как [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) и [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) для рисования форм на поверхности изображения с помощью разных кистей и перьев. Используя класс RasterImage Aspose.PSD, вы можете получить информацию о пикселях области изображения и манипулировать ею. Класс RasterImage содержит всю основную функциональность рисования, такую как получение и установка пикселей и другие методы для манипуляции изображением. Создайте новое изображение, используя любой из методов, описанных в создании файлов, и присвойте его экземпляру класса RasterImage. Используйте метод LoadPixels класса RasterImage для получения информации о пикселях части изображения. После получения массива пикселей вы можете манипулировать им, например, изменить цвет каждого пикселя. После манипулирования информацией о пикселях, установите ее обратно в нужную область изображения, используя метод SavePixels класса RasterImage. В следующем фрагменте кода показано, как рисовать изображения, используя основные функции.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
