# Introduction
## Build Tool
Gradle is used as a build tool for this project. Gradle is a powerful build tool that supports multiple programming languages and platforms. It is highly customizable and provides a rich set of plugins and features.

### Artifact Details
 - Group: com.rakuten.mu2
 - Artifact: project-name
 - Version: The guideline for versioning should be followed

### Gradle Wrapper
The Gradle Wrapper is a script that invokes a declared version of Gradle, downloading it beforehand if necessary. This ensures that the same version of Gradle is used by all developers, which helps to avoid compatibility issues.
 - The Gradle Wrapper files should be checked into the version control system.
 - Ensure the Gradle Wrapper files are up-to-date (or preferred version) with the latest version of Gradle.
 - The Gradle Wrapper should be used to build the project via the `gradlew` command.

### Dependency Versions
 - Explicit versions for dependencies should always be used in the build.gradle file. This ensures that the build is reproducible and that the versions of the dependencies being used are known.
 - The latest version of dependencies should always be used to ensure that the most up-to-date features and bug & security fixes are being utilized.
 - Dependency management plugins like `io.spring.dependency-management` should be used to manage dependencies in a structured way. For Azure dependencies, the `azure-spring-boot-bom` should be used to ensure compatibility and manage versions.
 - The `ext {}` block in the build.gradle file should be used to define dependency versions. This makes it easier to manage and update versions in a centralized way.

### Plugin Versions
 - org.springframework.boot: 3.3.6
 - io.spring.dependency-management: 1.1.6
 - org.jetbrains.kotlin.jvm: 2.1.0

# Coding

## Spring Application Flow
 - Controller: The controller layer should be used to handle incoming requests and return responses. It should be responsible for mapping requests to the appropriate service methods(if required). Controller can handle or modify exceptions and return the appropriate response(Better to handle by global exception handler).
 - Logic: If controller is calling multiple service layers then it should call the logic layer from where the service layers are called. This can be considered as facade layer.
 - Service: The service layer should contain the business logic of the application. It should be responsible for processing the data and performing the necessary operations.
 - Adapter: The adapter layer will be responsible to call external services, APIs or databases. 
 - Repository: The repository layer should be used to interact with the database. It should be responsible for reading and writing data to the database. If required external API calls can be stored here and return the response to the adapter layer. Necessary methods should be retried in this step.
 - Model: The model layer should contain the data objects used by the application. 

During the communication between layers
 - Data between layers should be transferred using DTOs (Data Transfer Objects). This helps to decouple the layers and provides a clear separation of concerns.
 - The caller of any method should get expected data or some exception. The method should not return null or any other unexpected value.
 -

## Coding Aspects
### Validations
 - Input parameters should be validated upon calling the controller method. 
 - @Valid annotation should be used to validate the input parameters. 
 - The validation should be done using the `jakarta.validation.constraints.` package.
 - If custom validation is required, a custom validator should be created and used for each of the purposes. Appropriate exception should be thrown if the validation fails.

### Uses of Spring Bean 
- Create necessary spring beans in a common place whenever applicable.
- The @Bean annotation should be used to define a bean.
- The @Qualifier annotation should be used to specify the name of the bean to be injected if there are multiple beans of the same type.

### Static Variables
 - Static variables should be avoided as much as possible. At first, properties through configurations should be used.
 - Common use cases of static variables are urls, status values or some default values. These can be avoided by defining them in configurations or creating enums.

### DI
 - Always use constructor injection for mandatory dependencies.

### Use when Instead of if-else Chains
 - When there are multiple if-else chains, it is better to use `when` expression.

### Use apply, let, run, also, with
 - `apply` should be used when an object needs to be initialized or configured.
 - `let` should be used when actions need to be performed on a nullable object or when the scope of a variable needs to be limited.
 - `run` should be used when multiple operations need to be performed on an object, and a result needs to be returned.
 - `also` should be used when side effects, such as logging or debugging, need to be performed without modifying the object.
 - `with` should be used when multiple operations need to be performed on an object, and a result needs to be returned, but the object itself is not needed.

### Utility methods and classes
 - Use top-level functions
 - Define classes for each of the types
 - Use extension functions to add functionality to existing classes (If required)




## Managing Configurations
 - The application.yml file should be used for Configuration Files: All the common configurations which are not supposed to be changed should be added in application.yml. This file is used to store common configurations that are shared across all environments.
 - Profile-Specific Configuration: Profiles should be used to manage different configurations for purposes (e.g., managing configurations for mltest).
 - Type-Safe Configuration with @ConfigurationProperties: Configuration properties should be defined in a type-safe manner using @ConfigurationProperties. This approach ensures that the configuration is validated at startup and provides a clear structure.
 - Passwords or other secrets: These types of sensitive information should be kept in safe storage like vault and should be avoided keeping these directly in configuration files.
 - External Configuration: External configuration should be used to keep the configuration separate from the codebase. This allows the configuration to be changed without rebuilding the application.

## Unknown/Unmanageable behaviors
 - If an unknown or unmanageable behavior is encountered, an exception should always be thrown. This ensures that the caller is aware of the issue and can handle it accordingly.
 - The appropriate exception type should be used to indicate the type of error that occurred. This makes it easier to handle the exception in a structured way.
 - The exception message and stack trace should always be logged to help with debugging and troubleshooting.
 - A retry mechanism should be implemented to handle transient errors. This can help to improve the reliability of the application. The configurations for the retry mechanism should be configurable.

## Handling Exceptions
 - @Validated should be used to validate the input parameters of the methods. This ensures that the input parameters are valid and helps to prevent errors.
 - @RestControllerAdvice should be used to handle exceptions globally. This allows for centralized exception handling and makes it easier to manage exceptions.
 - Custom exceptions should be used to handle specific error cases. This makes it easier to understand the error and handle it accordingly.
 - The exception message should be clear and informative. Better to create messages.properties file to store all the messages.

## Tests