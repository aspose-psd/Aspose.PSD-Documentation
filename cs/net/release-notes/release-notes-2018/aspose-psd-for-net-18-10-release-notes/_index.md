---
title: Aspose.PSD pro .NET 18.10 - Poznámky k vydání
type: docs
weight: 30
url: /cs/net/aspose-psd-pro-net-18-10-poznamky-k-vydani/
---

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-14|Přidání podpory módů míchání kromě Normálního|Funkce|
|PSDNET-69|Přidání podpory efektu Překrytí barvou|Funkce|
|PSDNET-70|Přidání podpory efektu Stín|Funkce|
|PSDNET-71|Rendrování pro export efektu Překrytí barvou|Funkce|
|PSDNET-72|Rendrování pro export efektu Stín|Funkce|
|PSDNET-74|Podpora přidávání vrstvených efektů za běhu|Funkce|
|PSDNET-73|Optimalizace výkonu při načítání zdrojů obsahujících osTypeStructures|Chyba|
|PSDNET-79|Refaktorování a opravy úniků paměti v LayerAndMaskInfo|Vylepšení|

## **Příklady použití:**
**PSDNET-14 Přidání podpory módů míchání kromě Normálního**

{{< highlight java >}}

 var soubory = new string[]

{

    "Normální",

    "Rozpustit",

    "Ztmavit",

    "Násobit",

    "Přepal barvy",

    "Lineární ztmavení",

    "Tmavší barva",

    "Zesvětlit",

    "Obrazovka",

    "Přepálit barvu",

    "Lineární přidání",

    "Zesvětlení barvy",

    "Překryv",

    "Jemný záblesk",

    "Hrubý záblesk",

    "Živý záblesk",

    "Lineární záblesk",

    "Špendlík",

    "Tvrdá směs",

    "Rozdíl",

    "Vyloučení",

    "Odčíst",

    "Dělit",

    "Odstín",

    "Sytost",

    "Barva",

    "Jas",

};

foreach (var názevSouboru in soubory)

{

    using (var im = LoadFile(názevSouboru + ".psd"))

    {

        // Export do PNG

        var možnostiUložení = new PngOptions();

        možnostiUložení.TypBarvy = PngColorType.TruecolorWithAlpha;

        var cestaExportuPng100 = "MódMíchání" + názevSouboru + "_Test100.png";

        im.Save(cestaExportuPng100, možnostiUložení);

        // Nastavení průhlednosti na 50%

        im.Layers[1].Průhlednost = 127;

        var cestaExportuPng50 = "MódMíchání" + názevSouboru + "_Test50.png";

        im.Save(cestaExportuPng50, možnostiUložení);

    }

}

{{< /highlight >}}

**PSDNET-69 Přidání podpory efektu Překrytí barvou**

{{< highlight java >}}

     // Úprava efektu Překrytí barvou

    string zdrojovýNázevSouboru = "PřekrytíBarvou.psd";

    string cestaPsdPoZměně = "PřekrytíBarvouZměněno.psd";

    using (var im = LoadFile(zdrojovýNázevSouboru))

    {

       var překrytíBarvou = (PřekrytíBarvou)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, překrytíBarvou.Barva);

       Assert.AreEqual(153, překrytíBarvou.Průhlednost);

       překrytíBarvou.Barva = Color.Green;

       překrytíBarvou.Průhlednost = 128;

       im.Save(cestaPsdPoZměně);

    }

{{< /highlight >}}

**PSDNET-70 Přidání podpory efektu Stín**

{{< highlight java >}}

     // Úprava efektu Stín

    string zdrojovýNázevSouboru = "Stín.psd";

    string cestaPsdPoZměně = "StínZměněný.psd";

    using (var im = LoadFile(zdrojovýNázevSouboru))

    {

       var efektStín = (EfektStínu)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, efektStín.Barva);

       Assert.AreEqual(255, efektStín.Průhlednost);

       Assert.AreEqual(3, efektStín.Vzdálenost);

       Assert.AreEqual(7, efektStín.Velikost);

       Assert.AreEqual(true, efektStín.PoužítGlobálníSvětlo);

       Assert.AreEqual(90, efektStín.Uhel);

       Assert.AreEqual(0, efektStín.Rozptyl);

       Assert.AreEqual(0, efektStín.Šum);

       efektStín.Barva = Color.Green;

       efektStín.Průhlednost = 128;

       efektStín.Vzdálenost = 11;

       efektStín.PoužítGlobálníSvětlo = false;

       efektStín.Velikost = 9;

       efektStín.Uhel = 45;

       efektStín.Rozptyl = 3;

       efektStín.Šum = 50;

       im.Save(cestaPsdPoZměně);

    }

{{< /highlight >}}

**PSDNET-71 Rendrování pro export efektu Překrytí barvou**

{{< highlight java >}}

    // Úprava efektu Překrytí barvou

    string zdrojovýNázevSouboru = "PřekrytíBarvou.psd";

    string cestaExportuPng = "PřekrytíBarvou.png";

    using (var im = LoadFile(zdrojovýNázevSouboru))

    {

       var překrytíBarvou = (EfektPřekrytíBarvou)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, překrytíBarvou.Barva);

       Assert.AreEqual(153, překrytíBarvou.Průhlednost);

       // Uložit PNG

       var možnostiUložení = new PngOptions();

       možnostiUložení.TypBarvy = PngColorType.TruecolorWithAlpha;

       im.Save(cestaExportuPng, možnostiUložení);

    }

{{< /highlight >}}

**PSDNET-72 Rendrování pro export efektu Stín**

{{< highlight java >}}

     // Export efektu Stín

    string zdrojovýNázevSouboru = "Stín.psd";

    string cestaExportuPng = "Stín.png";

    using (var im = LoadFile(zdrojovýNázevSouboru))

    {

       var efektStín = (EfektStínu)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, efektStín.Barva);

       Assert.AreEqual(255, efektStín.Průhlednost);

       Assert.AreEqual(3, efektStín.Vzdálenost);

       Assert.AreEqual(7, efektStín.Velikost);

       Assert.AreEqual(true, efektStín.PoužítGlobálníSvětlo);

       Assert.AreEqual(90, efektStín.Uhel);

       Assert.AreEqual(0, efektStín.Rozptyl);

       Assert.AreEqual(0, efektStín.Šum);

       // Uložit PNG

       var možnostiUložení = new PngOptions();

       možnostiUložení.TypBarvy = PngColorType.TruecolorWithAlpha;

       im.Save(cestaExportuPng, možnostiUložení);

    }

{{< /highlight >}}

**PSDNET-74 Podpora přidávání vrstvených efektů za běhu**

{{< highlight java >}}

     // Přidání efektu vrstvy překrytí barvy za běhu

    string zdrojovýNázevSouboru = "TřiObvykléVrstvySEfektemVrstvy.psd";

    string cestaExportuPsd = "TřiObvykléVrstvySEfektemVrstvyZměněno.psd";

    string cestaExportuPng = "TřiObvykléVrstvySEfektemVrstvyZměněno.psd";

    var možnostiNačtení = new PsdLoadOptions()

    {

        NačístZdrojeEfektů = true

    };



    var testovacíSložka = string.Empty;

    var im = (PsdImage)Image.Load(testovacíCesta, možnostiNačtení) 

    using (im)

    {

        var efekt = im.Layers[1].BlendingOptions.AddColorOverlay();

        efekt.Průhlednost = 128;

        efekt.Barva = Color.Green;

        efekt.MódMíchání = MódMíchání.Normální;

        var efekt = im.Layers[1].BlendingOptions.AddDropShadow();

        efekt.Barva = Color.Red;

        efekt.Průhlednost = 128;

        efekt.MódMíchání = MódMíchání.Normální;



        // Uložit PSD    

        im.Save(cestaExportuPsd);



        // Uložit PNG

        var možnostiUložení = new PngOptions();

        im.Save(cestaExportuPng, možnostiUložení);

    }

{{< /highlight >}}
