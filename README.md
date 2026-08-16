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

- **UserID:** código numérico de identificação cadastrado no banco;
- **Senha:** senha correspondente ao usuário.

Após clicar em **OK**, o sistema consulta a tabela `usuarios` no MySQL local, buscando a equivalência exata dos dados informados. Quando os dados estão corretos, o acesso é liberado, uma mensagem de sucesso é exibida e o usuário é encaminhado para a `TelaMenu`.

A tela também possui as opções:

- **Limpar:** apaga os dados preenchidos nos campos;
- **Fim:** encerra a aplicação;
- **OK:** valida o login e abre o sistema.

---

## 🧩 Funcionalidades

### Tela Menu

A `TelaMenu` organiza o acesso às operações disponíveis no sistema por meio de uma barra de menus superior contendo as guias **Usuário** — Consultar, Incluir, Alterar e Excluir — e **...** — Sair.

### Cadastro de usuários

A `TelaIncluir` permite inserir novos usuários no banco de dados. O formulário solicita:

- Nome completo;
- E-mail;
- Telefone;
- Senha.

O sistema conta com validações que exigem a confirmação exata da senha e garantem que o telefone contenha apenas números, limitado a 11 dígitos.

Após o cadastro bem-sucedido, o UserID é gerado automaticamente e exibido na tela para o usuário.

### Consulta de usuários

A `TelaConsultar` permite localizar as informações dos usuários cadastrados por meio de uma busca utilizando o UserID.

Os dados retornados — nome, e-mail, telefone e senha — são carregados automaticamente em campos bloqueados para edição.

### Alteração de usuários

A `TelaAlterar` busca o registro pelo UserID e habilita a modificação dos campos nome, e-mail, telefone e senha.

O campo de UserID possui um bloqueio de segurança estrutural, impedindo que o código identificador seja modificado. O formulário também valida se o número de telefone possui apenas caracteres numéricos antes de autorizar a atualização no banco de dados.

### Exclusão de usuários

A `TelaExcluir` localiza um cadastro pelo UserID e exibe seus dados para visualização.

Ao solicitar a exclusão, o sistema exibe uma caixa de diálogo exigindo a confirmação do usuário antes de remover o registro permanentemente do banco de dados.

---

## 🗄️ Banco de dados MySQL

O sistema utiliza o **MySQL** para armazenar os dados dos usuários e realizar as operações de cadastro, consulta, alteração, exclusão e autenticação.

A comunicação entre o Java e o MySQL é feita por meio do **JDBC**, utilizando o driver **MySQL Connector/J**.

A conexão utilizada no projeto aponta para um banco local com as seguintes configurações padrão definidas no código:

```java
jdbc:mysql://localhost:3306/sistema_usuarios

User: root
Password: 1234
```

### Importante

O projeto não utiliza banco remoto e não disponibiliza acesso ao banco da autora. Cada pessoa que quiser executar o sistema deverá configurar seu próprio ambiente local.

Para executar o projeto corretamente, será necessário:

1. Instalar o MySQL Server;
2. Iniciar o serviço do MySQL;
3. Criar um banco chamado `sistema_usuarios`;
4. Criar a tabela `usuarios`, contendo os campos correspondentes às consultas SQL:
   - `codigo` — chave primária e auto-incremento;
   - `nome`;
   - `email`;
   - `telefone`;
   - `senha`;
5. Cadastrar manualmente ou pelo banco pelo menos um usuário inicial para passar pela tela de login;
6. Configurar o MySQL Connector/J no projeto;
7. Ajustar as credenciais — `root` e `1234` — nas classes Java, caso a instalação local utilize outro usuário ou senha.

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
│   ├── TelaLogin.java
│   ├── TelaLogin.form
│   ├── TelaMenu.java
│   ├── TelaMenu.form
│   ├── TelaIncluir.java
│   ├── TelaIncluir.form
│   ├── TelaConsultar.java
│   ├── TelaConsultar.form
│   ├── TelaAlterar.java
│   ├── TelaAlterar.form
│   ├── TelaExcluir.java
│   ├── TelaExcluir.form
│   └── imagens utilizadas na interface
├── nbproject/
├── build.xml
├── manifest.mf
├── .gitignore
└── README.md
```

As telas do sistema foram desenvolvidas como formulários `JFrame` no Apache NetBeans.

Cada tela possui dois arquivos principais:

- O arquivo `.java`, que contém a lógica e o código da tela;
- O arquivo `.form`, que armazena as informações visuais utilizadas pelo GUI Builder do NetBeans.

A classe `TelaLogin.java` também contém o método `main`, responsável por iniciar a aplicação.

---

## ▶️ Como executar o projeto

1. Instale o **Java JDK**.
2. Instale o **Apache NetBeans**.
3. Instale o **MySQL Server**.
4. Instale ou adicione o **MySQL Connector/J** ao projeto.
5. Crie o banco de dados `sistema_usuarios`.
6. Crie a tabela `usuarios` e seus respectivos campos.
7. Cadastre um usuário no banco de dados.
8. Clone este repositório:

```bash
git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
```

9. Abra o projeto `STO_E01` no NetBeans.
10. Verifique as configurações da conexão com o MySQL em cada tela. O usuário padrão é `root` e a senha é `1234`.
11. Execute a classe `TelaLogin`.
12. Informe o código numérico e a senha de um usuário cadastrado no seu banco local.

---

## 🧪 Testes realizados

Durante o desenvolvimento, foram realizados testes locais para verificar:

- A validação de números no campo de telefone e seu limite de caracteres;
- A confirmação de igualdade na criação de senhas;
- A exibição da caixa de confirmação de segurança antes da exclusão permanente de um registro;
- A recuperação correta de chaves de auto-incremento após o cadastro de um novo usuário;
- O bloqueio contra edições nos campos de consulta;
- O tratamento de exceções, como letras preenchidas indevidamente no campo de UserID;
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
- Validação lógica de campos de formulário e tratamento de formatação;
- Criação de consultas SQL e uso do `LAST_INSERT_ID()`;
- Conexão Java com MySQL utilizando JDBC;
- Implementação de operações de CRUD e manipulação de `ResultSet`;
- Controle de acesso por autenticação básica;
- Versionamento e organização de pacotes para publicação no GitHub.

O projeto reforçou a importância de integrar interface, lógica de programação e banco de dados para construir uma aplicação funcional.

---

## 🚀 Possíveis melhorias futuras

Algumas melhorias que podem ser implementadas em versões futuras são:

- Utilização de `PreparedStatement` nas consultas SQL para evitar vulnerabilidades de SQL Injection;
- Criptografia ou hash das senhas;
- Criação de diferentes níveis de acesso;
- Separação da classe de conexão em um arquivo global único, evitando a repetição do `DriverManager` em cada tela;
- Criação de um script SQL disponibilizado no repositório para facilitar a criação da tabela local;
- Adição de testes automatizados.

---

## ⚠️ Observações

Este projeto foi desenvolvido para fins acadêmicos e de aprendizagem.

As credenciais presentes na conexão — `root` e `1234` — referem-se a um ambiente local utilizado durante o desenvolvimento do projeto. O projeto não oferece acesso a banco de dados remoto.

Para executar a aplicação, cada pessoa deve instalar e configurar seu próprio MySQL, criar o banco e cadastrar seus próprios usuários.

Não são utilizados dados reais de pessoas.

---

## 👩‍💻 Autoria

Projeto desenvolvido por:

### Carolina Yukari Kague

**Análise e Desenvolvimento de Sistemas (ADS)**  
**2026**

</div>
