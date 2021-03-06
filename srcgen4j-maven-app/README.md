srcgen4j-maven-app
==================
Application that takes a Maven pom.xml and executes the generator in a main method.

You can use this application to easily debug the generation process for any SrcGen4J project.

## Getting started
1. Add all dependencies necessary for the generation process to the [pom.xml](pom.xml)
2. Set any breakpoint you like in the generator classes
3. Run the [SrcGen4JMavenApp.java](src/main/java/org/fuin/srcgen4j/maven/SrcGen4JMavenApp.java) in debug mode.
   The only command line argument to provide is the directory where the Maven pom.xml is located.

## Relative paths
In case you have relative paths in your 'srcgen4j-config.xml', you need to change them to an absolute path.

For example:
```xml
<xtext:xtext-parser-config modelPath="src/main/resources" modelExt="ddd"
```

Should be:
```xml
<xtext:xtext-parser-config modelPath="/home/developer/my-project-to-debug/src/main/resources" modelExt="ddd"
```
