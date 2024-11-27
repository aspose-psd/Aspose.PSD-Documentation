---
title: Combinación admitida de modos de color y profundidad de bits en PSD
type: docs
weight: 80
url: /es/net/combinacion-admitida-de-modos-de-color-y-profundidad-de-bits-en-psd/
---

## **Descripción**
Aspose.PSD admite la apertura de archivos PSD con cualquier combinación de Modo de color y Profundidades de bits en archivos PSD de Adobe Photoshop. Puede abrir dichos archivos y utilizar la API de bajo nivel para modificar el contenido del archivo. Sin embargo, para algunas combinaciones menos populares pueden surgir problemas específicos, algunos de ellos relacionados con Limitaciones de modos de color.

## **Combinación admitida de exportación de modos de color y profundidad de bits en PSD en modo de solo lectura**

| | Bitmap | Escala de grises | Indexado | RGB | CMYK | Multicanal | Duotono | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Profundidad 1 | Sí[](https://issue.kharkov.dynabic.com/issues/PSDNET-283) | - | - | - | - | - | - | - |
| Profundidad 8 | - | Sí | Sí | Sí | Sí | No Q3-Q4 | No Q3-Q4 | Sí[](https://issue.kharkov.dynabic.com/issues/PSDNET-290) |
| Profundidad 16 | - | Sí | - | Sí | Sí | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-287) | - | No (Q3-Q4) |
| Profundidad 32 | - | Sí*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125) | - | Sí* | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-285) | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-288) | - | - |
\* Problemas menores en algunos casos

## **Combinación admitida de exportación de modos de color y profundidad de bits en PSD en modo editable**

| | Bitmap | Escala de grises | Indexado | RGB | CMYK | Multicanal | Duotono | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Profundidad 1 | Sí | - | - | - | - | - | - | - |
| Profundidad 8 | - | Sí | No | Sí | Sí | No Q3-Q4 | No Q3-Q4 | Sí* |
| Profundidad 16 | - | Sí | - | Sí | Sí* | - | - | No (Q3-Q4) |
| Profundidad 32 | - | No (Q3-Q4) | - | No (Q3-Q4) | - | - | - | - |
\* Problemas menores en algunos casos


Si necesita soporte para una combinación específica de Modo de color / Profundidad de bits, puede publicar en los [Foros de Aspose](https://forum.aspose.com/c/psd)
