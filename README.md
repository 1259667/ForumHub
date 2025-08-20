# ForumHub 🗨️

Um projeto de fórum desenvolvido em **Java com Spring Boot**, inspirado em plataformas de discussão como o Fórum da Alura.  
O objetivo é fornecer uma API REST para cadastro, listagem, atualização e exclusão de tópicos, com autenticação e autorização via **Spring Security**.

---

## 🚀 Tecnologias Utilizadas

- **Java 17**
- **Spring Boot 3**
  - Spring Web
  - Spring Data JPA
  - Spring Security
  - Validation
- **Banco de Dados MySQL**
- **Maven**
- **Lombok**
- **Postman** (para testes de API)

---

## 📂 Estrutura do Projeto

src/main/java/com/example/forumhub
├── api/dto/topic # DTOs para entrada e saída de dados
├── controller # Controllers (endpoints REST)
├── domain/topic # Entidade e regras de negócio
├── repository # Interfaces JPA para acesso ao banco
└── security # Configurações do Spring Security

yaml
Copiar
Editar

---

## 📑 Endpoints da API

### 🔐 Autenticação
- `POST /login` → autentica o usuário e retorna **JWT**

### 📝 Tópicos
- `POST /topicos` → cria um novo tópico  
- `GET /topicos` → lista tópicos com paginação  
- `GET /topicos/{id}` → detalha um tópico específico  
- `PUT /topicos/{id}` → atualiza informações de um tópico  
- `DELETE /topicos/{id}` → remove um tópico  

---

## 🛠️ Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/forumhub.git
Acesse a pasta do projeto:

bash
Copiar
Editar
cd forumhub
Configure o banco de dados MySQL no application.properties:

properties
Copiar
Editar
spring.datasource.url=jdbc:mysql://localhost/forumhub
spring.datasource.username=seuUsuario
spring.datasource.password=suaSenha
Rode a aplicação:

bash
Copiar
Editar
mvn spring-boot:run
A API estará disponível em:
👉 http://localhost:8080

🔒 Segurança
A autenticação é feita via JWT Token.

Após o login, inclua no Postman/Insomnia o header:

makefile
Copiar
Editar
Authorization: Bearer SEU_TOKEN_AQUI
📚 Próximos Passos
Implementar testes unitários e de integração.

Documentar a API com Swagger/OpenAPI.

Adicionar perfis de ambiente (dev/test/prod).

