# simple-weather

## Setup

To setup the project for local development start with these commands in your terminal.

```sh
$ git clone https://github.com/kelvearagao/simple-weather.git
$ cd simple-weather
$ mvn install
$ mvn exec:java -Dexec.mainClass=org.sonatype.mavenbook.weather.Main
```

To supply a zip code, we would use the -Dexec.args argument and pass in a zip code:

```sh
$ mvn exec:java -Dexec.mainClass=org.sonatype.mavenbook.weather.Main \
  -Dexec.args="70112"
```

# Installing Maven

The following sections outline the recommended best-practice for installing Maven on a variety of operating systems.

## Installing Maven on Linux, BSD and Mac OS X

Download the current release of Maven from ```http://maven.apache.org/download.html```. Choose a format that is convenient for you to work with. Pick an appropriate place for it to live, and expand the archive there. If you expanded the archive into the directory ```/usr/local/apache-maven-3.0.5```, you may want to create a symbolic link to make it easier to work with and to avoid the need to change any environment configuration when you upgrade to a newer version:

```sh
$ cd /usr/local
$ ln -s apache-maven-3.0.5 maven
$ export PATH=/usr/local/maven/bin:$PATH
```

Once Maven is installed, you need to add its ```bin``` directory in the distribution (in this example, ```/usr/local/maven/bin```) to your command path.

You’ll need to add the PATH configuration to a script that will run every time you login. To do this, add the following lines to ```.bash_login``` or ```.profile```.

```sh
export PATH=/usr/local/maven/bin:${PATH}
```

Once you’ve added these lines to your own environment, you will be able to run Maven from the command line.

## Installing Maven on Microsoft Windows

Installing Maven on Windows is very similar to installing Maven on Mac OS X, the main differences being the installation location and the setting of an environment variable. This book assumes a Maven installation directory of ```C:\Program Files\apache-maven-3.0.5```, but it won’t make a difference if you install Maven in another directory as long as you configure the proper environment variable. Once you’ve unpacked Maven to the installation directory, you will need to update the ```PATH``` environment variable:

```sh
C:\Users\tobrien > set PATH="c:\Program Files\apache-maven-3.0.5\bin";%PATH%
```

Setting this environment variable on the command line will allow you to run Maven in your current session. Unless you add them to the System or User environment variables through the Control Panel, you’ll have to execute these two lines every time you log into your system. You should modify both of these variables through the Control Panel in Microsoft Windows.

Setting Environment Variables

* Go into the ```Control Panel```
* Select ```System```
* Go in Advanced tab and click on ```Environment Variables```.
* Click on the Path variable in the lower System variables section and click the Edit button.
* Add the string ```"C:\Program Files\apache-maven-3.0.5\bin;"``` in the Variable value field to the front of the existing value and click on the OK button in this and the following dialogs.

## Testing a Maven Installation
Once Maven is installed, you can check the version by running ```mvn -v``` from the command line. If Maven has been installed, you should see something resembling the following output.

```
$ mvn -v
Apache Maven 3.0.5 (r01de14724cdef164cd33c7c8c2fe155faf9602da; 2013-02-19 05:51:28-0800)
Maven home: /usr/local/maven
Java version: 1.7.0_75, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.7.0_75.jdk/Contents/Home/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "10.8.5", arch: "x86_64", family: "mac"
```

If you see this output, you know that Maven is available and ready to be used. If you do not see this output, and your operating system cannot find the ```mvn``` command, make sure that your ```PATH``` environment variable and ```M2_HOME``` environment variable have been properly set.
