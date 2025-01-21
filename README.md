
<div align="center">

# ForumHub API
ForumHub é uma API RESTful desenvolvida com Spring Boot para gerenciar um fórum com postagens e usuários. Eficiente e segura, esta API oferece funcionalidades completas para autenticação, criação, listagem, atualização e exclusão de tópicos, com integrações ao Swagger para documentação interativa.

![licensa do repositorio](https://img.shields.io/badge/LICENSA-MIT-blue)
![status do projeto](https://img.shields.io/badge/STATUS-FINALIZADO-GREEN)
![estrelas do projeto](https://img.shields.io/github/stars/yo-melloo?style=social)

</div>

## 🚀 Tecnologias Utilizadas
- Java 17
- Spring Boot 3.0+
- Spring Security 
- Json Web Token
- Hibernate/JPA
- PostgreSQL
- Swagger/OpenAPI (documentação)
- Maven

## 📋 Funcionalidades
- **Postagens**
    - Criar Tópico: Cadastro de novas postagens no fórum.
    - Listar Tópicos:
    - Listagem paginada de todas as postagens.
    - Top 10 tópicos mais recentes.
    - Busca de tópicos por curso e ano.
    - Visualizar Tópico Específico: Detalhamento de uma postagem específica por ID.
    - Atualizar Tópico: Alteração de conteúdo de postagens existentes.
    - Excluir Tópico: Remoção definitiva de tópicos.
- **Usuários**
    - Autenticação:
    - Login com geração de token JWT.
    - Gerenciamento seguro de sessões.
## 🛠️ Uso da aplicação
### **Pré-requisitos**
- Java 17+
- Maven
- Banco de dados PostgreSQL configurado

---

1. Clone este repositório:

``` git
git clone https://github.com/yo-melloo/ForumHub-One-Challenge.git
cd forumhub-api
```

2. Configure o banco de dados no arquivo `application.properties`:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/forumhub
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

3. Compile o projeto:
`mvn clean install`

4. Execute a aplicação:
`mvn spring-boot:run`

5. Acesse a API:

- Base URL: http://localhost:8080
- Swagger UI: http://localhost:8080/swagger-ui.html

#### 🗂️ Endpoints Principais

---

- Postagem
`POST /topicos` - Cria um novo tópico.

`GET /topicos` - Lista todas as postagens (com paginação).

`GET /topicos/top10` - Retorna os 10 tópicos mais recentes.

`GET /topicos/buscar-ano-data` - Busca postagens por curso e ano.

`GET /topicos/{id}` - Busca uma postagem específica.

`PUT /topicos` - Atualiza uma postagem existente.

`DELETE /topicos/{id}` - Remove uma postagem.

- Usuários
`POST /login` - Autentica o usuário e obtem um token JWT.
## 🛡️ Observação de segurança
Esta API utiliza **Spring Security** com autenticação via **JWT (JSON Web Token)**. **Para acessar os endpoints protegidos, inclua o token no cabeçalho da requisição**:

`Authorization: Bearer <seu_token_jwt>`
## Autores

- [@yo-melloo](https://github.com/yo-melloo) - Autor
- README baseado no projeto de: [@AbinadabeDev](https://github.com/AbinadabeDev)
