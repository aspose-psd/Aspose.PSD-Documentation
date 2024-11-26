---
title: Приложение Aspose.PSD CLI NLP Editor для .NET
type: docs
weight: 10
url: /ru/net/cli/nlp-editor/
is_root: false
keywords: CLI Инструмент Photoshop NLP Обработка естественным языком PSD Консольная библиотека C# API
description: Приложение Aspose.PSD CLI NLP Editor для редактирования файлов PSD, PSB и AI. Автоматизация CI/CD без написания кода. Поддерживает обработку естественного языка для редактирования файлов PSD. Просто напишите свой запрос на естественном языке для выполнения таких операций, как конвертация, коррекция, изменение размера и др. Для работы не требуется установка Adobe Photoshop или Adobe Illustrator, и может быть запущено в консоли без дополнительного кода.
---

**![Логотип продукта Aspose.PSD для .NET](home_1.png)**

**Добро пожаловать в приложение Aspose.PSD NLP Editor CLI для .NET**

Приложение Aspose.PSD CLI NLP Editor является легковесной консольной утилитой для редактирования файлов PSD с использованием команд на естественном языке. Просто интегрируйте в CI/CD Pipeline.

**Отказ от ответственности**

Это экспериментальное приложение. Попробуйте его и оставьте отзыв. Любой отзыв высоко оценивается. Мы хотим поднять приложение без кода на новый уровень. Легкая интеграция в любую конвейерную сборку или бизнес-процесс — наша цель.

**Основные функции приложения Aspose.PSD NLP Editor CLI для .NET**

1. Выполнение операций с файлами PSD, PSB, AI с помощью команд на естественном языке.
2. Поддержка различных операций, таких как конвертация, коррекция, изменение размера и другие.
3. Автоматизация CI/CD без написания кода.
4. Поддержка написания запросов на естественном языке для редактирования файлов PSD.

## **Использование из командной строки:**

{{% alert color="primary" %}}
Сначала установите этот инструмент для dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Рекомендуем перед первым использованием запустить следующую команду:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
После этой команды вы сможете запускать это приложение с коротким именем nlp.cli вместо Aspose.PSD.CLI.NLP.Editor. Вы также можете указать собственное короткое имя.
{{% /alert %}}


**Доступные параметры для приложения Aspose.PSD.CLI.Crop**

| **Аргумент** | **Описание**                         |
|:-------------|:----------------------------------------|
| any text     | Обязательно. Ваша команда на естественном языке для обновления файла PSD или PSB      |
| license      | Путь к лицензии.                    |
| verbose      | Отображение более подробной информации о конкретной команде. |
| setup        | Создает файл .bat в папке с инструментами для быстрого вызова из консоли. Пример: --setup psd.nlp. Затем вы можете вызвать инструмент с командой psd.nlp |

**Примеры использования**

1. Эта команда сконвертирует первый найденный файл (который можно открыть с помощью aspose.psd) из текущей папки и сохранит его в формате png с прозрачностью. Также будет настроена лицензия. Вам нужно указать лицензию всего один раз. При последующих запусках лицензия будет использоваться из указанного пути. Эта команда покажет подробный журнал обработки NLP, если он доступен.
{{< highlight bash >}}
  nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Эта команда найдет файл с наиболее похожим именем на "smth.psd". Затем она скорректирует контраст и сохранит его в jpeg с лучшим качеством. Наименование выходного файла будет выведено. Это будет smth.jpg
{{< highlight bash >}}
Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality
{{< /highlight >}}

3. Эта команда наложит ветер на указанный путь к файлу и уменьшит его размер до 25%. Выходной файл будет выведен. Он будет сохранен в текущей папке консоли.
{{< highlight bash >}}
Resize file C:\Users\someuser\Desktop\input.psd to 25%
{{< /highlight >}}

4. Эта команда найдет файл input.psd в C:\Users\someuser\Desktop\. Затем она найдет слой с индексом 3 и изменит его размер на ширину 50px и высоту 100px. Затем этот слой будет сохранен как PDF в C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. Эта команда откроет файл smth.psd в текущей папке, но все эффекты будут отключены. Затем этот файл будет преобразован в формат BMP и сохранен как output.bmp в текущей папке.
 {{< highlight bash >}}
 Open smth.psd without effects and save it to output.bmp
  {{< /highlight >}}

**Обратитесь к [другим Приложениям Aspose.PSD CLI](https://docs.aspose.com/psd/net/cli) для .NET, если вам нужна поддержка форматов PSD, PSB и AI в вашем рабочем процессе**

1. [Aspose.PSD CLI Конвертация](/ru/psd/net/cli/convert)
2. [Aspose.PSD CLI Кадрирование](/ru/psd/net/cli/crop)
3. [Aspose.PSD CLI Изменение размера](/ru/psd/net/cli/resize)
4. [Aspose.PSD CLI Экспорт](/ru/psd/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/ru/psd/net/cli/nlp-editor)

**Обратитесь к Aspose.PSD для .NET или [другим платформам]**

Приложения Aspose.PSD CLI — это готовое решение для популярных операций. Если вам нужно гибкое решение, обратитесь к полной версии Aspose.PSD

1. [Aspose.PSD для .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD для Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD для Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Ресурсы Aspose.PSD для .NET**

Ниже приведены ссылки на некоторые полезные ресурсы, которые вам могут потребоваться для выполнения ваших задач.

- [Онлайн-документация Aspose.PSD CLI Applications для .NET](/ru/psd/net/cli/conversion)
- [Заметки о выпусках Aspose.PSD для CLI Applications для .NET](/ru/psd/net/cli/conversion/release-notes/)
- [Страница продукта Aspose.PSD для CLI Applications .NET](https://products.aspose.com/psd/net/cli)
- [Руководство по API Aspose.PSD для .NET](https://reference.aspose.com/net/psd)
- [Скачать примеры на GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Бесплатные форумы поддержки Aspose.PSD для .NET](https://forum.aspose.com/c/psd)
- [Помощь по платной поддержке Aspose.PSD для .NET](https://helpdesk.aspose.com/)
