# Inofficial Jetbrains PPA

This is a fork of the inofficial Jetbrains PPA which you can use to get the latest and greatest products from Jetbrains.

Currently, the following packages are supported and automatically updated using [TravisCI](https://travis-ci.org/jdeluyck/jetbrains-ppa).

* CLion `clion`
* DataGrip `datagrip`
* GoLand `goland`
* IntelliJ IDEA Community `intellij-idea-community`
* IntelliJ IDEA Ultimate `intellij-idea-ultimate`
* PhpStorm `phpstorm`
* PyCharm Community `pycharm-community`
* PyCharm Education `pycharm-education`
* PyCharm Professional `pycharm-professional`
* Rider `rider`
* RubyMine `rubymine`
* WebStorm `webstorm`

# Usage

To use it, enter the commands below, one by one. They download the correct GPG Key and add this repositories sources to your system sources.

```
curl -s https://ppa-jetbrains.kcore.org/file/ppa-jetbrains//4C57F7B442CA12CF.pub.ascc | sudo apt-key add -
echo "deb https://ppa-jetbrains.kcore.org/file/ppa-jetbrains/ bionic main" | sudo tee /etc/apt/sources.list.d/jetbrains-ppa.list > /dev/null
sudo apt-get update
```

To install for example IntelliJ Idea Ultimate, you can now run

```
sudo apt-get install intellij-idea-ultimate
```

If you have any issues, please [create a GitHub issue](https://github.com/jdeluyck/jetbrains-ppa/issues/new).

## I want another package

If you want a package for another Jetbrains product please [create a GitHub issue](https://github.com/jdeluyck/jetbrains-ppa/issues/new).

## Why not use the [official snap packages](https://snapcraft.io/search?q=jetbrains)?

Sure! If you like snap packages, go ahead. However, not all packages contained in this repository are already available as snap packages. And maybe you don't like snaps? :)

## Building the packages

To build a package, run the `build` script with a package folder:

    ./build-single-deb packages/<package>

To build intellij-idea-ultimate for example use:

    ./build-single-deb packages/intellij-idea-ultimate

## Why this was written

I hate manually downloading, extracting and moving the `*.tar.gz` from the
JetBrains website to get an IDE update. Unfortunately JetBrains does not have a
Debian repository.

There are already [existing](https://launchpad.net/~mmk2410/+archive/ubuntu/intellij-idea)
 [PPAs](https://launchpad.net/~vantuz/+archive/ubuntu/jetbrains).
However, none have continuous delivery or provide a wide range of JetBrains products.

---

This fork is maintained by Jonas Gröger. Automatically updated by [TravisCI](https://travis-ci.org/jdeluyck/jetbrains-ppa).

Original is maintained by [Jonas Gröger](https://github.com/JonasGroeger/jetbrains-ppa).
