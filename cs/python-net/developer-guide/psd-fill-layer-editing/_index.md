---
title: Aktualizace vrstvy vyplnění PSD pomocí Pythonu
weight: 100
type: docs
description: Příklady použití všech typů vrstev úprav včetně plnění barevnou vrstvou, plnění přechodem a plnění vzorem
keywords: [vrstva vyplnění, plnění barvou, plnění přechodem, plnění vzorem, psd api, python, ukázkový kód]
url: cs/python-net/psd-fill-layer-editing/
---

## **Přehled**

Pro vytvoření běžné vrstvy můžete použít funkci create_regular_layer poskytovanou v kódu. Tato funkce bere parametry left, top, width a height k definici pozice a velikosti vrstvy. Vytváří novou vrstvu, nastavuje její hranice a vyplňuje ji zadanou barvou.

Pro vytvoření vrstvy plnění barvou můžete použít metodu FillLayer.create_instance s parametrem FillType.COLOR. Po vytvoření vrstvy plnění můžete přistupovat k jejím nastavením plnění pomocí vlastnosti fill_settings a nastavit barvu pomocí vlastnosti color třídy ColorFillSettings. V poskytnutém kódu je barva nastavena na Color.coral. Vlastnost clipping vrstvy plnění je nastavena na 1, což způsobí, že vrstva bude fungovat jako vyjímací maska.

Pro vytvoření vrstvy plnění přechodem můžete použít metodu FillLayer.create_instance s parametrem FillType.GRADIENT. Stejně jako u vrstvy plnění barvou můžete přistupovat k nastavením plnění pomocí vlastnosti fill_settings a nastavit body barev přechodu a průhlednostní body. V poskytnutém kódu jsou body barev přechodu definovány pomocí třídy GradientColorPoint a body průhledností jsou definovány pomocí třídy GradientTransparencyPoint. Vlastnost clipping vrstvy plnění je také nastavena na 1.

Pro vytvoření vrstvy plnění vzorem můžete použít metodu FillLayer.create_instance s parametrem FillType.PATTERN. Opět můžete přistupovat k nastavením plnění pomocí vlastnosti fill_settings a nastavit data vzoru a další vlastnosti. V poskytnutém kódu jsou data vzoru definována pomocí třídy PatternFillSettings a vlastnost clipping je nastavena na 1.

Po vytvoření vrstev plnění můžete přidat je do obrazu PSD pomocí metody add_layer. Můžete také specifikovat zobrazení názvu a další vlastnosti pro každou vrstvu plnění.

Nakonec můžete uložit obraz PSD a odpovídající obrázek PNG pomocí poskytnutého kódu. Nastavení PNG jsou nastavena na použití barev s průhledností.

Prosím, zkontroluje celý příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}
