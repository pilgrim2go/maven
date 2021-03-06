[![Workflow Maven Package](https://github.com/drewctaylor/${project.artifactId}/workflows/workflow-maven-package/badge.svg)](https://github.com/drewctaylor/${project.artifactId}/workflows/workflow-maven-package/badge.svg)
[![Workflow Maven Deploy](https://github.com/drewctaylor/${project.artifactId}/workflows/workflow-maven-deploy/badge.svg)](https://github.com/drewctaylor/${project.artifactId}/workflows/workflow-maven-deploy/badge.svg)
[![Code Coverage](https://codecov.io/gh/drewctaylor/${project.artifactId}/branch/trunk/graph/badge.svg)](https://codecov.io/gh/drewctaylor/${project.artifactId})

# Maven

This is a parent POM. It ensures that child projects have a consistent configuration, including:

* Consistent Java release and source format (imports, spacing).
* Consistent Maven version and POM format (element ordering).
* Consistent Maven plugin and dependency version reporting.
* Consistent JaCoCo reporting.
* Consistent README.md location and variable filtering.

As well as:

* References to the following repositories:
  * https://maven.pkg.github.com/drewctaylor/algebraic-type
  * https://maven.pkg.github.com/drewctaylor/constrain
  * https://maven.pkg.github.com/drewctaylor/function
  * https://maven.pkg.github.com/drewctaylor/maven
  * https://maven.pkg.github.com/drewctaylor/require
  * https://maven.pkg.github.com/drewctaylor/type-encoded
* References to the following plugin repositories:
  * https://maven.pkg.github.com/drewctaylor/maven
  * https://maven.pkg.github.com/drewctaylor/javapoet-maven-plugin

## To Use Maven

To use maven:

1) Update the `~/.m2/settings.xml` to include a github username or github email address and a [github personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).

    For example:

    ```xml
    <settings>
        <servers>
            <server>
                <id>${project.artifactId}</id>
                <username>github-username-or-email-address</username>
                <password>github-personal-access-token</password>
            </server>
        </servers>
    </settings>
    ```

2) Update the `pom.xml` to include a reference to this parent POM.

    For example:

    ```xml
    <parent>
        <groupId>${project.groupId}</groupId>
        <artifactId>${project.artifactId}</artifactId>
        <version>${project.version}</version>
    </parent>
    ```

3) Update the `pom.xml` to include a reference to the plugin repository.

    For example:

    ```xml
    <repositories>
        <repository>
            <id>${project.artifactId}</id>
            <name>GitHub Packages</name>
            <url>https://maven.pkg.github.com/drewctaylor/${project.artifactId}</url>
        </repository>
    </repositories>
    ```