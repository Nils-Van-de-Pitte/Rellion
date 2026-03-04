# Rellion

> A next-generation Object-Relational Mapping engine for Java.

Rellion is an ambitious, performance-oriented ORM framework built entirely in pure Java.
It aims to redefine how applications interact with relational databases by combining clarity, architectural rigor, and predictable data access patterns into a cohesive data engine.

Rellion is framework-agnostic by design. It does not depend on Spring or any external container. It is built as a standalone infrastructure library that can integrate into any Java-based system.

---

## ✨ Vision

Rellion is designed as more than just a persistence layer.
It is a data mapping engine built to:

* Provide expressive and intuitive entity modeling
* Generate predictable and efficient SQL
* Preserve architectural transparency
* Minimize configuration
* Encourage clarity over hidden magic

Rellion focuses on making performance and correctness first-class concerns, not afterthoughts.

---

## 🧠 Philosophy

Rellion follows a few core principles:

### 1. Performance by Design

Efficient query generation and intelligent data loading are part of the core architecture.

### 2. Explicit over Implicit

Developers should understand what the ORM is doing. SQL generation and relationship handling should be predictable.

### 3. Minimal Magic

No hidden framework lifecycle. No container dependency. Just clean Java and explicit configuration.

### 4. Framework-Agnostic

Rellion works in:

* Plain Java applications
* Spring-based systems
* Micronaut / Quarkus environments
* CLI tools
* Microservices

---

## 🏗 Architecture Overview

Rellion is structured into modular components:

* **Entity Mapping Layer**
  Maps annotated Java classes to relational tables.

* **Session / Context Manager**
  Manages database connections and entity lifecycle.

* **Query Engine**
  Generates SQL dynamically based on entity metadata.

* **Hydration Engine**
  Converts result sets into fully constructed object graphs.

* **Relationship Resolver**
  Handles one-to-many and many-to-one associations efficiently.

---

## 🚀 Example Usage (Conceptual)

```java
Rellion Rellion = Rellion.builder()
    .dataSource(dataSource)
    .build();

User user = Rellion.find(User.class, 1L);

List<User> users = Rellion.query(User.class)
    .where("age > ?", 18)
    .fetch();
```

Rellion focuses on providing a clean and expressive API while maintaining control over how data is fetched and mapped.

---

## 📦 Technology Stack

* Java 21+
* JDBC
* Reflection & Annotations
* JUnit (testing)
* H2 / PostgreSQL (development & integration testing)

Rellion does not depend on Spring or any other framework.

---

## 🛣 Roadmap

### Phase 1 — Core Engine

* Entity annotations
* Basic CRUD operations
* Metadata extraction via reflection
* Simple SQL generation
* ResultSet hydration

### Phase 2 — Relationships

* One-to-many
* Many-to-one
* Join resolution
* Batch fetching strategies

### Phase 3 — Advanced Features

* Query builder API
* Transaction management
* Lazy loading
* Identity map / session caching

### Phase 4 — Ecosystem

* Documentation
* Benchmarking suite
* Framework integrations
* Potential multi-language exploration

---

## 🎯 Goals

Rellion is built as a serious engineering project to explore:

* Database internals
* Query optimization
* Design patterns (Unit of Work, Data Mapper, Identity Map)
* Systems-level Java development
* Infrastructure library design

---

Rellion is not just about mapping objects to tables.
It is about building a reliable, transparent, and scalable foundation for modern Java applications.
