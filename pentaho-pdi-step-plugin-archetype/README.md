## PDI Step Plugin Archetype

The pdi-step-plugin-archetype can be used as a basis for any Pentaho Data Integration Step that produces a community edition kar. It will create the basic folder structure, provide you with a template README.md and a common .gitignore file.

### Example Usage
```
mvn archetype:generate \
 -DarchetypeGroupId=org.pentaho \
 -DarchetypeArtifactId=pdi-step-plugin-archetype \
 -DarchetypeVersion=2.19 \
 -DgroupId=com.my.company \
 -DartifactId=my-step-plugin \
 -Dversion=1.0-SNAPSHOT \
 -Dplugin_class_name=MyStep \
 -Dplugin_name="My Step" \
 -Dplugin_category=Transform \
 -Dplugin_description="This is what my step does."
 
$ cd my-step-plugin

$ mvn clean install
```
_Be sure to update the artifactId, version, and package arguments to reflect your particular project._

This will generate the following project structure:
```
my-step-plugin/
├── .gitignore
├── README.md
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── com
    │   │       └── my
    │   │           └── company
    │   │               ├── MyStep.java
    │   │               ├── MyStepData.java
    │   │               ├── MyStepDialog.java
    │   │               ├── MyStepMeta.java
    │   │               └── MyStepStepAnalyzer.java
    │   └── resources
    │       ├── MyStep.svg
    │       ├── OSGI-INF
    │       │   └── blueprint
    │       │       └── blueprint.xml
    │       ├── com
    │       │   └── my
    │       │       └── company
    │       │           └── messages
    │       │               └── messages_en_US.properties
    │       └── my-step-plugin-feature.xml
    └── test
        └── java
            └── com
                └── my
                    └── company
```

To deploy copy the generated "my-step-plugin-1.0-SNAPSHOT.kar" into "data-integration\system\karaf\deploy"