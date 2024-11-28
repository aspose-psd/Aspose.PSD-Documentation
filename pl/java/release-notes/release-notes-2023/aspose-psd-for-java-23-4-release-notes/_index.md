---
title: Notatki wersji Aspose.PSD dla Javy 23.4
type: docs
weight: 40
url: /pl/java/aspose-psd-for-java-23-4-release-notes/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wersji dla [Aspose.PSD dla Javy 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

| **Klucz** | **Podsumowanie** | **Kategoria** |
| :- | :- | :- |
| PSDJAVA-446 | Przeniesienie pominiętej funkcjonalności z Aspose.PSD dla .Net do Aspose.PSD dla Javy | Usprawnienie |
| PSDJAVA-441 | Projektowanie klasy RawColor dla publicznego API, aby można ją było używać w API PSD zamiast przestarzałej struktury Color | Usprawnienie |
| PSDJAVA-418 | Integrowanie nowoczesnej Licencji Aspose.PSD | Usprawnienie |
| PSDJAVA-445 | Przeniesienie formatowania podczas edycji w programie Photoshop | Błąd |
| PSDJAVA-443 | Edycja tekstu za pomocą Części Tekstu nie zapisuje poprawnego wyniku | Błąd |
| PSDJAVA-444 | Początek i koniec stylów lub akapitów pojawia się w niewłaściwym miejscu podczas edycji warstwy tekstowej przez ITextPortion | Błąd |

# **Zmiany w publicznym API**
# **Dodane metody:**
- M: com.aspose.psd.FontSettings.getFontReplacements(java.lang.String)
- M: com.aspose.psd.FontSettings.getReplacementFont(java.lang.String)
- M: com.aspose.psd.FontSettings.setAllowedFonts(java.lang.String[])
- M: com.aspose.psd.FontSettings.setFontReplacements(java.lang.String, java.lang.String[])
- M: com.aspose.psd.FontSettings.isFontAllowed(java.lang.String)
- M: com.aspose.psd.License.setLicense(java.io.File)
- M: com.aspose.psd.License.getRenewSubscriptionStartMessage
- M: com.aspose.psd.License.getErrorCodeMessages
- M: com.aspose.psd.License.removeLicense
- T: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.#ctor(int, int, com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getSignature
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getKey
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getPsdVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getFilterEffectMasks
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getLength
- M: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.save(com.aspose.psd.StreamContainer, int)
- F: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.FEidTypeToolKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.FXidTypeToolKey
- T: com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource
- M: com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getDataSize
- ... (Pozostała część pominięta)

# **Usunięte metody:**
- M: com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M: com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- M: com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor
- M: com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short, byte[], byte[])
- M: com.aspose.psd.fileformats.psd.layers.Layer.saveData(java.io.OutputStream)
- ... (Pozostała część pominięta)

# **Przykłady użycia:**

**PSDJAVA-446. Przeniesienie pominiętej funkcjonalności z Aspose.PSD dla .Net do Aspose.PSD dla Java**

Proszę sprawdzić [API Reference dla Aspose.PSD dla Java](https://reference.aspose.com/psd/java/). Nie wszystkie przykłady użycia nowego API zostały skopiowane i przetestowane.

{{< highlight java >}}
        // Przykłady zostaną udostępnione później.
{{< /highlight >}}

**PSDJAVA-441. Projektowanie klasy RawColor dla publicznego API, aby można ją było używać w API PSD zamiast przestarzałej struktury Color**

{{< highlight java >}}
		PixelDataFormat rgb32Bpp = PixelDataFormat.getRgb32Bpp();
		RawColor color = new RawColor(rgb32Bpp);
		Color oldColor = Color.fromArgb(5, 1, 2, 3);

		// Pozostała część kodu
{{< /highlight >}}

**PSDJAVA-445. Przeniesienie formatowania podczas edycji w programie Photoshop**

{{< highlight java >}}
 // Pozostała część kodu
{{< /highlight >}}**PSDJAVA-443. Edycja tekstu za pomocą Części Tekstu nie zapisuje poprawnego wyniku**

{{< highlight java >}}
  // Kod dla PSDJAVA-443
{{< /highlight >}}

**PSDJAVA-444. Początek i koniec stylów lub akapitów pojawia się w niewłaściwym miejscu podczas edycji warstwy tekstowej przez ITextPortion**

{{< highlight java >}}
  // Kod dla PSDJAVA-444
{{< /highlight >}}

**PSDJAVA-445|Przeniesienie formatowania podczas edycji w programie Photoshop**

{{< highlight java >}}
  // Kod dla PSDJAVA-445
{{< /highlight >}}