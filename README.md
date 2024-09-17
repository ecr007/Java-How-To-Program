# Java-How-To-Program

## Java Directory Structure

MyJavaApp/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── mycompany/
│   │   │           └── myjavaapp/
│   │   │               ├── App.java
│   │   │               └── SomeOtherClass.java
│   │   └── resources/
│   │       └── config.properties
│   ├── test/
│       ├── java/
│       │   └── com/
│       │       └── mycompany/
│       │           └── myjavaapp/
│       │               └── AppTest.java
│       └── resources/
│
├── lib/
│   └── external-library.jar
│
├── build/
│   ├── classes/
│   ├── libs/
│   └── reports/
│
├── .gitignore
├── README.md
└── build.gradle or pom.xml

## Explanation

- src/main/java: Contains your main application code.

- src/main/resources: Contains resources needed by your main application (e.g., configuration files).

- src/test/java: Contains your test code.

- src/test/resources: Contains resources needed by your tests.

- lib: Contains any external libraries (JAR files) your project depends on.

- build: Contains files generated during the build process, such as compiled classes and packaged JARs.

- .gitignore: Specifies files and directories to be ignored by Git.

- README.md: Provides information about the project.

- build.gradle or pom.xml: Build configuration files for Gradle or Maven.

Note: The term SNAPSHOT in a version number indicates that this is a development version of the software.