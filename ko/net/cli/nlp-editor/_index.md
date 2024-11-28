---
title: Aspose.PSD CLI NLP 편집기 응용프로그램 (.NET용)
type: docs
weight: 10
url: /ko/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Natural-Language-Processing PSD Console C# Library PSD API
description: Aspose.PSD 기반 NLP 편집기 CLI 응용프로그램으로 PSD, PSB 및 AI 파일 형식을 지원합니다. 노코드 CI/CD 자동화를 제공하며, PSD 파일 편집을 위해 자연어 처리를 지원합니다. 자연어로 요청을 작성하여 변환, 조정, 크기 조절 등 다양한 작업을 수행할 수 있습니다. Adobe Photoshop 또는 Adobe Illustrator를 설치할 필요가 없으며 추가 코드 없이 콘솔에서 실행할 수 있습니다.
---

**![Aspose.PSD for .NET 제품 로고](home_1.png)**

**Aspose.PSD NLP 편집기 CLI 응용프로그램 (.NET용)에 오신 것을 환영합니다**

Aspose.PSD CLI NLP 편집기 응용프로그램은 자연어 명령을 사용하여 PSD 파일을 편집하는 가벼운 콘솔 유틸리티입니다. CI/CD 파이프라인에 쉽게 통합할 수 있습니다.

**면책사항**

이는 실험적인 응용프로그램입니다. 사용해보고 피드백을 남겨주세요. 모든 피드백을 높이 평가합니다. 노코드 응용프로그램을 다음 수준으로 끌어올리는 것이 목표입니다. 어떠한 빌드 파이프라인이나 비즈니스 프로세스에도 쉽게 통합할 수 있습니다.

**Aspose.PSD NLP 편집기 CLI 응용프로그램 (.NET용)의 주요 기능**

1. 자연어 명령을 사용하여 PSD, PSB, AI 파일에서 작업 수행
2. 변환, 조정, 크기 조절 등 다양한 작업 지원
3. 노코드 CI/CD 자동화
4. PSD 파일 편집을 위해 자연어로 요청 작성 지원

## **명령줄에서 사용법:**

{{% alert color="primary" %}}
먼저 이 dotnet 도구를 설치하세요:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

첫 사용 전에 다음 명령을 실행하는 것을 권장합니다:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
이 명령을 실행한 후에는 Aspose.PSD.CLI.NLP.Editor 대신 nlp.cli라는 짧은 이름으로 이 응용프로그램을 실행할 수 있습니다. 사용자 고유의 짧은 이름을 지정할 수 있습니다.
{{% /alert %}}

**Aspose.PSD.CLI.Crop 응용프로그램을 위한 사용 가능한 매개변수**

| **인수**     | **설명**                                 |
|:-------------|:----------------------------------------|
| any text     | 필수. PSD 또는 PSB 파일을 업데이트할 자연어 명령     |
| license      | 라이선스 경로                            |
| verbose      | 특정 명령에 대해 자세한 정보 출력           |
| setup        | 콘솔에서 빠르게 호출하기 위한 tools 폴더에 bat 파일 생성. 예: --setup psd.nlp. 그럼 psd.nlp 명령으로 도구를 호출할 수 있음 |

**사용 예**

1. 이 명령은 현재 폴더에서 찾은 첫 번째 파일(Aspose.PSD로 열 수 있는 파일)을 PNG 형식으로 투명도와 함께 저장합니다. 또한 라이선스가 설정됩니다. 라이선스는 한 번만 지정하면 다음 실행부터 지정된 경로에서 사용됩니다. 이 명령이 사용 가능한 경우 NLP 처리에 대한 자세한 로그를 표시합니다.
{{< highlight bash >}}
  nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. 이 몤령은 "smth.psd"와 가장 유사한 이름을 가진 파일을 찾습니다. 그런 다음 대조를 조정하고 최고 품질로 JPEG 형식으로 저장합니다. 출력 파일의 이름이 나옵니다. 파일 이름은 smth.jpg가 될 것입니다.
{{< highlight bash >}}
Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality
{{< /highlight >}}

3. 이 몤령은 지정된 경로의 파일을 연 다음 크기를 25%로 줄입니다. 출력 파일의 이름이 나옵니다. 이 파일은 콘솔의 현재 폴더에 저장됩니다.
{{< highlight bash >}}
Resize file C:\Users\someuser\Desktop\input.psd to 25%
{{< /highlight >}}

4. 이 명령은 C:\Users\someuser\Desktop\에 있는 input.psd 파일을 찾습니다. 그런 다음 인덱스 3에 해당하는 레이어를 찾아 너비 50픽셀, 높이 100픽셀로 크기를 조정합니다. 그런 다음 이 레이어를 C:\Users\someuser\Desktop\output.pdf에 PDF 형식으로 저장합니다.
{{< highlight bash >}}
 Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. 이 명령은 현재 폴더의 smth.psd를 엽니다. 그러나 모든 효과가 비활성화됩니다. 그런 다음 이 파일을 BMP 형식으로 변환하여 현재 폴더의 output.bmp로 저장합니다.
 {{< highlight bash >}}
 Open smth.psd without effects and save it to output.bmp
  {{< /highlight >}}

**다른 [Aspose.PSD CLI 응용프로그램](https://docs.aspose.com/psd/net/cli)을 확인하십시오** 

1. [Aspose.PSD CLI Convert](/psd/ko/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/ko/net/cli/crop)
3. [Aspose.PSD CLI Resize](/psd/ko/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/ko/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/ko/net/cli/nlp-editor)

**Aspose.PSD for .NET 또는 [다른 플랫폼] 확인**

Aspose.PSD CLI 응용프로그램은 인기 있는 작업을 위한 사용 준비 완료 솔루션입니다. 유연한 솔루션이 필요하면 Aspose.PSD의 전체 버전을 확인하십시오.

1. [Aspose.PSD for .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD for Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD for Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Aspose.PSD for .NET 리소스** 

아래는 작업을 수행하는 데 필요한 몇 가지 유용한 리소스에 대한 링크입니다.

- [.NET용 Aspose.PSD CLI 응용프로그램 온라인 설명서](/psd/ko/net/cli/conversion)
- [.NET용 Aspose.PSD CLI 응용프로그램 릴리스 노트](/psd/ko/net/cli/conversion/release-notes/)
- [.NET용 Aspose.PSD CLI 응용프로그램 제품 페이지](https://products.aspose.com/psd/net/cli)
- [.NET용 Aspose.PSD API 참조 가이드](https://reference.aspose.com/net/psd)
- GitHub 저장소에서 예제 다운로드하기](https://github.com/aspose-psd/CLI-Applications)
- [.NET용 Aspose.PSD 무료 지원 포럼](https://forum.aspose.com/c/psd)
- [.NET용 Aspose.PSD 유상 지원 도움말 데스크](https://helpdesk.aspose.com/)
