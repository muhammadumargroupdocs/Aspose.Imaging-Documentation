---
title: Uninstalling Aspose.Imaging for SharePoint License
type: docs
weight: 30
url: /sharepoint/uninstalling-aspose-imaging-for-sharepoint-license/
---

To uninstall Aspose.Imaging for SharePoint license, please use the steps below from the server console.

1. Retract the license solution from the farm: 

   stsadm.exe -o retractsolution -name Aspose.Imaging.SharePoint.License.wsp -immediate 
1. Execute administrative timer jobs to complete the retraction immediately: 

   stsadm.exe -o execadmsvcjobs 
1. Wait for the retraction to complete.
   You can check if the retraction has completed under the **Central Administration** menu, **Operations**, **Solution Management**. 
1. Remove the solution from the SharePoint solution store: 

   stsadm.exe -o deletesolution -name Aspose.Imaging.SharePoint.License.wsp
