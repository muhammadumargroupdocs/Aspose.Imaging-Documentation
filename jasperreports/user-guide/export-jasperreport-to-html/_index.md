---
title: Export JasperReport to HTML
type: docs
weight: 20
url: /jasperreports/export-jasperreport-to-html
---

{{% alert color="primary" %}}

Aspose.Imaging for JasperReports provides a class named ASHtml5CanvasExporter for exporting JasperReport to HTML.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to HTML.

**Java**

{{< highlight java >}}

ASHtml5CanvasExporter html5CanvasExporter = new ASHtml5CanvasExporter();
ASHtmlExportConfigurationImpl htmlExportConfiguration = new ASHtmlExportConfigurationImpl();
htmlExportConfiguration.setCanvasTagId("SomeId");
htmlExportConfiguration.setFullHtmlPage(true);
htmlExportConfiguration.setEncoding(StandardCharsets.UTF_8);

html5CanvasExporter.setConfiguration(htmlExportConfiguration);

ASExportInputImpl exporterInput = new ASExportInputImpl(jasperPrint);
html5CanvasExporter.setExporterInput(exporterInput);

ASExporterOutputImpl exporterOutput = new ASExporterOutputImpl("shapesExample.html");
html5CanvasExporter.setExporterOutput(exporterOutput);

html5CanvasExporter.exportReport();

{{< /highlight >}}
