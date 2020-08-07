---
title: Installing Aspose.Imaging for SharePoint License
type: docs
weight: 10
url: /sharepoint/installing-aspose-imaging-for-sharepoint-license/
---

{{% alert color="primary" %}} 

Once you are happy with your evaluation, you can [buy a license](http://www.aspose.com/purchase/default.aspx). Before purchasing make sure you understand and agree to the license terms. 

{{% /alert %}} 

The license is emailed to you after the order has been paid. The license is a .zip archive containing a regular SharePoint solution package.

This archive contains:

- Aspose.Imaging.SharePoint.License.wsp - The SharePoint solution package file. Aspose.Imaging for SharePoint License is packaged as a SharePoint solution to facilitate deployment/retraction across the server farm.
- readme.txt
#### **License installation instructions**
License installation is performed from the server console via stsadm.exe. The steps required to install the license are:

**Note**: The paths are omitted for clarity. You may need to add the actual path to stsadm.exe and/or the solution file when executing them.

1. Run stsadm to add the solution to the SharePoint solution store: 

   stsadm.exe -o addsolution -filename Aspose.Imaging.SharePoint.License.wsp 
1. Deploy the solution to all servers in the farm: 

   stsadm.exe -o deploysolution -name Aspose.Imaging.SharePoint.License.wsp -immediate -force 
1. Execute administrative timer jobs to complete the deployment immediately. 

   stsadm.exe -o execadmsvcjobs

**Note**: If Windows SharePoint Services Administration service is not started you get a warning when running the deployment step. Stsadm.exe relies on this service and Windows SharePoint Timer Service to replicate solution data across the farm. If these services are not running on the server farm, you may need to deploy the license on each server. 
