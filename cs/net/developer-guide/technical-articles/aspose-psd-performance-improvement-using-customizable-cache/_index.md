---
title: Zlepšení výkonu s pomocí nastavitelné cache
type: docs
weight: 20
url: /cs/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Zlepšení výkonu pomocí nastavitelné cache**
[Aspose.PSD](https://products.aspose.com/psd/family) využívá mezipaměť pro dočasné ukládání dat. Mechanismus je snadno použitelný, nastavitelný a transparentní. Zajišťuje, že při zpracování obrazu nevznikají žádné výkonnostní problémy. Tento článek vysvětluje, jak upravit mezipaměť s využitím API Aspose.PSD pro .NET.

### **Nastavení cache**
Pokud proces potřebuje dočasné ukládání dat, tato úložiště jsou vytvořena v cache. Mezipaměť může být umístěna buď v paměti, nebo na disku a je nastavena uživatelem. Jakmile dočasná data již nejsou potřebná, místo je uvolněno. Statistiky přiděleného místa lze kdykoliv zkontrolovat. Způsob, jakým Aspose.PSD přiděluje a používá mezipaměti, lze nastavit podle potřeby. Tato sekce popisuje různá nastavení a jejich výchozí hodnoty a kódové části níže ukazují, jak je lze použít.

### **Nastavení místa, kam je cache přidělována**
Pro přizpůsobení způsobu, jakým je přidělováno místo v cache, nastavte vlastnost [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Výchozí chování je takové, že je cache přidělena v paměti a pokud není v paměti dostatek místa, je přidělena na disk. Toto chování je zaznamenáno módem Auto. Auto mód je flexibilní a maximalizuje výkon. Existují také další módy:

- Mód CacheOnDiskOnly: přidělení pouze na disk.
- Mód CacheInMemoryOnly: přidělení pouze do paměti.

Vybrání módu CacheOnDiskOnly může vést k špatnému výkonu.

### **Nastavení velikosti cache**
Nastavte maximální prostor (v bytech), který lze přidělit na disku nebo v paměti, nastavením vlastností [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) a [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache). Výchozí hodnota obou hodnot je 0, což znamená, že zde neexistuje horní limit.

### **Kontrola přerozdělování cache**
Pokud není k dispozici dostatek místa v paměti (jak je specifikováno vlastností MaxMemoryForCache) při přidělení nové mezipaměti, je cache přidělena na disk. Pokud na disku není dostatek místa, je vyvolána výjimka. Proces přidělování cache se přesouvá z paměti na disk, ale ne naopak. Vlastnost [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) se používá k řízení přerozdělování paměti. Přerozdělování je nepravděpodobné u předem přidělených mezipamětí. Může se stát, když systém zjistí, že přidělené místo nebude postačující. Pokud je ExactReallocateOnly nastaveno na výchozí hodnotu, False, místo je přerozděleno do stejného média. Když je nastaveno na Pravda, přerozdělení nesmí překročit maximálně stanovené místo. V tomto případě je již přidělená mezipaměť v paměti (která vyžaduje přerozdělení) uvolněna a rozšířený prostor je přidělen na disk.

### **Ukázky programu**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
