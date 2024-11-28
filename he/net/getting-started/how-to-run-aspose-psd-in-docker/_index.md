---
title: כיצד להריץ Aspose.PSD ב Docker
type: docs
description: "הרצת Aspose.PSD בתוך מכולת Docker עבור Linux, Windows Server וכל מערכת הפעלה אחרת."
weight: 90
url: /he/net/how-to-run-aspose-psd-in-docker/
---

## דרישות מוקדמות

- עליך להתקין את Docker במערכת שלך. למידע אודות איך להתקין Docker ב-Windows או ב-Mac, ראה את הקישורים בקטע "ראה גם" (See Also).

- Visual Studio 2022.

- NET 6 SDK משמש בדוגמה זו.

- ניתן להוריד פרוייקט לדוגמה בעבודה מלאה בקישור: [https://github.com/aspose-psd/Aspose.PSD-Docker-Sample](https://github.com/aspose-psd/Aspose.PSD-Docker-Sample)


## אפליקציית Hello World

בדוגמה זו, תיצור אפליקציית קונסולה פשוטה שבה תפתח קובץ psd, תעדכן שכבת טקסט ותצייר בעזרת API גרפי. האפליקציה המתוארת יכולה להיות בנויה ולרוץ ב-Docker.

### יצירת אפליקציית הקונסולה

קדימון ליצירת תוכנית ה-Hello World, עקוב אחר השלבים הבאים:
1. לאחר שה-Docker מותקן, וודא כי הוא משתמש ב-Containers של Linux (ברירת המחדל). אם נדרש, בחר באפשרות Switch to Linux containers מתפריט ה-Desktop של Docker.
1. ב-Visual Studio, צור אפליקציית קונסולה NET 6.<br>
![קובץ דו-שיח של אפליקציית קונסולת NET 6](create-a-new-project.png)<br>
1. התקן את גרסת Aspose.PSD האחרונה מ-NuGet.<br>
![Aspose.PSD ב-NuGet](nuget-aspose-psd.png)<br>
1. מאחר שהאפליקציה תורץ על Linux, ייתכן שיהיה עליך להתקין גופנים נוספים. ייתכן שתעדיף את ttf-mscorefonts-installer.
1. שים לב, כדי להשתמש בתכונות העיקוליות של הטקסט על Linux עליך להוסיף את החבילות הבאות: apt-transport-https, libgdiplus, libc6-dev. הפקודות להוספתן ניתן למצוא בקובץ ה-dockerfile.
1. כאשר כל התלויות הנדרשות מתווספות, כתוב תוכנית פשוטה שפותחת את קובץ ה-PSD, מעדכנת שכבת טקסט ואז צורפת דבר משהו בעזרת גרפיקה.<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

שים לב שכדי לערוך שכבות טקסט עליך לקבל אישור רישיון. ניתן לקבל רישיון זמני באמצעות המאמר הבא: [https://purchase.aspose.com/temporary-license](https://purchase.aspose.com/temporary-license)
 
### קביעת Dockerfile

השלב הבא הוא ליצור ולהגדיר את ה-Dockerfile.

1. צור את ה-Dockerfile ושים אותו לצד קובץ הפתרון של האפליקציה שלך. שמור את שם הקובץ הזה בלי סיומת (הברירת מחדל).
1. ב-Dockerfile, ציין:

{{< highlight plain >}}
#ראה https://aka.ms/containerfastmode כדי להבין כיצד בפועל Visual Studio משתמש ב-Dockerfile זה כדי לבנות תמונות לתיקון בעת ניפוי מהיר יותר.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

#כדי להשתמש ביכולת לעדכן שכבות הטקסט עליך להוסיף את החבילות הבאות לתוך ה-container שלך
RUN apt-get update
RUN yes | apt-get install -y apt-transport-https
RUN yes | apt-get install -y libgdiplus
RUN yes | apt-get install -y libc6-dev

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build

WORKDIR /src
COPY ["AsposePsdDockerSample/AsposePsdDockerSample.csproj", "AsposePsdDockerSample/"]
RUN dotnet restore "AsposePsdDockerSample/AsposePsdDockerSample.csproj"
COPY . .
WORKDIR "/src/AsposePsdDockerSample"
RUN dotnet build "AsposePsdDockerSample.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "AsposePsdDockerSample.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "AsposePsdDockerSample.dll"]
{{< /highlight >}}

מעל זו Dockerfile פשוטה, הכוללת את ההוראות הבאות:

- התמונה של ה-SDK שיש להשתמש בה. כאן זו תמונת Microsoft .Net 6. Docker יוריד את זה בעת הקריאה לבנייה. הגרסה של ה-SDK מצוינת כפותח.
- לאחר מכן הוסף את התליות לתת את הצורה לטקסט.
- אחר כך, ייתכן שתצטרך להתקין כרטיסים מאחר והתמונה של ה-SDK מכילה מעט גופנים. כמו כן, תוכל להשתמש בגופנים מקומיים שהועתקו לתמונת ה-docker.
- ספריית עבודה, שנצוין בשורה הבאה.
- הפקודה להעתיק הכל לתוך ה-container, לפרסם את היישום ולציין את ה-Entry Point.

### בניית והרצת האפליקציה ב-Docker

#### בעזרת Visual Studio
הדרך הפשוטה לנסות את Aspose.PSD ב-Docker היא לפתוח את ויזואל סטודיו ולהפעיל את האפליקציה בעזרת Docker.
![הריץ את אפליקציית דוגמת Aspose.PSD ב-Docker בעזרת ויזואל סטודיו](psd-vs-run-using-docker-support.png)

#### בעזרת פקודת הפרומפט
ניתן לבנות ולהריץ את האפליקציה ב-Docker בעזרת פקודת הפורומפט. פתח את פנקס הפקודות האהוב עליך, שנה את התיקייה לתיקיה שבה האפליקציה ממוקמת (תיקיית שבה קובץ הפתרון וה-Dockerfile ממוקמים) והרץ את הפקודה הבאה:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

בפעם הראשונה שפקודה זו מופעלת עשוי לקחת זמן רב יותר, מאחר ו-Docker צריך להוריד את התמונות הדרושות. כאשר הפקודה הקודמת מושלמת, הרץ את הפקודה הבאה:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

שים לב לפרמטר ההרצה, מאחר שכפי שצוין למעלה, תיקייה במחשב המארח מורכבת לתיקיית ה-container, כדי לראות בקלות את תוצאות ביצועי האפליקציה. נתיבים ב-Linux רגישים לרישיות.

{{% /alert %}}


## דוגמאות נוספות

לקבלת דוגמאות נוספות איך ניתן להשתמש ב-Aspose.PSD ב-Docker, ראה את ה-[דוגמאות](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## ראה גם

- [התקן את Docker Desktop ב-Windows](https://docs.docker.com/docker-for-windows/install/)
- [התקן את Docker Desktop ב-Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- [החלף אל ה-container של Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- מידע נוסף באודות [ה-SDK של. NET Core](https://hub.docker.com/_/microsoft-dotnet-sdk)
