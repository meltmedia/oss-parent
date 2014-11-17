# meltmedia OSS Parent POM

[![Build Status](https://travis-ci.org/meltmedia/oss-parent.svg)](https://travis-ci.org/meltmedia/oss-parent)

A parent POM for meltmedia OSS projects.  This POM is designed to work with the 
[Sonatype OSS Maven Repository](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide).

## Using this POM

To use this POM as the parent of your project, add this to your projects POM:

    <parent>
      <groupId>com.meltmedia</groupId>
      <artifactId>meltmedia-oss</artifactId>
      <version>2-SNAPSHOT</version>
    </parent>

## What belongs in this POM?

This POM should only include general build and deployment information.  This POM should not include items related
to specific projects.  For instance, blocks like dependencies or dependencyManagement should not be added to this POM.

## Baseline Configuration

### Java

This POM defaults Java 1.8 source and target versions.  You can set `maven.compiler.source` and `maven.compiler.target` to change those settings.

### Javadocs

The javadoc plugin is configured to support Markdown comments with the [Pegdown Doclet](https://github.com/Abnaxos/pegdown-doclet).

### Format Lifecycle

This POM provides a `format` lifecycle extention, with the phases `pre-format`, `format` and `post-format`.  You can format a project using:

```
mvn format
```

### License Headers

During the `format` phase, Apache 2 license headers will be added to the project source.  You can set `project.project.inceptionYear`, `copyright.owner` and `copyright.email` to control the content in the header.
