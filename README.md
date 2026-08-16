<div align="center">

# 🗂️ Sistema de Gerenciamento de Usuários

### Aplicação desktop desenvolvida em Java para autenticação e gerenciamento de usuários

**Projeto acadêmico | Análise e Desenvolvimento de Sistemas (ADS) | 2026**

</div>

---

## 📌 Sobre o projeto

O **Sistema de Gerenciamento de Usuários** é uma aplicação desktop desenvolvida em **Java**, utilizando **Java Swing** para a construção das telas e **Apache NetBeans** como ambiente de desenvolvimento.

O projeto foi criado com finalidade acadêmica para aplicar conhecimentos de programação, desenvolvimento de interfaces gráficas, conexão com banco de dados e operações de CRUD.

A aplicação possui uma tela de login para autenticação e um menu principal que permite acessar as funcionalidades de gerenciamento de usuários.

O sistema foi desenvolvido para funcionar com um banco de dados **MySQL local**, utilizando conexão JDBC.

---

## 🎯 Objetivo

Desenvolver um sistema funcional de gerenciamento de usuários, aplicando na prática conceitos de desenvolvimento desktop e persistência de dados.

A proposta do projeto é oferecer:

- Validação do acesso de usuários por meio de login;
- Cadastro de novos usuários;
- Consulta de usuários cadastrados;
- Alteração de informações existentes;
- Exclusão de usuários;
- Organização das operações em uma interface gráfica simples;
- Armazenamento dos dados em um banco MySQL local.

O projeto também representa uma etapa importante de aprendizado sobre a integração entre uma interface desenvolvida em Java e um banco de dados relacional.

---

## 🔐 Tela de login

O sistema começa pela tela de login, na qual o usuário informa:

- **UserID:** código de identificação cadastrado no banco;
- **Senha:** senha correspondente ao usuário.

Após clicar em **OK**, o sistema consulta a tabela `usuarios` no MySQL local. Quando os dados estão corretos, o acesso é liberado e o usuário é encaminhado para o menu principal.

A tela também possui as opções:

- **Limpar:** apaga os dados preenchidos nos campos;
- **Fim:** encerra a aplicação;
- **OK:** valida o login e abre o sistema.

---

## 🧩 Funcionalidades

### Menu principal

O menu principal organiza o acesso às operações disponíveis no sistema.

### Cadastro de usuários

Permite inserir novos usuários no banco de dados, armazenando as informações necessárias para o acesso ao sistema.

### Consulta de usuários

Permite localizar e visualizar informações de usuários cadastrados.

### Alteração de usuários

Permite modificar dados de um usuário existente.

### Exclusão de usuários

Permite remover um usuário cadastrado no banco de dados.

---

## 🗄️ Banco de dados MySQL

O sistema utiliza o **MySQL** para armazenar os dados dos usuários e realizar as operações de cadastro, consulta, alteração, exclusão e autenticação.

A comunicação entre o Java e o MySQL é feita por meio do **JDBC**, utilizando o driver **MySQL Connector/J**.

A conexão utilizada no projeto aponta para um banco local:

```java
jdbc:mysql://localhost:3306/sistema_usuarios
```

Isso significa que a aplicação procura o banco no próprio computador em que está sendo executada.

### Importante

O projeto **não utiliza banco remoto** e não disponibiliza acesso ao banco da autora. Cada pessoa que quiser executar o sistema deverá configurar seu próprio ambiente local.

Para executar o projeto, será necessário:

1. Instalar o MySQL Server;
2. Iniciar o serviço do MySQL;
3. Criar um banco chamado `sistema_usuarios`;
4. Criar a tabela `usuarios`;
5. Criar os demais objetos necessários para as operações do CRUD;
6. Cadastrar pelo menos um usuário na tabela de login;
7. Configurar o MySQL Connector/J no projeto;
8. Ajustar as credenciais da conexão caso sejam diferentes da instalação local.

Os dados utilizados no desenvolvimento são fictícios e foram criados exclusivamente para testes acadêmicos.

---

## 💻 Tecnologias utilizadas

- **Java** — linguagem de programação;
- **Java Swing** — criação das interfaces gráficas;
- **Apache NetBeans** — IDE e ferramenta de construção visual das telas;
- **JDBC** — comunicação entre a aplicação e o banco;
- **MySQL** — banco de dados relacional;
- **MySQL Connector/J** — driver JDBC;
- **Git** — controle de versão;
- **GitHub** — hospedagem do código-fonte.

---

## 📁 Estrutura do projeto

```text
STO_E01/
├── src/
│   ├── FrameLogin.java
│   ├── FrameLogin.form
│   ├── FrameMenu.java
│   ├── FrameMenu.form
│   ├── FrameIncluir.java
│   ├── FrameIncluir.form
│   ├── FrameConsultar.java
│   ├── FrameConsultar.form
│   ├── FrameAlterar.java
│   ├── FrameAlterar.form
│   ├── FrameExcluir.java
│   ├── FrameExcluir.form
│   └── imagens da interface
├── nbproject/
├── build.xml
├── manifest.mf
├── .gitignore
└── README.md
```

Os arquivos `.java` contêm a lógica das telas, enquanto os arquivos `.form` armazenam as informações visuais utilizadas pelo GUI Builder do NetBeans.

---

## ▶️ Como executar o projeto

1. Instale o **Java JDK**.
2. Instale o **Apache NetBeans**.
3. Instale o **MySQL Server**.
4. Instale ou adicione o **MySQL Connector/J** ao projeto.
5. Crie o banco de dados `sistema_usuarios`.
6. Crie as tabelas necessárias para o login e para o CRUD.
7. Cadastre um usuário no banco de dados.
8. Clone este repositório:

```bash
git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
```

9. Abra o projeto `STO_E01` no NetBeans.
10. Verifique as configurações da conexão com o MySQL.
11. Execute a classe `FrameLogin`.
12. Informe o código e a senha de um usuário cadastrado no seu banco local.

---

## 🧪 Testes realizados

Durante o desenvolvimento, foram realizados testes locais para verificar:

- A abertura correta da tela de login;
- A validação de usuário existente;
- A validação de senha;
- O bloqueio de usuários inexistentes;
- A abertura do menu após o login;
- O cadastro de novos usuários;
- A consulta de registros;
- A alteração de informações;
- A exclusão de usuários;
- A comunicação entre a aplicação Java e o MySQL.

Todos os dados utilizados nos testes são fictícios e não representam usuários reais.

---

## 📚 Aprendizados

O desenvolvimento deste projeto permitiu praticar diferentes etapas da construção de uma aplicação desktop.

Entre os principais aprendizados estão:

- Criação de interfaces com Java Swing;
- Uso do GUI Builder do NetBeans;
- Organização de telas por meio de `JFrame`;
- Implementação de eventos de botões;
- Validação de campos de formulário;
- Criação de consultas SQL;
- Conexão Java com MySQL utilizando JDBC;
- Implementação de operações de CRUD;
- Controle de acesso por login;
- Organização de um projeto para publicação no GitHub.

O projeto reforçou a importância de integrar interface, lógica de programação e banco de dados para construir uma aplicação funcional.

---

## 🚀 Possíveis melhorias futuras

Algumas melhorias que podem ser implementadas em versões futuras são:

- Utilização de `PreparedStatement` nas consultas SQL;
- Criptografia ou hash das senhas;
- Criação de diferentes níveis de acesso;
- Validação mais completa dos campos;
- Separação da classe de conexão em um pacote próprio;
- Melhor organização dos pacotes Java;
- Inclusão de mensagens de erro mais específicas;
- Criação de um script SQL para facilitar a configuração do banco;
- Adição de testes automatizados;
- Desenvolvimento de uma versão web ou mobile.

---

## ⚠️ Observações

Este projeto foi desenvolvido para fins acadêmicos e de aprendizagem.

As credenciais presentes na conexão referem-se a um ambiente local utilizado durante o desenvolvimento. O projeto não oferece acesso a banco de dados remoto.

Para executar a aplicação, cada pessoa deve instalar e configurar seu próprio MySQL, criar o banco e cadastrar seus próprios usuários.

Não são utilizados dados reais de pessoas.

---

## 👩‍💻 Autoria

Projeto desenvolvido por:

### Carolina Yukari Kague

**Análise e Desenvolvimento de Sistemas (ADS)**  
**2026**

</div>
