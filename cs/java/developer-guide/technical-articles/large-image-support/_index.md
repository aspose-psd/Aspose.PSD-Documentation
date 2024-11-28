---
title: Podpora velkých obrázků
type: docs
weight: 60
url: /cs/java/podpora-velkych-obrazku/
---

## **Podpora velkých obrázků**
Vzhledem k omezením standardní knihovny Java v procesování obrázků jsme představili nový mechanismus pro podporu velkých obrázků. Nový přístup překonává omezení, ale kvůli omezením velikosti dat jsou maximálně podporované rozměry pro vytváření a načítání 2,147,483,647 x 2,147,483,647 pixelů.
### **Práce s velkými obrázky**
Aspose.PSD má vylepšený výkon a podporu pro velké obrázky. Obrázky o velikosti stovek megabajtů již nejsou problém, takže můžete vytvářet, načítat a kreslit přes tyto obrázky. Avšak kvůli částečnému zpracování a zacházení s výjimkami OutOfMemoryException může být výkon u velkých obrázků velmi nízký. To je způsobeno tím, že Aspose.PSD se snaží přerozdělit menší množství dat pro zpracování a každý krok přerozdělení je velmi nákladný. Výhody nové architektury jsou zjevné:

- Neexistuje žádné omezení velikosti obrázku.
- Nejste omezeni pamětí dostupnou na vašem počítači.

Pokud se setkáte se zpomaleným zpracováním, doporučuje se zvýšit celkové množství paměti RAM, aby se všechny vaše pixely vešly do paměti. Pokud to neuděláte, zpracování je stále možné, ale pomalejší. Postup je následující:

- Zavolejte metodu LoadPartialPixels s požadovaným obdélníkem a delegátem pro příjem načtených pixelů.
 
Aspose.PSD se snaží načíst celý obdélník.

- Pokud je k dispozici dostatek paměti na to, aby se všechny pixely vešly, pak jsou všechny pixely jednoduše vráceny volajícímu.
- Pokud není dostatek paměti, volající dostane podmnožinu pixelů zevnitř zadaného obdélníku. Až budou tyto pixely zpracovány, volající obdrží další obdélník. Zpracování končí, když je zpracován celý obdélník.

Aspose.PSD se snaží extrahovat co nejvíce řádků. Pokud není dostatek paměti na to, aby se vešel jediný řádek pixelů, pak je jeden řádek rozdělen na části odpovídající obdélníkům s výškou 1. Můžete také kreslit na velké obrázky. Kreslicí proces se snaží ovlivnit celý požadovaný obdélník. Pokud není dostatek paměti, kreslení se provádí na částečných obdélníích, dokud není nakreslena celá plocha. Navíc Aspose.PSD podporuje ukládání a exportování velkých obrázků. Uložte zdrojový obrázek na disk nebo jej exportujte do jiného formátu souboru. Proces ukládání nebo exportu se provádí pomocí částečných obdélníků, pokud je to potřebné. 
### **Podporované formáty obrázků**
Pro zpracování velkých obrázků jsou podporovány následující formáty:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Výše uvedené formáty mohou být bezpečně zpracovány prostřednictvím vytváření, úpravy, používání kreslicích operací, ukládání na disk nebo exportování bez ohledu na velikost obrázku.
