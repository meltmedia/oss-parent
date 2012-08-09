meltmedia OSS Parent POM
====================

A parent POM for meltmedia OSS projects.  This POM is designed to work with the 
[Sonatype OSS Maven Repository](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide).

Uning this POM
--------------

To use this POM as the parent of your project, add this to your projects POM:

    <parent>
      <groupId>com.meltmedia</groupId>
      <artifactId>meltmedia-oss</artifactId>
      <version>1</version>
    </parent>

What belongs in this POM?
-------------------------

This POM should only include general build and deployment information.  This POM should not include items related
to specific projects.  For instance, blocks like dependencies or dependencyManagement should not be added to this POM.

Applying OSS Licenses
---------------------

This POM includes the [maven-license-plugin](http://code.google.com/p/maven-license-plugin/).  Please read the documentation of this project for information relating
to setting up and applying licenses.