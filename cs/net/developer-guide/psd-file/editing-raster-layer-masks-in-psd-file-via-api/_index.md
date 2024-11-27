---
title: Úprava rámových mask v rastru v souboru PSD pomocí API
type: docs
weight: 20
url: /cs/uprava-ramovych-mask-v-rastru-v-souboru-psd-pomoci-api/
---

## **Přehled**
**K automatizaci úprav formátu PSD a změny souboru PSD bez programu Adobe® Photoshop® můžete použít níže uvedené API Aspose.PSD. Jsou zde k dispozici ukázky kódu C# a .NET, které vám mohou pomoci upravit soubory PSD.**

Použitím rámových a vektorových masek PSD můžeme skrýt a zobrazit pixely vrstvy bez jejich trvalého smazání. Rastrické masky jsou též nazývány maskou vrstvy nebo uživatelskou maskou. Přístup jak k rastrickým, tak k vektorovým maskám v Aspose.PSD je poskytován prostřednictvím vlastnosti vrstvy [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata), která může být instancí tříd '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' a '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)', které jsou potomky abstraktní třídy 'LayerMaskData'. Pokud má vrstva jak rastrické, tak vektorové masky, pak je poskytována instance třídy [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). Pokud vrstva obsahuje pouze rastrickou nebo vektorovou masku, pak je poskytnuta instance třídy [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort). Pokud je vlastnost LayerMaskData null, pak vrstva nemá žádné masky nebo pouze vypnutou vektorovou masku.

|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Rastrická maska a vypnutá vektorová maska LayerMaskDataShort</p><p>Vypnutá rastrická maska LayerMaskDataShort</p><p>Rastrická maska a vektorová maska LayerMaskDataFull</p><p>Rastrická maska LayerMaskDataShort</p><p>Vektorová maska LayerMaskDataShort</p><p>Vypnutá vektorová maska null (Ale zdroj vektoru je přítomen)</p>|
| :- | :- |

## **Jak získat rástrovou masku vrstvy v souboru PSD?**
Nejdříve bychom měli zjistit, zda má vrstva jak vektorové, tak vrstvové masky:

Níže uvedený ukázkový kód ukazuje, jak získat rástrovou masku vrstvy

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

V opačném případě je typ vlastnosti vrstvy LayerMaskData LayerMaskDataShort. V tomto případě zkontrolujeme, zda má vrstva pouze rastrickou masku kontrolou vlastnosti Flags. Neměla by obsahovat [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** vlajku, jinak je maska vektorová cache**.**

Získání úryvku kódu masky:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Pokud potřebujete **extrahovat rástrovou masku** jako LayerMaskDataShort (pro další manipulace) dokonce tehdy, když jsou přítomny obě masky, mělo by být extrahováno LayerMaskDataFull a převedeno na LayerMaskDataShort. Na oba případy může být použit následující kód:

Extrahování rástrové masky ze souboru PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **Jak zjistit, zda má vrstva v souboru PSD rástrovou masku?**
Následující kód v jazyce C# vám může pomoci zjistit, zda má vrstva rástrovou masku:

Jak zjistit, zda je na vrstvu PSD aplikována rastrická maska [/psd/net/psd-layer/]

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **Jak odebrat / přidat / aktualizovat rástrovou masku vrstvy v souboru PSD?**
Pouhé odebrání / přidání / aktualizace LayerMaskData není dostatečné pro správné uložení, protože se neaktualizují kanály; i když to může poskytnout správné vykreslování. To nemění kanály masky:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Měli bychom použít metodu AddLayerMask vrstvy pro odstranění / přidání / aktualizaci.

Tímto přidáváme/aktualizujeme jak masku, tak kanály:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Tímto odstraníme jak masku, tak kanály:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **Odebrání rástrové masky vrstvy v obrázku PSD**
Nejprve zkontrolujeme, zda je maska ve zkráceném formátu a pokud to není vektorová maska, můžeme jednoduše zavolat metodu AddLayerMask s hodnotou null pro smazání rastrické masky. Pokud je v plném formátu, musíme ji převést na zkrácený formát a ponechat pouze vektorovou masku. Pro odstranění masky vrstvy lze použít následující ukázkový kód v jazyce C# .NET:

Ukázkový kód, jak odstranit vrstvovou masku ze souboru PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **Aktualizace rástrové masky vrstvy v obraze PSD**
To je přímočaré: pokud je maska ve zkráceném formátu, musíme změnit ImageData a MaskRectangle pokud je to nutné, jinak [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)a [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)by měly být změněny. Pro aktualizaci masky vrstvy lze použít následující ukázkový kód v jazyce C# .NET:

Aktualizace masky vrstvy PSD s C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Zde je příklad možných akcí, které změní rástrovou masku. Tento invertuje masku uživatele vrstvy:

Aktualizace masky vrstvy PSD s C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **Aktualizace vektorové masky ve souboru PSD, když je přítomna rástrová maska vrstvy**
Předpokládá se, že uživatel již změnil zdrojovou cestu vektoru. Poté může aktualizovat vektorovou masku jednoduše zavoláním metody [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask)vrstvy:

Aktualizace [vektorové masky vrstvy PSD ](/psd/cs/net/layer-vector-mask/)s C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **Přidání rastrické masky vrstvy v souboru PSD**
Pokud vrstva nemá žádnou masku, můžeme přidat zadanou rástrovou masku jednoduše zavoláním metody AddLayerMask vrstvy.

Pokud maska nemá vlajku [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags), pak již obsahuje rastrickou masku a musíme ji aktualizovat, jak je popsáno výše. Jinak, pokud je tato maska ve zkráceném formátu, převedeme ji na plný formát. Pokud ne, použijeme ji tak, jak je. Poté aktualizovat UserMaskData, UserMaskRectangle a další vlastnosti s danými vlastnostmi masky. Pro přidání (aktualizaci) masky vrstvy lze použít následující ukázkový kód v jazyce C# .NET:

Přidání nové masky vrstvy do souboru PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Jak zjistit, zda je vrstvová maska povolena?**
Pro zjištění stavu povolení vrstvové rástrové masky můžeme zkontrolovat stav vlajky LayerMaskFlags.Disabled ve vlastnosti Flags pro LayerMaskDataShort nebo v poli RealFlags pro LayerMaskDataFull. Pro získání stavu povolení masky vrstvy lze použít následující ukázkový kód v jazyce C# .NET:

Zkontrolovat, zda je maska aktivní:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}

## **Jak povolit nebo zakázat rástrovou masku vrstvy?**
Pro povolení nebo zakázání rástrové masky vrstvy můžeme změnit stav vlajky LayerMaskFlags.Disabled ve vlastnosti Flags pro LayerMaskDataShort nebo v poli RealFlags pro LayerMaskDataFull. Pro změnu stavu povolení masky vrstvy lze použít následující ukázkový kód v jazyce C# .NET:

Povolit nebo zakázat rastrickou masku vrstvy:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}

