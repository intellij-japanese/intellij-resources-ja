# intellij-resources

Here is a repository to store intellj platforms resources which is a source of translation.

## Subtree of mother project

Here is a child repository for intelli_resources_ja project and refered as git subtree.

## Files

* README.md: this file
* source.build: Gradle build sub project that describe how to generaete l10n resources.

## Directory structure

* intellijCommunity: copy of intellij-community/resource-en/src
* plugins: resources of plugins.
* android: contents from lib/resources-en.jar in Android Studio
* product: place holder for contents from lib/resources-en.jar in JetBrains products.


## Product place holder

A product folder is just an empty directory.

If you want to generate resources for JetBrains product lines such as pycharm,
you can extract english resources into place holder `product` in intellij_resources_ja
project. You may get build/product.jar as a result.
It may work for your product, or it is a chance to join and contribute
as a translators team member.

## Rules and generated files

This repository is intend to sourced in OmegaT project.
Gradle script assumes transteted files are generated in target directory.
