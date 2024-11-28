---
title: Bilinen Sorunlar
type: docs
weight: 40
url: /tr/net/bilinen-sorunlar/
---

## **.NET Compact Framework**
- Belirli Windows sürümleri, örneğin Windows Mobile 5.0-6.0 gibi belirli Windows sürümlerinde, sertifika ile imzalı (.NET Compact Framework) çekirdek yapıları beklenen şekilde çalışmamakta ve doğru şekilde yüklenememektedir (Bir TypeLoadException hatası oluşmaktadır). Sorunu aşmak için kullanıcının herhangi bir sertifikayı kaldırması ve sonra güncellenmiş yapıyı kullanması gerekmektedir. Lütfen not edin ki bu değişikliği kendi riskinizde yaparsınız ve bu tür bir yapı değişikliği nedeniyle geçerli çalışmayı garanti etmiyoruz. Ayrıca güvenlik tehdidi potansiyeli olduğu için imzasız yapılar göndermiyoruz. Bunun yerine müşterilerimizin, mümkünse, bu tür eski işletim sistemlerini kullanmaktan kaçınmaları ve/veya sertifika imzalama sorunlarını çözen yeni sürümlere veya hizmet paketlerine geçmeleri gerekmektedir.
