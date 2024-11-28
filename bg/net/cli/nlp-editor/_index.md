---
title: Aspose.PSD CLI Редактор на NLP Приложение за .NET
type: docs
weight: 10
url: /bg/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Обработка на естествен език Формати за файлове PSD, PSB и AI Конзолна библиотека на C# PSD API
description: Aspose.PSD базирано NLP редактор с конзолен интерфейс за PSD, PSB и AI формати на файлове. Автоматизация на CI/CD без необходимост от код. Поддържа обработка на естествен език за редактиране на PSD файлове. Просто напишете заявката си на естествен език, за да извършите различни операции като конверсия, корекция, оразмеряване и други. Не се изисква инсталиране на Adobe Photoshop или Adobe Illustrator и може да се изпълнява от конзолата без допълнителен код.
---

**![Лого на продукта Aspose.PSD за .NET](home_1.png)**

**Добре дошли в приложението за CLI на Aspose.PSD NLP Редактор за .NET**

Приложението Aspose.PSD CLI NLP Editor е лек конзолен инструмент за редактиране на PSD файлове с помощта на команди на естествения език. Лесно се интегрира в CI/CD конвейерите.

**Отказ от отговорност**

Това е експериментално приложение. Моля, опитайте го и оставете обратна връзка. Всяка обратна връзка се цени. Искаме да отведем приложението без код на следващото ниво. Лесната интеграция във всяка среда за създаване на команди или бизнес процес е нашата цел.

**Основен функционал на приложението за CLI на Aspose.PSD NLP Редактор за .NET**

1. Изпълнение на операции върху файлове PSD, PSB, AI с команди на естествения език.
2. Поддържа различни операции като конверсия, корекция, оразмеряване и други.
3. Автоматизация на CI/CD без необходимост от код.
4. Поддържа написването на заявки на естествен език за редактиране на PSD файлове.

## **Използване от командния ред**

{{% alert color="primary" %}}
Първоначално инсталирайте този инструмент за dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Препоръчваме, преди първото използване, изпълнете следната команда:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
След тази команда ще можете да използвате това приложение със съкращеното име nlp.cli вместо Aspose.PSD.CLI.NLP.Editor. Можете да посочите ваше собствено съкращение.
{{% /alert %}}

**Налични параметри за приложението за изрязване Aspose.PSD.CLI**

| **Аргумент** | **Описание**                         |
|:-------------|:----------------------------------------|
| всякакъв текст     | Задължително. Вашата команда на естествения език за актуализиране на файл PSD или PSB      |
| лиценз      | Път до лиценза.                    |
| подробно      | Показване на повече информация за конкретна команда. |
| настройка        | Създава bat файл в папка с инструменти за бързо извикване от конзолата. Пример: --setup psd.nlp. Тогава можете да извиквате инструмента с команда psd.nlp |


**Примери за използване**

1. Тази команда ще конвертира първия намерен файл (който може да се отвори с Aspose.PSD) от текущата папка и ще го запише във формат png с прозрачност. Лицензът също ще бъде настроен. Трябва да посочите лиценз само веднъж. Следващите изпълнения ще използват лиценза от посочения път. Тази команда ще покаже подробен протокол на обработката на NLP, ако е наличен. 
{{< highlight bash >}}
  nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Тази команда намира файла с най-сходно име на "smth.psd". След това ще коригира контраста и ще го запише в jpeg с най-добро качество. Името на изходния файл ще бъде отпечатано. То ще бъде smth.jpg
{{< highlight bash >}}
Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality
{{< /highlight >}}

3. Тази команда ще намери файл на посочения път и ще намали неговия размер до 25%. Изходният файл ще бъде отпечатан. Той ще бъде запазен в текущата папка на конзолата.
{{< highlight bash >}}
Resize file C:\Users\someuser\Desktop\input.psd to 25%
{{< /highlight >}}

4. Тази команда ще намери файл input.psd в C:\Users\someuser\Desktop\. След това ще намери слой с индекс 3 и ще го оразмери до ширина 50px и височина 100px. След това този слой ще бъде запазен като PDF в C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. Тази команда ще отвори smth.psd в текущата папка, но всички ефекти ще бъдат деактивирани. И след това този файл ще бъде конвертиран в BMP формат и като output.bmp в текущата папка.
 {{< highlight bash >}}
 Open smth.psd without effects and save it to output.bmp
  {{< /highlight >}}

**Моля, проверете другите [Aspose.PSD CLI Приложения](https://docs.aspose.com/psd/net/cli) за .NET, ако имате нужда от добавяне на поддръжка за PSD, PSB и AI формати към вашия работен процес**

1. [Aspose.PSD CLI Конвертиране](/psd/bg/net/cli/convert)
2. [Aspose.PSD CLI Изрязване](/psd/bg/net/cli/crop)
3. [Aspose.PSD CLI Оразмеряване](/psd/bg/net/cli/resize)
4. [Aspose.PSD CLI Експорт](/psd/bg/net/cli/export)
5. [Aspose.PSD CLI Редактор на NLP](/psd/bg/net/cli/nlp-editor)

**Моля, проверете Aspose.PSD за .NET или [други платформи]**

Aspose.PSD CLI Приложенията са готово за използване решение за популярни операции. Ако имате нужда от гъвкаво решение, моля, проверете пълната версия на Aspose.PSD

1. [Aspose.PSD за .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD за Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD за Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Ресурси за Aspose.PSD за .NET**

По-долу са връзки към някои полезни ресурси, които може да ви потребителски към вашите задачи.

- [Aspose.PSD CLI Приложения за .NET Онлайн Документация](/psd/bg/net/cli/conversion)
- [Aspose.PSD за CLI Приложения за .NET Бележки за изданието](/psd/bg/net/cli/conversion/release-notes/)
- [Aspose.PSD за CLI Приложения .NET Страница на продукта](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD за .NET API Ръководство за справка](https://reference.aspose.com/net/psd)
- [Изтеглете примери от хранилището на GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD за .NET Форум за безплатна поддръжка](https://forum.aspose.com/c/psd)
- [Aspose.PSD за .NET Платена помощна система за поддръжка](https://helpdesk.aspose.com/)
