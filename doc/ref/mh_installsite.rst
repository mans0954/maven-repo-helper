mh\_installsite:
~~~~~~~~~~~~~~~~

Usage:

::

    mh_installsite [option]... [pom] [site-file]

Installs the site.xml file in /usr/share/maven-repo, at the correct
location for Maven.

Where:

::

    [pom] is the location of the POM associated with the site.xml file to install.
      GroupId, artifactId and version will be extracted from this file.
    [site-file] is the location of the site.xml to install.

Options:

::

    -h --help: show this text
    -V --version: show the version
    -p<package> --package=<package>: name of the Debian package which will contain the site file
    -e<version>, --set-version=<version>: set the version for the POM, do not use the version declared in the POM file.
    -r<rules> --rules=<rules>: path to the file containing the rules to apply when cleaning the POM.
      Optional, the default location is debian/maven.rules
      Maven rules are used here to extract the groupId, artifactId and version from the POM file.
    -v --verbose: show more information while running
    -n --no-act: don't actually do anything, just print the results
    --skip-clean-pom: don't clean the pom, assume that a previous action ran mh_cleanpom with the correct options.
      mh_cleanpom is run only to extract the groupId, artifactId and version of the jar

