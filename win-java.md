---
title: Installing Java on Windows
---

# Installing Java on Windows

OpenRefine is a Java application.
On Windows, the easiest way to use Refine is to download the "Windows kit with embedded Java" package which includes everything needed to run Refine (to reiterate: *you do not need to install Java!*). 

If you already have an up to date Java installed on your system, you can download the "Windows kit" package.

You can check if you already have Java by opening Command Prompt and typing `java --version`.

*It is always a good idea to [uninstall any old or out of date Java versions](https://java.com/en/download/help/remove_olderversions.html) on your machine!*

## Installing Java

If you want to install Java on your Windows system you have a few options depending on your needs. 
In the past most people used "Oracle Java", however, in 2019 Oracle [significantly changed their license terms](https://www.oracle.com/java/technologies/javase/jdk-faqs.html), which limits what is considered "personal use". 
*If you are installing Java on a work or research computer you are safer using an open alternative unless your organization pays for a license.*

I recommend using the Adopt OpenJDK installer which is just as easy to install as Oracle Java, but is free and openly licensed.

### Adopt OpenJDK (Recommended)

[Adopt OpenJDK](https://adoptopenjdk.net/) provides installers for openly licensed Java. 
This effort is [supported by major tech companies](https://adoptopenjdk.net/about.html) (outside of Oracle). 

- Visit the [Adopt OpenJDK](https://adoptopenjdk.net/about.html) page.
- Select the most recent LTS version (*OpenJDK 11 (LTS)* as of this writing) and HotSpot JVM, then click the download button (.MSI installer).
- Double click the installer to run:
    - Accept the licence.
    - On "Custom Setup" options, use the default options, plus add option "Updating the JAVA_HOME environment variable".
    - Click Next to finish installation.

### Oracle Java

[Oracle Java](https://java.com/en/download/) is the most common installer people have used in the past.
It is "free" for personally use, but is *not* openly licensed.
However, in 2019 Oracle [significantly changed their license terms](https://www.oracle.com/java/technologies/javase/jdk-faqs.html), which limits what is considered "personal use". 
*If you are installing Java on a work or research computer you are safer using an open alternative unless your organization pays for a license.*

- Visit [Oracle Java download](https://java.com/en/download/) page.
- Download the installer (64-bit version should be default)
- Double click the installer to run.
- Oracle will sometimes include additional "recommended" applications other than Java as a check box in the installer--be sure to uncheck the "recommended" option to avoid adding bundled spamware to your system!

### Oracle OpenJDK Builds

As an alternative to their officially licensed version, Oracle provides openly licensed [Oracle OpenJDK Builds](https://jdk.java.net/).
This option provides the Java package, but not an installer--thus installation is manual and not very convenient.

- Visit [Oracle OpenJDK Builds](https://jdk.java.net/) page.
- Click the "Ready for use" JDK version link.
- Download the package for your system (i.e. "Windows / x64").
- Unzip the downloaded package 
- Copy the complete folder (something like "jdk-15.0.2") into a sensible location (i.e. `C:\jdk-15.0.2`)
- Manually edit your system variables (see next section)

#### Edit Windows System Variables

*In most cases this is only necessary if using the Oracle OpenJDK Builds (without an installer).* 
You will need to manually edit your system variables to add Java to your Path. 

- Open Settings, search for "environment variables", and choose the "Edit environment variables for your account" option
- (alternatively, Control Panel > System > System properties > "Advanced" tab, click "Environment Variables" button)
- In "Environment variables" window: 
    - Highlight "Path" and click "Edit"
    - In the "Path" window, click "New", add the file path to the "bin" folder inside the Java package you downloaded (e.g. `C:\jdk-15.0.2\bin` ), and click okay.
    - Click "New", name the variable "JAVA_HOME", add the file path to the main folder of your Java package (e.g. `C:\jdk-15.0.2`, without \bin), and click okay.
    - Click "Okay"
