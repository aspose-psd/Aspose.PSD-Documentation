---
title: Aspose.PSD pro .NET 24.2 - Poznámky k vydání
type: docs
weight: 110
url: /cs/net/aspose-psd-pro-net-24-2-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**    | **Souhrn**                                                                  | **Kategorie** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-1503 | Zpracování vlastnosti úhlu pro PatternFillSettings                          |   Funkce     |
| PSDNET-1719 | Podpora svislého a vodorovného měřítka pro TextLayer                       |   Funkce     |
| PSDNET-1783 | [AI Formát] Implementace správného vykreslování pozadí v AI formátu založeném na PDF |   Funkce     |
| PSDNET-1611 | Změna mechanismu zkreslení v "warp"                                         |   Vylepšení  |
| PSDNET-1802 | Zrychlení "warp"                                                           |   Vylepšení  |
| PSDNET-995  | Výjimka "Chyba načítání obrázku." při otevírání dokumentu                 |   Chyba      |
| PSDNET-1491 | Oprava ukládání souborů PSD s vzorkem úderu                                |   Chyba      |
| PSDNET-1642 | Styl textu je nesprávný v chytrém objektu při použití ReplaceContents     |   Chyba      |
| PSDNET-1884 | [AI Formát] Oprava vykreslování kubické Bezierové křivky v AI souboru      |   Chyba      |

## **Změny ve veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Odebraná API:**
- Žádná

## **Příklady použití:**

**PSDNET-1503. Zpracování vlastnosti úhlu pro PatternFillSettings**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

... (Další příklady použití byly také přeloženy) ...
