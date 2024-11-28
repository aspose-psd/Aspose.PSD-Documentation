---
title: 예제 실행 방법
type: 문서
weight: 90
url: /ko/net/how-to-run-the-examples/
description: GitHub에 호스팅된 PSD 파일 형식 라이브러리와 관련된 예제를 실행하는 방법을 배웁니다.
---

## **소프트웨어 요구 사항**
예제를 다운로드하고 실행하기 전에 다음 요구 사항을 충족하는지 확인하십시오.

1. Visual Studio 2010 또는 그 이상
1. Visual Studio에 NuGet 패키지 관리자가 설치되어 있는지 확인하십시오. Visual Studio에 최신 NuGet API 버전이 설치되어 있는지 확인하십시오. NuGet 패키지 관리자를 설치하는 방법에 대한 자세한 내용은 [여기](http://docs.nuget.org/ndocs/guides/install-nuget)를 참조하십시오.
1. Tools->Options->NuGet Package Manager->Package Sources로 이동하여 옵션 **nuget.org**가 선택되어 있는지 확인하싀오.
1. 예제 프로젝트는 NuGet 자동 패키지 복원 기능을 사용하므로 사용 중인 컴퓨터에서 인터넷 연결이 활성화되어 있어야 합니다. 예제를 실행할 기계에서 인터넷 연결이 활성화되어 있지 않은 경우 예제 프로젝트에서 Aspose.Imaging.dll에 참조를 추가하는 방법은 [Installation](/psd/ko/net/installation/)을 확인하십시오.
## **GitHub에서 다운로드**
.NET용 Aspose.PSD의 모든 예제는 [GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET)에 호스팅되어 있습니다.

- 즐겨 사용하는 GitHub 클라이언트를 사용하여 저장소를 클론하거나 [여기](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip)에서 ZIP 파일을 다운로드할 수 있습니다.
- ZIP 파일의 내용을 컴퓨터의 임의의 폴더에 압축 해제하십시오. 모든 예제는 **Examples** 폴더에 있습니다.
- C#용 Visual Studio 솔루션 파일이 있습니다.
- 프로젝트는 Visual Studio 2013에서 작성되었지만 솔루션 파일은 Visual Studio 2010 SP1 이상과 호환됩니다.
- Visual Studio에서 솔루션 파일을 열고 프로젝트를 빌드하십시오.
- 처음 실행할 때 종속성은 자동으로 NuGet을 통해 다운로드됩니다.
- **Examples**의 루트 폴더에있는 **Data** 폴더는 C# 예제에서 사용하는 입력 파일이 포함되어 있습니다. **Data** 폴더를 예제 프로젝트와 함께 다운로드하는 것이 필수적입니다.
- RunExamples.cs 파일을 열고, 모든 예제는 여기에서 호출됩니다.
- 프로젝트 내부에서 실행하려는 예제에 대한 주석을 제거하십시오.

문제 설정 또는 예제 실행 중 문제가 발생한 경우 우리 포럼을 통해 언제든지 문의하십시오.
## **기여하기**
예제를 추가하거나 개선하고 싶다면 프로젝트에 기여하도록 권장합니다. 이 저장소에있는 모든 예제 및 샘플 프로젝트는 오픈 소스이며 자유롭게 당신의 응용 프로그램에서 사용할 수 있습니다.

기여하려면 저장소를 포크하고 소스 코드를 편집하여 풀 요청을 만들 수 있습니다. 변경 사항을 검토하고 도움이 되었다고 판단되면 저장소에 포함될 것입니다.

