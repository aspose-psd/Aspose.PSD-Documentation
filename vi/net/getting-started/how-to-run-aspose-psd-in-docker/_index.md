---
title: Cách Chạy Aspose.PSD trong Docker
type: docs
description: "Chạy Aspose.PSD trong một container Docker cho Linux, Windows Server và bất kỳ hệ điều hành nào."
weight: 90
url: /vi/net/how-to-run-aspose-psd-in-docker/
---

## Điều Kiện Tiên Quyết

- Docker phải được cài đặt trên hệ thống của bạn. Để biết thêm thông tin về cách cài đặt Docker trên Windows hoặc Mac, tham khảo các liên kết trong phần "Xem Thêm".

- Visual Studio 2022.

- NET 6 SDK được sử dụng trong ví dụ.

- Bạn có thể tải dự án mẫu hoàn toàn hoạt động tại https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Ứng Dụng Hello World

Trong ví dụ này, bạn tạo một ứng dụng console Hello World đơn giản mà mở một tệp psd, cập nhật lớp văn bản và vẽ bằng cách sử dụng API Graphics. Ứng dụng đã mô tả có thể được xây dựng và chạy trong Docker.

### Tạo Ứng Dụng Console

Để tạo chương trình Hello World, làm theo các bước dưới đây:
1. Khi Docker đã được cài đặt, đảm bảo rằng nó sử dụng Linux Containers (mặc định). Nếu cần, chọn tùy chọn Chuyển sang Linux containers từ menu Docker Desktop.
1. Trong Visual Studio, tạo ứng dụng console NET 6.<br>
![Hộp thoại dự án ứng dụng console NET 6](create-a-new-project.png)<br>
1. Cài đặt phiên bản Aspose.PSD mới nhất từ NuGet.<br>
![Aspose.PSD trên NuGet](nuget-aspose-psd.png)<br>
1. Vì ứng dụng sẽ chạy trên Linux, bạn có thể cần cài đặt các phông chữ bổ sung. Bạn có thể muốn ttf-mscorefonts-installer.
1. Lưu ý rằng để sử dụng các tính năng vẽ Văn Bản trên Linux, bạn cần thêm các gói sau: apt-transport-https, libgdiplus, libc6-dev. Các lệnh thêm chúng có thể được tìm thấy trong dockerfile.
1. Khi đã thêm tất cả các phụ thuộc cần thiết, viết một chương trình đơn giản mở Tệp PSD, cập nhật Lớp Văn bản và sau đó Vẽ một cái gì đó sử dụng đồ họa:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

Lưu ý rằng để chỉnh sửa các lớp văn bản, bạn cần nhận giấy phép. Bạn có thể nhận giấy phép tạm thời bằng cách sử dụng bài viết sau: https://purchase.aspose.com/temporary-license
 
### Cấu Hình Dockerfile

Bước tiếp theo là tạo và cấu hình Dockerfile.

1. Tạo Dockerfile và đặt nó cạnh tệp giải pháp của ứng dụng của bạn. Giữ tên tệp này không có phần mở rộng (mặc định).
1. Trong Dockerfile, chỉ định:

{{< highlight plain >}}
#Xem https://aka.ms/containerfastmode để hiểu cách Visual Studio sử dụng Dockerfile này để xây dựng hình ảnh của bạn để gỡ lỗi nhanh hơn.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Để sử dụng khả năng cập nhật các lớp văn bản, bạn cần thêm các gói sau vào container của mình
RUN apt-get update
RUN yes | apt-get install -y apt-transport-https
RUN yes | apt-get install -y libgdiplus
RUN yes | apt-get install -y libc6-dev

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build

WORKDIR /src
COPY ["AsposePsdDockerSample/AsposePsdDockerSample.csproj", "AsposePsdDockerSample/"]
RUN dotnet restore "AsposePsdDockerSample/AsposePsdDockerSample.csproj"
COPY . .
WORKDIR "/src/AsposePsdDockerSample"
RUN dotnet build "AsposePsdDockerSample.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "AsposePsdDockerSample.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "AsposePsdDockerSample.dll"]
{{< /highlight >}}

Trên đây là một Dockerfile đơn giản, chứa các hướng dẫn sau:

- Image SDK sẽ được sử dụng. Ở đây là hình ảnh Microsoft .Net 6. Docker sẽ tải nó khi xây dựng được chạy. Phiên bản SDK được chỉ định là một thẻ.
- Sau đó, thêm các phụ thuộc để vẽ văn bản.
- Sau đó, bạn có thể cần cài đặt Fonts vì hình ảnh SDK chứa rất ít Fonts. Bạn cũng có thể sử dụng Fonts địa phương được sao chép vào hình ảnh Docker.
- Thư mục làm việc, được chỉ định trong dòng tiếp theo.
- Lệnh sao chép mọi thứ vào container, xuất bản ứng dụng và chỉ định điểm nhập.

### Xây Dựng và Chạy Ứng Dụng trong Docker

#### Sử Dụng Visual Studio
Cách đơn giản nhất để thử Aspose.PSD trong Docker là mở Visual Studio và triển khai ứng dụng bằng Docker support
![Chạy ứng dụng mẫu Aspose.PSD trong docker bằng Visual Studio](psd-vs-run-using-docker-support.png)

#### Sử Dụng Dòng Lệnh
Ứng dụng có thể được xây dựng và chạy trong Docker bằng cách sử dụng dòng lệnh. Mở dòng lệnh yêu thích của bạn, thay đổi thư mục đến thư mục chứa ứng dụng (thư mục chứa tệp giải pháp và Dockerfile) và chạy lệnh sau:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

Lần đầu tiên lệnh này được thực thi có thể mất thời gian hơn, vì Docker cần tải xuống các hình ảnh cần thiết. Khi lệnh trước đã hoàn tất, chạy lệnh sau:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Chú ý đến đối số mount, vì như đã đề cập trước, một thư mục trên máy chủ được gắn vào thư mục của container, để dễ dàng xem kết quả của việc thực thi ứng dụng. Đường dẫn trong Linux phân biệt chữ hoa chữ thường.

{{% /alert %}}


## Ví Dụ Thêm

Để biết thêm ví dụ về cách bạn có thể sử dụng Aspose.PSD trong Docker, hãy xem [ví dụ](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Xem Thêm

- [Cài Đặt Docker Desktop trên Windows](https://docs.docker.com/docker-for-windows/install/)
- [Cài Đặt Docker Desktop trên Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Tùy chọn [Chuyển sang Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Thông tin thêm về [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
