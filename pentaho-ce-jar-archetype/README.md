## Pentaho CE Jar Archetype

A project archetype for creating the structure of a new java project within the Pentaho ecosystem.

The pentaho-ce-jar-archetype can be used as a basis for any project (or even submodule) that produces a community edition jar. It will create the basic folder structure, provide you with a template README.md and a common .gitignore file.

### Example Usage
```
$ mvn archetype:generate                              \
     -DarchetypeGroupId=org.pentaho                   \
     -DarchetypeArtifactId=pentaho-ce-jar-archetype   \
     -DarchetypeVersion=1.0.24                         \
     -DgroupId=org.pentaho                            \
     -DartifactId=my-pentaho-project                  \
     -Dversion=1.0-SNAPSHOT                         \
     -Dpackage=org.pentaho.my.project
     
$ cd my-pentaho-project

$ mvn clean install
```
_Be sure to update the artifactId, version, and package arguments to reflect your particular project._

This will generate the following project structure:
```
my-pentaho-project/
├── README.md
├── pom.xml
└── src
    ├── it
    │   ├── java
    │   └── resources
    ├── main
    │   ├── java
    │   │   └── org
    │   │       └── pentaho
    │   │           └── my
    │   │               └── project
    │   │                   └── MyClass.java
    │   └── resources
    └── test
        ├── java
        │   └── org
        │       └── pentaho
        │           └── my
        │               └── project
        │                   └── MyClassTest.java
        └── resources
```