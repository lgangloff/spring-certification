<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

### Spring Professional Certification Practice Test (Advanced Level)

---

#### **Question 1: Spring Architecture**

**What was the primary motivation behind Spring's shift from XML-based configuration to Java-based configuration?**

1. To eliminate the need for dependency injection
2. To improve type safety and leverage IDE tooling
3. To reduce startup time by avoiding reflection
4. To simplify integration with legacy systems

**Correct Answer:** 2
**Explanation:** Java-based configuration (`@Configuration`, `@Bean`) provides compile-time type checking, better refactoring support, and IDE assistance compared to XML. This shift aimed to enhance developer productivity and reduce configuration errors.

---

#### **Question 2: Core Container Modules**

**Which Spring module is responsible for managing bean lifecycles and dependency resolution?**

1. `spring-core`
2. `spring-beans`
3. `spring-context`
4. `spring-expression`

**Correct Answer:** 2
**Explanation:** The `spring-beans` module implements the `BeanFactory`, which handles bean instantiation, dependency injection, and lifecycle management. `spring-context` builds on this by adding application-level features like AOP and event propagation.

---

#### **Question 3: Java Configuration**

**Given the configuration below, what happens when `@ComponentScan` is used without arguments?**

```java  
@Configuration  
@ComponentScan  
public class AppConfig {}  
```

1. Scans all packages under the class's package
2. Scans only classes annotated with `@Bean`
3. Disables component scanning entirely
4. Scans the `org.springframework.stereotype` package

**Correct Answer:** 1
**Explanation:** `@ComponentScan` without arguments defaults to scanning the package of the class declaring the annotation and its subpackages for `@Component`, `@Service`, etc..

---

#### **Question 4: Bean Conflicts**

**How does Spring resolve conflicts when two beans of the same type are declared in separate `@Configuration` classes?**

1. Throws a `NoUniqueBeanDefinitionException`
2. Uses the bean from the configuration class loaded first
3. Prioritizes the bean with `@Primary`
4. Merges the bean definitions

**Correct Answer:** 1
**Explanation:** Without `@Primary` or qualifiers, Spring throws an exception due to ambiguous bean matching. `@Primary` can override this behavior to prioritize a specific bean.

---

#### **Question 5: Dependency Injection**

**Which injection method is recommended for mandatory dependencies in Spring?**

1. Setter injection
2. Field injection with `@Autowired`
3. Constructor injection
4. Method injection via `@Bean`

**Correct Answer:** 3
**Explanation:** Constructor injection ensures immutability, avoids `NullPointerExceptions`, and makes dependencies explicit. It’s the recommended approach for required dependencies.

---

#### **Question 6: Circular Dependencies**

**How does Spring handle circular dependencies when using constructor injection?**

1. Automatically resolves them via proxy objects
2. Throws a `BeanCurrentlyInCreationException`
3. Uses lazy initialization by default
4. Ignores the circular reference

**Correct Answer:** 2
**Explanation:** Constructor injection cannot resolve circular dependencies because beans must be fully initialized before injection. Spring detects this and throws an exception.

---

#### **Question 7: @Qualifier vs @Primary**

**When should `@Qualifier` be used instead of `@Primary`?**

1. To prioritize a bean for autowiring
2. To resolve ambiguity between multiple beans of the same type
3. To enable lazy initialization
4. To mark a bean as optional

**Correct Answer:** 2
**Explanation:** `@Qualifier` explicitly selects a bean by name or custom qualifier, while `@Primary` designates a default candidate. Use `@Qualifier` when multiple beans exist and no default is appropriate.

---

#### **Question 8: Conditional Bean Registration**

**Which annotation enables bean registration only if a specific property is set in `application.properties`?**

1. `@ConditionalOnProperty`
2. `@Profile`
3. `@DependsOn`
4. `@Lazy`

**Correct Answer:** 1
**Explanation:** `@ConditionalOnProperty(name = "my.property", havingValue = "true")` registers the bean only if the property matches. `@Profile` activates beans based on environment profiles.

---

#### **Question 9: Bean Scope**

**What is the default scope of a bean declared with `@Bean` in a `@Configuration` class?**

1. Prototype
2. Request
3. Singleton
4. Session

**Correct Answer:** 3
**Explanation:** By default, Spring beans are singletons. The container creates a single instance per Spring IoC container.

---

#### **Question 10: Expression Language**

**Which SpEL expression injects a system property into a field?**

```java  
@Value("___")  
private String javaVersion;  
```

1. `#{systemProperties['java.version']}`
2. `${java.version}`
3. `@systemProperties['java.version']`
4. `&amp;{java.version}`

**Correct Answer:** 2
**Explanation:** `${}` is used for property placeholders, while `#{}` evaluates SpEL expressions. Here, `${java.version}` injects the value of the `java.version` system property.

---

### Summary

This test evaluates advanced knowledge of Spring Framework architecture, Java configuration, and dependency management—key areas for the Spring Professional certification. Focus on understanding bean lifecycle management, annotation-driven configuration, and resolving complex dependency scenarios.

