---
title: Aspose.PSD pro .NET 19.3 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/aspose-psd-pro-net-19-3-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro Aspose.PSD pro .NET 19.3

{{% /alert %}} 

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-104|Vyobrazení otočených textových vrstev pomocí Transformační matice|Funkce|
|PSDNET-96| Implementace vyobrazení efektu Obrys s plněním barvou pro export|Funkce|
|PSDNET-112|Transformátory InnerData poškozují některé vrstvy s vektorovými maskami|Chyba|
|PSDNET-113|Při aktualizaci textové vrstvy pro obrázek PSD dojde k chybě při otevření v programu Photoshop|Chyba|

## **Změny ve veřejném rozhraní API**
# **Přidaná rozhraní API:**
- Žádné
# **Odstraněná rozhraní API:**
- Žádné

## **Příklady použití:**
**PSDNET-104. Vyobrazení otočených textových vrstev pomocí Transformační matice**

{{< highlight java >}}

 string nazevSouboru = "TransformovanyText.psd";

string cestaExportu = "TransformovanyTextExport.psd";

string cestaExportuPng = "TransformovanyTextExport.png";

var im = (PsdImage) Image.Load(nazevSouboru);

using(im) {

 im.Save(cestaExportu);

 im.Save(cestaExportuPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Implementace vyobrazení efektu Obrys s plněním barvou pro export**

{{< highlight java >}}

  // Implementace vyobrazení efektu Obrys s plněním barvou pro export

 string nazevSouboru = "KomplexniObrys.psd";

 string cestaExportu = "KomplexniObrysVyobrazeni.psd";

 string cestaExportuPng = "KomplexniObrysVyobrazeni.png";

 var moznostiNahrani = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(nazevSouboru, moznostiNahrani)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var efekt = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var nastaveni = (ColorFillSettings) efekt.FillSettings;

   nastaveni.Color = Color.DeepPink;

  }

  // Uložit psd

  im.Save(cestaExportu, new PsdOptions());

  // Uložit png

  im.Save(cestaExportuPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Transformátory InnerData poškozují některé vrstvy s vektorovými maskami**

{{< highlight java >}}

 // Transformátory InnerData poškozují některé vrstvy s vektorovými maskami

var souborZdroje = "1.psd";

var cestaPng = "RotaceOtoceniTest2617.png";

var cestaPsd = "RotaceOtoceniTest2617.psd";

var typOtoceni = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(souborZdroje))) {

 im.RotateFlip(typOtoceni);

 im.Save(cestaPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(cestaPsd);

}

{{< /highlight >}}

**PSDNET-113. Při aktualizaci textové vrstvy obrázku PSD dojde k chybě při otevření v programu Photoshop**

{{< highlight java >}}

 string nazevSouboru = "Test.psd";

string cestaExportu = "Vysledek.psd";

using(Image image = Image.Load(nazevSouboru)) {

 if (!(image is PsdImage)) {

  return;

 }

 PsdImage psdImage = (PsdImage) image;

 Layer[] vrstvy = psdImage.Layers;

 for (int index = vrstvy.Length - 1; index >= 0; index--) {

  Layer vrstva = vrstvy[index];

  if (!(vrstva is TextLayer)) {

   continue;

  }

  TextLayer textovaVrstva = (TextLayer) vrstva;

  textovaVrstva.UpdateText("\\()");

 }

 PsdOptions moznostiObr = new PsdOptions(psdImage);

 psdImage.Save(cestaExportu, moznostiObr);

}

// Soubor musí být otevřen bez výjimky a musí být čitelný pro Photoshop

using(Image image = Image.Load(cestaExportu)) {}

{{< /highlight >}}
