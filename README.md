<div align="center">

🗂️ Sistema de Gerenciamento de Usuários
Sistema desktop em Java para cadastro, consulta, alteração e exclusão de usuários, com autenticação via login
Análise e Desenvolvimento de Sistemas (ADS) | Projeto Acadêmico | 2026

</div>

📌 Sobre o projeto
O Sistema de Gerenciamento de Usuários é uma aplicação desktop desenvolvida em Java, utilizando Java Swing para a interface gráfica e Apache NetBeans como ambiente de desenvolvimento.

O sistema foi criado como projeto acadêmico com o objetivo de aplicar, na prática, conceitos de programação orientada a objetos, construção de interfaces gráficas, lógica de autenticação e integração de uma aplicação Java com um banco de dados relacional.

O projeto simula um cenário comum em sistemas corporativos: o controle de acesso e o gerenciamento de usuários por meio de operações de CRUD (Create, Read, Update, Delete), precedidas por uma tela de login.

🎯 Objetivo
Desenvolver um sistema funcional que demonstre, na prática, habilidades em:

Programação orientada a objetos em Java;

Construção de interfaces gráficas com Java Swing;

Autenticação de usuários por meio de tela de login;

Operações completas de CRUD (cadastrar, consultar, alterar e excluir);

Conexão de uma aplicação Java com um banco de dados MySQL via JDBC;

Organização de um projeto Java dentro do ambiente NetBeans;

Versionamento de código com Git e publicação em repositório no GitHub.

Mais do que apenas um sistema funcional, o projeto representa uma etapa de aprendizado prático sobre como uma aplicação desktop se conecta a um banco de dados e gerencia informações de usuários de forma estruturada.

🧩 Funcionalidades
O sistema conta com as seguintes telas e funcionalidades:

Tela de Login: autenticação do usuário por código e senha, validados diretamente no banco de dados;

Tela de Menu: ponto central de navegação entre as funcionalidades do sistema;

Cadastrar usuário: inclusão de novos registros no banco de dados;

Consultar usuário: busca e visualização de usuários já cadastrados;

Alterar usuário: edição das informações de um usuário existente;

Excluir usuário: remoção de um registro do banco de dados.

Cada uma dessas telas foi desenvolvida como um JFrame no NetBeans, utilizando o GUI Builder (Matisse), o que gera, para cada tela, um arquivo .java (lógica) e um arquivo .form (layout visual).

🗄️ Banco de Dados (MySQL)
O sistema utiliza o MySQL como banco de dados relacional, acessado por meio da API JDBC (Java Database Connectivity) com o driver MySQL Connector/J.

A conexão é estabelecida através da classe responsável pelo acesso ao banco, utilizando uma URL no formato:

java
jdbc:mysql://localhost:3306/sistema_usuarios
Isso significa que o sistema busca o banco de dados localmente, no computador de quem estiver executando a aplicação. O projeto não disponibiliza nem depende de um banco de dados remoto: cada pessoa que for executar o sistema deve configurar seu próprio ambiente MySQL local.

O que é necessário para rodar o sistema
Para executar o projeto corretamente, é preciso:

Ter o MySQL Server instalado e em execução;

Criar um banco de dados chamado sistema_usuarios;

Criar a tabela usuarios, contendo, no mínimo, as colunas de código e senha utilizadas na autenticação;

Cadastrar manualmente ao menos um usuário nessa tabela para conseguir realizar login;

Ter o driver MySQL Connector/J configurado nas bibliotecas do projeto no NetBeans;

Ajustar, se necessário, o usuário e a senha de conexão utilizados no código para que correspondam à configuração do seu MySQL local.

Observação importante
As credenciais de conexão presentes no código (usuário e senha do MySQL) são referentes a um ambiente local de desenvolvimento acadêmico e não representam acesso a nenhum banco de dados remoto ou pessoal. Nenhum dado real de usuários é utilizado no projeto — todos os registros são fictícios e criados apenas para fins de teste e demonstração.

Por não haver um banco de dados hospedado remotamente, é necessário que cada pessoa configure seu próprio MySQL local para conseguir executar o sistema e acessar a tela de login.

💻 Tecnologias utilizadas
Java — linguagem de programação principal;

Java Swing — construção da interface gráfica desktop;

Apache NetBeans — ambiente de desenvolvimento (IDE) e GUI Builder;

JDBC — conexão entre a aplicação Java e o banco de dados;

MySQL — sistema gerenciador de banco de dados relacional;

Git e GitHub — controle de versão e hospedagem do código-fonte.

📁 Estrutura do projeto
text
STO_E01/
├── src/
│   ├── FrameLogin.java / .form
│   ├── FrameMenu.java / .form
│   ├── FrameIncluir.java / .form
│   ├── FrameConsultar.java / .form
│   ├── FrameAlterar.java / .form
│   ├── FrameExcluir.java / .form
│   └── (demais classes e imagens da interface)
├── nbproject/
├── build.xml
├── manifest.mf
├── .gitignore
└── README.md
▶️ Como executar o projeto
Clone este repositório:

bash
git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
Abra o projeto no Apache NetBeans.

Instale e inicie o MySQL no seu computador.

Crie o banco de dados sistema_usuarios.

Crie a tabela usuarios com as colunas utilizadas pelo sistema (código e senha, no mínimo).

Cadastre um usuário de teste diretamente no banco, para conseguir acessar a tela de login.

Verifique se o driver MySQL Connector/J está adicionado às bibliotecas do projeto.

Ajuste o usuário e a senha de conexão no código, caso sejam diferentes da sua instalação local do MySQL.

Execute o projeto a partir da classe FrameLogin.

Faça login com o usuário cadastrado e navegue pelas funcionalidades de cadastro, consulta, alteração e exclusão.

📚 Aprendizados
Este projeto proporcionou aprendizado prático sobre como uma aplicação desktop em Java se conecta a um banco de dados relacional e gerencia informações por meio de operações de CRUD.

Foi possível compreender, na prática, conceitos como:

A importância de separar a lógica de conexão do restante do sistema;

Como o Java Swing organiza componentes visuais em JFrames e Panels;

Como o JDBC estabelece comunicação entre a aplicação e o MySQL;

A relevância de validar corretamente as credenciais do usuário durante o login;

Como funciona o versionamento de código com Git e a publicação de um projeto no GitHub.

Mais do que apenas implementar telas e comandos SQL, o projeto reforçou a importância de compreender o fluxo completo de uma aplicação: da interface gráfica até a persistência dos dados no banco.

👩‍💻 Autoria
Projeto desenvolvido por:

Carolina Yukari Kague
Análise e Desenvolvimento de Sistemas (ADS)
2026

</div>
