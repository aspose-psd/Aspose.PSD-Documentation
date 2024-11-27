---
title: Aspose.PSD pro .NET 21.9 - Poznámky k vydání
type: docs
weight: 40
url: /cs/net/aspose-psd-pro-net-21-9-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-574|Nastavte RLE kompresi jako výchozí pro ukládání PSD souboru a zabráníte vytvoření velkého výstupu PSD|Funkce|
|PSDNET-747|Podpora vrstev efektů překrytí s režimem barev vícekanálových souborů PSD|Funkce|
|PSDNET-951|Po vytvoření nové vrstvy je její vlastnost Resources null, což brání manipulacím (např. změně velikosti)|Chyba|
|PSDNET-955|Nepodpora kompresních metod ZipWithPrediction pro 8 bitů|Chyba|

## **Změny v veřejném API**
# **Přidaná API:**
- žádná

# **Odstraněná API:**
- žádná

## **Příklady použití:**

**PSDNET-574. Nastavte RLE kompresi jako výchozí pro ukládání PSD souboru a zabráníte vytvoření velkého výstupu PSD**

{{< highlight csharp >}}
            string cestaVstupnihoSouboru = "soubor.psd";
            string vystup1 = "vystup_puvodni.psd";
            string vystup2 = "output_psdOptions.psd";

            using (Image obraz = Image.Load(cestaVstupnihoSouboru))
            {
                obraz.Save(vystup1);
                obraz.Save(vystup2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Podpora vrstev efektů překrytí s režimem barev vícekanálových souborů PSD**

{{< highlight csharp >}}
            var nazevSouboru = "VsechnyEfekty.psd";
            var vystupniSoubor = "VsechnyEfekty_vystup.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Neměla by být vyvolána výjimka
            using (var im = Image.Load(nazevSouboru, loadOptions))
            {
                // Neměla by být vyvolána výjimka
                im.Save(vystupniSoubor);
            }
{{< /highlight >}}

**PSDNET-951. Po vytvoření nové vrstvy je její vlastnost Resources null, což brání manipulacím (např. změně velikosti)**

{{< highlight csharp >}}
            string PSDSoubor = "Vrstva1.psd";
            string souborVrstva1 = "Vrstva2.png";
            string souborVrstva2 = "Vrstva3.png";
            string nazevVystupu = "finalni_vystup.psd";

            void NahraditBarvu(RasterImage obraz, Color staraBarva, int rozdil, Color novaBarva)
            {
                var pixely = obraz.LoadArgb32Pixels(obraz.Bounds);
                var delka = pixely.Length;

                var staraR = staraBarva.R;
                var staraG = staraBarva.G;
                var staraB = staraBarva.B;
                var novaBarvaHodnota = novaBarva.ToArgb();

                for (int i = 0; i < delka; i++)
                {
                    // Červená
                    var r = (byte)((pixely[i] >> 16) & 0xff);
                    // Zelená
                    var g = (byte)((pixely[i] >> 8) & 0xff);
                    // Modrá
                    var b = (byte)(pixely[i] & 0xff);

                    int skutecnyRozdil = Math.Abs(r - staraR) + Math.Abs(g - staraG) + Math.Abs(b - staraB);

                    if (skutecnyRozdil <= rozdil)
                    {
                        pixely[i] = novaBarvaHodnota;
                    }
                }

                obraz.SaveArgb32Pixels(obraz.Bounds, pixely);
            }

            Layer Vrstva2 = null;
            Layer Vrstva3 = null;
            using (PsdImage obraz = (PsdImage)Image.Load(PSDSoubor))
            {
                #region Přidání vrstvy 1

                using (var stream = new FileStream(souborVrstva1, FileMode.Open))
                {
                    Vrstva2 = new Layer(stream);
                    
                    Vrstva2.Resize(obraz.Width, obraz.Height);
                    var sirka = Vrstva2.Width;
                    var vyska = Vrstva2.Height;

                    Vrstva2.Left = 675;
                    Vrstva2.Top = 0;

                    Vrstva2.Right = Vrstva2.Left + sirka;
                    Vrstva2.Bottom = Vrstva2.Top + vyska;

                    obraz.AddLayer(Vrstva2);
                }

                #endregion

                using (var stream = new FileStream(souborVrstva2, FileMode.Open))
                {
                    Vrstva3 = new Layer(stream);
                    // Nahrazení bílé barvy průhledností
                    NahraditBarvu(Vrstva3, Color.White, 256, Color.Transparent);
                    Vrstva2.DrawImage(new Point(0, 0), Vrstva3);
                }

                obraz.Save(nazevVystupu, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Nepodpora kompresních metod ZipWithPrediction pro 8 bitů**

{{< highlight csharp >}}
            string cestaVstupnihoSouboru = "zipTest698.psd";
            string vystupZip8 = "vystup_Zip8bit.psd";
            string vystupZip16 = "vystup_Zip16bit.psd";

            using (PsdImage obraz = (PsdImage)Image.Load(cestaVstupnihoSouboru))
            {
                obraz.Save(vystupZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                obraz.Save(vystupZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
