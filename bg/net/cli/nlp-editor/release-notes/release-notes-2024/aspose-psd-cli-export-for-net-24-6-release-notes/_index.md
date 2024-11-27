---
title: Аспост.PSD CLI NLP Редактор за .NET 24.6 - Бележки към изданието
type: docs
weight: 90
url: /bg/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Тази страница съдържа бележки към изданието за [Аспост.PSD CLI NLP Редактор за .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Ключ**    | **Резюме**                                                                                   | **Категория** |
|:------------|:---------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Начално издание на Аспост.PSD CLI Приложения: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor | Подобрение    |


## **Примери за използване:**

**PSDNET-2110. Първоначално издание на приложението Аспост.PSD CLI NLP Редактор**

## **Използване от командния ред:**

{{% alert color="primary" %}}
Първоначално инсталирайте този дотнет инструмент:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Препоръчваме преди първото използване да стартирате следната команда:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
След тази команда ще можете да стартирате това приложение с краткото име nlp.cli вместо Aspose.PSD.CLI.NLP.Editor. Можете да посочите собственото си кратко име.
{{% /alert %}}

**Примери за използване**

1. Тази команда ще конвертира първия намерен файл (който може да бъде отворен с aspose.psd) от текущата папка и ще го запази във формат png с прозрачност. Също така, лицензът ще бъде настроен. Трябва да посочите лиценз само веднъж. При последващи стартиране, лицензът ще се използва от посочения път. Тази команда ще покаже високодетайлния дневник за обработката на NLP, ако е наличен.
{{< highlight bash >}}nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Тази команда намира файла с най-сходно име на "smth.psd". После ще настрои контраста и ще го запази в jpeg формат с най-добро качество. Името на изходния файл ще бъде отпечатано. То ще бъде smth.jpg 
{{< highlight bash >}}Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality{{< /highlight >}}

3. Тази команда ще завърти файл по посочения път и ще намали размера му на 25%. Името на изходния файл ще бъде отпечатано. Той ще бъде запазен в текущата папка на конзолата.
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd to 25%{{< /highlight >}}

4. Тази команда ще намери файла input.psd в C:\Users\someuser\Desktop\. След това ще намери слой с индекс 3 и ще я преоразмери на ширина 50px и височина 100px. След това този слой ще бъде запазен като PDF в C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. Тази команда ще отвори smth.psd в текущата папка, но всички ефекти ще бъдат деактивирани. След това този файл ще бъде конвертиран в BMP формат и като изходен файл output.bmp в текущата папка.
 {{< highlight bash >}}Open smth.psd without effects and save it to output.bmp{{< /highlight >}}

**Отказ от отговорност**

Това е експериментално приложение. Моля, опитайте го и оставете обратна връзка. Всяка обратна връзка е високо оценена. Нашата цел е да отведем приложението NO-Code на следващото ниво. Лесната интеграция във всяка сборна линия или бизнес процес е нашата цел.
