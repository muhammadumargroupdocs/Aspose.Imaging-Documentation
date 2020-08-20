---
title: Prepare JasperPrint for export
type: docs
weight: 10
url: /jasperreports/prepare-jasperprint-for-export
---

{{% alert color="primary" %}}

Aspose.Imaging for JasperReports provides a class named JasperFillManager for preparing JasperPrint for export.

{{% /alert %}}

The following code snippet demonstrates how to export the jasperPrint object to some file path.

**Java**

{{< highlight java >}}

JasperReport jasperReport = JasperCompileManager.compileReport("shapesReport.jrxml");
JasperPrint jasperPrint = JasperFillManager.fillReport(jasperReport, null, new JREmptyDataSource());

{{< /highlight >}}
