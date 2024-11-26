---
title: 압축된 이미지 위에 그리기시 성능 저하 방지
type: docs
weight: 10
url: /ko/net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **압축된 이미지 위에 그리기시 성능 저하 방지**
가끔 압축된 이미지 위에 매우 복잡한 그래픽 작업을 수행하고 싶은 경우가 있습니다. Aspose.PSD가 이미지를 압축하고 풀어야 하는 경우 성능 저하가 발생할 수 있습니다. 또한 압축된 이미지 위에 그리기도 성능 저하를 일으킬 수 있습니다.

### **해결책**
성능 저하를 방지하려면 그래픽 작업을 수행하기 전에 이미지를 압축 해제되거나 원시 형식으로 변환하는 것을 권장합니다.

### **파일 경로 사용**
다음 예에서 PSD 이미지가 원시 형식(압축 없음)으로 변환되고 디스크에 저장됩니다. 그리기 작업이 수행되기 전에 압축 해제된 이미지가 다시로드됩니다. BMP 및 GIF 파일에도 동일한 기술이 적용됩니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}

### **스트림 객체 사용**
다음 코드 스니펫에서는 PSD 이미지가 메모리스트림을 사용하여 원시 형식(압축 없음)으로 변환되고 디스크에 저장되는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
