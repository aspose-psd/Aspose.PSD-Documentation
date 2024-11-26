---
title: "วิธีการรัน Aspose.PSD ใน Docker"
type: docs
description: "รัน Aspose.PSD ในคอนเทนเนอร์ Docker สำหรับ Linux, Windows Server และ OS ใด ๆ"
weight: 90
url: /th/net/how-to-run-aspose-psd-in-docker/
---

## ข้อกำหนดพื้นฐาน

- ต้องมี Docker ติดตั้งในระบบของคุณ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการติดตั้ง Docker บน Windows หรือ Mac โปรดอ้างอิงที่ลิงก์ในส่วน "ดูเพิ่มเติม".

- Visual Studio 2022.

- NET 6 SDK ใช้ในตัวอย่าง.

- คุณสามารถดาวน์โหลดโปรเจกต์ตัวอย่างที่ทำงานอย่างสมบูรณ์ได้ที่ https://github.com/aspose-psd/Aspose.PSD-Docker-Sample

## แอปพลิเคชัน Hello World

ในตัวอย่างนี้ คุณจะสร้างแอปพลิเคชันคอนโซล Hello World ที่เปิดไฟล์ psd, อัปเดตเลเยอร์ข้อความ และวาดโดยใช้ Graphics API เข้าถึงแอปพลิเคชันที่ถูกบริหารจัดการและรันใน Docker

### การสร้างแอปพลิเคชันคอนโซล

เพื่อสร้างโปรแกรม Hello World สามารถทำตามขั้นตอนด้านล่าง:
1. เมื่อ Docker ถูกติดตั้ง ตรวจสอบให้แน่ใจว่ามันใช้ Linux Containers (ค่าเริ่มต้น) หากจำเป็นให้เลือกตัวเลือก Switch to Linux containers จากเมนู Docker Desktops
1. เปิด Visual Studio และสร้างแอปพลิเคชันคอนโซล .NET 6<br>
![กว้าง-Ready console application project dialog](create-a-new-project.png)<br>
1. ติดตั้ง Aspose.PSD เวอร์ชันล่าสุดจาก NuGet<br>
![Aspose.PSD on NuGet](nuget-aspose-psd.png)<br>
1. เนื่องจากแอปพลิเคชันจะรันบน Linux คุณอาจจำเป็นต้องติดตั้งฟอนต์เพิ่มเติม คุณอาจต้องการติดตั้ง ttf-mscorefonts-installer
1. โปรดทราบ ในการใช้คุณลักษณะการแสดงข้อความบน Linux คุณต้องเพิ่มชุดแพคเกจต่อไปนี้: apt-transport-https, libgdiplus, libc6-dev คำสั่งในการเพิ่มหาได้ในไฟล์ dcokerfile
1. เมื่อเพิ่มสารสำคัญทุกอย่างแล้ว เขียนโปรแกรมง่าย ๆ ที่เปิดไฟล์ PSD อัปเดตเลเยอร์ข้อความ แล้ววาดบางสิ่งโดยใช้กราฟิก:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

โปรดทราบว่าเพื่อแก้ไขเลเยอร์ข้อความ คุณต้องรับใบอนุญาต คุณสามารถรับใบอนุญาตชั่วคราวได้ โดยใช้บทความต่อไปนี้: https://purchase.aspose.com/temporary-license

### การกำหนด Dockerfile

ขั้นตอนถัดไปคือการสร้างและกำหนดค่า Dockerfile

1. สร้าง Dockerfile และวางไว้ข้างๆ ไฟล์โซลูชันของแอปพลิเคชันของคุณ นี่คือค่าเริ่มต้น
1. ใน Dockerfile ระบุ:

{{< highlight plain >}}
#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# เพื่อใช้ความสามารถในการอัปเดตเลเยอร์ข้อความ คุณต้องเพิ่มแพ็กเกจต่อไปนี้ลงในคอนเทนเนอร์ของคุณ
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

ข้างต้นเป็น Dockerfile ที่เรียบง่าย ประกอบด้วยคำบรรยายต่อไปนี้:

- รูปภาพ SDK ที่จะใช้ ที่นี่คือรูปเวอร์ชั่น Microsoft .NET 6 Docker จะดาวน์โหลดเมื่อเรียกใช้การสร้าง ระบุเป็นแท็กเวอร์ชั่น SDK
- จากนั้นเพิ่มลงไปยังบริเวณเพื่อแสดงข้อความทั้งหมด
- หลังจากนั้น คุณอาจต้องติดตั้งฟอนต์ เนื่องจากภาพ SDK มีเพียงเล็กน้อย นอกจากนี้คุณยังสามารถใช้ฟอนต์ท้องถิ่นที่คัดลอกลง Docker image
- ไดเร็กทอรีการทำงาน ที่ระบุไว้ในบรรทัดถัดไป
- คำสั่งที่เป็นการคัดลอกทุกอย่างไปยังคอนเทนเนอร์ การเผยแพร่แอปพลิเคชัน และระบุจุดเข้างาน

### การสร้างและรันแอปพลิเคชันใน Docker

#### การใช้ Visual Studio
วิธีที่ง่ายที่สุดที่จะลอง Aspose.PSD ใน Docker คือเปิด Visual Studio และเปิดแอปพลิเคชันโดยใช้การรองรับ Docker
![การรัน Aspose.PSD app ตัวอย่างใน Docker โดยใช้ Visual Studio](psd-vs-run-using-docker-support.png)

#### การใช้ Command Prompt
แอปพลิเคชันสามารถสร้างและรันใน Docker โดยใช้ Command Prompt เปิด Command Prompt ที่คุณชอบ และเปลี่ยนไปยังไดเร็กทอรีที่มีแอปพลิเคชัน (โฟลเดอร์ที่มีไฟล์โซลูชันและ Dockerfile) และรันคำสั่งต่อไปนี้:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

ครั้งแรกที่คำสั่งนี้ถูกดำเนินการ อาจใช้เวลานานกว่าเนื่องจาก Docker ต้องดาวน์โหลดรูปภาพที่ต้องการ หลังจากที่การดำเนินการก่อนหน้าเสร็จสิ้นลงให้รันคำสั่งต่อไปนี้:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}}

ให้สนใจถึงอาร์กิวเมนต์การติดตั้ง เนื่องจากเช่นที่กล่าวไว้ก่อนหน้า โฟลเดอร์บนเครื่องโฮสต์ถูกติดตั้งลงในโฟลเดอร์ของคอนเทนเนอร์ เพื่อให้สามารถดูผลการกระทำของแอปพลิเคชันได้ง่าย จำเป็นต้องมีการตรวจสอบการใช้ PATH ใน Linux ที่ต้องระบุพิมพ์ใหญ่และพิมพ์เล็ก

{{% /alert %}}

## ตัวอย่างเพิ่มเติม

สำหรับตัวอย่างเพิ่มเติมเกี่ยวกับวิธีที่คุณสามารถใช้ Aspose.PSD ใน Docker โปรดดูที่ [ตัวอย่าง](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

## ดูเพิ่มเติม

- [ติดตั้ง Docker Desktop บน Windows](https://docs.docker.com/docker-for-windows/install/)
- [ติดตั้ง Docker Desktop บน Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- [เปลี่ยนเป็น Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) option
- ข้อมูลเพิ่มเติมเกี่ยวกับ [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
