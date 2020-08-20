---
title: Export JasperReport to WEBP
type: docs
weight: 70
url: /jasperreports/export-jasperreport-to-webp
---

{{% alert color="primary" %}}

Aspose.Imaging for JasperReports provides a class named ASWebPExporter for exporting JasperReport to WEBP.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to WEBP.

**Java**

{{< highlight java >}}

ASWebPExporter webPExporter = new ASWebPExporter();
ASWebpExportConfigurationImpl webpExportConfiguration = new ASWebpExportConfigurationImpl();
webpExportConfiguration.setQuality(50);
webPExporter.setConfiguration(webpExportConfiguration);

exporterInput = new ASExportInputImpl(jasperPrint);
webPExporter.setExporterInput(exporterInput);

exporterOutput = new ASExporterOutputImpl("shapesExample.webp");
webPExporter.setExporterOutput(exporterOutput);

webPExporter.exportReport();

{{< /highlight >}}
