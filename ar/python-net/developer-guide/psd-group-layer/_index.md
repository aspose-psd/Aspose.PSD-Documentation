---
title: مثال على استخدام طبقات المجموع في Aspose.PSD لـ Python
weight: 100
type: docs
description: استخدام طبقة المجموع في ملف PSD عبر Python
keywords: [طبقة المجموع, طبقة المجموع, إضافة طبقة للمجموع, واجهة برمجة التطبيقات لملف PSD, Python, عينة الكود]
url: /ar/python-net/psd-group-layer/
---

## **نظرة عامة**

العمل مع طبقات المجموع في Aspose.PSD لـ Python هو ميزة قوية تسمح لك بتنظيم وتلاعب الطبقات داخل صورة PSD. توفر طبقات المجموع ، المعروفة أيضًا باسم طبقات الحافظة، طريقة لتجميع عدة طبقات معًا وتطبيق تحويلات أو تأثيرات على الفريق بأكمله.

في هذا المثال ، ننشئ أولاً صورة PSD جديدة باستخدام طريقة PsdImage.create. ثم ، ننشئ كائن طبقة مجموعة جديدة باستخدام طريقة add_layer_group لكائن PsdImage. نقدم اسم طبقة الفريق ("مجلد") ، والفهرس الذي يجب إدراجه فيه (0) ، وعلم بولياني يشير إلى ما إذا كان يجب أن تكون طبقة المجموع مرئية (صحيح).

بعد ذلك ، ننشئ طبقتين ونعين أسماء العرض الخاصة بهما باستخدام خاصية display_name. نضيف هذه الطبقات إلى طبقة المجموع باستخدام طريقة add_layer.

وأخيرًا ، يمكننا الوصول إلى الطبقات داخل المجموع باستخدام خاصية layers لكائن LayerGroup. في المثال ، نؤكد أن أسماء عرض الطبقات الأولى والثانية في المجموع هي "طبقة 1" و "طبقة 2" على التوالي.

بعد تلاعب طبقات المجموع ، يمكننا حفظ صورة PSD المعدلة باستخدام طريقة الحفظ لكائن PsdImage.

هذا مجرد مثال أساسي لبدء العمل مع طبقات المجموع باستخدام Aspose.PSD لـ Python. توفر المكتبة العديد من الميزات المتقدمة لتلاعب وتحويل الطبقات داخل صور PSD. يمكنك الرجوع إلى وثائق Aspose.PSD لـ Python للحصول على مزيد من التفاصيل والأمثلة حول العمل مع طبقات المجموع وميزات أخرى من المكتبة.

للعمل مع طبقات المجموع في Aspose.PSD لـ Python ، يمكنك استخدام فئة LayerGroup. فيما يلي مقطع كود مثال يوضح كيفية إنشاء طبقة مجموعة ، إضافة طبقات إليها ، وحفظ صورة PSD المعدلة.

يرجى التحقق من المثال الكامل.

## **المثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}