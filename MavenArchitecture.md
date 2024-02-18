# Maven Architecture

## Maven Repository
The Maven repository serves as a storage location for Maven artifacts or dependencies, typically JAR files. These dependencies are specified in a file called `pom.xml`. The `pom.xml` file contains information about Java classes, resources, and other dependencies. There are two types of repositories:

- **Local Repository:** Maven downloads dependencies defined in the `pom.xml` file into the local repository from the central or remote repository.
- **Central/Remote Repository:** This is the central storage location for Maven artifacts.

![image](https://github.com/discover-devops/MAVEN/assets/53135263/c156d226-e365-4ac5-9639-a12d7abd9ef5)



## Maven Usage
Maven is a versatile tool that offers several benefits:

- **Project Building:** Easily build projects with Maven.
- **Dependency Management:** Add JARs and other project dependencies effortlessly.
- **Project Information:** Obtain project-related information, including log documents, dependency lists, and unit test reports.
- **Central Repository Updates:** Facilitates updating the central repository with JARs and dependencies.
- **Build Variety:** Build projects into various output types like JAR, WAR, etc., without the need for extensive scripting.
- **Integration with Source Control:** Integrate projects seamlessly with source control systems such as Subversion or Git.
- **Build Lifecycle Management:** Manage the project's build lifecycle, including compilation, testing, packaging, and deployment.
- **Standard Project Structure:** Provides a standard project structure for easy navigation and file location.
- **Multi-Module Projects:** Support for working on multiple related projects simultaneously and efficient management of dependencies.
- **Plugin Extensibility:** Utilize Maven plugins for additional functionalities like code coverage analysis and static code analysis.
- **Customization:** Highly customizable to meet specific project needs and requirements.
- **Dependency Management Simplification:** Simplifies the process of managing project dependencies, ensuring correct library and framework versions.

## Maven pom.xml File
The `pom.xml` file, short for Project Object Model, is essential for Maven operations. It is an XML file containing project and configuration information used by Maven to build the project. Key components of the `pom.xml` file include:

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.project.loggerapi</groupId>
    <artifactId>LoggerApi</artifactId>
    <version>0.0.1-SNAPSHOT</version>

    <!-- Add typical dependencies for a web application -->
    <dependencies>
        <dependency>
            <groupId>org.apache.logging.log4j</groupId>
            <artifactId>log4j-api</artifactId>
            <version>2.11.0</version>
        </dependency>
    </dependencies>
</project>
```

### Elements used for Creating pom.xml file:

- **project:** Root element of the `pom.xml` file.
- **modelVersion:** Indicates the version of the POM model in use (e.g., 4.0.0 for Maven 2 and Maven 3).
- **groupId:** Unique identifier for the project group, often similar to the root Java package name.
- **artifactId:** Name of the project being built.
- **version:** Version number of the project.

### Key Components:

- **dependencies:** Defines a list of project dependencies.
- **dependency:** Describes each dependency with groupId, artifactId, and version.
- **name:** Gives a name to the Maven project.
- **scope:** Defines the scope for the Maven project (e.g., compile, runtime, test, provided, system).
- **packaging:** Specifies the output type for the project, such as JAR or WAR.
