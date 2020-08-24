---
title: Export JasperReport to DICOM
type: docs
weight: 50
url: /jasperreports/export-jasperreport-to-dicom
---

{{% alert color="primary" %}}

Aspose.Imaging for JasperReports provides a class named ASDicomExporter for exporting JasperReport to DICOM.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to DICOM.

**Java**

{{< highlight java >}}

ASDicomExporter dicomExporter = new ASDicomExporter();
ASDicomExportConfigurationImpl dicomExportConfiguration = new ASDicomExportConfigurationImpl();
dicomExporter.setConfiguration(dicomExportConfiguration);

exporterInput = new ASExportInputImpl(jasperPrint);
dicomExporter.setExporterInput(exporterInput);

exporterOutput = new ASExporterOutputImpl("shapesExample.dcm");
dicomExporter.setExporterOutput(exporterOutput);

dicomExporter.exportReport();

{{< /highlight >}}
