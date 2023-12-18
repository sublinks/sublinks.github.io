---
---
# Style Guides

It is best practice to use the `.editorconfig` file located in the repository.

## Java Style Guide (Based on Google's Java Style Guide)

1. **Source File Basics**
- **File Name:** The source file name consists of the case-sensitive name of the top-level class it contains, plus the `.java` extension.
- **File Encoding:** UTF-8.
- **Special Characters:** Use Unicode escape sequences only for non-printable characters.

2. **Source File Structure**
- **Order of Sections:** package statement, import statements, class, or interface declarations.
- **Import Statements:** Wildcard imports are not used; imports are neither line-wrapped nor column-aligned.

3. **Formatting**
- **Braces:** Use K&R style braces.
- **Indentation:** Use two spaces for indentation, not tabs.
- **One Statement Per Line:** Each statement is followed by a line-break.
- **Column Limit:** 100 or 120 characters.
- **Whitespace:** Use horizontal whitespace and vertical whitespace sparingly and purposefully.
- **Blank line:** A blank line immeditely after method declarations before the body of the method.

4. **Naming**
- **Package Names:** All lowercase, with consecutive words simply concatenated together.
- **Class Names:** Written in UpperCamelCase.
- **Method Names:** Written in lowerCamelCase.
- **Constant Names:** All uppercase, with words separated by underscores.
- **Non-constant Field Names:** Written in lowerCamelCase.
- **Parameter Names:** Written in lowerCamelCase.
- **Local Variable Names:** Written in lowerCamelCase.

5. **Programming Practices**
- **@Override:** Always used on methods overriding or implementing methods from a superclass or interface.
- **Caught Exceptions:** Either rethrown or logged, not ignored.
- **Static Members:** Qualified using class.
- **Finalizers:** Avoided.

### Spring Boot Specific Conventions

1. **Configuration Classes**
- Use `@Configuration` classes for defining beans and import them using `@Import` in main application class.

2. **Service Layer**
- Define service interfaces and implement them in service classes. Annotate service implementations with `@Service`.

3. **Repository Layer**
- Use Spring Data JPA `@Repository` interfaces for database operations.

4. **Controller Layer**
- Use `@RestController` for RESTful controllers and `@Controller` for MVC controllers. Clearly define request mappings.

5. **Application Properties**
- Define properties in `application.properties` or `application.yml`. Use type-safe configuration properties.

6. **Exception Handling**
- Use `@ControllerAdvice` for global exception handling.

7. **Logging**
- Use appropriate logging levels (DEBUG, INFO, WARN, ERROR) and use placeholders for log messages.

8. **Unit and Integration Testing**
- Write meaningful unit tests with `@SpringBootTest` for integration tests.

9. **Dependency Injection**
- Prefer constructor injection over field injection.

10. **Use of `Lombok`**
- Utilize **`Lombok`** annotations for reducing boilerplate code where appropriate.

Remember, these are high-level guidelines. For detailed coding standards, you should refer to the Google Java Style Guide
and supplement it with Spring Boot's best practices. The key is consistency and clarity in the project's codebase.