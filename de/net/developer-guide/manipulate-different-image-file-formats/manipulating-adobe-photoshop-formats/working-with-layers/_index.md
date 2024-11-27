---
title: Arbeiten mit Ebenen
type: docs
weight: 150
url: /de/net/working-with-layers/
---

## **Erstellen einer Ebenengruppe**
Eine Ebenengruppe besteht aus einer oder mehreren Ebenen und dient dazu, ähnliche oder verwandte Ebenen zu organisieren. Mit Aspose.PSD für .NET können Sie eine Ebenengruppe erstellen. Hierfür wurde in der Klasse **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** eine neue Methode **[AddLayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)** hinzugefügt, die die Ebenengruppe hinzufügt.

Die Schritte zum Erstellen von Ebenengruppen sind wie folgt:

- Erstellen Sie eine Instanz eines Bildes unter Verwendung der Klasse PsdImage mit einer festgelegten Breite, Höhe und Bildeoptionen.
- Erstellen Sie eine **[LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup)** mit dem angegebenen Gruppennamen und Index.
- Erstellen Sie eine Instanz der Layer-Klasse und weisen Sie das PSD-Bild zu.
- Fügen Sie die erstellte Ebene der Ebenengruppe unter Verwendung der AddLayer-Methode hinzu, die von der LayerGroup-Klasse bereitgestellt wird.
- Speichern Sie die Ergebnisse.

Der folgende Code zeigt Ihnen, wie Sie eine Ebenengruppe erstellen können.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Umbenennen einer Ebene**
Sie können jeden beliebigen Namen verwenden, aber die übliche Praxis ist es, eine allgemeine Beschreibung des Objekts oder Elements zu verwenden, das sich auf dieser Ebene befindet. Dieser Artikel zeigt, wie Sie den Namen einer Ebene unter Verwendung von Aspose.PSD für .NET ändern können. Hierfür wurde in der Layer-Klasse ein neues **[DisplayName](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname)** -Eigenschaft hinzugefügt, um einen Layernamen ordnungsgemäß anzuzeigen. Es wurde festgestellt, dass wenn Photoshop einen Layernamen unter Verwendung der **[Name](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name)** -Eigenschaft speichert, koreanische Zeichen als byte 63'?' in ASCII gespeichert werden. Wenn Sie also einen Layernamen ordnungsgemäß anzeigen möchten, verwenden Sie die **DisplayName** -Eigenschaft, da die **Name** -Eigenschaft koreanische Zeichen nicht unterstützt.

Das folgende Codebeispiel zeigt, wie Sie einen Layer umbenennen können.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **Unterstützung von verknüpften Ebenen**
Das Verknüpfen von Ebenen ist ähnlich wie das Gruppieren von Ebenen. Wenn Sie zwei oder mehr Ebenen miteinander verknüpfen, ermöglicht es Ihnen, bestimmte Änderungen an beiden verknüpften Ebenen vorzunehmen. Beispielsweise, wenn Sie Transformationen auf eine Ebene anwenden, werden sie auf alle anderen verknüpften Ebenen angewendet. Dieser Artikel zeigt, wie Sie verknüpfte Ebenen abrufen und trennen können, indem Sie [Aspose.PSD](https://products.aspose.com/psd) verwenden.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
