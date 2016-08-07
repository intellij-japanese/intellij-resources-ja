# intellij-resources

Here is a repository to store intellj platforms resources which is a source of translation.

## Directory structure

* intellij-community: copy of intellij-community/resource-en/src
* android: contents from lib/resources-en.jar in Android Studio
* product/idea: place holder for contents from lib/resources-en.jar in Intellij Idea community Edition
* product/pycharm: place holder for contents from lib/resources-en.jar in PyCharm community Edtion


## Submodule

A android` directory are configured as git submodule.
It refers a repository: https://github.com/intellij-japanese/src-android-studio-resources

To retrive android studio resource date:

``
$ git submodule update
``


