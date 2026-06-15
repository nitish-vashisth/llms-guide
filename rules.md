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









 
    
