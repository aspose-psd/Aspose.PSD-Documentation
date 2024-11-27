---
title: تعديل توازن الألوان لطبقة التعديل
type: docs
weight: 30
url: /ar/java/layer-types/adjustment-layer/color-balance/
---

# العمل مع طبقة توازن الألوان في فوتوشوب باستخدام جافا

في هذه المقالة، سنقوم بـ **تعديل توازن الألوان للصورة** ذات تنسيق ملف PSD باستخدام جافا. سنستخدم مكتبة خاصة تسمى Aspose.PSD لجافا والتي تعتبر أداة للتلاعب بمستندات فوتوشوب.

نظرًا لأن المكتبة تعمل مع تنسيق ملف PSD، فإنها تحتوي على [جميع الميزات تقريباً](https://docs.aspose.com/psd/java/features/) المتاحة في محرر فوتوشوب و **طبقة تعديل توازن الألوان**، وهي مناسبة تمامًا لهذه المهمة، ليست استثناءً.

تسمح طبقة تعديل توازن الألوان بتغيير التوازن بين الألوان الأساسية (RGB) والألوان الطمسية (CMY) للظلال، والنصف الداكن، والمظهر بطريقة بسيطة وسريعة.

## تعديل توازن الألوان

كما ذُكر سابقًا، تعديل توازن الألوان في Aspose.PSD لجافا عبارة ببساطة عن **موازن بين الألوان الأساسية والألوان الطمسية**. يعني ذلك وجود ثلاث مقاييس لكل زوج من الألوان (سماوي/أحمر، أزرق/أخضر، أصفر/أزرق). ستزيد كثافة اللون الخاص في الزوج إذا تحركت القيمة نحوه والعكس صحيح. بالإضافة إلى ذلك، تلك الأزواج الثلاثة تعود لكل منطقة من نطاق الظلال، والنصف الداكن، والمظهر وهو ما يزيد من مرونة هذا النوع من التعديلات.

لذا، دعونا نطبق هذه المعرفة عمليًا. على سبيل المثال، سنختار صورة ملونة بلون أحمر لوجه امرأة (b). الوجه به تدرج لون أحمر كبير ونحن نعتزم تصحيح ذلك عن طريق **إضافة طبقة تعديل توازن الألوان** للحد من اللون الأحمر وزيادة السماوي بشكل أساسي (a) للحصول على وجه يبدو أكثر طبيعية (c). مرة أخرى، هناك الكثير من العمل لإتمام هذه الصورة ولكن ضمن هذه المقالة هذا كل ما سنقوم به.

![مثال على طبقة تعديل توازن الألوان](color-balance-adjustment-layer-example-figure-1.png) واجهة برمجة التطبيقات (API) لطبقة تعديل توازن الألوان لها تصميم مسطح. لذلك، [طبقة تعديل توازن الألوان](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) تمثل كل ما تحتاج إليه. أولاً، حافظ على سطوع الضوء لأنه معطل افتراضياً. بعد ذلك، أضف قليلاً من اللون الأخضر والمزيد من اللون الأصفر للظلال باستخدام الأساليب المقابلة (تحتوي أسماء على اسم منطقة نطاق الظل وأسماء الألوان في الزوج اللوني)، ثم أضف المزيد من السماوي وقليلاً من الأزرق للنصف الداكن، وأخيرًا أضف المزيد من السماوي بجانب قليل من القرمزي والأزرق:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

الآن، لدينا الصورة التي كنا نرغب في الحصول عليها! إنها بسيطة جدًا، أليس كذلك؟

كما عليك أن _قيمة كل زوج لوني يجب أن تكون في النطاق من -100 إلى 100_ وهي تتضمن القيم السلبية للألوان الطمسية والإيجابية للألوان الأساسية على التوالي، تمامًا كما في محرر فوتوشوب.

يرجى الرجوع لدليل الواجهة البرمجية لدينا لمعرفة المزيد من التفاصيل التقنية حول [طبقة تعديل توازن الألوان](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## الاستنتاج

في هذه المقالة، قد اكتسبنا فهمًا حول كيفية تعديل توازن الألوان للصورة برمجيًا باستخدام جافا باستخدام مكتبة Aspose.PSD لجافا. تحتوي المكتبة على واجهة برمجة التطبيقات الشاملة للعمل مع طبقات تعديل توازن الألوان في مستندات فوتوشوب.