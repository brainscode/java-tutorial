---
title: Install Java IDE
toc: false
sidebar: labs_sidebar
folder: env_setup
permalink: /env_setup_install_ide.html
summary: |-
    The Java Toolkit comes packaged with a Build-in JDK version or without JDK.
    <br/><br/>
    In order for you to be able to run the Java IDE, you need to install JDK if needed and make sure it's compatible with your IDE version.
applies_to: [lab]
---

## Install Netbeans

There are many Java IDE here we are using **Netbeans IDE**. [NetBeans IDE 8.2 Installation Instructions](https://netbeans.org/community/releases/82/install.html){:target="_blank"}.

**Without JDK:**

[Download NetBeans IDE](https://netbeans.org/downloads/index.html){:target="_blank"}

**With JDK:**

[Download NetBeans IDE](http://www.oracle.com/technetwork/java/javase/downloads/jdk-netbeans-jsp-142931.html){:target="_blank"}

{% include troubleshooting.html content="
        JDK 8 is required for installing and running the Java SE, Java EE and All NetBeans Bundles. NetBeans 8.2 does not run on JDK9! Using JDK 9 with NetBeans IDE ?
        <a href=\"https://jaxenter.com/netbeans/using-apache-netbeans-incubating-jdk-9\" target=\"_blank\">Go here.</a>
" %}

Make sure you have the correct version installed of Java which is compatible with Netbeans IDE version.

## Install NetBeans IDE 8.2

### Microsoft Windows and Linux

**1)** After the download completes, run the installer.

-   For Windows, the installer executable file has the .exe extension. Double-click the installer file to run it.
-   For Linux platforms, the installer file has the .sh extension. For these platforms, you need to make the installer files executable by using the following command: `chmod +x <installer-file-name>`. Type `./<installer-file-name>` to run the installer.

{% include important.html content="
The installation directory must be empty and the user profile you are using to run the installer must have read/write permissions for this directory.
" %}

**2)** Click `Install` to begin the installation.

**3)** At the Setup Complete page, provide anonymous usage data if desired, and click `Finish`.

### OS X

**1)**  After the download completes, run the installer. The installer file has the .dmg extension.

**2)**  On the panel that opens double-click the package icon. The package has the .pkg extension. The installation wizard starts.

**3)**  Click Continue when the "This package will run a program to determine if the software can be installed." dialog box is displayed.

**4)**  At the Introduction page of the installation wizard, click Continue. 

{% include note.html content="
If the JDK version is older than the recommended JDK 8, download and install the latest JDK update from Java SE Downloads page and restart the NetBeans IDE installer.
" %}

**5)** Review the license agreement and click Continue. Click Accept in the pop-up window to accept the license.

**6)** At the Select a Destination page, select the drive and click Continue.

**7)** If you downloaded the All or Java EE bundle, you can customize your installation. On the last installation wizard panel, press the Customize button 1. in the bottom left-hand side of the panel. The tree of products is displayed.

**8)** Select the products you want to install.

**9)** Enter the administrator's name and password for your system and click OK to begin the installation. 

## Continue

Once you have installed JDK, proceed to [Java Path Setup](env_setup_classpath.html).
