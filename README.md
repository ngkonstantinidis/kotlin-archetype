[![GitHub release](https://img.shields.io/github/release/ngkonstantinidis/kotlin-archetype/all.svg)](https://api.github.com/repos/ngkonstantinidis/kotlin-archetype/releases/latest)
[![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/iluwatar/java-design-patterns/master/LICENSE.md)

# Kotlin Maven Archetype

An archetype to create a skeleton for a maven kotlin project.

## Usage

The artifact is available at a private repository. In order to use this archetype, you have to add this repository to your `.m2/settings.xml` and then execute the maven command. So:

To add the maven repository add the following block to your `.m2/settings.xml`:

```xml
<settings>
  ...

  <profiles>
      <profile>
          <id>myMavenRepoRead</id>
          <activation>
              <property>
                  <name>!doNotUseMyMavenRepo</name>
              </property>
          </activation>
          <properties>
              <myMavenRepoReadUrl>https://mymavenrepo.com/repo/x5FrKJ9Lug5fctVFg8Mx/</myMavenRepoReadUrl>
          </properties>
      </profile>
  </profiles>

  <activeProfiles>
    <activeProfile>myMavenRepoRead</activeProfile>
  </activeProfiles>
  ...
</settings>
```

After that, execute the following code

```bash
mvn archetype:generate \
    -DgroupId=foo \
    -DartifactId=bar \
    -Dversion=1.0.0-SNAPSHOT \
    -DarchetypeGroupId=ngk.maven.archetype \
    -DarchetypeArtifactId=kotlin \
    -DarchetypeVersion=1.1.0
```
