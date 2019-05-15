# Amazon Corretto 8 Installation Instructions for Debian\-Based and RPM\-Based Linux Distributions<a name="generic-linux-install"></a>

This topic describes how to install Amazon Corretto 8 on Debian\-based and RPM\-based Linux distributions\. 

If you need to install Amazon Corretto 8 on Amazon Linux 2, see [Installing on Amazon Linux 2](amazon-linux-install.md)\.

## Install Amazon Corretto 8 on Debian\-Based Linux<a name="debian-install-instruct"></a>

This section describes how to install and uninstall Amazon Corretto 8 on a host or container running a Debian\-based operating system\.

### Download and Install the Debian Package Manually<a name="debian-deb-install-instruct"></a>

1.  Download the Linux x64 `.deb` file from the [Downloads](downloads-list.md) page\. Before you install the JDK, install the `java-common` package\.   
**Example**  

   ```
   sudo apt-get update && sudo apt-get install java-common
   ```

1.  Install the `.deb` file by using `sudo dpkg --install`\.   
**Example**  

   ```
   sudo dpkg --install java-1.8.0-amazon-corretto-jdk_8.212.04-2_amd64.deb
   ```

### Verify Your Installation<a name="debian-deb-verify"></a>

 In the terminal, run the following command to verify the installation\. 

**Example**  

```
java -version
```
Expected output for 8u212:   

```
openjdk version "1.8.0_212"
OpenJDK Runtime Environment Corretto-8.212.04.2 (build 1.8.0_212-b04)
OpenJDK 64-Bit Server VM Corretto-8.212.04.2 (build 25.212-b04, mixed mode)
```

 If you see a version string that doesn't mention `Corretto`, run the following command to change the default `java` or `javac` providers\. 

**Example**  

```
sudo update-alternatives --config java
```
If you're using the JDK, you should also run the following\.  

```
sudo update-alternatives --config javac
```

### Uninstall Amazon Corretto 8<a name="debian-deb-uninstall"></a>

You can uninstall Amazon Corretto 8 by using the following command\.

Uninstall JDK:

**Example**  

```
sudo dpkg --remove java-1.8.0-amazon-corretto-jdk
```

## Install Amazon Corretto 8 on RPM\-Based Linux<a name="rpm-linux-install-instruct"></a>

### Download and install RPM package manually<a name="rpm-install-instruct"></a>

1.  Download the Linux x64 `.rpm` file from the [Downloads](downloads-list.md) page\. 

1.  Install the downloaded `.rpm` file using `yum localinstall`\.   
**Example**  

   ```
   sudo yum localinstall java-1.8.0-amazon-corretto-devel-1.8.0_212.b04-2.x86_64.rpm
   ```

### Verify Your Installation<a name="rpm-verify"></a>

 In the terminal, run the following command to verify the installation\. 

**Example**  

```
java -version
```
This is the expected output for 8u212:   

```
openjdk version "1.8.0_212"
OpenJDK Runtime Environment Corretto-8.212.04.2 (build 1.8.0_212-b04)
OpenJDK 64-Bit Server VM Corretto-8.212.04.2 (build 25.212-b04, mixed mode)
```

 If you see a version string that doesn't mention `Corretto`, run the following command to change the default `java` or `javac` providers\. 

**Example**  

```
sudo alternatives --config java
```
If you're using the JDK, you should also run the following\.  

```
sudo alternatives --config javac
```

### Uninstall Amazon Corretto 8<a name="rpm-uninstall"></a>

You can uninstall Amazon Corretto 8 by using the following

Uninstall JDK:

**Example**  

```
sudo yum remove java-1.8.0-amazon-corretto-devel
```