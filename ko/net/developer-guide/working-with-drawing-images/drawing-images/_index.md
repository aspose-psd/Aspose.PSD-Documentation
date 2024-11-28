---
title: 이미지 그리기
type: 문서
weight: 10
url: /ko/net/drawing-images/
---

## **선 그리기**
이 예제는 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스를 사용하여 이미지 표면에 선 모양을 그리는 방법을 보여줍니다. 작업을 설명하기 위해 예제는 높이와 너비를 지정한 새 이미지를 만들고, Graphics 클래스에 의해 노출된 DrawLine 메서드를 사용하여 이미지 표면에 선을 그립니다. 이미지가 생성되면 Graphics 클래스에 의해 노출된 Clear 메서드를 사용하여 배경색을 설정합니다. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) 메서드는 두 점 구조체를 연결하며 이미지에 선을 그리는 데 사용됩니다. 이 메서드에는 Point 클래스의 인스턴스와 점 또는 Point/PointF 구조체의 좌표 쌍을 인수로 사용하는 여러 오버로드가 있습니다. Pen 클래스는 선, 곡선 및 도형을 그리는 데 사용되는 객체를 정의합니다. Pen 클래스에는 지정된 색상, 너비 및 브러시로 선을 그리기 위한 여러 오버로드된 생성자가 있습니다. SolidBrush 클래스는 특정 색상으로 계속해서 그리는 데 사용됩니다. 마지막으로 이미지를 bmp 파일 형식으로 내보냅니다. 다음 코드 조각은 이미지 표면에 선 모양을 그리는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **타원 그리기**
타원 그리기 예제는 그리기 모양 시리즈의 두 번째 항목입니다. 이미지 표면에 타원 모양을 그리기 위해 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스를 사용합니다. 작업을 설명하기 위해 예제는 높이와 너비를 지정한 새 이미지를 만들고, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스에 의해 노출된 DrawEllipse 메서드를 사용하여 이미지 표면에 타원 모양을 그립니다. 이미지가 생성된 후에는 Graphics 클래스의 Clear 메서드를 사용하여 이미지의 배경색을 설정합니다. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 DrawEllipse 메서드는 바운딩 사각형 구조체로 지정된 이미지 표면에 타원 모양을 그리는 데 사용됩니다. 이 메서드에는 Pen 및 Rectangle/RectangleF 클래스의 인스턴스 또는 좌표 쌍, 높이 및 너비를 인수로 사용하는 여러 오버로드가 있습니다. Pen 클래스는 선, 곡선 및 도형을 그리는 데 사용되는 객체를 정의합니다. Pen 클래스에는 지정된 색상, 너비 및 브러시로 선을 그리기 위한 여러 오버로드된 생성자가 있습니다. Rectangle 클래스는 위치와 크기를 나타내는 네 개의 정수를 저장합니다. Rectangle 클래스에는 지정된 크기와 위치로 사각형 구조체를 그리기 위한 여러 오버로드된 생성자가 있습니다. SolidBrush 클래스는 특정 색상으로 계속해서 그리는 데 사용됩니다. 마지막으로 이미지를 bmp 파일 형식으로 내보냅니다. 다음 코드 조각은 이미지 표면에 타원 모양을 그리는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **사각형 그리기**
이 예제는 이미지 표면에 사각형 모양을 그립니다. 작업을 설명하기 위해 예제는 높이와 너비를 지정한 새 이미지를 만들고, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스에 의해 노출된 DrawRectangle 메서드를 사용하여 이미지 표면에 사각형 모양을 그립니다. 먼저 PsdImage를 생성하고 높이와 너비를 지정합니다. 그런 다음, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 Clear 메서드를 사용하여 이미지의 배경색을 설정합니다.

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 DrawRectangle 메서드는 직사각형 구조체로 지정된 이미지 표면에 사각형 모양을 그리는 데 사용됩니다. 이 메서드에는 Pen 및 Rectangle/RectangleF 클래스의 인스턴스 또는 좌표 쌍, 너비, 높이가 인수로 사용되는 여러 오버로드가 있습니다. Rectangle 클래스는 위치와 크기를 나타내는 네 개의 정수를 저장합니다. Rectangle 클래스에는 지정된 크기와 위치로 사각형 구조체를 그리기 위한 여러 오버로드된 생성자가 있습니다. 마지막으로 이미지를 bmp 파일 형식으로 내보냅니다. 다음 코드 조각은 이미지 표면에 사각형 모양을 그리는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **호 그리기**
이 그리기 모양 시리즈의 세션에서는 이미지 표면에 호 모양을 그립니다. BMP 이미지에서 작업을 보여주기 위해 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)의 DrawArc 메서드를 사용합니다. 먼저 높이와 너비가 지정된 새 PsdImage를 만듭니다. 이미지가 생성된 후에는 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스에 의해 노출된 Clear 메서드를 사용하여 이미지의 배경색을 설정합니다.

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 DrawArc 메서드는 이미지 표면에 호 모양을 그리는 데 사용됩니다. DrawArc는 사각형 구조체나 좌표 쌍으로 지정된 타원의 일부를 나타냅니다. 이 메서드에는 Pen 클래스의 인스턴스 및 Rectangle / RectangleF 구조체 또는 좌표 쌍, 너비 및 높이가 인수로 사용되는 여러 오버로드가 있습니다. 마지막으로 이미지를 bmp 파일 형식으로 내보냅니다. 다음 코드 조각은 이미지 표면에 호 모양을 그리는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **베지어 곡선 그리기**
이 예제는 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스를 사용하여 이미지 표면에 베지어 곡선 모양을 그리는 방법을 보여줍니다. 작업을 설명하기 위해 예제는 높이와 너비를 지정한 새 이미지를 만들고, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스에 의해 노출된 DrawBezier 메서드를 사용하여 이미지 표면에 베지어 모양을 그립니다. 이미지가 생성되면 Graphics 클래스에 의해 노출된 Clear 메서드를 사용하여 배경색을 설정합니다.

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 DrawBezier 메서드는 네 개의 Point 구조체로 정의된 이미지 표면에 베지어 스플라인 모양을 그리는 데 사용됩니다. 이 메서드에는 Pen 클래스의 인스턴스 및 네 개의 정렬된 좌표 쌍 또는 네 개의 Point/PointF 구조체 또는 Point/PointF 구조체의 배열이 인수로 사용되는 여러 오버로드가 있습니다. Pen 클래스는 선, 곡선, 도형을 그리는 데 사용되는 객체를 정의합니다. Pen 클래스에는 지정된 색상, 너비 및 브러시로 선을 그리는 여러 오버로드가 있습니다. 마지막으로 이미지를 bmp 파일 형식으로 내보냅니다. 다음 코드 조각은 이미지 표면에 베지어 모양을 그리는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **코어 기능을 사용한 이미지 그리기**
Aspose.PSD는 이미지 생성을 포함한 많은 가치 있는 기능을 제공하는 라이브러리입니다. 이미지의 비트맵 정보를 조작하는 것과 같은 핵심 기능을 사용하거나 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 및 [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)와 같은 고급 기능을 사용하여 다양한 브러시 및 펜을 사용하여 이미지 표면에 모양을 그릴 수 있습니다. Aspose.PSD의 RasterImage 클래스를 사용하면 이미지 영역의 픽셀 정보를 검색하고 조작할 수 있습니다. RasterImage 클래스에는 픽셀 가져오기, 설정 및 이미지 조작을 위한 기타 메서드가 포함되어 있습니다. 파일 생성에 설명된 메서드 중 하나를 사용하여 새 이미지를 만들고, RasterImage 클래스의 인스턴스에 할당합니다. RasterImage 클래스의 LoadPixels 메서드를 사용하여 이미지의 일부의 픽셀 정보를 검색합니다. 픽셀 배열을 얻은 후에는 각 픽셀의 색을 변경하는 방식으로 조작할 수 있습니다. 픽셀 정보를 조작한 후에는 RasterImage 클래스의 SavePixels 메서드를 사용하여 이미지의 원하는 영역에 다시 설정합니다. 다음 코드 조각은 코어 기능을 사용하여 이미지를 그리는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

