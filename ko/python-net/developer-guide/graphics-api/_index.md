---
title: PSD 파일에서 레이어를 편집하는 Graphics API 사용
weight: 100
type: docs
description: Aspose.PSD를 위한 Python의 Graphics API 사용 예시
keywords: [레이어 업데이트, 원 그리기, 타원 그리기, 채운 원 그리기, 그래픽, psd api, python, 코드 샘플]
url: ko/python-net/graphics-api/
---

## **개요**
먼저, Image.load() 메서드를 사용하여 PSD 파일을 로드하거나 스크래치에서 Psd Image를 생성해야 합니다. 예시에서 inputFile 변수는 PSD 파일 경로를 나타내고, loadOpt는 로드 옵션(있는 경우)을 나타냅니다.

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
다음으로, psdImage.layers[0] 구문을 사용하여 PSD 이미지의 첫 번째 레이어에 액세스할 수 있습니다. 이렇게하면 조작할 수 있는 레이어 개체에 대한 참조가 제공됩니다.

```python 
layer = psdImage.layers[0]
```
레이어를 편집하려면 레이어를 매개변수로 전달하여 Graphics 개체를 만들어야 합니다. 이 객체는 모양을 그리고 브러시를 적용하는 데 다양한 메서드를 제공합니다.

```python 
graphics = Graphics(layer)
```
코드 예시에서는 타원 모양의 외곽선의 색상과 굵기를 정의하기 위해 Pen 개체가 생성됩니다. Color.alice_blue 상수는 색상을 나타내며, 필요에 따라 굵기를 조절할 수 있습니다.

```python 
pen = Pen(Color.alice_blue)
```
비슷하게, LinearGradientBrush 개체를 생성하여 타원 모양의 채우기 색상을 정의합니다. Rectangle(250, 250, 150, 100)은 타원 모양의 위치와 크기를 나타내며, Color.red 및 Color.aquamarine은 그라데이션의 시작 및 끝 색상을 나타냅니다.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
레이어에 타원 모양을 그리려면 graphics.draw_ellipse() 메서드를 사용할 수 있습니다. Rectangle(100, 100, 200, 200)은 타원 모양의 위치와 크기를 나타냅니다.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
그라데이션 브러시로 타원 모양을 채우려면 graphics.fill_ellipse() 메서드를 사용할 수 있습니다. Rectangle(250, 250, 150, 100)은 타원 모양의 위치와 크기를 나타냅니다.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
레이어에 원하는 변경을 가한 후에는 psdImage.save() 메서드를 사용하여 수정된 PSD 이미지를 저장할 수 있습니다. 예시에서 psdName 변수는 수정된 PSD 파일을 저장할 경로를 나타냅니다.

```python 
psdImage.save(psdName)
```
추가적으로, PngOptions 클래스를 사용하여 PNG와 같은 다른 형식의 수정된 이미지를 저장할 수도 있습니다. pngName 변수는 PNG 파일을 저장할 경로를 나타냅니다.

```python 
psdImage.save(pngName, PngOptions())
```
여기까지! 이제 Aspose.PSD의 Python Graphics API를 사용하여 PSD 파일의 레이어를 편집하는 데 성공했습니다. 이미지 편집 기능을 향상시키기 위해 Aspose.PSD 라이브러리의 더 많은 기능과 기능을 탐색해 보세요.

전체 예시를 확인해 주세요.

## **예시**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}
