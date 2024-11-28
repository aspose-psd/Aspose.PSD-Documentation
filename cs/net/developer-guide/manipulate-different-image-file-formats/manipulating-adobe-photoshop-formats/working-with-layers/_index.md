---
title: Práce s vrstvami
type: docs
weight: 150
url: /cs/net/prace-s-vrstvami/
---

## **Vytvoření skupiny vrstev**
Skupina vrstev se skládá z jedné nebo více vrstev a pomáhá organizovat podobné nebo související vrstvy. S pomocí Aspose.PSD pro .NET můžete vytvořit skupinu vrstev. Pro tento účel byla do třídy **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** přidána nová metoda **[AddLayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)** pro přidání skupiny vrstev. 

Postup pro vytvoření skupin vrstev je následující:

- Vytvořte instanci obrázku pomocí třídy PsdImage se specifikovanou šířkou, výškou a možnostmi obrázku.
- Vytvořte **[LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup)** se zadaným názvem skupiny a indexem.
- Vytvořte instanci třídy Layer a přiřaďte ji k obrázku PSD.
- Přidejte vytvořenou vrstvu do skupiny vrstev pomocí metody AddLayer vystavené třídou LayerGroup.
- Uložte výsledky.

Následující ukázka kódu vám ukáže, jak vytvořit skupinu vrstev.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}

## **Přejmenování vrstvy**
Můžete použít jakékoliv jméno, které byste chtěli, ale typickou praxí je použití obecného popisu objektu nebo prvku, který se nachází na této vrstvě. Tento článek ukazuje, jak můžete změnit název vrstvy pomocí Aspose.PSD pro .NET. Pro tento účel byla do třídy vrstvy přidána nová vlastnost **[DisplayName](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname)** pro správné zobrazení názvu vrstvy. Bylo zjištěno, že když Photoshop uloží název vrstvy pomocí vlastnosti **[Name](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name)**, pak jsou korejské znaky uloženy jako bajt 63 '?' v ASCII. Pokud tedy chcete název vrstvy zobrazit správně, použijte vlastnost **DisplayName**, protože vlastnost **Name** nepodporuje korejské znaky.

Následující ukázkový kód ukazuje, jak můžete přejmenovat vrstvu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Podpora propojených vrstev**
Propojení vrstev je podobné seskupování vrstev. Pokud propojíte dvě nebo více vrstev, umožní vám to provést určité změny na obou propojených vrstvách. Například pokud aplikujete transformace na jednu vrstvu, budou se aplikovat na všechny ostatní propojené vrstvy. Tento článek ukazuje, jak můžete získat a odpojit propojené vrstvy pomocí [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
