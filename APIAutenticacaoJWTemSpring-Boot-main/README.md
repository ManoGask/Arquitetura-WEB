# 🚀 API de Autenticação e Autorização JWT (Spring Boot)

Esta API realiza autenticação e autorização com **JWT (JSON Web Tokens)**, gerando tokens para usuários autenticados e protegendo endpoints com validação interna. Ideal para aplicações RESTful seguras e escaláveis.

---

## ✅ Funcionalidades

- Login de usuários e emissão de tokens JWT.
- Validação de tokens e extração de claims.
- Proteção de endpoints com base em roles (ex: USER, ADMIN).
- Integração com Swagger (OpenAPI) para documentação.
- Banco H2 em memória para testes rápidos.
- Testes com JUnit e integração com JMeter.

---

## 🧰 Tecnologias e Dependências

- **Spring Boot 3.x**
- `spring-boot-starter-web`
- `spring-boot-starter-security`
- `spring-boot-starter-oauth2-resource-server`
- `spring-boot-starter-data-jpa`
- `h2database`
- `lombok`
- `springdoc-openapi-ui`
- `spring-boot-starter-test`
- `spring-boot-devtools`

---

## ⚙️ Executando o Projeto

```bash
# Clone o projeto
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio

# Compile e execute
./mvnw spring-boot:run

# Usuários para Testes

Administrador
username: admin  
password: 123456  
role: ADMIN
''
Usuário Comum
username: user  
password: password  
role: USER

