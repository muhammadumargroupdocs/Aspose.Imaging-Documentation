---
title: Export JasperReport to EMF
type: docs
weight: 60
url: /jasperreports/export-jasperreport-to-emf
---

{{% alert color="primary" %}}

Aspose.Imaging for JasperReports provides a class named ASEmfExporter for exporting JasperReport to EMF.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to EMF.

**Java**

{{< highlight java >}}

// Example 1

ASEmfExporter emfExporter = new ASEmfExporter();
ASEmfExportConfigurationImpl emfExportConfiguration = new ASEmfExportConfigurationImpl();
emfExporter.setConfiguration(emfExportConfiguration);

exporterInput = new ASExportInputImpl(jasperPrint);
emfExporter.setExporterInput(exporterInput);

exporterOutput = new ASExporterOutputImpl("shapesExample.emf");
emfExporter.setExporterOutput(exporterOutput);

emfExporter.exportReport();

// Example 2

ASEmfExporter emzExporter = new ASEmfExporter();
emfExportConfiguration = new ASEmfExportConfigurationImpl();
emfExportConfiguration.setCompress(true);
emzExporter.setConfiguration(emfExportConfiguration);

exporterInput = new ASExportInputImpl(jasperPrint);
emzExporter.setExporterInput(exporterInput);

exporterOutput = new ASExporterOutputImpl("shapesExample.emz");
emzExporter.setExporterOutput(exporterOutput);

emzExporter.exportReport();

{{< /highlight >}}
