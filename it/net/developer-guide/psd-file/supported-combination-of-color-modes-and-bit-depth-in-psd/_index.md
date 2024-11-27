---
title: Combinazione supportata delle modalità colore e profondità di bit in PSD
type: docs
weight: 80
url: /it/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Descrizione**
Aspose.PSD supporta l'apertura dei file PSD con qualsiasi combinazione di Modalità Colore e Profondità di Bit nei file PSD di Adobe Photoshop. Puoi aprire tali file e utilizzare l'API a basso livello per modificare il contenuto del file. Ma per alcune combinazioni meno popolari possono esserci problemi specifici, alcuni dei quali legati alle limitazioni delle Modalità Colore.

## **Combinazione di esportazione supportata delle modalità colore e profondità di bit in PSD in modalità di sola lettura**

| |Bitmap|Scala di grigi|Indicizzato|RGB|CMYK|Multicanale|Duotono|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Profondità 1|Sì[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Profondità 8|-|Sì|Sì|Sì|Sì|No Q3-Q4|No Q3-Q4|Sì[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Profondità 16|-|Sì|-|Sì|Sì|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|No (Q3-Q4)|
|Profondità 32|-|Sì*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Sì*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Problemi minori in alcuni casi

## **Combinazione di esportazione supportata delle modalità colore e profondità di bit in PSD in modalità modificabile**

| |Bitmap|Scala di grigi|Indicizzato|RGB|CMYK|Multicanale|Duotono|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Profondità 1|Sì|-|-|-|-|-|-|-|
|Profondità 8|-|Sì|No|Sì|Sì|No Q3-Q4|No Q3-Q4|Sì*|
|Profondità 16|-|Sì|-|Sì|Sì*|-|-|No (Q3-Q4)|
|Profondità 32|-|No (Q3-Q4)|-|No (Q3-Q4)|-|-|-|-|
\* Problemi minori in alcuni casi

Se hai bisogno del supporto di una specifica combinazione di Modalità Colore / Profondità di Bit, puoi postare su [Aspose Forums](https://forum.aspose.com/c/psd)
