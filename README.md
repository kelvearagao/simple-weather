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
