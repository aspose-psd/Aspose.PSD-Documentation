---
title: Aktualizace plné vrstvy PSD pomocí Javy
weight: 100
type: docs
description: Příklady použití všech typů vrstev úprav, včetně plné barvy, přechodové plné a plné s motivem
keywords: [plná vrstva, plná barva, přechodová plná, plné s motivem, api psd, java, ukázkový kód]
url: cs/java/aktualizace-plne-vrstvy-psd/
---

## **Přehled**

Vytvoření běžné vrstvy zahrnuje použití funkce createRegularLayer, která vyžaduje parametry pro definici pozice a velikosti vrstvy. Tato funkce vytvoří novou vrstvu, nastaví její hranice a vyplní ji zadanou barvou.

Pro vrstvu s plnou barvou využíváte metodu FillLayer.createInstance s parametrem FillType.Color. Jakmile je plná vrstva vytvořena, přistupujte ke svým plnícím nastavením prostřednictvím vlastnosti fill_settings a nastavte požadovanou barvu pomocí vlastnosti color třídy ColorFillSettings. V tomto kontextu je barva nastavena na Color.getCoral(). Navíc je vlastnost clipping plné vrstvy nastavena na 1, což způsobí, že funguje jako ořezová maska.

Plnivé vrstvy s přechodem jsou vytvářeny podobně pomocí metody FillLayer.createInstance, ale s parametrem FillType.Gradient. Stejně jako u plných barevných vrstev přistupujete ke svým plnícím nastavením prostřednictvím fill_settings a nastavíte body gradientových barev a průhlednostní body. V tomto příkladu jsou body gradientových barev definovány pomocí třídy GradientColorPoint a průhlednostní body pomocí třídy GradientTransparencyPoint. Vlastnost clipping plné vrstvy je také nastavena na 1.

Vrstvy plněné motivem jsou vytvářeny pomocí FillLayer.createInstance s parametrem FillType.Pattern. Znovu přistupte ke plnícím nastavením prostřednictvím fill_settings a nastavte data vzoru a další vlastnosti. V tomto kódu jsou data vzoru definována pomocí třídy PatternFillSettings a vlastnost clipping je nastavena na 1.

Jakmile jsou plné vrstvy vytvořeny, přidejte je do obrázku PSD pomocí metody addLayer a specifikujte zobrazovaný název a další vlastnosti pro každou plnou vrstvu.

Nakonec uložte obrázek PSD a jeho odpovídající PNG obrázek s poskytnutým kódem. Možnosti PNG jsou konfigurovány k použití skutečné barvy s alfa pro průhlednost.

Podívejte se na celý příklad pro více podrobností.

## **Příklad**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
