[![Workflow Maven Package](https://github.com/drewctaylor/maven/workflows/workflow-maven-package/badge.svg)](https://github.com/drewctaylor/maven/workflows/workflow-maven-package/badge.svg)
[![Workflow Maven Deploy](https://github.com/drewctaylor/maven/workflows/workflow-maven-deploy/badge.svg)](https://github.com/drewctaylor/maven/workflows/workflow-maven-deploy/badge.svg)
[![Code Coverage](https://codecov.io/gh/drewctaylor/maven/branch/trunk/graph/badge.svg)](https://codecov.io/gh/drewctaylor/maven)

# Maven

This is a parent POM. It ensures that child projects have a consistent configuration, including:

* Consistent Java release and source format (imports, spacing).
* Consistent Maven version and POM format (element ordering).
* Consistent Maven plugin and dependency version reporting.
* Consistent JaCoCo reporting.
* Consistent README.md location and variable filtering.

## To Use Maven

To use maven:

1) Update the `~/.m2/settings.xml` to include a github username or github email address and a [github personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).

    For example:

    ```xml
    <settings>
        <servers>
            <server>
                <id>maven</id>
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
        <groupId>io.github.drewctaylor</groupId>
        <artifactId>maven</artifactId>
        <version>1.0.0-SNAPSHOT</version>
    </parent>
    ```

3) Update the `pom.xml` to include a reference to the plugin repository.

    For example:

    ```xml
    <repositories>
        <repository>
            <id>maven</id>
            <name>GitHub Packages</name>
            <url>https://maven.pkg.github.com/drewctaylor/maven</url>
        </repository>
    </repositories>
    ```