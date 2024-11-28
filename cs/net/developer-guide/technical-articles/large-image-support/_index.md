---
title: Podpora Velkých Obrázků
type: docs
weight: 40
url: /cs/net/podpora-velkych-obrazku/
---

## **Podpora Velkých Obrázků**
Vzhledem k omezujícím faktorům standardní knihovny .NET ohledně velikosti obrázků, jsme zavedli nový mechanismus pro podporu velkých obrázků. Nový přístup překonává omezení, ale kvůli omezením velikosti dat jsou maximální podporované rozměry pro vytváření a načítání 2 147 483 647 x 2 147 483 647 pixelů.
### **Práce s Velkými Obrázky**
Aspose.PSD má vylepšený výkon a podporu pro velké obrázky. Obrázky o velikosti stovek megabajtů již nejsou problémem, takže je můžete vytvářet, načítat a kreslit na ně. Avšak z důvodu částečného zpracování a zacházení s výjimkami OutOfMemoryException může být výkon velmi nízký při velmi velkých obrázcích. To je způsobeno faktem, že Aspose.PSD se pokouší znovu přiřadit menší množství dat k zpracování a každý krok přiřazení je velmi nákladný. Výhody nové architektury jsou zjevné:

- Neexistuje žádné omezení velikosti obrázku.
- Nejste limitováni dostupnou pamětí na vašem počítači.

Pokud máte pomalé zpracování, doporučuje se zvýšit celkové množství paměti RAM tak, aby se všechny vaše pixely vešly do paměti. Pokud to neuděláte, zpracování je stále možné, ale pomalejší. Postup je následující:

- Zavolejte metodu [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) s požadovaným obdélníkem a delegátem k přijímání načtených pixelů na daných souřadnicích.

Aspose.PSD se snaží načíst celý obdélník.

- Pokud je k dispozici dostatečná paměť pro umístění všech pixelů, jsou jednoduše vráceny volajícímu.
- Pokud není dostatek paměti, volající obdrží podmnožinu pixelů zevnitř zadaného obdélníku. Když jsou tyto pixely zpracovány, volající obdrží další obdélník. Zpracování končí po zpracování celého obdélníku.

Aspose.PSD se snaží extrahovat co nejvíce řádků. Pokud není dostatek paměti pro umístění jednoho řádku pixelů, je jeden řádek rozdělen na části odpovídající obdélníkům s výškou 1. Také můžete kreslit na velké obrázky. Kreslicí proces se snaží ovlivnit celý požadovaný obdélník. Pokud není dostatek paměti, je kresleno na částečných obdélnících, dokud není vykreslena celá plocha. Navíc Aspose.PSD podporuje ukládání a exportování velkých obrázků. Uložte zdrojový obrázek na disk nebo jej exportujte do jiného formátu souboru. Ukládání nebo exportní proces se provádí pomocí částečných obdélníků, je-li to vyžadováno. 
### **Podporované Formáty Obrázků**
Pro zpracování velkých obrázků jsou podporovány následující formáty:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Výše uvedené formáty mohou být bezpečně zpracovány tím, že se vytvoří, upraví, použijí kreslicí operace, uloží na disk nebo exportují bez ohledu na velikost obrázku.
