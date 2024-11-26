---
title: PSD, PSB ve AI dosyalarını açın ve bunları PDF, PNG, TIFF, GIF, BMP, JPEG formatlarına dönüştürün
weight: 100
type: docs
description: Örnek PSD, PSB ve AI dosyalarının diğer formatlara dönüştürülmesi
keywords: [psd açma, ai açma, psb açma, png'e dönüştürme, pdf'e dönüştürme, jpeg'e dönüştürme, tiff'e dönüştürme, psd api, python, kod örneği]
url: tr/python-net/acik-psd-psb-ai-resimlerini-pdf-jpeg-png-tiff-bmp-gif-bmp-olarak-donustur/
---

## **Genel Bakış**
PSD, PSB ve AI dosyalarını farklı formatlara dönüştürmek için Python'da Aspose.PSD kütüphanesini kullanabilirsiniz. Bu kütüphane, dönüştürme sürecini özelleştirmek için çeşitli seçenekler ve ayarlar sunar.

İlk olarak, gerekli sınıfları ve modülleri Aspose.PSD kütüphanesinden içe aktarmanız gerekir. Kodu çalıştırmadan önce kütüphaneyi kurduğunuzdan emin olun.

Bu kodda, PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB ve PSD gibi farklı formatlar için çeşitli seçenekleri tanımlıyoruz. Bu seçenekler çıktı dosyasını gereksinimlerinize göre özelleştirmenizi sağlar.

Daha sonra, dosya uzantılarını kendi kaydetme seçeneklerine eşleyen bir formats adlı sözlük tanımlarız.

PSD dosyasını diğer formatlara dönüştürmek için, PsdImage.load() yöntemini kullanarak PSD dosyasını yüklemeniz ve ardından formatlar sözlüğünde döngü oluşturmanız gerekir. Her bir formatta çıktı dosya adını belirtin ve resmi image.save() yöntemini kullanarak kaydedin.

Benzer şekilde, bir AI dosyasını diğer formatlara dönüştürmek için, AiImage.load() yöntemini kullanarak AI dosyasını yükleyin ve formatlar sözlüğünde döngü oluşturun. Çıktı dosya adını belirtin ve resmi image.save() yöntemini kullanarak kaydedin.

Kaynak PSD ve AI dosyaları için doğru dosya yollarını sağladığınızdan emin olun.

Bu kadar! Artık Aspose.PSD'yi Python için kullanarak PSD, PSB ve AI dosyalarını çeşitli formatlara dönüştürebilirsiniz.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokümantasyon-Python-Aspose-Psd-acik-psd-psb-ai-resimlerini-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
