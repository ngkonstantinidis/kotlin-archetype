[![GitHub (pre-)release](https://img.shields.io/github/release/ngkonstantinidis/kotlin-archetype/all.svg)](https://github.com/ngkonstantinidis/kotlin-archetype/releases)

# Kotlin Maven Archetype

A simple archetype to create a skeleton for a maven kotlin project.

## Clone and Build

To use this archetype you should clone this repository and build the project.

```bash
git clone https://github.com/ngkonstantinidis/kotlin-archetype.git
cd kotlin-archetype
mvn clean install
```

## Usage

```bash
mvn archetype:generate \
    -DgroupId=foo \
    -DartifactId=bar \
    -Dversion=1.0.0-SNAPSHOT \
    -DarchetypeGroupId=ngk.maven \
    -DarchetypeArtifactId=kotlin-archetype \
    -DarchetypeVersion=1.0.0
```
