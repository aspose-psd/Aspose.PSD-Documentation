---
title: Vrstva úprav kanálového mixéru
type: docs
weight: 30
url: /cs/java/layer-types/adjustment-layer/channel-mixer/
---

# Práce s vrstvou úprav kanálového mixéru v Java

Dnes se podíváme na to, jak programaticky míchat barvy kanálů v dokumentech Photoshopu v Javě. Jelikož editor Photoshopu nepodporuje skriptování v Javě, použijeme speciální knihovnu pro manipulaci s formátem souboru PSD nazvanou Aspose.PSD for Java.

Knihovna obsahuje **API pro práci s barevnými kanály**. Existuje několik způsobů, jak smíchat barvy, ale v tomto článku se zaměříme na vrstvu úprav kanálového mixéru.

API vrstvy úprav kanálového mixéru **umožňuje hrát si s barevnými kanály** k vytvoření různých barevných efektů a dokonce převést obrázek na černobílý. Následně se podíváme, jak aplikovat vrstvu úprav kanálového mixéru na existující dokument Photoshopu pomocí Aspose.PSD for Java, ale nejdříve si povíme o obecných funkcích API.

## Přehled API

Při vytváření vrstvy úprav kanálového mixéru není nic zvláštního. Může být přidána pomocí [výchozí tovární metody](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) vracející instanci třídy ChannelMixerLayer. Tato třída obsahuje obecnou funkcionalitu, jako je možnost monochromie a metodu pro získání výstupního kanálu. Konkrétní výstupní kanál může být jedním ze dvou typů: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) nebo [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Typ [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) závisí na [režimu barev](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) obrázku.

## Učiňte obrázek monochromatickým

Nyní se podívejme na příklad aplikace vrstvy úprav kanálového mixéru na existující dokument Photoshopu. Jelikož tento typ vrstvy úprav zatím nepodporuje přednastavení (presety), **znovu vytvoříme přednastavení Černá a Bílá Infrakamera (RGB) Photoshopu** (a). Tento preset bude aplikován na obrázek kvetoucího stromu (b). Výsledkem má být efekt infračervené fotografie (c).

![Příklad vrstvy úprav kanálového mixéru](channel-mixer-adjustment-psd-layer-figure-1.png) Nejprve, pro znovuvytvoření přednastavení Černá a Bílá Infrakamera (RGB) Photoshopu je nutné povolit příznak monochromie a nastavit vhodné hodnoty pro každou barvu (červenou, zelenou a modrou) pro šedý výstupní kanál:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

Obrázek musí být v režimu barev RGB, aby kód fungoval (kvůli přetypování na třídu RgbMixerChannel). Režim barev CMYK je také podporován, ale pouze pro obrázky s odpovídajícím režimem barev.

Mějte na paměti, že hodnota každé barvy, stejně jako vlastnost Constant, musí být v rozsahu od -200 do 200.

## Závěr

V tomto článku jsme zvážili, jak pracovat s Kanálovým mixérem API Aspose.PSD for Java pro úpravu barev v barevných kanálech a převod obrázku na černobílý.
