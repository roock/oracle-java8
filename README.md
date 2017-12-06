Introduction
------------

Java 8 packages for Debian.

orginal can be founde at: https://github.com/rraptorr/oracle-java8
This repository only supports amd64 builds.
The prepare steps has been included in the main debian buildpackage script
Has been successfully tested with Jenkins+jenkins-debian-glue+cowbuilder


Supported Debian versions
-------------------------

So far packages were tested on following Debian versions:

- stretch amd64
- jessie amd64
- wheezy amd64

I do not have resources to test packages on Ubuntu. However, if one
finds any problem on Ubuntu, feel free to report an issue and I will
try to resolve it.

Usage
-----

To create packages on your own:

- apt-get install debhelper curl unzip
- git clone git://github.com/rraptorr/oracle-java8.git
- cd oracle-java8
- sh ./prepare.sh
- dpkg-buildpackage -uc -us
- install any missing packages that dpkg-buildpackage complains about
  and repeat

Legal
-----

Oracle does not permit to distribute repackaged binaries of Java, so
be advised that hosting any public repository with Java packages is
probably illegal (at least in some parts of the world).

On the other hand, this repository contains only scripts, that allows
one to repackage Oracle Java in Debian friendly way. No binaries are
or will be hosted.
