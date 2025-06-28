# AutheticUser - API de Autenticação com JWT

Este projeto foi desenvolvido com **Spring Boot** e oferece autenticação baseada em **JWT (JSON Web Token)**. Abaixo você encontrará instruções para rodar a aplicação, acessar ferramentas úteis e realizar testes de carga.

---

## ✅ Pré-requisitos

Certifique-se de que os seguintes requisitos estão instalados na sua máquina:

- Java 11 ou superior
- Maven
- JMeter (para testes de carga)

---

## 🚀 Executando a Aplicação

1. **Clone o repositório:**

```bash
git clone https://github.com/seuusuario/autheticuser.git
cd autheticuser
```

2. **Compile o projeto com Maven:**

```bash
mvn clean install
```

3. **Execute a aplicação:**

```bash
mvn spring-boot:run
```

A aplicação estará disponível em:  
👉 `http://localhost:8080`

---

## 📄 Documentação da API (Swagger)

A documentação interativa da API está disponível em:  
👉 `http://localhost:8080/swagger-ui/index.html#/Autenticação/login`

### Testando o login via Swagger:

- Endpoint: `POST /auth/login`
- Corpo da requisição:

```json
{
  "username": "admin",
  "password": "123456"
}
```

---

## 🗃️ Acessando o Console do H2

Você pode acessar o console do banco H2 em:  
👉 `http://localhost:8080/h2-console`

### Credenciais:

- **JDBC URL:** `jdbc:h2:mem:testdb`
- **Usuário:** `sa`
- **Senha:** *(deixe em branco)*

---

## 🧪 Testes de Carga com JMeter

### Etapas:

1. **Criar novo plano de teste:**
   - `File > New`

2. **Adicionar Thread Group:**
   - Clique com o botão direito em Test Plan > `Add > Threads (Users) > Thread Group`
   - Configurações:
     - **Number of Threads (users):** 200
     - **Ramp-up period (seconds):** 20
     - **Loop Count:** 10 *(ou marque "Forever" para execução contínua)*

3. **Adicionar requisição HTTP:**
   - Clique com o botão direito no Thread Group > `Add > Sampler > HTTP Request`
   - Parâmetros:
     - **Name:** Login Request
     - **Protocol:** http
     - **Server Name or IP:** localhost
     - **Port Number:** 8080
     - **Method:** POST
     - **Path:** /auth/login
     - **Body Data:**

```json
{
  "username": "admin",
  "password": "123456"
}
```

4. **Adicionar Header HTTP:**
   - Clique com o botão direito em Login Request > `Add > Config Element > HTTP Header Manager`
   - Configure:
     - **Name:** `Content-Type`
     - **Value:** `application/json`

5. **Visualizar resultados:**
   - Clique com o botão direito em Thread Group > `Add > Listener > View Results Tree`

---

## 📫 Contato

Em caso de dúvidas ou sugestões, sinta-se à vontade para abrir uma issue ou pull request neste repositório.

---
