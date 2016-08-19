# OmegaT project to translate IntelliJ platform resources in Japanese.
This project is a community translation project to build a Japanese Resources for IntelliJ platforms.

JetBrains decided they don't provide Japanese translation resources for their
product after it had released Japanese editions in 2006.
https://www.jetbrains.com/company/press/press-archive/pr_060206.html

## Prerequisite

You need to have Java Runtime Environment version 1.8 or later.

## How to generate resource file for Intellij community

Please call Gradle build system `gradlew` command from console.

```
$ ./gradlew build
```

If you runs it on MS Windows platform, please call batch file.

```
$ .\gradlew.bat build
```

Generator depends on a couple of libraries and applications, you need to connect
your platform to internet. If you are behind proxy server or firewall, please
refer Gradle documentation how to configure Gradle for network connections.
It will download some jar files from https://jcenter.bintray.com repository.
Then it convert source English resource files with translation result into
Japanese resources.

You can get the IDE's resources as `build/distribution/<name>.zip`
Also you can get plugins resources as `build/distribution/plugins.zip`

Which name will become intellijCommunity, android and so on.

## Instalation of localizaed resources

Please find a place where IntelliJ platform has been installed.

Place resource files into ```/where/intellij/platform/insalled/lib/resources_ja.jar```.
You can extract zip file as follows:

```
$ cd /where/intellij/platform/installed
$ unzip /where/resource/download/intellijPlatform.zip
```

For plugins ```/where/intellij/platform/installed/plugins/<plugin name>/lib/resources_ja.jar```
You also extract plugin resources as follows:

```
$ cd /where/intellij/platform/installed
$ unzip /where/resource/download/plugins.zip
```

## How to generate resource file for JetBrains products

Please check product installed directory such as /opt/JetBrains/idea-IC2016.2/.
You may find English resource file in lib/resources-en.jar

Please extract it into product directory.

```
$ cd source/product/
$ jar xf /where/your/idea/installed/lib/resources-en.jar
```

then you can generate translated resource.

## How to translate

The project use OmegaT, Computer Aided Translation tool.
OmegaT is an Open Source Software and freely available for translators.
It is a kind of a translation memory.

The repository is designed to work with OmegaT team features. This means
translators who work on the repository are collaborative team.

If you want to use other tools you can generate TMX file by OmegaT and export
it at project root as `intellij-resources-ja-level1.tmx`.

## Contributions

There are two way to contirbute to the project.

### Translation

Translation updates are not supporeted to merge with PR. Instead of push a request,
please ask us to join as a member who can write a repository.

OmegaT has a team feature. It automatically push translation contribution
onto github repository.

If you want to join, please leave a issue to express your will.

We use custom version of OmegaT Version 4.0 snapshot for automation of the project.
Also we bundles custom plugin that support XML fils in IntelliJ platform.
You should use gradle to launch custom OmegaT;

```
$ ./gradlew omegat
```

It automatically start omegat GUI and prepare environment for you.
You need to install JRE 1.8 or later to run OmegaT.


### Build tools

You are welcome to fork the project and to send a pull request.
Please submit an issue before making a patch, and pleaes include
an issue number as a part of a commit message.


## FAQ

- Q) Are there any official Japanese version of IntelliJ IDEs?
- A) No. There is no supported Japanese version. If you want to use IDEs with localized resources, it may not be supporeted by JetBrains, and you should do it with your own risk. Please also see a discussion on jetbrains support forum.
　 https://intellij-support.jetbrains.com/hc/en-us/community/posts/206917695-Localized-IDEA-Chinese-Japanese-

- Q) Where is a detailed explanation how to localize IntelliJ Platform.
- A) see. http://www.jetbrains.org/intellij/sdk/docs/reference_guide/localization_guide.html

## License

Translation memories are distributed on the Apache 2.0 License.


## Copyright

Copyright 2013      Yuzo Morioka

Copyright 2013      GH@morizo999

Copyright 2016      Hiroshi Miura
