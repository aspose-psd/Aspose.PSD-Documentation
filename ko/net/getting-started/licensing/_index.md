---
title: 라이선스
type: docs
weight: 70
url: /ko/net/licensing/
description: NuGet에서 PSD Photoshop C# 라이브러리를 평가하고 파일 또는 스트림을 사용하여 라이선스를 적용하여 설치된 평가판의 제한 사항을 제거합니다.
---

## **평가 버전 제한 사항**
Aspose.PSD for .NET의 평가 버전을 [NuGet](https://www.nuget.org/packages/Aspose.psd/)에서 다운로드할 수 있습니다. 평가 버전은 몇 가지 제한 사항이 있는 완전히 라이센스 된 버전과 동일한 기능을 제공합니다. Aspose.PSD를 구매하면 라이센스를 적용하기만 하면 설치된 평가판에서 제한 사항을 제거할 수 있습니다. Aspose.PSD for .NET의 평가 버전은 다음과 같은 두 가지 제한 사항만 가지고 있습니다:

- **각 이미지에 워터마크**: 저장, 수정 또는 내보낸 이미지에 "평가용으로만. Aspose.PSD로 작성. 저작권 2010-2018 Aspose Pty Ltd."라는 워터마크가 있습니다. 전체 워터마크가 맞지 않는 작은 이미지에는 이미지를 횡으로 가로지르는 대각선 두 줄이 있습니다.
- **핵심 그리기 기능 지원 없음**: 평가 모드에서는 이미지 픽셀을 이미지로 불러오거나 저장할 수 없습니다. 이미지를 그리기 위해 고급 그리기 기능을 사용하십시오. 이 제한은 핵심 그리기 기능에 의존하는 기능에 영향을 줍니다. Aspose.PSD for .NET을 사용하면 자체 파일 형식을 등록할 수 있습니다. 그러나 이 기능은 핵심 그리기 기능에 의존하기 때문에 평가 모드에서 사용하지 않는 것이 좋습니다. 왜냐하면 이 파일의 내용을 변경할 수 없기 때문입니다.

Aspose.PSD for .NET의 평가 제한 사항 없이 테스트하려면 30일 임시 라이센스를 요청하십시오. 자세한 내용은 [임시 라이센스를 어떻게 받을 수 있는지?](https://purchase.aspose.com/temporary-license)를 참조하십시오.
## **라이센스 파일에 대해**
Aspose.PSD를 평가한 후 만족스러운 경우 [Aspose 웹사이트](https://purchase.aspose.com/default.aspx)에서 라이센스를 구매할 수 있습니다. 제공되는 다양한 구독 유형에 익숙해지십시오. 궁금한 점이 있으면 언제든 [Aspose의 판매팀](https://company.aspose.com/contact)에 문의하십시오. 모든 Aspose 라이센스에는 소프트웨어 업그레이드를 위한 1년 구독이 포함되어 있습니다. 첫 해 이후에는 구독을 갱신하여 최신 기능을 계속 받을 수 있습니다. 기술 지원은 무료이며 라이센스가 있는 사용자 및 평가 사용자 모두에게 [지원 포럼](https://forum.aspose.com/)를 통해 제공됩니다. 라이센스는 제품 이름, 라이센스된 개발자 수, 구독 만료 날짜 등과 같은 세부 정보가 포함된 XML 파일입니다. 이 파일은 디지털으로 서명되므로 수정하지 마십시오: 실수로 줄 바꿈을 추가하면 파일이 무효화됩니다. Aspose.PSD를 구매한 후 이미지를 만들거나 편집하거나 그 외 조작하기 전에 라이센스를 적용해야 합니다. 라이센스를 적용하지 않으면 출력 이미지에 평가용 워터마크가 표시됩니다. 애플리케이션이나 개발 프로세스당 한 번만 라이센스를 설정하면 됩니다.
## **애플리케이션에 라이센스 적용 위치**
라이센스를 적용하는 위치는 개발 중인 애플리케이션 유형에 따라 다릅니다. 다음 단순한 규칙을 따르십시오:

- 애플리케이션 도메인당 한 번만 라이센스를 적용하십시오. License.SetLicense를 여러 번 호출하면 해를 끼칠 수 있지만 프로세서 시간을 낭비합니다.
- Aspose.PSD for .NET 클래스를 사용하기 전에 라이센스를 적용하십시오.
- **Windows Forms 또는 콘솔 애플리케이션**: Aspose.PSD for .NET 클래스를 사용하기 전에 시작 코드에서 License.SetLicense를 호출하십시오.
- **ASP.NET 애플리케이션**: Global.asax.cs(Global.asax.vb) 파일의 Application_Start 보호된 메소드에서 License.SetLicense를 호출하십시오. 이렇게 하면 애플리케이션이 시작될 때 한 번 호출됩니다. Page_Load 메소드 내부에서 License.SetLicense를 호출하지 마십시오. 그렇게 하면 라이센스가 웹 페이지가 로드될 때마다 로드됩니다.
- **Silverlight 애플리케이션**: App.xaml.cs(App.xaml.vb) 파일의 Application_Startup 이벤트에서 License.SetLicense를 호출하십시오.
- **클래스 라이브러리**: Aspose.PSD를 사용하는 클래스의 정적 생성자에서 License.SetLicense를 호출하십시오. 정적 생성자는 클래스의 인스턴스가 생성되기 전에 실행되므로 Aspose.PSD 라이센스가 올바르게 설정됨이 보장됩니다.
## **라이센스 적용**
NuGet의 [다운로드 페이지](https://www.nuget.org/packages/Aspose.psd/)에서 Aspose.PSD의 평가 버전을 손쉽게 다운로드할 수 있습니다. 평가 버전은 Aspose.PSD의 라이센스 버전과 완전히 동일한 기능을 제공합니다. 라이센스를 구매하고 라이센스를 적용하기 위해 몇 줄의 코드를 추가하면 평가 버전이 라이센스로 변환됩니다.
### **파일 또는 스트림 사용**
평가 제한 사항으로 작업하지 않으려면 Aspose.PSD를 사용하기 전에 라이센스를 설정해야 합니다. 애플리케이션(또는 프로세스)당 한 번만 라이센스를 설정해야 합니다.
### **파일에서 라이센스 적용**
라이센스를 적용하는 가장 간단한 방법은 라이센스 파일을 Aspose.PSD.dll과 동일한 폴더에 넣는 것입니다. 그런 다음 코드에서 전체 경로 대신 파일 이름을 지정할 수 있습니다.



{{< highlight java >}}

// License의 인스턴스 생성 및 전체 경로를 사용하여 라이센스 적용

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}



SetLicense 메소드를 호출할 때 라이센스 이름은 라이센스 파일 이름과 동일해야 합니다. 예를 들어 라이센스 파일 이름을 "Aspose.PSD.lic.xml"로 변경한 경우 SetLicense 메소드에도 이 라이센스 이름을 사용해야 합니다.
### **스트림을 사용하여 라이센스 적용**
아래와 같이 스트림에서 라이센스를 로드하는 것도 가능합니다.



{{< highlight java >}}



// License의 인스턴스 생성 및 스트림을 사용하여 라이센스 적용

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);

{{< /highlight >}}
### **라이센스 상태 확인**
Aspose.PSD.License 클래스에는 라이센스가 올바르게 설정된 경우 true를 반환하는 IsLicensed 속성이 있습니다.



{{< highlight java >}}

License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("라이센스가 설정되었습니다!");

}

{{< /highlight >}}
### **내장 리소스 사용**
라이센스를 애플리케이션과 함께 패키징하여 손실되지 않도록 하는 실용적인 방법은 Aspose.PSD를 호출하는 어셈블리 중 하나로 임베드된 리소스로 포함하는 것입니다. 라이센스 파일을 내장 리소스로 포함하는 방법:

1. Visual Studio .NET에서 **파일** 메뉴를 클릭하고 **기존 항목 추가**를 선택하십시오.
1. 프로젝트에 라이센스 파일(확장자 .lic)을 포함하십시오.
1. 솔루션 탐색기에서 파일을 선택하십시오.
1. 속성 창에서 **빌드 작업**을 **임베디드 리소스**로 설정하십시오.

Microsoft .NET Framework에서 내장된 라이센스에 액세스하기 위해 System.Reflection.Assembly의 GetExecutingAssembly 또는 GetManifestResourceStream 메소드를 호출할 필요가 없습니다. 대신 프로젝트의 리소스로 파일을 내장하고 그런 다음 SetLicense 메소드에 라이센스 파일 이름을 전달하십시오. License 클래스는 자동으로 내장된 리소스에서 라이센스 파일을 찾습니다. 아래 예시는 라이센스를 임베드된 리소스로 포함하고 애플리케이션에 적용하는 방법을 보여줍니다.



{{< highlight java >}}

// License 클래스를 인스턴스화

Aspose.PSD.License license = new Aspose.PSD.License();



// 임베디드 라이센스 파일의 이름 전달

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **라이센스 상태 확인**
Aspose.PSD.License 클래스에는 라이센스가 올바르게 설정된 경우 true를 반환하는 IsLicensed 속성이 있습니다.



{{< highlight java >}}

License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("라이센스가 설정되었습니다!");

}

{{< /highlight >}}
