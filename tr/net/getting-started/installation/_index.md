---
title: Kurulum
type: dokümantasyon
weight: 50
url: /tr/net/kurulum/
description: NuGet veya Package Manager Console kullanarak PSD dosya biçimi kitaplığını yükleyin.
---

## **Aspose.PSD'u .NET Üzerinden NuGet ile Yükleme**
NuGet, Aspose API'lerini .NET için indirip yüklemenin en kolay yoludur. Microsoft Visual Studio'yu açın ve NuGet paket yöneticisine erişin. Arama çubuğuna "aspose" yazarak istediğiniz Aspose API'sini bulun. "Yükle" ye tıklayarak seçilen API indirilir ve projenize referans eklenir.

![todo:image_alt_text](installation_1.png)

## **Aspose.PSD'yi Package Manager Console Kullanarak Yükleme veya Güncelleme**
Aspose.PSD API'sini [paket yöneticisi konsolu](https://www.nuget.org/packages/Aspose.psd/) kullanarak referans olarak eklemek için aşağıdaki adımları takip edebilirsiniz:

1. Visual Studio'da çözümünüzü/projenizi açın.
1. Araçlar -> Kütüphane Paket Yöneticisi -> Paket Yöneticisi Konsolu'nu açmak için menüden seçin.

![todo:image_alt_text](installation_2.png)

“**Install-Package Aspose.Psd**” komutunu yazın ve Enter'a basarak en son tam sürümü uygulamanıza yükleyin. Ayrıca komuta "**-prerelease**" takısını ekleyerek en son sürümün yamaları da yüklenebilir.

![todo:image_alt_text](installation_3.png)

İndirme işleminin devam ettiğini gösteren **"Aspose.PSD Yükleniyor"** ipucunu konsol penceresinin alt kısmında göreceksiniz.

![todo:image_alt_text](installation_4.png)

İndirme tamamlandığında aşağıdaki onay mesajlarını göreceksiniz. [Aspose EULA](https://company.aspose.com/legal/eula) ile ilgili değilseniz, URL'de referans verilen lisansı okumanız iyi bir fikir olabilir.

![todo:image_alt_text](installation_5.png)

Artık Aspose.PSD'nin başarıyla uygulamanıza eklenip referanslandığını görmelisiniz.

![todo:image_alt_text](installation_6.png)

Paket yöneticisi konsolunda, **“Update-Package Aspose.Psd”** komutunu kullanarak Aspose.Psd paketindeki güncellemeleri kontrol edip varsa yükleyebilirsiniz. Ayrıca en son sürümü güncellemek için "-prerelease" takısını ekleyebilirsiniz.
## **Paylaşılan Sunucu Ortamında Çalışırken Dikkat Edilmesi Gerekenler**
Tüm Aspose .NET bileşenleriyle Tam Güven izin setiyle çalışması önerilir. Çünkü Aspose .NET bileşeni bazen kayıt defteri ayarlarına ve sanal dizin dışındaki dosyalara erişim sağlaması gerekebilir, örneğin fontları okurken vb. Ayrıca, Aspose.NET bileşenleri, bazı durumlarda çalışabilmek için Tam Güven izinlerine ihtiyaç duyan çekirdek .NET sistem sınıflarına dayanmaktadır.

Farklı şirketlerden gelen uygulamaları barındıran İnternet Hizmet Sağlayıcıları genellikle Orta Güvenlik Seviyesi'ni zorlarlar. .NET 2.0 durumunda, böyle bir güvenlik seviyesi, Aspose.Words'ün düzgün çalışmasını etkileyebilecek aşağıdaki kısıtlamaları belirleyebilir.

- **RegistryPermission** mevcut değildir. Bu, belgeleri oluştururken yüklü fontları sıralamak için kayıt defterine erişemeyeceğiniz anlamına gelir.
- **FileIOPermission** kısıtlıdır. Bu, yalnızca uygulamanızın sanal dizin hiyerarşisindeki dosyalara erişebileceğiniz anlamına gelir. Bu potansiyel olarak, dışa aktarma sırasında fontlar okunamaz demektir.

Yukarıda belirtilen nedenlerden dolayı, Aspose.PSD'nin Tam Güven izinleriyle çalışması önerilir. Farklı görevleri yerine getirirken kütüphanenin bazı özelliklerinin Orta güvenlikte çalışırken bazılarının çalışmadığını fark edebilirsiniz (örneğin, işleme örneği) bu çoğunlukla GDI+ görüntü işleme çağrılarından kaynaklanabilir.
## **.NET Core DLL'leri MSI paketi yoluyla Yükleme**
**Lütfen dikkat:** MSI paketi yoluyla yüklenen .Net Standard dll'sini kullanıyorsanız, .Net Standard sürümü ile çalışabilmesi için gerekli bağımlılıkları eklemelisiniz.

|**Görsel Studio bağımlılıkları ekran görüntüsü**|**CsProj dosya parçası:**|
| :- | :- |
|![todo:image_alt_text](installation_7.png)|<ItemGroup><p></p><p>`    `<PackageReference Include="System.Drawing.Common" Version="4.5.1" /></p><p>`    `<PackageReference Include="System.Text.Encoding.CodePages" Version="4.5.0" /></p><p></p></ItemGroup>|
## **Sistem Gereksinimleri**
### **Desteklenen İşletim Sistemleri:**
- Microsoft Windows 2000 Professional ve Sunucu (SP2 önerilir)
- Microsoft Windows XP Professional ve Ev Sürümü
- Microsoft Windows 2003 Sunucu
- Microsoft Windows Vista
- Microsoft Windows 2008 Sunucu
- Microsoft Windows 2008 Sunucu R2
- Microsoft Windows 7
- Microsoft Windows 8
- Microsoft Windows 10
- Microsoft Windows 11
### **Desteklenen Platformlar:**
- Window formları
- Web formları
- Visual Studio 2005
- Visual Studio 2008
- Visual Studio 2010
- Visual Studio 2012
- Visual Studio 2013
- Visual Studio 2015
- Visual Studio 2017
- Visual Studio 2019
- Visual Studio 2022

Aspose.PSD yukarıda listelenen işletim sistemlerinin x86 ve x64 sürümleri için çalışır.
### **Desteklenen Çerçeveler:**
Aspose.PSD .NET için aşağıdaki .NET çerçevelerini destekler:

- .NET Framework sürümü 2.0 veya daha yeni
- .NET Standard 2.0
