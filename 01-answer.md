<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

### Spring Professional Certification Practice Test

**Topics:** Spring Framework Introduction, Java Configuration, Dependency Management

---

#### **1. Spring Architecture**

What architectural pattern does Spring Framework primarily follow?
A) Model-View-Controller (MVC)
B) Dependency Injection (DI) / Inversion of Control (IoC)
C) Microservices
D) Service-Oriented Architecture (SOA)

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** Spring is built around the Dependency Injection (DI) and Inversion of Control (IoC) pattern, where objects receive dependencies from an external source (the Spring IoC container) rather than creating them internally.
</details>

---

#### **2. Core Spring Modules**

Which module provides the fundamental **BeanFactory** implementation?
A) `spring-core`
B) `spring-beans`
C) `spring-context`
D) `spring-expression`

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** The `spring-beans` module contains the `BeanFactory` implementation, which manages bean instantiation, configuration, and lifecycle.
</details>

---

#### **3. Java Configuration**

What is the purpose of the `@Bean` annotation in a `@Configuration` class?
A) To mark a class as a Spring component
B) To define a bean in the Spring IoC container
C) To enable component scanning
D) To inject dependencies into a field

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** `@Bean` annotates methods in a `@Configuration` class to register their return values as beans in the Spring container.
</details>

---

#### **4. @ComponentScan**

What happens if `@ComponentScan` is applied without specifying a base package?
A) Scans all packages in the classpath
B) Scans the package of the `@Configuration` class
C) Disables component scanning
D) Throws an error

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** By default, `@ComponentScan` scans the package of the class where it is declared and its subpackages.
</details>

---

#### **5. Dependency Injection**

Which injection method ensures immutability for mandatory dependencies?
A) Setter injection
B) Field injection
C) Constructor injection
D) Method injection

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** C
**Explanation:** Constructor injection allows dependencies to be declared as `final`, ensuring immutability and avoiding `NullPointerExceptions`.
</details>

---

#### **6. @Autowired Behavior**

What happens if multiple beans of the same type exist and `@Autowired` is used without `@Qualifier`?
A) Spring selects the `@Primary` bean
B) Throws `NoUniqueBeanDefinitionException`
C) Injects all beans as a collection
D) Uses the bean with the name matching the field

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** Without `@Qualifier` or `@Primary`, Spring cannot resolve ambiguity between multiple beans of the same type and throws an exception.
</details>

---

#### **7. @Qualifier Usage**

When is `@Qualifier` necessary?
A) To mark a bean as optional
B) To resolve conflicts between beans of the same type
C) To enable lazy initialization
D) To define a bean’s scope

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** `@Qualifier` explicitly identifies a bean by name or custom qualifier when multiple candidates exist.
</details>

---

#### **8. Circular Dependencies**

How does Spring handle circular dependencies with constructor injection?
A) Uses proxy objects
B) Throws `BeanCurrentlyInCreationException`
C) Automatically resolves them
D) Ignores the dependency

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** Constructor injection requires dependencies to be fully initialized upfront, making circular dependencies unresolvable and resulting in an exception.
</details>

---

#### **9. SpEL (Spring Expression Language)**

Which expression injects a system property into a field using `@Value`?
A) `#{systemProperties['java.version']}`
B) `${java.version}`
C) `@systemProperties['java.version']`
D) `&amp;{java.version}`

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** `${}` is used for property placeholders, while `#{}` evaluates SpEL expressions. `java.version` is a system property.
</details>

---

#### **10. Bean Scope**

What is the default scope of a Spring bean?
A) Prototype
B) Singleton
C) Request
D) Session

<details>
<summary>Answer \& Explanation</summary>

**Correct Answer:** B
**Explanation:** By default, Spring beans are singletons, meaning one instance per IoC container.
</details>

---

**Format Note:** Copy-paste this Markdown into any editor supporting collapsible sections (e.g., Obsidian, VS Code) to view explanations.

