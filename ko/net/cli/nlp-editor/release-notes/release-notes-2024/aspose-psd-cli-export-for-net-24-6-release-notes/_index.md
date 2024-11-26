---
title: Aspose.PSD CLI NLP 편집기 for .NET 24.6 - 릴리스 노트
type: docs
weight: 90
url: /ko/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD CLI NLP 편집기 for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **항목**     | **요약**                                                                                 | **카테고리** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI 앱의 첫 릴리스: Aspose.PSD.CLI.Export 및 Aspose.PSD.CLI.NLP.Editor |  향상 |


## **사용 예시:**

**PSDNET-2110. Aspose.PSD CLI NLP 편집기 애플리케이션의 첫 릴리스**

## **명령줄에서 사용:**

{{% alert color="primary" %}}
먼저 이 닷넷 도구를 설치하십시오:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

첫 사용 전에 다음 명령을 실행하는 것을 권장합니다:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
이 명령을 실행한 후에 Aspose.PSD.CLI.NLP.Editor 대신 nlp.cli의 짧은 이름으로 이 애플리케이션을 실행할 수 있습니다. 사용자 정의 짧은 이름을 지정할 수도 있습니다.
{{% /alert %}}

**사용 예시**

1. 이 명령은 현재 폴더에서 찾은 첫 번째 파일(Aspose.psd로 열 수 있는)을 투명한 png 형식으로 변환합니다. 또한 라이센스가 설정됩니다. 라이센스는 한 번만 지정하면됩니다. 다음 실행에서는 지정된 경로에서 라이센스가 사용됩니다. 이 명령은 NLP 처리의 상세 로그를 표시할 수 있습니다.
{{< highlight bash >}}nlp.cli 파일을 투명도가 있는 png 형식으로 변환합니다. --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. 이 명령은 "smth.psd"에 가장 유사한 이름의 파일을 찾습니다. 그런 다음 대조를 조정하고 최상의 품질로 jpeg로 저장합니다. 출력 파일의 이름이 인쇄됩니다. 이는 smth.jpg가 될 것입니다.
{{< highlight bash >}}smth.psd에서 이름이 ellipse인 레이어의 대조를 조절하고 최상의 품질로 output.jpg에 저장합니다{{< /highlight >}}

3. 이 명령은 지정된 경로의 파일을 찾아 크기를 25%로 축소합니다. 출력 파일은 인쇄됩니다. 이것은 콘솔의 현재 폴더에 저장될 것입니다.
{{< highlight bash >}}C:\Users\someuser\Desktop\input.psd 파일의 크기를 25%로 조정합니다{{< /highlight >}}

4. 이 명령은 C:\Users\someuser\Desktop\에서 input.psd 파일을 찾습니다. 그런 다음 레이어 인덱스 3을 찾아 너비가 50px이고 높이가 100px로 조정합니다. 그런 다음 이 레이어는 C:\Users\someuser\Desktop\output.pdf에 PDF로 저장됩니다.
{{< highlight bash >}}C:\Users\someuser\Desktop\input.psd의 인덱스 3 레이어 크기를 너비 50px, 높이 100px로 조정하여 C:\Users\someuser\Desktop\output.pdf에 저장합니다{{< /highlight >}}

5. 이 몤령은 현재 폴더의 smth.psd를 엽니다. 그러나 모든 효과가 비활성화됩니다. 그런 다음이 파일은 BMP 형식으로 변환되어 현재 폴더의 output.bmp로 저장됩니다.
{{< highlight bash >}}효과 없이 smth.psd를 열어 output.bmp로 저장합니다{{< /highlight >}}

**면책 조항**

이것은 실험적인 애플리케이션입니다. 사용해보고 피드백을 남겨주십시오. 모든 피드백은 매우 감사히 받습니다. NO-Code 애플리케이션을 다음 수준으로 이끌기를 바랍니다. 어떠한 빌드 파이프라인이나 비즈니스 프로세스에도 쉽게 통합할 수 있도록 하는 것이 우리의 목표입니다.

