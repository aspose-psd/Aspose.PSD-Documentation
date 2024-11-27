---
title: Aspose.PSD für .NET 20.9 - Versionshinweise
type: docs
weight: 40
url: /de/net/aspose-psd-fuer-net-20-9-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-408|Unterstützung von SoLEResource (Smart Object Layer Externe Ressource)|Feature|
|PSDNET-614|Unterstützung von verknüpften Smartobjekten|Feature|
|PSDNET-615|Unterstützung von eingebetteten Smartobjekten|Feature|
|PSDNET-690|Ändern des Textes in einer gegebenen PSD-Datei und Speichern ändert einige Ebenen und viele Textparameter|Bug|
|PSDNET-696|FillLayer werden nach der Erstellung nicht aktualisiert und können nicht korrekt gerendert werden|Bug|
|PSDNET-712|Regression: Aspose.PSD 20.8.0 kann die Datei nicht öffnen|Bug|
|PSDNET-714|In einer spezifischen PSD-Datei bricht das Ändern der Textebene die Positionswerte|Bug|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
[…]



```csharp
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metric
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PerspectiveOther
- […]
```

**Beispiele für die Verwendung:**
**PSDNET-408. Unterstützung von SoLEResource (Smart Object Layer Externe Ressource)**
```csharp
            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("Erwartet true"));
                }
            }

            void AssertSindGleich(object actual, object expected)
            {
                var areEqual = object.Equals(actual, expected);
                if (!areEqual && actual is Array && expected is Array)
                {
                    var actualArray = (Array)actual;
                    var expectedArray = (Array)actual;
                    if (actualArray.Length == expectedArray.Length)
                    {
                        for (int i = 0; i < actualArray.Length; i++)
                        {
                            if (!object.Equals(actualArray.GetValue(i), expectedArray.GetValue(i)))
                            {
                                break;
                            }
                        }

                        areEqual = true;
                    }
                }

                if (!areEqual)
                {
                    throw new FormatException(
                        string.Format("Tatsächlicher Wert {0} unterscheidet sich von erwartetem {1}.", actual, expected));
                }
            }
[…]
```

**PSDNET-614. Unterstützung von verknüpften Smartobjekten**
```csharp
        void AssertSindGleich(object actual, object expected)
        {
            var areEqual = object.Equals(actual, expected);
            if (!areEqual && actual is Array && expected is Array)
            {
                var actualArray = (Array)actual;
                var expectedArray = (Array)actual;
                if (actualArray.Length == expectedArray.Length)
                {
                    for (int i = 0; i < actualArray.Length; i++)
                    {
                        if (!object.Equals(actualArray.GetValue(i), expectedArray.GetValue(i)))
                        {
                            break;
                        }
                    }

                    areEqual = true;
                }
            }

            if (!areEqual)
            {
                throw new FormatException(
                    string.Format("Tatsächlicher Wert {0} unterscheidet sich von erwartetem {1}.", actual, expected));
            }
        }

        string rootDataDir = "PSDNET614_1\\";
[…]
```

**PSDNET-615. Unterstützung von eingebetteten Smartobjekten**
```csharp
            void AssertSindGleich(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(
                        string.Format("Tatsächlicher Wert {0} unterscheidet sich von erwartetem {1}.", actual, expected));
                }
            }
[…]
```

**PSDNET-690. Ändern des Textes in einer gegebenen PSD-Datei und Speichern ändert einige Ebenen und viele Textparameter**
```csharp
[…]
```

**PSDNET-696. FillLayer werden nach der Erstellung nicht aktualisiert und können nicht korrekt gerendert werden**
```csharp
[…]
```

**PSDNET-712. Regression: Aspose.PSD 20.8.0 kann die Datei nicht öffnen**
```csharp
[…]
```

**PSDNET-714. In einer spezifischen PSD-Datei bricht das Ändern der Textebene die Positionswerte**
```csharp
[…]
```