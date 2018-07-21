---
title: Java Path Setup
toc: false
sidebar: labs_sidebar
folder: env_setup
permalink: /env_setup_classpath.html
summary: The PATH variable gives the location of executable files. It is possible to run a program without specifying the PATH but you will need to give full path of executable like %SystemRoot%\TEMP instead of using TEMP or TMP variable.
applies_to: [lab]
---

## How to set Environment Variables in Java: Path and Classpath

### In Windows

The CLASSPATH variable gives location of the Library Files.

Let's look into the steps to set the PATH and CLASSPATH 

1.  Right Click on the My Computer and select the Properties.

    {% include note.html content="
        Some have `This PC` name for `My Computer` whereas you have to run by Administrator Privileges.
    " %}

1.  Click on Advanced system settings.

    ![](./images/labs/path_setup/path1.png)

1.  Click on Environment Variables

    ![](./images/labs/path_setup/path2.png)
	
1.  Click on `New...` Button of User variables.

1.  Type **PATH** in the Variable name field.

    ![](./images/labs/path_setup/path3.png)
	
1.  Copy the path location of bin folder where JDK is installed. 

    ![](./images/labs/path_setup/path4.png)
	
1.  Paste path location of bin folder in Variable value and click on `OK` Button. 

    ![](./images/labs/path_setup/path5.png)

### In Linux

Let's see how to set path in Linux OS:

{% include command.html content="$ export PATH=$PATH:/home/jdk1.6.01/bin/ " %}

### In Ubuntu Linux

Edit the system Path file /etc/profile

{% include command.html content="$ sudo gedit /etc/profile " %}

Add following lines in end.

{% include code.html lang="bash" content="JAVA_HOME=/usr/lib/jvm/jdk1.x.x -- Where your JDK is installed
PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
export JAVA_HOME
export JRE_HOME
export PATH" %}

{% include command.html content="$ source /etc/profile " %}

### Verify the output.

-  Open a terminal and run the following command:

{% include command.html content="$ javac -version" %}

## Continue

Proceed to [Lab 1 - First Program](lab1_overview.html).
