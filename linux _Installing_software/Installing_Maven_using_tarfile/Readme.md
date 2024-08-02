# Installing Maven Using Tar files In Linux Machine 
### What is Maven ?
Maven is a build automation tool developed using the Java programming language. It is primarily used for Java-based projects to manage the build process, including source code compilation, testing, packaging, and more.

### Maven Installation :
To Install, we need to install openjdk because these two are interact. the maven is been run using java.
To install Apache Maven on a Linux system using a .tar.gz file, follow these detailed steps:

__Step 1__: Download Maven
* Navigate to the directory where you want to download Maven, such as ~/Downloads:
```

cd ~/Downloads
```

* Download the latest Maven binary distribution. For example, to download Maven 3.9.8:
```

wget https://downloads.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.tar.gz

```

 __Step 2__: Extract the Archive
* Create a directory for Maven, typically in /opt:
```
sudo mkdir /opt/maven
```

* Extract the downloaded .tar.gz file into the /opt/maven directory:
``` 

sudo tar -xvzf apache-maven-3.9.8-bin.tar.gz -C /opt/maven --strip-components=1
```

__Step 3__: Set Up Environment Variables
* Open your profile configuration file (e.g., .bashrc, .bash_profile, or /etc/profile):
```

nano ~/.bashrc
```

- Add the following lines to set the M2_HOME and update the PATH:
```

export M2_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```

- Save the file and exit the editor. Then, apply the changes:
```

source ~/.bashrc
```

__Step 4__: Verify Installation
* To confirm that Maven is installed correctly, check the version:
```

mvn -v
```

* the output will seems like this,
```
$ mvn -version
Apache Maven 3.9.8 (cecedd343002696d0abb50b32b541b8a6ba2883f)
Maven home: /opt/apache-maven-3.9.8
Java version: 13.0.1, vendor: Oracle Corporation, runtime: /opt/jdk-16.0.1
Default locale: en, platform encoding: UTF-8
OS name: "linux", version: "4.15.0-47-generic", arch: "amd64", family: "unix"
```