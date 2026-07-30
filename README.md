# 💊 Farmácia API RESTful

<p align="center">

![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-OpenAPI-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)
![Render](https://img.shields.io/badge/Render-Deploy-46E3B7?style=for-the-badge&logo=render&logoColor=black)

</p>

---

# 📖 Sobre o Projeto

A **Farmácia API RESTful** é uma aplicação desenvolvida com **Java Spring Boot** para gerenciamento de uma rede de farmácias.

A API permite o gerenciamento completo de:

- 📦 Produtos
- 🗂️ Categorias
- 👤 Usuários
- 🔐 Autenticação de usuários

O projeto segue os princípios de uma arquitetura REST, utilizando Spring Boot, Spring Data JPA, Bean Validation e PostgreSQL para persistência dos dados.

---

# 🚀 Tecnologias Utilizadas

- Java 17+
- Spring Boot 3
- Spring Data JPA
- Spring Security
- Bean Validation
- PostgreSQL
- Swagger / OpenAPI 3
- Insomnia
- Git
- GitHub
- Render

---

# 🌐 Deploy

### API

https://projeto-final-bloco-02-8mz6.onrender.com

### Documentação Swagger

https://projeto-final-bloco-02-8mz6.onrender.com/swagger-ui/index.html

---

# 📂 Estrutura da API

## 📁 Categorias

| Método | Endpoint                  | Descrição                 |
| ------ | ------------------------- | ------------------------- |
| GET    | `/categorias`             | Lista todas as categorias |
| GET    | `/categorias/{id}`        | Busca categoria por ID    |
| GET    | `/categorias/tipo/{tipo}` | Busca categoria por tipo  |
| POST   | `/categorias`             | Cadastra uma categoria    |
| PUT    | `/categorias`             | Atualiza uma categoria    |
| DELETE | `/categorias/{id}`        | Remove uma categoria      |

---

## 📦 Produtos

| Método | Endpoint                        | Descrição                      |
| ------ | ------------------------------- | ------------------------------ |
| GET    | `/produtos`                     | Lista todos os produtos        |
| GET    | `/produtos/{id}`                | Busca produto por ID           |
| GET    | `/produtos/nome/{nome}`         | Busca produtos por nome        |
| GET    | `/produtos/preco_menor/{preco}` | Busca produtos com preço menor |
| GET    | `/produtos/preco_maior/{preco}` | Busca produtos com preço maior |
| POST   | `/produtos`                     | Cadastra um produto            |
| PUT    | `/produtos`                     | Atualiza um produto            |
| DELETE | `/produtos/{id}`                | Remove um produto              |

---

## 👤 Usuários

| Método | Endpoint              | Descrição               |
| ------ | --------------------- | ----------------------- |
| POST   | `/usuarios/cadastrar` | Cadastra um usuário     |
| POST   | `/usuarios/logar`     | Realiza login           |
| GET    | `/usuarios/all`       | Lista todos os usuários |
| GET    | `/usuarios/{id}`      | Busca usuário por ID    |
| PUT    | `/usuarios/atualizar` | Atualiza um usuário     |

---

# 📝 Exemplo de Requisição

## Cadastro de Produto

```json
{
  "nome": "Dipirona 500mg",
  "descricao": "Analgésico e antitérmico",
  "preco": 12.90,
  "quantidade": 100,
  "categoria": {
    "id": 1
  },
  "usuario": {
    "id": 1
  }
}
```

---

# 🛠️ Como Executar o Projeto

## 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
```

---

## 2. Entre na pasta

```bash
cd NOME-DO-REPOSITORIO
```

---

## 3. Configure o banco PostgreSQL

Crie um banco PostgreSQL e configure o arquivo:

```
src/main/resources/application.properties
```

Exemplo:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/farmacia
spring.datasource.username=postgres
spring.datasource.password=sua_senha

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## 4. Execute a aplicação

Pela IDE ou utilizando o Maven:

```bash
./mvnw spring-boot:run
```

ou

```bash
mvn spring-boot:run
```

---

## 5. Acesse

API

```
http://localhost:8080
```

Swagger

```
http://localhost:8080/swagger-ui/index.html
```

---

# 📚 Documentação

Toda a documentação da API está disponível através do Swagger.

Ela permite:

- visualizar todos os endpoints;
- testar requisições;
- visualizar modelos de dados;
- autenticar usuários.

---

# 🔒 Autenticação

Os endpoints protegidos utilizam autenticação de usuários.

Fluxo:

1. Cadastrar usuário;
2. Realizar login;
3. Utilizar o token retornado nas requisições autenticadas.

---

# 📁 Estrutura do Projeto

```
src
 ├── controller
 ├── model
 ├── repository
 ├── security
 ├── service
 ├── configuration
 └── FarmaciaApplication.java
```

---

# 📌 Ferramentas Utilizadas

- IntelliJ IDEA / Eclipse
- PostgreSQL
- Insomnia
- Swagger UI
- GitHub
- Render

---

# 👨‍💻 Autor

**Daniel Chaves**

GitHub:

https://github.com/DaniChaves10

---

# ⭐ Se este projeto foi útil...

Deixe uma ⭐ no repositório!

Isso ajuda bastante e incentiva novos projetos.