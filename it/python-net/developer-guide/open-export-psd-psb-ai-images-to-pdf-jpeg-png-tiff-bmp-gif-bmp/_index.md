---
title: Aprire file PSD, PSB e AI ed esportarli in PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Esempio di esportazione dei file PSD, PSB e AI in altri formati
keywords: [aprire psd, aprire ai, aprire psb, esportare in png, esportare in pdf, esportare in jpeg, esportare in tiff, api psd, python, esempio di codice]
url: it/python-net/aprire-esportare-immagini-psd-psb-ai-in-pdf-jpeg-png-tiff-bmp-gif/
---

## **Panoramica**
Per convertire i file PSD, PSB e AI in formati diversi, è possibile utilizzare la libreria Aspose.PSD in Python. Questa libreria fornisce varie opzioni e impostazioni per personalizzare il processo di conversione.

Innanzitutto, è necessario importare le classi e i moduli necessari dalla libreria Aspose.PSD. Assicurati di aver installato la libreria prima di eseguire il codice.

In questo codice, definiamo varie opzioni per formati diversi, come PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB e PSD. Queste opzioni ti permettono di personalizzare il file di output in base alle tue esigenze.

Successivamente, definiamo un dizionario "formats" che mappa le estensioni dei file alle rispettive opzioni di salvataggio.

Per convertire un file PSD in altri formati, è necessario caricare il file PSD utilizzando PsdImage.load() e quindi iterare attraverso il dizionario dei formati. Per ciascun formato, specificare il nome del file di output e salvare l'immagine utilizzando il metodo image.save().

Analogamente, per convertire un file AI in altri formati, caricare il file AI utilizzando AiImage.load() e iterare attraverso il dizionario dei formati. Specificare il nome del file di output e salvare l'immagine utilizzando il metodo image.save().

Assicurati di fornire i percorsi corretti dei file PSD e AI di origine.

Ecco fatto! Ora puoi utilizzare questo codice per convertire i file PSD, PSB e AI in vari formati utilizzando Aspose.PSD per Python.

Consulta l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
