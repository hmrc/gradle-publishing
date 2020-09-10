
# gradle-publishing

This repository provides Gradle plugins/ scripts etc which are used to canonicalise the artefact publishing process for HMRC MDTP Gradle projects.

# Publishing

This project is published as tags in Github, this is facilitated by the [nebula-publishing-plugin][1].

To perform a snapshot release:

    ./gradlew final release

To perform a final release:

    ./gradlew snapshot release
    
# Usage

To use scripts/ plugins from this project in another Gradle project, simply use the `apply from: "<url>"` behaviour in Gradle.

To avoid non-deterministic builds, it is strongly recommended to use a particular release of this project, rather than just pulling from the default branch, so please check the available release tags before sourcing any files. e.g.

    apply from: "https://raw.githubusercontent.com/hmrc/gradle-publishing/v0.2.0/<some-file>" 
    
## Bintray Distribution

The `hmrc_bintray_distribution_plugin.gradle` file provides a plugin which distributes CITO artefacts from Artifactory to HMRC's public Bintray repository.

[1]: https://github.com/nebula-plugins/nebula-publishing-plugin

