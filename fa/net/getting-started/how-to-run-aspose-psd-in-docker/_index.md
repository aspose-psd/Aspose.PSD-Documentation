---
title: چگونگی اجرای Aspose.PSD در Docker
type: docs
description: "اجرای Aspose.PSD در یک کانتینر Docker برای لینوکس، ویندوز سرور و هر سیستم عامل دیگر."
weight: 90
url: /fa/net/how-to-run-aspose-psd-in-docker/
---

## پیش‌نیازها

- باید Docker روی سیستم شما نصب باشد. برای اطلاعات بیشتر در مورد نصب Docker بر روی ویندوز یا مک، به لینک‌های موجود در بخش "منابع مرتبط" مراجعه کنید.

- ویژوال استودیو ۲۰۲۲.

- NET 6 SDK در مثال استفاده شده است.

- شما می‌توانید نمونه پروژه کاملاً کاربردی را از https://github.com/aspose-psd/Aspose.PSD-Docker-Sample دانلود کنید.


## اپلیکیشن سلام دنیا

در این مثال، یک اپلیکیشن مشابه سلام دنیا ایجاد می‌کنید که یک فایل psd را باز می‌کند، لایه متن را به‌روزرسانی می‌کند و از طریق رابط برنامه کاربری گرافیکی نقاشی می‌کند. برنامه توصیف‌شده می‌تواند در Docker ساخته و اجرا شود.

### ایجاد اپلیکیشن کنسول

برای ایجاد برنامه سلام دنیا، مراحل زیر را دنبال کنید:
1. یک بار که Docker نصب شده است، مطمئن شوید که از کانتینرهای لینوکس استفاده می‌کند (پیش‌فرض). در صورت نیاز، گزینه Switch to Linux containers را از منوی Docker Desktop انتخاب کنید.
1. در ویژوال استودیو، یک برنامه کنسول NET 6 ایجاد کنید.<br>
![جعبه‌گفتگوی ایجاد برنامه کنسول NET 6](create-a-new-project.png)<br>
1. آخرین نسخه Aspose.PSD را از NuGet نصب کنید.<br>
![Aspose.PSD در NuGet](nuget-aspose-psd.png)<br>
1. از آنجایی که برنامه بر روی لینوکس اجرا خواهد شد، ممکن است نیاز به نصب فونت‌های اضافی باشد. ممکن است ttf-mscorefonts-installer را تحویل بگیرید.
1. توجه داشته باشید که برای استفاده از ویژگی‌های رندرینگ متن در لینوکس، باید بسته‌های زیر را اضافه کنید: apt-transport-https، libgdiplus، libc6-dev. دستورات اضافه کردن آنها می‌تواند در فایل داکر پیدا شود.
1. هنگامی که تمام وابستگی‌های مورد نیاز اضافه شدند، برنامه‌ای ساده بنویسید که فایل PSD را باز کند، لایه متن را به‌روز کند و سپس چیزی را با استفاده از گرافیک رسم کند:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

توجه کنید که برای ویرایش لایه‌های متن، باید لایسنس را بگیرید. می‌توانید لایسنس موقت بگیرید، از مقاله زیر استفاده کنید: https://purchase.aspose.com/temporary-license

### پیکربندی یک Dockerfile

مرحله بعد ایجاد و پیکربندی فایل Dockerfile است.

1. Dockerfile را ایجاد کرده و کنار فایل راه‌حل برنامه خود قرار دهید. این نام فایل بدون پسوند باقی بماند (پیش‌فرض).
1. در Dockerfile، مشخص کنید:

{{< highlight plain >}}
#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# برای استفاده از قابلیت به‌روزرسانی لایه‌های متن، باید بسته‌های زیر را به کانتینر خود اضافه کنید
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

موارد فوق یک Dockerfile ساده است، که شامل دستورات زیر است:

- تصویر SDK برای استفاده. اینجا تصویر Microsoft .NET 6 استفاده شده است. Docker آن را هنگام اجرای دستور ساخته دانلود خواهد کرد. نسخه SDK با برچسب مشخص شده است.
- سپس وابستگی‌ها برای رندر کردن متن را اضافه کنید.
- سپس ممکن است نیاز به نصب فونت‌ها داشته باشید زیرا تصویر SDK حاوی تعداد کمی از فونت‌ها است. همچنین می‌توانید از فونت‌های محلی کپی‌شده به تصویر Docker استفاده کنید.
- دایرکتوری کاری که در خط بعد مشخص شده است.
- دستور کپی هر چیزی به کانتینر، انتشار برنامه و مشخص‌کردن نقطه ورود.

### ساخت و اجرا کردن برنامه در Docker

#### استفاده از ویژوال استودیو
ساده‌ترین راه برای امتحان Aspose.PSD در Docker، باز کردن ویژوال استودیو و اجرای برنامه با پشتیبانی از Docker است
![اجرای نمونه برنامه Aspose.PSD در داکر با استفاده از ویژوال استودیو](psd-vs-run-using-docker-support.png)

#### استفاده از خط فرمان
برنامه می‌تواند با استفاده از خط فرمان در Docker ساخته و اجرا شود. دستورات زیر را بر روی خط فرمان مورد علاقه خود اجرا کنید. به پوشه‌ای که حاوی برنامه است (پوشه‌ای که فایل راه‌حل و فایل Dockerfile در آن قرار دارند) بروید و دستور زیر را اجرا کنید:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

اولین بار که این دستور اجرا می‌شود ممکن است زمان بیشتری بگیرد، چون Docker باید تصاویر مورد نیاز را دانلود کند. وقتی دستور قبلی اجرا شد، دستور زیر را اجرا کنید:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

به مسیر متصل شوید، زیرا، همان‌طور که از قبل گفته شد، یک پوشه روی ماشین میزبان به پوشه کانتینر نصب می‌شود تا به راحتی نتایج اجرای برنامه را ببینید. مسیرها در لینوکس حساس به بزرگی و کوچکی حروف هستند.

{{% /alert %}}


## نمونه‌های بیشتر

برای دیدن نمونه‌های بیشتری از چگونگی استفاده از Aspose.PSD در Docker، به [نمونه‌ها](https://github.com/aspose-psd/Aspose.PSD-for-.NET) مراجعه کنید.


## منابع مرتبط

- [نصب Docker Desktop روی ویندوز](https://docs.docker.com/docker-for-windows/install/)
- [نصب Docker Desktop روی مک](https://docs.docker.com/docker-for-mac/install/)
- [ویژوال استودیو 2022، NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- گزینه [Switch to Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- اطلاعات اضافی در مورد [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

