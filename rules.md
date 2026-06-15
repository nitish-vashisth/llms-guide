# rovodev instructions

## Overview

This repository uses Java with Spring Boot. To ensure code quality, maintainability, and
consistency, please adhere to the following
standards and best practices when contributing or reviewing pull requests.

---

## General Coding Standards

- **Follow Language Conventions:**
  - Java: [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
- **Line Length:**
  - Limit lines to 120 characters.
- **Naming Conventions:**
  - Classes: PascalCase (e.g., `UserService`).
  - Methods/Functions: camelCase (e.g.,`getUserById')
  - Variables: camelCase (e.g., `userName`).
  - Constants: UPPER SNAKE_CASE (e.g.,`MAX_RETRY_COUNT`). 
- **Comments:**
  - Use Javadoc for public classes and methods.
  - Write clear, concise comments where necessary.
  - Remove commented-out code before merging.
 
---

## Spring Boot Best Practices

- **Component Scanning:**
  - Use @Component`, `@Service`, `@Repository` and @Controller' appropriately.
- **Configuration:**
  - Externalize configuration using application.properties' or `application.yml.
  - Avoid hardcoding values.
- **Dependency Injection:**
  - Prefer constructor injection over field injection (Avoid `@Autowired directly on fields).
- **Exception Handling:**
  - Use `@ControllerAdvice for global exception handling.
  - Return meaningful error messages and appropriate HTTP status codes.
  - Don't catch and just rethrow them.
- **Validation:**
  - Use @Valid and validation annotations for request DTOS.
- **Logging:**
  - Use Loggers and declare correctly like `private static final Logger logger = LoggerFactory.getLogger(ClassName.class);`.
  - Avoid logging sensitive information.
- **Testing:**
- Write unit and integration tests for all new features.
- Test validation, edge cases, and exception flows
- Write Integration Tests for all service endpoints.
- Each test should validate a single scenario or behavior.
- Structure tests to follow the AAA (Arrange-Act-Assert) pattern.
- **Immutability:**
  - Create immutable object where possible
- **API Documentation:**
  - Use Swagger/OpenAPI annotations to document all REST endpoints.
- **Performance Considerations:**
  - Ensure efficient use of resources in API design.
- **Thread Safety and Concurrency:**
  - Review code for thread safety and proper handling of concurrency in shared resources or services
- **Error Handling Consistency:**
  - Ensure error responses follow a consistent structure (e.g., using a standard ErrorResponse` class).
- **Asynchronous Programming:**
  - Use proper asynchronous programming techniques (e.g., CompletableFuture`, `@Async) and avoid blocking calls in non-blocking contexts.

---

## Additional Best Practices

- **Dependency Management:**
  - Remove unused dependencies from `pom.xml`
-  **Access Modifiers:**
  -  Use appropriate access modifiers (e.g.,`private`, `protected`, `public') to encapsulate class members.
  - Prefer 'final' for variables that don't change.
  - Always declare static methods first, followed by public, protected and private methods.
- **Security Best Practices:**
  - Avoid hardcoded secrets or credentials.
  - Use tools like Spring Boot's @Configuration Properties or externalized secrets management (e.g., AWS Secrets Manager, HashiCorp
- **Code Coverage:**
  - Maintain a minimum code coverage threshold (e.g., 80%) using tools like JaCoCo/SonarQube Coverage.
- **Code Formatting Tools:**
  - Integrate automated code formatting tools (e.g., Checkstyle for Java) into the CI/CD pipeline.
- **Documentation for Complex Logic:**
  - Document complex business logic or workflows in the code or supplementary design documents.
- **CI/CD Integration:**
- Ensure all PRS pass CI/CD checks, including build success, test execution, and static code analysis.

---

## Java Practices
- **Indentation:**
  - Use 4 spaces for indentation; avoid tabs.
- **Annotations:**
  - Use @Override for overridden methods.
  - Use @NotNull' and @Nullable' annotations where applicable.
- **Streams and Lambdas:**
  - Prefer streams for collection processing but avoid overly complex stream chains.
  - Use method references (Class:: method`) where possible.
- **Logging:**
  - Use SLF4J for logging
  - Avoid using `System.out.println` or `printStackTrace`.
