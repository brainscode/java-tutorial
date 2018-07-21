---
title: How to Install JDK
toc: false
sidebar: labs_sidebar
folder: env_setup
permalink: /env_setup_install_jdk.html
summary: According to Sun, 3 billion devices run Java. There are many devices where Java is currently used.
applies_to: [lab]
---

## Check if JDK is Already Installed

Open a terminal and run the following command to check Java JRE:

{% include command.html content="$ java -version" %}

Or run the following command to check Java Compiler:

{% include command.html content="$ javac -version" %}

- Verify the output.

    1.  If the command returns not found or a version number less than `java version "1.6.x_xx"`, continue to [Download JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html){:target="_blank"} for your operating system.

    1.  If you already have JDK `v1.6.x` or later, proceed to [Java Path Setup](env_setup_classpath.html).

## Install JDK

Select your Operating System:

Java Help Center - [Installing Java](https://www.java.com/en/download/help/index_installing.xml){:target="_blank"}

<ul id="osTabs" class="nav nav-tabs">
    <li class="active"><a href="#windows" data-toggle="tab">Windows</a></li>
    <li><a href="#macOS" data-toggle="tab">macOS</a></li>
    <li><a href="#linux" data-toggle="tab">Linux</a></li>
    <li><a href="#solaris" data-toggle="tab">Solaris</a></li>
</ul>
<div class="tab-content">
    <div role="tabpanel" class="tab-pane active" id="windows">
        <ol>
         <p><b>Install Java on Windows </b><a href="https://www.java.com/en/download/help/windows_offline_download.xml" target="_blank">Help</a></p>
	  <li>
            <p> Click on <code class="highlighter-rouge">Download</code> JDK. For Java latest version.</p>
            <p><b> Add-on:</b> or you can download IDE (Netbeans). Click on <code class="highlighter-rouge">Download</code> JDK with NetBeans.</p>
          </li>
          <li>
            <p> Next,</p>
          </li>
          <li>
            <p> Accept License Agreement</p>
	  </li>
          <li>	<p>Download latest JDK version (32-bit or 64 bit) of Java for Windows.</p>
	  </li>
          <li>	<p>When the download is complete, run the setup to install JDK. Click <code class="highlighter-rouge">Next</code>.</p>
	  </li>
          <li>	<p>When the installation is completed click <code class="highlighter-rouge">Close</code>.</p>
		<p></p>
	  </li>
          <li>
            <p>Proceed to <a href="env_setup_install_ide.html">Install IDE</a>.</p>
          </li>
        </ol>
    </div>

    <div role="tabpanel" class="tab-pane" id="macOS">
        <ol>
         <p><b>Install Java on Mac </b><a href="https://www.java.com/en/download/help/mac_install.xml" target="_blank">Help</a></p>
	  <li>
            <p> Click on <code class="highlighter-rouge">Download</code> JDK. For Java latest version.</p>
          </li>
          <li>
            <p> Next,</p>
          </li>
          <li>
            <p> Accept License Agreement</p>
	  </li>
          <li>	<p>Download latest JDK version of Java for macOS.</p>
	  </li>
          <li>	<p>When the download is complete, run the setup to install JDK. Click <code class="highlighter-rouge">Next</code>.</p>
	  </li>
          <li>	<p>When the installation is completed click <code class="highlighter-rouge">Close</code>.</p>
		<p></p>
	  </li>
          <li>
            <p>Proceed to <a href="env_setup_install_ide.html">Install IDE</a>.</p>
          </li>
        </ol>
    </div>

    <div role="tabpanel" class="tab-pane" id="linux">
        <ol>
         <p><b>Install Java on Linux </b><a href="https://www.java.com/en/download/help/linux_install.xml" target="_blank">Help</a></p>
	  <li>
            <p> Click on <code class="highlighter-rouge">Download</code> JDK. For Java latest version.</p>
          </li>
          <li>
            <p> Next,</p>
          </li>
          <li>
            <p> Accept License Agreement</p>
	  </li>
          <li>	<p>Download latest JDK (32-bit) rpm, tar.gz file and to install <a href="https://www.java.com/en/download/help/linux_x64_install.xml" target="_blank">(64-bit)</a> Java for Linux.</p>
	  </li>
          <li>	<p>When the (32-bit) JDK download is complete, Change to the directory in which you want to install. Type:</p>
		<p><code class="highlighter-rouge">cd directory_path_name</code></p>
		<p>For example, to install the software in the /usr/java/ directory, Type:</p>
		<p><code class="highlighter-rouge">cd /usr/java/</code></p>
	  </li>
          <li>	<p>Move the .tar.gz archive binary to the current directory, Unpack the tarball and install Java</p>
		<p><code class="highlighter-rouge">tar zxvf jdk-xxxx-linux-i586.tar.gz</code></p>
	  </li>
          <li>	<p>The Java files are installed in a directory called /usr/java/jdk-xx/ in the current directory.</p>
		<p>Delete the <code class="highlighter-rouge">rm -rf *.tar.gz</code> file if you want to save disk space.</p>
	  </li>
          <li>
            <p>If you using Java for RPM based Linux Platforms, Go to <a href="https://www.java.com/en/download/help/linux_install.xml">Java for RPM based Linux Platforms</a>.</p>
          </li>
          <li>
            <p>Proceed to <a href="env_setup_install_ide.html">Install IDE</a>.</p>
          </li>
        </ol>
    </div>

    <div role="tabpanel" class="tab-pane" id="solaris">
        <ol>
         <p><b>Install Java on Solaris SPARC </b><a href="https://www.java.com/en/download/help/solaris_install.xml" target="_blank">Help</a></p>
	  <li>
            <p> Click on <code class="highlighter-rouge">Download</code> JDK. For Java latest version.</p>
          </li>
          <li>
            <p> Next, Accept License Agreement</p>
          </li>
          <li>
            <p> Change directory to the location where you would like to be installed. </p>
            <p> <code class="highlighter-rouge">cd directory_path_name</code> </p>
            <p> For example, to install the software in the /usr/java directory: </p>
            <p> <code class="highlighter-rouge">cd /usr/java</code> </p>
	  </li>
          <li>	<p>Move the .tar.gz archive binaries to the current directory.</p>
	  </li>
          <li>	<p>Unpack the tarball and install Java </p>
            <p><b>On 64-bit SPARC processors:</b> <code class="highlighter-rouge">gzip -dc jdk-xxx-solaris-sparcv9.tar.gz | tar xf -</code> </p>
            <p><b>On x64/EM64T processors:</b> <code class="highlighter-rouge">gzip -dc jdk-xxx-solaris-x64.tar.gz | tar xf -</code> </p>
	  </li>
          <li>
            <p>Proceed to <a href="env_setup_install_ide.html">Install IDE</a>.</p>
          </li>
        </ol>
    </div>
</div>

{% comment %}
## Windows

Following are steps to install Java in **Windows**.

**Step 1)** Click on `Download` JDK. For Java latest version.

**Add-on:** or you can download IDE (Netbeans). Click on `Download` JDK with NetBeans.

**Step 2)** Next, 

1.  Accept License Agreement

1.  Download latest Java JDK for your version (32 or 64 bit) of Java for Windows.

**Step 3)** When the download is complete, run the setup to install JDK. Click `Next`.

**Step 4)** When the installation is completed click `Close`.

1.  Proceed to [Install IDE](env_setup_install_ide.html#).

{% endcomment %}
