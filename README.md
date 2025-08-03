# Workshop Spring Boot 3 com JPA

Projeto de estudo para aprender e demonstrar o uso de **Spring Boot 3**, **JPA** e **Hibernate** na criação de uma **API RESTful** para gerenciamento de entidades como pedidos e produtos.

## 🚀 Visão Geral

Este workshop apresenta um sistema básico com as seguintes características:

- Entidades JPA representando pedidos, produtos etc.
- Spring Data JPA para persistência de dados.
- Perfis de execução configuráveis (ex.: `dev`, `prod`).
- Tratamento de exceções personalizadas para APIs REST.
- Rastreamento de datas/timestamps para auditoria de criação e atualização.
- Relacionamentos entre entidades (ex.: pedidos contendo vários produtos).

## 🧪 Tecnologias Utilizadas

- Java 17+
- Spring Boot 3
- Spring Data JPA + Hibernate
- Banco de dados relacional (H2, PostgreSQL ou MySQL)
- Maven como gerenciador de dependências e build

## 📁 Estrutura do Projeto

```
├── src
│   ├── main
│   │   ├── java/...        // pacotes com entidades, repositórios, controladores, serviços
│   │   └── resources       // application.yml/properties, scripts SQL, data.sql, etc.
├── pom.xml
├── mvnw, mvnw.cmd          // wrapper Maven
└── .gitignore
```

## 🔧 Como Executar o Projeto Localmente

1. Clone o repositório:

```bash
git clone https://github.com/sebastiao25759/workshop-springboot3-jpa.git
cd workshop-springboot3-jpa
```

2. Configure o perfil de execução, se necessário (por exemplo, em `application-dev.yml` ou `application-prod.yml`).

3. Execute via Maven wrapper:

```bash
./mvnw spring-boot:run
```

4. Acesse os endpoints REST usando `http://localhost:8080` (ou a porta configurada).

## 🧩 Endpoints de Exemplo

```
GET    /orders              - lista todos os pedidos  
GET    /orders/{id}         - obtém pedido por ID  
POST   /orders              - cria um novo pedido  
PUT    /orders/{id}         - atualiza um pedido existente  
DELETE /orders/{id}         - exclui um pedido  

GET    /products            - lista todos os produtos  
... e demais endpoints para produtos
```

## 🎯 Funcionalidades Principais

- CRUD completo para entidades como `Order`, `Product`.
- Relações configuradas com anotações JPA (`@OneToMany`, `@ManyToOne`, etc.).
- Versionamento de dados usando timestamps (`createdAt`, `updatedAt`).
- Exceções tratadas via controlador global com respostas padronizadas.

## 🛠️ Dependências & Build

- Spring Boot Starter Web  
- Spring Boot Starter Data JPA  
- Driver do banco de dados (H2, PostgreSQL, MySQL)  
- Lombok (caso utilizado)  

Para empacotar o projeto:

```bash
./mvnw clean package
```

## ✅ Como Contribuir

1. Faça um fork do repositório.
2. Crie uma branch com a feature ou correção:

```bash
git checkout -b feature/nome-da-feature
```

3. Compartilhe suas mudanças via pull request.

## 📄 Licença

Distribuído sob a **Licença MIT**. Consulte o arquivo [`LICENSE`](LICENSE) para mais informações.

## 🧠 Recursos Adicionais

- [Documentação Oficial do Spring Data JPA](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/)
- [Guia: Accessing Data with JPA – Spring.io](https://spring.io/guides/gs/accessing-data-jpa/)
