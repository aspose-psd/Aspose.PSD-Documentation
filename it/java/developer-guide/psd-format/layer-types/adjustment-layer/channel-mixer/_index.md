---
title: Layer di aggiustamento del mixer di canale
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/channel-mixer/
---

# Lavorare con il layer di aggiustamento del mixer di canale di Photoshop in Java

Oggi vedremo come mescolare i colori dei canali nei documenti di Photoshop in modo programmato in Java. Poiché l'editor di Photoshop non supporta lo scripting Java, utilizzeremo una libreria di manipolazione del formato file PSD chiamata Aspose.PSD per Java.

La libreria contiene **API per lavorare con i canali di colore**. Ci sono diverse modalità per mescolare i colori ma, in questo articolo, ci concentreremo sul layer di aggiustamento del mixer di canale.

L'API del layer di aggiustamento del mixer di canale **consente di giocare con i canali di colore** per creare immagini tinte o effetti di colore creativi diversi o anche convertire l'immagine in bianco e nero. In seguito, vedremo come applicare il layer di aggiustamento del mixer di canale a un documento esistente di Photoshop usando Aspose.PSD per Java, ma prima dobbiamo parlare delle funzionalità generali dell'API.

## Panoramica dell'API

Non c'è niente di speciale nella creazione del layer di aggiustamento del mixer di canale. Può essere aggiunto attraverso [il metodo factory predefinito](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) che restituisce un'istanza della classe ChannelMixerLayer. Questa classe contiene funzionalità generali come l'opzione Monochrome e un metodo per ottenere un canale di output. Un particolare canale di output può essere di due tipi: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) o [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Il tipo di [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) dipende dalla [modalità di colore](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) dell'immagine.

## Rendere l'immagine monocromatica

Ora, consideriamo un esempio di applicazione del layer di aggiustamento del mixer di canale a un documento di Photoshop esistente. Poiché questo tipo di layer di aggiustamento non supporta ancora i preset, ricreeremo il preset di Photoshop Bianco e Nero Infrarosso (RGB) (a). Il preset verrà applicato all'immagine di un albero in fiore (b). Come risultato, vogliamo ottenere l'effetto della fotografia infrarossi (c).

![Esempio di Layer di Aggiustamento del Mixer di Canale](channel-mixer-adjustment-psd-layer-figure-1.png) Prima, per ricreare il preset di Photoshop Bianco e Nero Infrarosso (RGB) è necessario abilitare il flag monocromatico e impostare i valori grezzi appropriati per ciascun colore (rosso, verde e blu) per il canale di output Grigio:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

L'immagine deve essere in modalità colore RGB affinché il codice funzioni (a causa del casting alla classe RgbMixerChannel). La modalità colore CMYK è anche supportata ma solo per immagini con la corrispondente modalità colore.

Tieni presente che il valore di ciascun colore così come la proprietà Constant devono essere compresi nell'intervallo da -200 a 200.

## Conclusione

In questo articolo abbiamo considerato come lavorare con l'API del mixer di canale di Aspose.PSD per Java per regolare i colori nei canali di colore e convertire l'immagine in bianco e nero.
