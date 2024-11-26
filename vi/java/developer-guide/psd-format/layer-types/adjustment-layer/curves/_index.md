---
title: Lớp Điều chỉnh đường cong
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/curves/
---

# Làm việc với lớp điều chỉnh đường cong trong Photoshop bằng Java

Mục tiêu của bài viết này là để thể hiện khả năng của thư viện Aspose.PSD cho Java khi **làm việc với các lớp điều chỉnh đường cong** trong tài liệu Adobe® Photoshop®. Thư viện hoàn toàn tự động. Do đó, nó hoạt động mà không cần cài đặt trình chỉnh sửa ảnh Photoshop. [Danh sách đầy đủ các tính năng](https://docs.aspose.com/psd/java/features/) có thể được tìm thấy trong cơ sở kiến thức của chúng tôi. Được rồi, quay lại với đường cong.

## Tổng quan API

Công cụ Đường cong có thể được đại diện bằng một đường (đường cong) trên một đồ thị với điểm nhấn ở góc phải phía trên và bóng đổ ở góc phải dưới.

Thư viện cung cấp API để làm việc với đường cong, cụ thể là lớp [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Tuy nhiên, lớp này có **hai phương pháp hoàn toàn khác nhau** để làm việc với đường cong. Do đó, nó có thể được chỉnh sửa ở một trong hai chế độ tại một thời điểm:

- Liên tục (đường cong được đại diện bằng một đường cong với các điểm ở những nơi cong)
- Rời rạc (đường cong được đại diện bằng một đường chấm chấm)

Vì vậy, thư viện có hai cách để chỉnh sửa đường cong bằng cách sử dụng [quản lý liên tục](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) và [quản lý rời rạc](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) tương ứng. Tiếp theo, chúng tôi sẽ giải thích cách sử dụng từng cái trên một ví dụ cụ thể.

## Điều chỉnh màu sắc và độ tương phản bằng Quản lý Liên tục của Đường cong

[Quản lý Liên tục của Đường cong](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **cấu hình các điểm cong của một đường cong liên tục** cho kênh tổng hợp (RGB) cũng như cho từng kênh màu cụ thể. Để minh họa, một số điều chỉnh Đường cong (a) sẽ được áp dụng cho một bức ảnh đã được làm tối của dàn nhạc (b) để thu được một bức ảnh sáng hơn với nhiều màu ấm hơn (c):

![Hình ảnh Lớp Điều chỉnh Đường cong 1](curves-psd-adjustment-layer-figure-1.png)

Vì có hai người quản lý, cần chọn rõ ràng một người (quản lý liên tục trong trường hợp này), trước khi bắt đầu sử dụng nó. Sau đó, chúng ta có thể thêm trực tiếp các điểm trên đường cong tại tọa độ nhất định cho các kênh màu mong muốn (tổ hợp RGB, đỏ và lam tương ứng) để tái tạo hình dạng của đường cong:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Gốc tọa độ nằm ở góc dưới bên trái. Giá trị tọa độ cao nhất của một điểm bị giới hạn theo kiểu dữ liệu (byte) và bằng 255 (127 cho kiểu có dấu).

Còn một số [phương pháp khác](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) bạn có thể sử dụng.

## Điều chỉnh độ tương phản sử dụng Quản lý Rời rạc của Đường cong

Quản lý Rời rạc của Đường cong cũng cho phép đặt điểm trên đường cong (thay đổi màu sắc và độ tương phản thực sự), nhưng khác biệt là họ thực hiện nó theo cách khác. Đầu tiên, **đường cong bao gồm các điểm** hoặc chấm (không phải là một đường liền mạch). Thứ hai, người quản lý này **không đặt một điểm nào đó ở bất kỳ vị trí nào** trên đồ thị. Thay vào đó, nó **di chuyển điểm lên hoặc xuống** với phạm vi giá trị giữa 255 và 0 tương ứng. Mặc định, giá trị của các điểm đường cong tăng các mức tăng dần để tạo hình một đường cong có góc 45 độ.

Vậy, với điều đó trong đầu, dễ dàng tái tạo bản thiết lập &quot;Âm (RBG)&quot; của Photoshop (a) và áp dụng nó vào một bức ảnh xám của một thung lũng (b) để cuối cùng có một biểu diễn âm bản của thung lũng (c).

![Hình ảnh Lớp Điều chỉnh Đường cong 2](curves-psd-adjustment-layer-figure-2.png) Trước hết, đừng quên chọn người quản lý tương ứng để có thể sử dụng nó và sau đó đặt giá trị điểm trên đường cong theo thứ tự giảm dần bắt đầu từ 255 đến 0 cho mỗi điểm trên đường cong (tổng cộng là 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Người quản lý cũng cung cấp một số [phương pháp khác](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) để quản lý đường cong.

## Kết luận

Trong bài viết này, chúng ta đã biết cách làm việc với các lớp điều chỉnh đường cong trong tài liệu Photoshop bằng việc sử dụng Aspose.PSD cho Java theo hai cách hoàn toàn khác nhau (quản lý liên tục và rời rạc).
