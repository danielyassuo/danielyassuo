# 👋 Hi, I'm Daniel Yassuo

### 💻 Software Engineering Student | Java Backend Developer

🎓 Software Engineering student at **UniFil**
☕ Focused on **Backend Development with Java & Spring Boot**
🚀 Building **REST APIs, backend applications and microservices**
📚 Continuously improving my knowledge in **Software Architecture, Testing and Backend Development**

---

## 🛠️ Tech Stack

### Backend

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square\&logo=openjdk\&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square\&logo=springboot\&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square\&logo=springsecurity\&logoColor=white)
![Hibernate](https://img.shields.io/badge/JPA%20%2F%20Hibernate-59666C?style=flat-square\&logo=hibernate\&logoColor=white)

### Databases

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square\&logo=postgresql\&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square\&logo=mysql\&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square\&logo=mongodb\&logoColor=white)

**Relational:** PostgreSQL · MySQL
**NoSQL:** MongoDB

### Testing

![JUnit](https://img.shields.io/badge/JUnit-25A162?style=flat-square\&logo=junit5\&logoColor=white)
![Mockito](https://img.shields.io/badge/Mockito-78C257?style=flat-square\&logo=mockito\&logoColor=white)

**Unit Testing · JUnit · Mockito**

---

## 💡 What I Work With

* ☕ **Java & Spring Boot**
* 🌐 **RESTful APIs**
* 🔐 **Spring Security & JWT**
* 🗃️ **JPA / Hibernate**
* 🐘 **PostgreSQL & MySQL**
* 🍃 **MongoDB**
* 🧪 **JUnit & Mockito**
* 🐳 **Docker & Docker Compose**
* 📖 **Swagger / OpenAPI**
* 🔄 **Git & GitHub**

---

## 🤝 Methodologies & Practices

* **Agile Methodologies**
* **Scrum**
* **Kanban**
* **Clean Code**
* **Software Development Best Practices**

🏅 **Certificate:** Agile Methodologies — Javanauta

---

## 🌎 Languages

* 🇧🇷 **Portuguese** — Native
* 🇺🇸 **English** — Intermediate

---

## 📚 Currently Learning

* Microservices Architecture
* Hexagonal Architecture
* Automated Testing
* Software Design & Best Practices
* Clean Code

---

## 📂 Projects

#Portuguese : 
# API de Gestão de Usuários

API REST para cadastro, autenticação e gerenciamento de usuários, desenvolvida em **Java com Spring Boot**.

## 🚀 Tecnologias

- Java + Spring Boot
- Spring Security + JWT (autenticação/autorização)
- Spring Data JPA / Hibernate
- PostgreSQL
- MapStruct (conversão entre DTOs e entidades)
- OpenFeign (integração com API externa ViaCEP para preenchimento de endereço)
- Springdoc OpenAPI (Swagger) para documentação dos endpoints
- Docker / Docker Compose

## ✅ Testes

Cobertura de testes unitários em todas as camadas principais da aplicação:

- **Converters** (`UsuarioConverter`, `UsuarioMapper`, `UsuarioUpdateMapper`)
- **Service** (`UsuarioService`)
- **Controller** (`UsuarioController`)

> Desenvolvedor certificado em Testes Unitários.

## 🔧 Como executar

```bash
git clone https://github.com/danielyassuo/usuarios.git
cd usuarios
docker-compose up -d
./gradlew bootRun
```

A documentação dos endpoints fica disponível via Swagger UI após subir a aplicação.


# API Agendador de Tarefas

API REST responsável pelo agendamento e gerenciamento de tarefas dos usuários, desenvolvida em **Java com Spring Boot**.

## 🚀 Tecnologias

- Java + Spring Boot
- Spring Security + JWT (autenticação/autorização)
- Spring Data MongoDB
- MapStruct (conversão entre DTOs e entidades)
- OpenFeign (integração com outros microsserviços, como o sistema de notificações)
- Docker

## 🔗 Integração

Este serviço faz parte de um ecossistema de microsserviços que inclui:

- [API de Gestão de Usuários](https://github.com/danielyassuo/usuarios)
- [Sistema de Notificação](https://github.com/danielyassuo/sistema-notificacao)
- [BFF do Agendador de Tarefas](https://github.com/danielyassuo/bff-agendador-tarefas) (consome esta API)

## 🔧 Como executar

```bash
git clone https://github.com/danielyassuo/agendador-tarefas.git
cd agendador-tarefas
docker build -t agendador-tarefas .
./gradlew bootRun
```
# Sistema de Notificação

Serviço responsável pelo envio de notificações por **e-mail** aos usuários que agendam tarefas, desenvolvido em **Java com Spring Boot**.

## 🚀 Tecnologias

- Java + Spring Boot
- Spring Boot Starter Mail (envio de e-mails)
- Thymeleaf (templates de e-mail)
- Docker

## 🔗 Integração

Este serviço faz parte de um ecossistema de microsserviços responsável por notificar o usuário sempre que uma tarefa é agendada no [Agendador de Tarefas](https://github.com/danielyassuo/agendador-tarefas), sendo consumido pelo [BFF do Agendador de Tarefas](https://github.com/danielyassuo/bff-agendador-tarefas).

## 🔧 Como executar

```bash
git clone https://github.com/danielyassuo/sistema-notificacao.git
cd sistema-notificacao
docker build -t sistema-notificacao .
./gradlew bootRun
```
# BFF - Agendador de Tarefas

**Back-End For Front-End** que unifica e orquestra as APIs do ecossistema Agendador de Tarefas, desenvolvido em **Java com Spring Boot**.

## 🧩 Sobre o projeto

Através do **OpenFeign / FeignClient**, este BFF consome as demais APIs do ecossistema:

- [API de Gestão de Usuários](https://github.com/danielyassuo/usuarios)
- [API Agendador de Tarefas](https://github.com/danielyassuo/agendador-tarefas)
- [Sistema de Notificação](https://github.com/danielyassuo/sistema-notificacao)

Ele centraliza o fluxo de:

- Cadastro e login de usuário com **autenticação JWT**
- Agendamento e exclusão de tarefas

## 🚀 Tecnologias e boas práticas

- Java + Spring Boot
- OpenFeign / FeignClient (comunicação entre microsserviços)
- Spring Security + JWT
- Lombok
- Springdoc OpenAPI (Swagger) para documentação dos endpoints
- Clean Code
- SonarQube (análise estática, vulnerabilidades e code smells)
- Docker / Docker Compose
- CI/CD com GitHub Actions

## 🔧 Como executar

```bash
git clone https://github.com/danielyassuo/bff-agendador-tarefas.git
cd bff-agendador-tarefas
docker-compose up -d
./mvnw spring-boot:run
```

> Para o fluxo completo funcionar, os serviços de Usuários, Agendador de Tarefas e Notificação também precisam estar em execução.

#English : 

# User Management API

REST API for user registration, authentication and management, built with **Java and Spring Boot**.

## 🚀 Tech Stack

- Java + Spring Boot
- Spring Security + JWT (authentication/authorization)
- Spring Data JPA / Hibernate
- PostgreSQL
- MapStruct (DTO ↔ entity mapping)
- OpenFeign (integration with the external ViaCEP API for address lookup)
- Springdoc OpenAPI (Swagger) for endpoint documentation
- Docker / Docker Compose

## ✅ Tests

Unit test coverage across the main application layers:

- **Converters** (`UsuarioConverter`, `UsuarioMapper`, `UsuarioUpdateMapper`)
- **Service** (`UsuarioService`)
- **Controller** (`UsuarioController`)

> Certified in Unit Testing.

## 🔧 How to run

```bash
git clone https://github.com/danielyassuo/usuarios.git
cd usuarios
docker-compose up -d
./gradlew bootRun
```

Endpoint documentation is available via Swagger UI once the application is up.

# Task Scheduler API

REST API responsible for scheduling and managing users' tasks, built with **Java and Spring Boot**.

## 🚀 Tech Stack

- Java + Spring Boot
- Spring Security + JWT (authentication/authorization)
- Spring Data MongoDB
- MapStruct (DTO ↔ entity mapping)
- OpenFeign (integration with other microservices, such as the notification system)
- Docker

## 🔗 Integration

This service is part of a microservices ecosystem that includes:

- [User Management API](https://github.com/danielyassuo/usuarios)
- [Notification System](https://github.com/danielyassuo/sistema-notificacao)
- [Task Scheduler BFF](https://github.com/danielyassuo/bff-agendador-tarefas) (consumes this API)

## 🔧 How to run

```bash
git clone https://github.com/danielyassuo/agendador-tarefas.git
cd agendador-tarefas
docker build -t agendador-tarefas .
./gradlew bootRun
```

# Notification System

Service responsible for sending **email** notifications to users who schedule tasks, built with **Java and Spring Boot**.

## 🚀 Tech Stack

- Java + Spring Boot
- Spring Boot Starter Mail (email sending)
- Thymeleaf (email templates)
- Docker

## 🔗 Integration

This service is part of a microservices ecosystem, responsible for notifying the user whenever a task is scheduled in the [Task Scheduler](https://github.com/danielyassuo/agendador-tarefas), and is consumed by the [Task Scheduler BFF](https://github.com/danielyassuo/bff-agendador-tarefas).

## 🔧 How to run

```bash
git clone https://github.com/danielyassuo/sistema-notificacao.git
cd sistema-notificacao
docker build -t sistema-notificacao .
./gradlew bootRun
```

# Task Scheduler BFF

**Back-End For Front-End** that unifies and orchestrates the APIs of the Task Scheduler ecosystem, built with **Java and Spring Boot**.

## 🧩 About the project

Using **OpenFeign / FeignClient**, this BFF consumes the other APIs in the ecosystem:

- [User Management API](https://github.com/danielyassuo/usuarios)
- [Task Scheduler API](https://github.com/danielyassuo/agendador-tarefas)
- [Notification System](https://github.com/danielyassuo/sistema-notificacao)

It centralizes the flow of:

- User registration and login with **JWT authentication**
- Scheduling and deleting tasks

## 🚀 Tech Stack & Best Practices

- Java + Spring Boot
- OpenFeign / FeignClient (service-to-service communication)
- Spring Security + JWT
- Lombok
- Springdoc OpenAPI (Swagger) for endpoint documentation
- Clean Code
- SonarQube (static analysis, vulnerability and code smell checks)
- Docker / Docker Compose
- CI/CD with GitHub Actions

## 🔧 How to run

```bash
git clone https://github.com/danielyassuo/bff-agendador-tarefas.git
cd bff-agendador-tarefas
docker-compose up -d
./mvnw spring-boot:run
```

> For the full flow to work, the User Management, Task Scheduler, and Notification services also need to be running.


## 👤 Autor

**Daniel Yassuo da Rocha Rodrigues**
Desenvolvedor Backend Java | Spring Boot
[LinkedIn](https://linkedin.com/in/danielYassuo) · [GitHub](https://github.com/danielyassuo)

---

## 📫 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square\&logo=linkedin\&logoColor=white)](https://linkedin.com/in/danielYassuo)

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square\&logo=github\&logoColor=white)](https://github.com/danielyassuo)

