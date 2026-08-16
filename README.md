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

Após clicar em **OK**, o sistema consulta a tabela `usuarios` no MySQL local buscando a equivalência exata dos dados informados. Quando os dados estão corretos, o acesso é liberado, uma mensagem de sucesso é exibida e o usuário é encaminhado para a `TelaMenu`.

A tela também possui as opções:

- **Limpar:** apaga os dados preenchidos nos campos;
- **Fim:** encerra a aplicação;
- **OK:** valida o login e abre o sistema.

---

## 🧩 Funcionalidades

### Tela Menu

A `TelaMenu` organiza o acesso às operações disponíveis no sistema por meio de uma barra de menus superior contendo as guias "Usuário" (Consultar, Incluir, Alterar, Excluir) e "..." (Sair).

### Cadastro de usuários

A `TelaIncluir` permite inserir novos usuários no banco de dados. O formulário solicita **Nome Completo**, **E-mail**, **Telefone** e **Senha**. O sistema conta com validações que exigem a confirmação exata da senha e garantem que o telefone contenha apenas números, limitados a 11 dígitos. Após o cadastro bem-sucedido, o `UserID` é gerado de forma automática e exibido na tela para o usuário.

### Consulta de usuários

A `TelaConsultar` permite localizar as informações dos usuários cadastrados por meio de uma busca utilizando o `UserID`. Os dados retornados (Nome, E-mail, Telefone e Senha) são carregados automaticamente em campos bloqueados para edição.

### Alteração de usuários

A `TelaAlterar` busca o registro pelo `UserID` e habilita a modificação dos campos Nome, E-mail, Telefone e Senha. O campo de `UserID` possui um bloqueio de segurança estrutural, impedindo que o código identificador seja modificado[cite: 1]. O formulário também valida se o número de telefone possui apenas caracteres numéricos antes de autorizar a atualização no banco de dados[cite: 1].

### Exclusão de usuários

A `TelaExcluir` localiza um cadastro pelo `UserID` e exibe seus dados para visualização[cite: 1]. Ao solicitar a exclusão, o sistema exibe uma caixa de diálogo exigindo a confirmação do usuário antes de remover o registro permanentemente do banco de dados[cite: 1].

---

## 🗄️ Banco de dados MySQL

O sistema utiliza o **MySQL** para armazenar os dados dos usuários e realizar as operações de cadastro, consulta, alteração, exclusão e autenticação[cite: 1].

A comunicação entre o Java e o MySQL é feita por meio do **JDBC**, utilizando o driver **MySQL Connector/J**.

A conexão utilizada no projeto aponta para um banco local com as seguintes credenciais padrão definidas no código[cite: 1]:

```java
jdbc:mysql://localhost:3306/sistema_usuarios
User: "root"
Password: "1234"
