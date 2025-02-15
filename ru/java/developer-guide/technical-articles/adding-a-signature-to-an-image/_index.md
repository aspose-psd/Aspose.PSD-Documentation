---
title: Добавление подписи к изображению
type: docs
weight: 10
url: /ru/java/adding-a-signature-to-an-image/
---

## **Добавление подписи**

Добавление подписи к изображению иногда требуется для цифровой подписи изображений с целью предотвращения подделки. Другая мысль может быть в том, чтобы обрабатывать изображение более как если бы оно отображалось в галерее. Какова бы ни была причина, API Aspose.PSD предоставляет возможность добавления подписи на изображение, используя простейший механизм, как объяснено ниже. Обратите внимание, что в этом примере используется класс Graphics для рисования другого изображения с подписью на поверхность оригинального изображения. Чтобы продемонстрировать операцию, мы загрузим изображение PSD с диска и нарисуем другое изображение с подписью на поверхность оригинального изображения, используя метод DrawImage класса Graphics. Мы сохраним результирующее изображение в формате PNG, используя класс PngOptions. Ниже приведен пример кода, демонстрирующий, как добавить подпись к изображению. Исходный код примера разбит на части, чтобы упростить его понимание. Шаг за шагом пример показывает, как:

- Загрузить первичные и вторичные (с подписью) изображения.
- Создать и инициализировать объект Graphics.
- Нарисовать изображение с использованием метода DrawImage класса Graphics.
- Сохранить результат в формате PNG.
### **Примеры программ**
#### **Загрузка изображений**
Сначала создайте экземпляры класса Image для загрузки образцовых изображений с диска.
#### **Создание и инициализация объекта Graphics**
После загрузки изображений создайте и инициализируйте объект класса Graphics, используя объект первичного изображения.
#### **Нанесение вторичного изображения на первичное изображение**
Затем, используя метод DrawImage класса Graphics, добавьте вторичное изображение на первичное изображение. Есть несколько вариантов перегрузок метода DrawImage, который принимает объект Image в качестве первого параметра, в то время как все остальные параметры соответствуют месту, где должно быть нарисовано изображение. Для целей демонстрации следующий код использует версию перегрузки DrawImage, которая принимает объект Point в качестве второго параметра и пытается нарисовать подпись в правом нижнем углу первичного изображения.
#### **Сохранение изображения**
Наконец, сохраните изображение обратно на локальный диск в виде файла PNG, используя класс PngOptions.
#### **Полный исходный код**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}
