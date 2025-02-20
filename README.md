# 21FS Software Engineering Lab SERVER (SoPra)
This repository includes the backend part of the semester project of the course SoPra ([source repository](https://github.com/sopra-fs21-group-22/server/tree/68b6c0e700eb64f837b6b61b28a7c22d47e19e40)). The code is written in `Java 15`. This is only the *SERVER*, to view the *CLIENT* switch to [this repository](https://github.com/maettuu/21FS-Software-Engineering-Lab-CLIENT).

Main packages: `springframework`, `jsonwebtoken`, `JUnit`, `mockito`, `slf4j.Logger`, `javax.persistence`, `util`, `sql`

## Introduction BANG!

The aim of this project is to implement the server-side of a digital version of the popular card game **BANG!**, to be playable in a browser.

## Technologies

- Java
- GitHub (Actions)
- Heroku
- REST API

## High-level components

[Player Table Entity](src/main/java/ch/uzh/ifi/hase/soprafs21/entity/PlayerTable.java)
- Most information during a game is in this class or referenced in this class

[Player Table Service](src/main/java/ch/uzh/ifi/hase/soprafs21/service/PlayerTableService.java)
- A large portion of actions during a game are performed by this class' methods

[Controllers](src/main/java/ch/uzh/ifi/hase/soprafs21/controller/gameStateControllers)
- These files receive incoming communication from the client-side and are therefore paramount to the project.

## Launch and Deployment

Download your IDE of choice: (e.g., [Eclipse](http://www.eclipse.org/downloads/), [IntelliJ](https://www.jetbrains.com/idea/download/)), [Visual Studio Code](https://code.visualstudio.com/) and make sure Java 15 is installed on your system (for Windows-users, please make sure your JAVA_HOME environment variable is set to the correct version of Java).

1. File -> Open... -> SoPra Server Template
2. Accept to import the project as a `gradle project`

To build right click the `build.gradle` file and choose `Run Build`

### VS Code
The following extensions will help you to run it more easily:
-   `pivotal.vscode-spring-boot`
-   `vscjava.vscode-spring-initializr`
-   `vscjava.vscode-spring-boot-dashboard`
-   `vscjava.vscode-java-pack`
-   `richardwillis.vscode-gradle`

**Note:** You'll need to build the project first with Gradle, just click on the `build` command in the _Gradle Tasks_ extension. Then check the _Spring Boot Dashboard_ extension if it already shows `soprafs21` and hit the play button to start the server. If it doesn't show up, restart VS Code and check again.

### Building with Gradle

You can use the local Gradle Wrapper to build the application.

Plattform-Prefix:

-   MAC OS X: `./gradlew`
-   Linux: `./gradlew`
-   Windows: `./gradlew.bat`

More Information about [Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html) and [Gradle](https://gradle.org/docs/).

### Build

```bash
./gradlew build
```

### Run

```bash
./gradlew bootRun
```

### Test

```bash
./gradlew test
```

## Roadmap

- Adding other users as friends
- Creating private lobbies
- Implement Expansions from the physical game

## Authors and acknowledgment

>E. Heggli, M. Mylaeus, R. Bommeli, R. Bättig, Y. Meister

## License

Licensed under GNU General Public License v3.0
- See [License](LICENSE)
