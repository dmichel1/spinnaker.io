---
title: "Triggering pipelines with Artifactory"
linkTitle: "JFrog Artifactory"
weight:
description: >
  Add a [JFrog Artifactory](https://jfrog.com/artifactory/) trigger to your pipeline.
---

This guide explains how to add a [JFrog
Artifactory](https://jfrog.com/artifactory/) trigger to your pipeline.

> Currently, the Artifactory trigger only works with Maven artifacts.

## Prerequisites

This guide assumes you have the following:

* An Artifactory search configured in Spinnaker (see the documentation for the [hal config repository artifactory](/docs/reference/halyard/commands/#hal-config-repository-artifactory)  Halyard commands).

* A Maven account configured in Spinnaker (see the documentation for the [hal config artifact maven](/docs/reference/halyard/commands/#hal-config-artifact-maven)  Halyard commands).

* Artifact support [enabled](/docs/reference/artifacts/#enabling-artifact-support).

## Adding an Artifactory Trigger

1. Create a pipeline.

1. In the __Configuration__ stage of your new pipeline, add a trigger.

1. In the __Type__ menu, select __Artifactory__. This brings up the following
screen:

    ![](artifactory-trigger.png)

1. In the __Artifactory Name__ menu, select an Artifactory search.

2. In the __Artifact Constraints__ menu, select __"Define a new artifact__.
This brings up the following screen:

    ![](expected-artifact.png)

1. Enter a name in the __Display Name__ field or leave the autogenerated
default.

1. In the __Account__ menu, select a Maven account.

1. In the __Maven Coordinate__ field, enter the Maven coordinates of the
artifact.

1. Click __Save Artifact__.
