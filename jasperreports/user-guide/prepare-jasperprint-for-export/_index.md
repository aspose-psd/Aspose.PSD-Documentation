---
title: Prepare JasperPrint for export
type: docs
weight: 10
url: /jasperreports/prepare-jasperprint-for-export
---

{{% alert color="primary" %}}

JasperReports library provides a class named JasperFillManager for preparing JasperPrint for export.

{{% /alert %}}

The following code snippet demonstrates how to create JasperPrint object to prepare a report for further image export.

**Java**

{{< highlight java >}}

JasperReport jasperReport = JasperCompileManager.compileReport("shapesReport.jrxml");
JasperPrint jasperPrint = JasperFillManager.fillReport(jasperReport, null, new JREmptyDataSource());

{{< /highlight >}}
