---
title: Cara Menjalankan Aspose.PSD di Docker
type: docs
description: "Jalankan Aspose.PSD di dalam kontainer Docker untuk Linux, Windows Server, dan OS lainnya."
weight: 90
url: /id/net/cara-menjalankan-aspose-psd-di-docker/
---

## Persyaratan

- Docker harus terpasang di sistem Anda. Untuk informasi tentang cara menginstal Docker di Windows atau Mac, lihat tautan di bagian "Lihat Juga".

- Visual Studio 2022.

- NET 6 SDK digunakan dalam contoh ini.

- Anda dapat mengunduh proyek contoh yang sepenuhnya berfungsi di https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Aplikasi Hello World

Pada contoh ini, Anda akan membuat aplikasi konsol Hello World sederhana yang membuka file psd, memperbarui lapisan teks, dan menggambar menggunakan API Grafis. Aplikasi yang dijelaskan dapat dibangun dan dijalankan di Docker.

### Membuat Aplikasi Konsol

Untuk membuat program Hello World, ikuti langkah-langkah berikut:
1. Setelah Docker terinstal, pastikan bahwa Anda menggunakan Kontainer Linux (default). Jika perlu, pilih opsi Beralih ke kontainer Linux dari menu Docker Desktop.
1. Di Visual Studio, buat aplikasi konsol NET 6.<br>
![Dialog proyek aplikasi konsol NET 6](create-a-new-project.png)<br>
1. Pasang versi terbaru Aspose.PSD dari NuGet.<br>
![Aspose.PSD di NuGet](nuget-aspose-psd.png)<br>
1. Karena aplikasi akan dijalankan di Linux, Anda mungkin perlu menginstal font tambahan. Anda dapat menggunakan ttf-mscorefonts-installer.
1. Perhatikan, untuk menggunakan Fitur Penyajian Teks di Linux, Anda perlu menambahkan paket-paket berikut: apt-transport-https, libgdiplus, libc6-dev. Perintah untuk menambahkannya dapat ditemukan di dokfile.
1. Setelah semua dependensi yang diperlukan ditambahkan, tulis program sederhana yang membuka File PSD, memperbarui Lapisan Teks, lalu Menggambar sesuatu menggunakan grafis:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs" >}}

Perhatikan bahwa untuk mengedit lapisan teks Anda perlu mendapatkan lisensi. Anda dapat mendapatkan lisensi sementara, menggunakan artikel berikut: https://purchase.aspose.com/temporary-license
 
### Mengonfigurasi Dockerfile

Langkah berikutnya adalah membuat dan mengonfigurasi Dockerfile.

1. Buat Dockerfile dan letakkan di sebelah file solusi aplikasi Anda. Simpan nama file ini tanpa ekstensi (default).
1. Di Dockerfile, tentukan:

{{< highlight plain >}}
#Lihat https://aka.ms/containerfastmode untuk memahami bagaimana Visual Studio menggunakan Dockerfile ini untuk membangun citra Anda agar memungkinkan debugging lebih cepat.

FROM mcr.microsoft.com/dotnet/runtime:6.0 SEBAGAI dasar
WORKDIR /app

# Untuk menggunakan kemampuan memperbarui lapisan teks, Anda perlu menambahkan paket-paket berikut ke kontainer Anda
RUN apt-get update
RUN yes | apt-get install -y apt-transport-https
RUN yes | apt-get install -y libgdiplus
RUN yes | apt-get install -y libc6-dev

FROM mcr.microsoft.com/dotnet/sdk:6.0 SEBAGAI build

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

Di atas adalah Dockerfile sederhana yang berisi instruksi berikut:

- Citra SDK yang akan digunakan. Di sini adalah citra Microsoft .Net 6. Docker akan mengunduhnya ketika pembangunan dijalankan. Versi SDK ditentukan sebagai tag.
- Kemudian Anda menambahkan dependensi untuk merender teks.
- Setelah itu, Anda mungkin perlu menginstal Font karena citra SDK berisi sedikit sekali font. Anda juga dapat menggunakan font lokal yang disalin ke citra docker.
- Direktori kerja, yang ditentukan dalam baris berikutnya.
- Perintah untuk menyalin semua ke kontainer, menerbitkan aplikasi, dan menentukan titik masuk.

### Membangun dan Menjalankan Aplikasi di Docker

#### Menggunakan Visual Studio
Cara termudah untuk mencoba Aspose.PSD di Docker adalah membuka Visual Studio dan menjalankan aplikasi menggunakan dukungan Docker.
![Jalankan aplikasi contoh Aspose.PSD di docker menggunakan Visual Studio](psd-vs-run-using-docker-support.png)

#### Menggunakan Command Prompt
Aplikasi dapat dibangun dan dijalankan di Docker menggunakan command prompt. Buka command prompt favorit Anda, ubah direktori ke folder dengan aplikasi (folder di mana file solusi dan Dockerfile ditempatkan) dan jalankan perintah berikut:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

Saat pertama kali perintah ini dijalankan, mungkin akan memakan waktu lebih lama, karena Docker perlu men-download citra yang diperlukan. Setelah perintah sebelumnya selesai, jalankan perintah berikut:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Perhatikan argumen mount, karena, seperti yang disebutkan sebelumnya, folder di mesin host dipasang ke folder kontainer, untuk dengan mudah melihat hasil menjalankan aplikasi. Path di Linux bersifat case sensitive.

{{% /alert %}}


## Contoh Lainnya

Untuk contoh-contoh lebih lanjut tentang cara Anda dapat menggunakan Aspose.PSD di Docker, lihat [contoh](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Lihat Juga

- [Instal Docker Desktop di Windows](https://docs.docker.com/docker-for-windows/install/)
- [Instal Docker Desktop di Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Opsi [Beralih ke kontainer Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Informasi tambahan tentang [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
