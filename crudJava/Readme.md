# CRUD Java com Relacionamentos entre Entidades

## 📋 Sobre o Projeto
Este projeto demonstra uma aplicação web Java completa que implementa operações CRUD (Create, Read, Update, Delete) com relacionamentos entre entidades. A aplicação utiliza:

- Java EE/Jakarta EE para a camada backend
- JSF (JavaServer Faces) para a interface web
- JPA com Hibernate para persistência de dados
- Maven para gerenciamento de dependências

## 🏗️ Arquitetura e Estrutura
O projeto segue o padrão MVC (Model-View-Controller) organizado em quatro camadas principais:

1. **Camada de Modelo**: Contém as entidades que representam as tabelas do banco de dados
2. **Camada de Repositório**: Responsável pelas operações básicas de banco de dados
3. **Camada de Serviço**: Implementa a lógica de negócio e regras de validação
4. **Camada de Apresentação**: Interface web construída com JSF e XHTML

## 🔗 Relacionamentos Implementados
O projeto exemplifica dois tipos fundamentais de relacionamentos entre entidades:

### Relação Um-para-Muitos (One-to-Many)
- Implementado entre as entidades `Pessoa` e `Telefone`
- Uma Pessoa pode possuir múltiplos Telefones
- Cada Telefone pertence a uma única Pessoa
- Configurado com operações em cascata para manter a integridade dos dados

### Relação Muitos-para-Muitos (Many-to-Many)
- Implementado entre as entidades `Aluno` e `Curso`
- Um Aluno pode se matricular em vários Cursos
- Um Curso pode ter vários Alunos matriculados
- Utiliza uma tabela de junção para mapear o relacionamento

## 🚀 Funcionalidades Principais
- Cadastro, consulta, atualização e remoção de entidades
- Validação de dados na camada de serviço
- Navegação entre entidades relacionadas
- Interface intuitiva para gerenciamento dos relacionamentos
- Tratamento adequado de exceções e mensagens ao usuário

## 💻 Tecnologias Utilizadas
- **Backend**: Java EE 8, JPA 2.2, EJB 3.2
- **Frontend**: JSF 2.3, Facelets (XHTML), CSS básico
- **Banco de Dados**: Configurável (padrão com H2 embarcado)
- **Ferramentas**: Maven para build, JUnit para testes

## 📌 Pré-requisitos
Para executar o projeto localmente, você precisará de:

- JDK 11 ou superior
- Servidor de aplicação Java EE (TomEE, WildFly, GlassFish)
- Maven 3.6+
- IDE de desenvolvimento (recomendado)

## 🔧 Configuração e Execução
1. Clone o repositório
2. Configure as propriedades do banco de dados
3. Execute o build com Maven
4. Faça deploy no servidor de aplicação
5. Acesse a aplicação pelo navegador

O projeto está pronto para ser extendido com novas funcionalidades ou integrado a outros sistemas. A arquitetura limpa e a organização do código facilitam a manutenção e evolução da aplicação.
