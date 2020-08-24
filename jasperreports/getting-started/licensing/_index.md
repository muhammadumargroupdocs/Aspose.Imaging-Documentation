---
title: Licensing
type: docs
weight: 40
url: /jasperreports/licensing/
---

To apply a license:

Save the license file to a folder on your disk. For example C:\Lic\Aspose.Imaging.JasperReport.lic.
Call the License.setLicense(filename) method and pass the file name as an argument. When this statement is called, the license is set and the evaluation message will no longer appears on top of the images.
The following code snippet sets the license for Aspose.Imaging for JasperReports.

{{< highlight csharp >}}

// Set license

License lic = new License();

lic.setLicense("C:\Lic\Aspose.Imaging.JasperReports.lic");

{{< /highlight >}}

{{% alert color="primary" %}}

You need to call the setLicense() method only once per process or application.

{{% /alert %}}
