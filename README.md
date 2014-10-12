# meltmedia OSS Parent POM

[![Build Status](https://travis-ci.org/meltmedia/oss-parent.svg)](https://travis-ci.org/meltmedia/oss-parent)

A parent POM for meltmedia OSS projects.  This POM is designed to work with the 
[Sonatype OSS Maven Repository](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide).

## Using this POM

To use this POM as the parent of your project, add this to your projects POM:

    <parent>
      <groupId>com.meltmedia</groupId>
      <artifactId>meltmedia-oss</artifactId>
      <version>1</version>
    </parent>

## What belongs in this POM?

This POM should only include general build and deployment information.  This POM should not include items related
to specific projects.  For instance, blocks like dependencies or dependencyManagement should not be added to this POM.
