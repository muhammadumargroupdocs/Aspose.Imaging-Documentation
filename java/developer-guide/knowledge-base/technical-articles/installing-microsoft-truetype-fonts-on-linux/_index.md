---
title: Installing Microsoft TrueType Fonts on Linux
type: docs
weight: 70
url: /java/installing-microsoft-truetype-fonts-on-linux/
---

{{% alert color="primary" %}} 

Microsoft True Type Fonts (TTFs) are quite commonly found throughout the web. However, for Linux users, the most of these True Type fonts don’t come pre-installed in some distributions. Aspose.Imaging for Java requires these fonts to be installed on the machine to properly render the glyph present in an input metafile. If required fonts are not found on the machine or not accessible to the JDK/JRE then Aspose.Imaging for Java will not render those glyph while converting metafiles to raster image formats.

{{% /alert %}} 

In scenarios as discussed above, it is recommend to install the required TTFs on machine before executing the conversion process. Below provided information will guide you step by step to install the Microsoft's most famous TTFs on Linux distributions such as Fedora, Red Hat Enterprise Linux (RHEL) & CentOS.

You may require 'root' level privileges therefore login as 'root' or get sudo configured.

Here’s how to do it using the Terminal.

1. Make sure you have the following RPM packages installed. 
   1. **rpm-build**: If not installed, use the following command to install the rpm-build package 

{{< highlight java >}}

 yum install rpm-build cabextract ttmkfdir

{{< /highlight >}}

1. **wget**: If not installed, use the following command 

{{< highlight java >}}

 yum \-y install wget

{{< /highlight >}}

1. Download the latest msttcorefonts spec file from SourceForge using the command as follow, 

{{< highlight java >}}

 wget http://corefonts.sourceforge.net/msttcorefonts-2.5-1.spec

{{< /highlight >}}

1. Build a RPM file using the previously downloaded spec file and the following command, 

{{< highlight java >}}

 rpmbuild \-ba msttcorefonts-2.5-1.spec

{{< /highlight >}}

1. The RPM file will be stored in: /root/rpmbuild/RPMS/noarch/, install it as follow, 

{{< highlight java >}}

 rpm \-ivh /root/rpmbuild/RPMS/noarch/msttcorefonts-2.5-1.noarch.rpm 

{{< /highlight >}}

1. Restart the machine to make the changes take effect.

{{% alert color="primary" %}} 

The instructions provided above will install the Microsoft TTFs package including the following font-families:

1. Andale Mono
1. Arial Black/Arial (Bold, Italic, Bold Italic)
1. Comic Sans MS (Bold)
1. Courier New (Bold, Italic, Bold Italic)
1. Georgia (Bold, Italic, Bold Italic)
1. Impact
1. Tahoma
1. Times New Roman (Bold, Italic, Bold Italic)
1. Trebuchet (Bold, Italic, Bold Italic)
1. Verdana (Bold, Italic, Bold Italic)
1. Webdings

{{% /alert %}} 

As discussed above, if you do not have the required fonts installed on the Linux environment, you will not be able to get the correct rendering while converting metafiles to raster formats where the font used in the metafile could be any. It is quite possible that the required font does not exist in the Microsoft's core package. In such scenarios, it is recommended to acquired the required font and install it manually using the following steps. 

You may require 'root' level privileges therefore login as 'root' or get sudo configured.

Here’s how to install a particular font.

1. Download the required font and place it in any directory such as Downloads directory.
1. Create a new directory with mkdir command and name the new directory as msfonts 

{{< highlight java >}}

 mkdir /usr/share/fonts/msfonts

{{< /highlight >}}

.

1. Copy the downloaded font to the directory created in above step. For the sake of demonstration, consider the downloaded font file name is Symbol.ttf then the command would be 

{{< highlight java >}}

 cp SYMBOL.TTF /usr/share/fonts/msfonts/

{{< /highlight >}}

1. Rebuild font cache files using 

{{< highlight java >}}

 fc-cache -fv

{{< /highlight >}}

1. Perform the conversion.
