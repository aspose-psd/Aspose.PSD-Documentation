---
title: Przykład użycia warstw grup w Aspose.PSD dla C#
weight: 100
type: docs
description: Wykorzystanie warstwy grupowej pliku PSD za pomocą C#
keywords: [warstwa grupowa, warstwa grupy, dodawanie warstwy do grupy, api PSD, C#, csharp, przykład kodu]
url: pl/net/psd-group-layer/
---

## Przegląd

Warstwy grup w Aspose.PSD dla C# pozwalają na efektywne organizowanie i manipulowanie warstwami w pliku PSD. Korzystając z warstw folderów, można grupować wiele warstw razem i stosować transformacje lub efekty do całej grupy.

Ten przykład demonstruje tworzenie nowego obrazu PSD za pomocą `PsdImage.Create`. Następnie tworzony jest nowy obiekt `LayerGroup` za pomocą `AddLayerGroup` z obiektu `PsdImage`. Warstwa grupy otrzymuje nazwę "Folder", zostaje wstawiona na indeksie 0 i ustawiona jako widoczna.

Kolejno, tworzone są dwie obiekty `Layer` z ustawionymi właściwościami `DisplayName`. Te warstwy są dodawane do warstwy grupy za pomocą `AddLayer`.

Warstwy wewnątrz grupy można uzyskać za pomocą właściwości `Layers` obiektu `LayerGroup`. Przykład zakłada, że nazwy wyświetlania pierwszej i drugiej warstwy w grupie to "Warstwa 1" i "Warstwa 2".

Po modyfikacji warstw grupy, zaktualizowany obraz PSD jest zapisywany za pomocą metody `Save` obiektu `PsdImage`.

Ten podstawowy przykład wprowadza pracę z warstwami grupowymi za pomocą Aspose.PSD dla C#. Biblioteka oferuje zaawansowane funkcje do manipulowania i transformowania warstw w plikach PSD. Aby uzyskać bardziej szczegółowe przykłady i funkcje, zapoznaj się z dokumentacją Aspose.PSD dla C#.

Poniżej przedstawiono przykładowy kod demonstrujący użycie warstw grup w Aspose.PSD dla C#:

## Przykład

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Aby uzyskać bardziej szczegółowe informacje i przykłady, odwiedź [dokumentację Aspose.PSD dla C#](https://docs.aspose.com/psd/net/).
