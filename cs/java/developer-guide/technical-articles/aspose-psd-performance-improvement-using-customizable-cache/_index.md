---
title: Zlepšení výkonu Aspose.PSD pomocí upravitelné cache
type: docs
weight: 30
url: /cs/java/aspose-psd-zlepseni-vykonu-pomoci-upravitelne-cache/
---

## **Zlepšení výkonu pomocí upravitelné Cache**
Aspose.PSD používá caching pro dočasné uložení dat. Mechanismus je jednoduchý na použití, upravitelný a transparentní. Zajišťuje, že při zpracování obrázku nejsou žádné problémy s výkonem. Tento článek vysvětluje, jak upravit cache s API Aspose.PSD pro Javu.

### **Upravení cache**
Když proces potřebuje dočasné uložení dat, toto uložení se alokuje v cache. Cache může být ve paměti nebo na disku a je nastavena uživatelem. Když dočasná data již nejsou potřebná, místo je uvolněno. Statistiky alokovaného místa lze kdykoli zkontrolovat. Způsob, jakým Aspose.PSD alokuje a používá cache, lze upravit. Tato část popisuje různá nastavení a jejich výchozí hodnoty a ukázkové kódy níže ukazují, jak je lze použít.

### **Nastavení, kde je cache alokována**
Chcete-li upravit způsob, jak je alokováno cache místo, nastavte vlastnost CacheType. Výchozí chování je takové, že cache je alokována v paměti a když v paměti není k dispozici žádné místo, je alokována na disk. Toto chování je zachyceno režimem Auto. Režim Auto je flexibilní a maximalizuje výkon. Existují také další režimy:

- Režim CacheOnDiskOnly: alokace pouze na disk.
- Režim CacheInMemoryOnly: alokace pouze do paměti.

Volba režimu CacheOnDiskOnly může způsobit špatný výkon.

### **Nastavení velikosti cache**
Nastavte maximální místo (v bytech), které může být alokováno na disku nebo v paměti nastavením vlastností MaxDiskSpaceForCache a MaxMemoryForCache. Výchozí hodnota obou hodnot je nastavena na 0, což znamená, že neexistuje žádný horní limit.

### **Ovládání přerozdělování cache**
Pokud v paměti není k dispozici dostatek místa (jak je uvedeno vlastností MaxMemoryForCache) při alokaci nové cache, je cache alokována na disk. Pokud na disku není dostatek místa, je vyvolána výjimka. Proces alokace cache se přesouvá z paměti na disk, ale ne obráceně. Vlastnost ExactReallocateOnly slouží k ovládání přerozdělování paměti. Přerozdělování se pravděpodobně vyskytne u předem alokovaných cache. Může se to stát, když systém zjistí, že alokované místo nebude postačující. Pokud je ExactReallocateOnly nastavena na výchozí hodnotu False, místo je přealokováno do stejného média. Když je nastavena na True, přerozdělení nemůže překročit maximálně nastavené místo. V tomto případě je stávající alokovaná cache v paměti (která vyžaduje přerozdělení) uvolněna a rozšířené místo je alokováno na disku.

### **Příklady programů**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}
