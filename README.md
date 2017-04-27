Use Github as a Maven Artifact Repository
---
This is sample based on the [this SO][1] answer on how to use a github repo as a repository for our maven artifacts.

Usage
---
Add this to your `pom.xml` and you're good to go:

    <repositories>
        <repository>
            <id>alidg-repo</id>
            <url>https://raw.github.com/alimate/string-utils/mvn-repo/</url>
            <snapshots>
                <enabled>true</enabled>
                <updatePolicy>always</updatePolicy>
            </snapshots>
        </repository>
    </repositories>
    
And this dependency:

    <dependency>
        <groupId>me.alidg</groupId>
        <artifactId>string-utils</artifactId>
        <version>0.0.1</version>
    </dependency>


[1]: http://stackoverflow.com/a/14013645/1393484
