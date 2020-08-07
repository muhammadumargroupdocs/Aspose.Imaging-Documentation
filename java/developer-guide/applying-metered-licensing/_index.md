---
title: Applying Metered Licensing
type: docs
weight: 10
url: /java/applying-metered-licensing/
---

{{% alert color="primary" %}} 

Aspose.Imaging for Java provides the functionality to use metered licensing mechanism. Aspose.Imaging for Java has introduced **Metered** class in the API to accomplish this job.

{{% /alert %}} 
### **Applying Metered Licensing**
Here are the simple steps to use the **Metered** class.

1. Create an instance of **Metered** class.
1. Pass public & private keys to **setMeteredKey** method.
1. Do processing (perform imaging task).
1. Call method **getConsumptionQuantity** of the **Metered** class.
1. It will return the amount/quantity of API requests that you have consumed so for.

Below is the code demonstration:

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-files-MeteredLicensing-MeteredLicensing.java" >}}
