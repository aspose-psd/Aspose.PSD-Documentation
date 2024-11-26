---
title: Otwórz pliki PSD, PSB i AI i wyeksportuj je do formatów PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Przykład eksportu plików PSD, PSB i AI do innych formatów
keywords: [otwórz psd, otwórz ai, otwórz psb, eksportuj do png, eksportuj do pdf, eksportuj do jpeg, eksportuj do tiff, psd api, python, przykład kodu]
url: pl/python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Przegląd**
Aby konwertować pliki PSD, PSB i AI do różnych formatów, możesz użyć biblioteki Aspose.PSD w języku Python. Ta biblioteka oferuje różne opcje i ustawienia, pozwalające dostosować proces konwersji.

Najpierw musisz zaimportować niezbędne klasy i moduły z biblioteki Aspose.PSD. Upewnij się, że biblioteka jest zainstalowana przed uruchomieniem kodu.

W tym kodzie definiujemy różne opcje dla różnych formatów, takich jak PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB i PSD. Te opcje pozwalają dostosować plik wyjściowy według Twoich wymagań.

Następnie definiujemy słownik `formats`, który mapuje rozszerzenia plików na ich odpowiednie opcje zapisu.

Aby skonwertować plik PSD do innych formatów, musisz załadować plik PSD za pomocą PsdImage.load(), a następnie przeiterować przez słownik `formats`. Dla każdego formatu określ nazwę pliku wyjściowego i zapisz obraz za pomocą metody image.save().

Podobnie, aby skonwertować plik AI do innych formatów, załaduj plik AI za pomocą AiImage.load() i przeiteruj przez słownik `formats`. Określ nazwę pliku wyjściowego i zapisz obraz za pomocą metody image.save().

Upewnij się, że podajesz poprawne ścieżki plików źródłowych PSD i AI.

To wszystko! Teraz możesz użyć tego kodu do konwertowania plików PSD, PSB i AI do różnych formatów za pomocą Aspose.PSD dla Pythona.

Proszę sprawdź pełen przykład.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
