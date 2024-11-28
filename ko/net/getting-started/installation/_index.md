---
title: 설치
type: 문서
weight: 50
url: /ko/net/installation/
description: NuGet 또는 Package Manager 콘솔을 사용하여 PSD 파일 형식 라이브러리를 설치합니다.
---

## **NuGet을 통한 Aspose.PSD for .NET 설치**
NuGet은 .NET용 Aspose API를 다운로드하고 설치하는 가장 쉬운 방법입니다. Microsoft Visual Studio 및 NuGet 패키지 관리자를 엽니다. 원하는 Aspose API를 찾기 위해 "aspose"를 검색합니다. "설치"를 클릭하면 선택한 API가 다운로드되어 프로젝트에 참조됩니다.

![할 일: 이미지 대체 텍스트](installation_1.png)
## **Package Manager 콘솔을 사용하여 Aspose.PSD 설치 또는 업데이트**
다음 단계를 따라 패키지 관리자 콘솔을 열어 [Aspose.PSD API](https://www.nuget.org/packages/Aspose.psd/)를 참조할 수 있습니다:

1. Visual Studio에서 솔루션/프로젝트를 엽니다.
1. 메뉴에서 Tools -> Library Package Manager -> Package Manager Console을 선택하여 패키지 관리자 콘솔을 엽니다.

![할 일: 이미지 대체 텍스트](installation_2.png)

명령 " **Install-Package Aspose.Psd**"를 입력하고 Enter를 눌러 응용 프로그램에 최신 풀 릴리스를 설치합니다. 또는 "**-prerelease**" 접미사를 추가하여 최신 릴리스(핫 픽스를 포함한)를 설치하도록 명령을 지정할 수도 있습니다.

![할 일: 이미지 대체 텍스트](installation_3.png)

다운로드가 진행 중임을 나타내는 **"Aspose.PSD 설치 중"** 팁이 창 아래에 나타납니다.

![할 일: 이미지 대체 텍스트](installation_4.png)

다운로드가 완료되면 다음 확인 메시지가 표시됩니다. [Aspose EULA](https://company.aspose.com/legal/eula)에 익숙하지 않다면 URL에서 참조된 라이선스를 읽는 것이 좋습니다.

![할 일: 이미지 대체 텍스트](installation_5.png)

이제 Aspose.PSD가 응용 프로그램에 성공적으로 추가되고 참조되었음을 확인할 수 있습니다.

![할 일: 이미지 대체 텍스트](installation_6.png)

패키지 관리자 콘솔에서 명령 " **Update-Package Aspose.Psd**"를 사용하여 Aspose.Psd 패키지의 업데이트를 확인하고 적용할 수 있습니다. 최신 릴리스로 업데이트하려면 "-prerelease" 접미사를 추가할 수도 있습니다.
## **공유 서버 환경에서 실행 시 고려 사항**
모든 Aspose .NET 구성 요소는 풀 Trust 권한 집합으로 실행하는 것이 권장됩니다. 왜냐하면 Aspose .NET 구성 요소는 가끔 레지스트리 설정 및 가상 디렉토리 외의 위치에 있는 파일에 액세스해야 할 수도 있기 때문입니다. 또한 Aspose.NET 구성 요소들은 핵심 .NET 시스템 클래스에 기반하여 일부 경우에는 Full Trust 권한이 필요합니다.

다른 회사에서 여러 애플리케이션을 호스팅하는 인터넷 서비스 제공업체는 대부분 중간 Trust 보안 수준을 부여합니다. .NET 2.0의 경우 해당 보안 수준은 Aspose.Words의 적절한 작동을 방해할 수 있는 다음 제약 사항을 설정할 수 있습니다.

- **RegistryPermission**을 사용할 수 없습니다. 이는 문서 렌더링 시 설치된 글꼴을 나열하는 데 필요한 레지스트리에 액세스할 수 없음을 의미합니다.
- **FileIOPermission**이 제한됩니다. 이는 애플리케이션의 가상 디렉토리 계층 구조 내 파일에만 액세스할 수 있음을 의미합니다. 이로 인해 내보내기 중에 글꼴을 읽을 수 없을 수도 있습니다.

위에서 언급한 이유로 Aspose.PSD는 전체 Trust 권한에서 실행하는 것이 권장됩니다. Medium trust에서 다른 작업을 수행할 때 라이브러리 기능이 작동하는 경우가 있고(예: 렌더링) 작동하지 않는 경우도 있을 수 있습니다. 이것은 GDI+ 이미지 처리에 대한 호출 때문일 수 있습니다.


## **MSI 패키지를 통해 설치된 .NET Core DLL로 작업**
**참고:** MSI 패키지를 통해 .Net Standard dll을 사용하는 경우에는 .Net Standard 버전과 함께 작동하려면 필요한 종속성을 추가해야 합니다.

|**Visual Studio 종속성 스크린샷**|**CsProj 파일 조각:**|
| :- | :- |
|![할 일: 이미지 대체 텍스트](installation_7.png)|<ItemGroup><p></p><p>`    `<PackageReference Include="System.Drawing.Common" Version="4.5.1" /></p><p>`    `<PackageReference Include="System.Text.Encoding.CodePages" Version="4.5.0" /></p><p></p></ItemGroup>|

## **시스템 요구 사항**
### **지원되는 운영 체제:**
- Microsoft Windows 2000 Professional 및 Server (SP2 권장)
- Microsoft Windows XP Professional 및 Home Edition
- Microsoft Windows 2003 Server
- Microsoft Windows Vista
- Microsoft Windows 2008 Server
- Microsoft Windows 2008 Server R2
- Microsoft Windows 7
- Microsoft Windows 8
- Microsoft Windows 10
- Microsoft Windows 11
### **지원되는 플랫폼:**
- 윈도우 폼
- 웹 폼
- Visual Studio 2005
- Visual Studio 2008
- Visual Studio 2010
- Visual Studio 2012
- Visual Studio 2013
- Visual Studio 2015
- Visual Studio 2017
- Visual Studio 2019
- Visual Studio 2022

Aspose.PSD는 위에 나열된 운영 체제의 x86 및 x64 버전 모두에서 작동합니다.
### **지원되는 Framework:**
Aspose.PSD for .NET은 다음과 같은 .NET 프레임워크를 지원합니다:

- .NET Framework 버전 2.0 이상
- .NET Standard 2.0
