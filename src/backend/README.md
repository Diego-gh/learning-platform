# Getting Started

### Running the Application

#### Prerequisites

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) 17 or higher
- [VS Code](https://code.visualstudio.com/) with the Extension Pack for Java installed

#### Steps to Run

1. Open this project folder in VS Code
2. Install the [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) if not already installed
3. Open the terminal in VS Code (`Ctrl + ~` or `View > Terminal`)
4. Run the application using Maven:
   ```bash
   ./mvnw spring-boot:run
   ```
   Or on Windows:
5. The application will start and be available at `http://localhost:8080`

#### Alternative: Run from VS Code UI

- **Right-click on ProjectApplication.java** and select:
  - `Run` to start the application
  - `Debug` to start with debugging enabled
- **Use the Run and Debug sidebar** (`Ctrl + Shift + D`):
  - Click the green "Run and Debug" button or select a debug configuration from the dropdown

## Reference Documentation

For further reference, please consider the following sections:

- [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
- [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/4.0.0/maven-plugin)
- [Create an OCI image](https://docs.spring.io/spring-boot/4.0.0/maven-plugin/build-image.html)
- [Spring Web](https://docs.spring.io/spring-boot/4.0.0/reference/web/servlet.html)
- [Spring Data JPA](https://docs.spring.io/spring-boot/4.0.0/reference/data/sql.html#data.sql.jpa-and-spring-data)

## Guides

The following guides illustrate how to use some features concretely:

- [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
- [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
- [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)
- [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

### Maven Parent overrides

Due to Maven's design, elements are inherited from the parent POM to the project POM.
While most of the inheritance is fine, it also inherits unwanted elements like `<license>` and `<developers>` from the parent.
To prevent this, the project POM contains empty overrides for these elements.
If you manually switch to a different parent and actually want the inheritance, you need to remove those overrides.
