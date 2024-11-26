---
title: 이미지 그리기
type: 문서
weight: 10
url: /ko/java/drawing-images/
---

## **선 그리기**
이 예제는 Graphics 클래스를 사용하여 이미지 표면에 선 모양을 그리는 방법을 보여줍니다. 작업을 설명하기 위해 예제는 새 이미지를 생성하고 Graphics 클래스에 의해 노출된 DrawLine 메서드를 사용하여 이미지 표면에 선을 그립니다. 먼저, 높이와 너비를 지정하는 PsdImage를 생성합니다.

이미지가 생성되면 Graphics 클래스에 의해 노출된 Clear 메서드를 사용하여 배경색을 설정합니다. Graphics 클래스의 DrawLine 메서드는 두 점 구조를 연결하는 이미지에 선을 그리는 데 사용됩니다. 이 메서드에는 Pen 클래스의 인스턴스 및 점 또는 Point/PointF 구조체의 좌표 쌍을 인수로 사용하는 여러 개의 오버로드가 있습니다. Pen 클래스는 선, 곡선 및 도형을 그리는 데 사용되는 객체를 정의합니다. Pen 클래스에는 지정된 색상, 너비 및 브러시로 선을 그리기 위한 여러 개의 오버로드된 생성자가 있습니다. SolidBrush 클래스는 특정 색상으로 계속해서 그리는 데 사용됩니다. 마지막으로 이미지가 BMP 파일 형식으로 내보내집니다. 다음 코드 조각은 이미지 표면에 선 모양을 그리는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **타원 그리기**
타원 그리기 예제는 도형 그리기 시리즈의 두 번째 기사입니다. 이미지 표면에 타원 모양을 그리기 위해 Graphics 클래스를 사용합니다. 작업을 설명하기 위해 예제는 새 이미지를 생성하고 Graphics 클래스에 의해 노출된 DrawEllipse 메서드를 사용하여 이미지 표면에 타원 모양을 그립니다. 먼저, 높이와 너비를 지정하는 PsdImage를 생성합니다.

이미지를 생성한 후, Graphics 클래스 객체를 만들고 초기화하고 Clear 메서드를 사용하여 이미지 배경색을 설정합니다. Graphics 클래스의 DrawEllipse 메서드는 바운딩 사각형 구조체로 지정된 이미지 표면에 타원 모양을 그리는 데 사용됩니다. 이 메서드에는 Pen 및 Rectangle/RectangleF 클래스의 인스턴스 또는 좌표 쌍, 높이 및 너비를 인수로 사용하는 여러 개의 오버로드가 있습니다. Pen 클래스는 선, 곡선 및 도형을 그리는 데 사용되는 객체를 정의합니다. Pen 클래스에는 지정된 색상, 너비 및 브러시로 선을 그리기 위한 여러 개의 오버로드된 생성자가 있습니다. Rectangle 클래스는 사각형의 위치와 크기를 나타내는 네 개의 정수 세트를 저장합니다. Rectangle 클래스에는 지정된 크기와 위치로 사각형 구조체를 그리기 위한 여러 개의 오버로드된 생성자가 있습니다. SolidBrush 클래스는 특정 색상으로 계속해서 그리는 데 사용됩니다. 마지막으로 이미지가 BMP 파일 형식으로 내보내집니다. 다음 코드 조각은 이미지 표면에 타원 모양을 그리는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **직사각형 그리기**
이 예제에서는 이미지 표면에 직사각형 모양을 그립니다. 작업을 설명하기 위해 예제는 새 이미지를 생성하고 Graphics 클래스에 의해 노출된 DrawRectangle 메서드를 사용하여 이미지 표면에 직사각형 모양을 그립니다. 먼저, 높이와 너비를 지정하는 PsdImage를 생성합니다. 그런 다음, Graphics 클래스의 Clear 메서드를 사용하여 이미지의 배경색을 설정합니다. 

Graphics 클래스의 DrawRectangle 메서드는 사각형 구조체에 의해 지정된 이미지 표면에 직사각형 모양을 그리는 데 사용됩니다. 이 메서드에는 Pen 및 Rectangle/RectangleF 클래스의 인스턴스 또는 좌표 쌍, 너비 및 높이를 인수로 사용하는 여러 개의 오버로드가 있습니다. Rectangle 클래스는 사각형의 위치와 크기를 나타내는 네 개의 정수 세트를 저장합니다. Rectangle 클래스에는 지정된 크기와 위치로 사각형 구조체를 그리기 위한 여러 개의 오버로드된 생성자가 있습니다. 마지막으로 이미지가 BMP 파일 형식으로 내보내집니다. 다음 코드 조각은 이미지 표면에 직사각형 모양을 그리는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **호 그리기**
도형 그리기 시리즈의 이 세션에서는 이미지 표면에 호 모양을 그립니다. 작업을 설명하기 위해 DrawArc 메서드를 사용하여 BMP 이미지에서 작업을 시연할 것입니다. 먼저, 높이와 너비를 지정하는 PsdImage를 생성합니다. 이미지가 생성되면 Graphics 클래스에 의해 노출된 Clear 메서드를 사용하여 배경색을 설정합니다.

Graphics 클래스의 DrawArc 메서드는 이미지 표면에 호 모양을 그리는 데 사용됩니다. DrawArc는 직사각형 구조체나 좌표 쌍으로 지정된 타원의 일부를 나타냅니다. 이 메서드에는 Pen 클래스 및 Rectangle/RectangleF 구조체의 인스턴스 또는 좌표 쌍, 너비 및 높이를 인수로 사용하는 여러 개의 오버로드가 있습니다. 마지막으로 이미지가 BMP 파일 형식으로 내보내집니다. 다음 코드 조각은 이미지 표면에 호 모양을 그리는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **베지에 곡선 그리기**
이 예제는 Graphics 클래스를 사용하여 이미지 표면에 베지에 곡선 모양을 그리는 방법을 보여줍니다. 작업을 설명하기 위해 예제는 새 이미지를 생성하고 Graphics 클래스에 의해 노출된 DrawBezier 메서드를 사용하여 이미지 표면에 베지에 곡선 모양을 그립니다. 먼저, 높이와 너비를 지정하는 PsdImage를 생성합니다. 이미지가 생성되면 Graphics 클래스에 의해 노출된 Clear 메서드를 사용하여 배경색을 설정합니다.

Graphics 클래스의 DrawBezier 메서드는 네 개의 Point 구조체로 정의된 이미지 표면에 베지에 곡선 모양을 그리는 데 사용됩니다. 이 메서드에는 Pen 클래스의 인스턴스 및 네 순서쌍 좌표 또는 네 Point/PointF 구조체 또는 Point/PointF 구조체 배열을 인수로 사용하는 여러 오버로드가 있습니다. Pen 클래스는 선, 곡선 및 도형을 그리는 데 사용되는 객체를 정의합니다. Pen 클래스에는 지정된 색상, 너비 및 브러시로 선을 그리는 데 사용되는 여러 오버로드된 생성자가 있습니다. 마지막으로 이미지가 BMP 파일 형식으로 내보내집니다. 다음 코드 조각은 이미지 표면에 베지에 곡선을 그리는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **코어 기능을 사용한 이미지 그리기**
Aspose.PSD는 이미지 생성을 포함한 여러 유용한 기능을 제공하는 라이브러리입니다. 이미지의 비트맵 정보를 조작하거나 그래픽 및 그래픽 경로와 같은 고급 기능을 사용하여 다양한 브러시와 펜을 사용하여 이미지 표면에 도형을 그릴 수 있는 코어 기능을 사용하세요. Aspose.PSD의 RasterImage 클래스를 사용하면 이미지 영역의 픽셀 정보를 검색하고 조작할 수 있습니다. RasterImage 클래스에는 이미지 조작을 위한 픽셀 가져오기 및 설정 및 기타 이미지 조작을 위한 메서드 등 전체 코어 그리기 기능이 포함되어 있습니다. Creating Files에 설명된 메서드 중 하나를 사용하여 새 이미지를 만들고 RasterImage 클래스의 인스턴스에 할당하세요. RasterImage 클래스의 LoadPixels 메서드를 사용하여 이미지 일부의 픽셀 정보를 검색하세요. 픽셀 배열이 있는 경우 각 픽셀의 색상을 변경하는 등 조작할 수 있습니다. 픽셀 정보를 조작한 후 RasterImage 클래스의 SavePixels 메서드를 사용하여 이미지의 원하는 영역에 설정하세요. 다음 코드 조각은 코어 기능을 사용하여 이미지를 그리는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
