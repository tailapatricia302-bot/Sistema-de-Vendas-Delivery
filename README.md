# SISTEMA DE VENDAS WEB

## 1. Descrição Geral

O Sistema de Vendas Web é uma aplicação desenvolvida em PHP utilizando Arquitetura MVC, Programação Orientada a Objetos (POO) e banco de dados MySQL.

O sistema foi criado para automatizar o gerenciamento de clientes, empresas, produtos, pedidos e usuários, proporcionando maior organização, agilidade e controle das operações comerciais.

A plataforma permite o cadastro e gerenciamento de informações essenciais para o funcionamento de uma empresa, centralizando todos os processos em um único ambiente.

---

# 2. Objetivos

## Objetivo Geral

Desenvolver um sistema web para gerenciamento de vendas, produtos, clientes e pedidos, utilizando boas práticas de programação e arquitetura MVC.

## Objetivos Específicos

* Gerenciar usuários do sistema;
* Controlar cadastros de clientes;
* Gerenciar empresas cadastradas;
* Realizar cadastro e manutenção de produtos;
* Controlar pedidos realizados pelos clientes;
* Garantir autenticação e segurança de acesso;
* Facilitar a administração das informações da empresa.

---

# 3. Funcionalidades do Sistema

## Autenticação

* Login de usuários;
* Logout do sistema;
* Controle de sessão;
* Restrição de acesso às áreas administrativas.

## Usuários

* Cadastro de usuários;
* Edição de usuários;
* Exclusão de usuários;
* Listagem de usuários cadastrados.

## Clientes

* Cadastro de clientes;
* Atualização de informações;
* Exclusão de clientes;
* Consulta de clientes cadastrados.

## Empresas

* Cadastro de empresas;
* Alteração de dados;
* Exclusão de empresas;
* Consulta de empresas cadastradas.

## Produtos

* Cadastro de produtos;
* Edição de produtos;
* Exclusão de produtos;
* Consulta de produtos;
* Upload de imagens dos produtos.

## Pedidos

* Cadastro de pedidos;
* Alteração de pedidos;
* Exclusão de pedidos;
* Consulta de pedidos;
* Registro dos produtos vinculados ao pedido.

## Carrinho de Compras

* Adição de produtos;
* Remoção de produtos;
* Atualização de quantidades;
* Finalização de pedidos.

---

# 4. Regras de Negócio

1. Apenas usuários autenticados poderão acessar o sistema administrativo.
2. Todo usuário deverá possuir login e senha válidos.
3. Produtos deverão possuir nome, descrição e preço cadastrados.
4. Um pedido deverá conter pelo menos um produto.
5. Um cliente poderá realizar vários pedidos.
6. Todo pedido realizado ficará com status **Pendente** até aprovação do Administrador.
7. Apenas usuários com perfil **Administrador** poderão aprovar ou rejeitar vendas.
8. Somente pedidos aprovados poderão ser finalizados.
9. Produtos excluídos ou inativos não poderão ser vendidos.
10. O sistema registrará a data e hora das principais operações realizadas.
11. Cada pedido deverá possuir um status válido (Pendente, Aprovado, Rejeitado ou Finalizado).
12. O valor total do pedido será calculado automaticamente com base nos produtos selecionados.


# 5. Principais Entidades do Sistema

## Usuário

* id
* nome
* email
* senha

## Cliente

* id
* nome
* telefone
* email
* endereço

## Empresa

* id
* razão_social
* cnpj
* telefone
* endereço

## Produto

* id
* nome
* descrição
* preço
* imagem

## Pedido

* id
* cliente_id
* data_pedido
* valor_total
* status

---

# 6. Estrutura do Projeto

## 📂 Estrutura do Projeto

```text
projeto/
│
├── app/
│   ├── controllers/
│   │   ├── AdminController.php
│   │   ├── AuthController.php
│   │   ├── ClienteController.php
│   │   ├── EmpresaController.php
│   │   ├── HomeController.php
│   │   ├── PedidoController.php
│   │   ├── ProdutoController.php
│   │   └── UsuarioController.php
│   │
│   ├── core/
│   │   ├── Controller.php
│   │   ├── Model.php
│   │   └── Router.php
│   │
│   ├── models/
│   │   ├── Cliente.php
│   │   ├── Empresa.php
│   │   ├── Pedido.php
│   │   ├── Produto.php
│   │   └── Usuario.php
│   │
│   └── views/
│       ├── auth/
│       │   ├── admin_login.php
│       │   ├── cadastro.php
│       │   ├── login.php
│       │   └── logout.php
│       │
│       ├── carrinho/
│       │   └── index.php
│       │
│       ├── clientes/
│       │   ├── cadastrar.php
│       │   ├── editar.php
│       │   ├── excluir.php
│       │   ├── index.php
│       │   └── listar.php
│       │
│       ├── dashboard/
│       │   └── index.php
│       │
│       ├── empresas/
│       │   ├── cadastrar.php
│       │   ├── editar.php
│       │   ├── excluir.php
│       │   └── listar.php
│       │
│       ├── home/
│       │   └── index.php
│       │
│       ├── pedidos/
│       │   ├── cadastrar.php
│       │   ├── editar.php
│       │   ├── excluir.php
│       │   ├── listar.php
│       │   └── sucesso.php
│       │
│       ├── produtos/
│       │   ├── cadastrar.php
│       │   ├── editar.php
│       │   ├── excluir.php
│       │   ├── form.php
│       │   ├── index.php
│       │   └── listar.php
│       │
│       └── usuarios/
│           ├── cadastrar.php
│           ├── editar.php
│           ├── excluir.php
│           └── listar.php
│
├── config/
│   └── database.php
│
├── database/
│   └── sistema_vendas.sql
│
├── public/
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   └── script.js
│   │
│   ├── img/
│   │   ├── x-tudo.jpg
│   │   ├── x-salada.jpg
│   │   ├── x-bacon.jpg
│   │   ├── x-egg.jpg
│   │   ├── x-calabresa.jpg
│   │   ├── batata frita tradicional.jpg
│   │   ├── batata smile.jpg
│   │   └── ...
│   │
│   └── uploads/
│
├── index.php
└── README.md
```

# 7. Tecnologias Utilizadas

* PHP 8+
* MySQL
* HTML5
* CSS3
* JavaScript
* PDO
* Programação Orientada a Objetos (POO)
* Arquitetura MVC

---



# 8. Funcionalidades Extras

* Dashboard administrativo;
* Upload de imagens;
* Carrinho de compras;
* Controle de acesso;
* Gerenciamento completo de produtos;
* Gerenciamento completo de clientes;
* Gerenciamento completo de pedidos;
* Gerenciamento completo de empresas.

---

# 9. Benefícios Esperados

* Organização dos processos comerciais;
* Facilidade no gerenciamento de dados;
* Centralização das informações;
* Maior produtividade dos usuários;
* Melhor controle de clientes e produtos;
* Facilidade de manutenção e expansão do sistema.

---

# 10. Desenvolvedores

**Taila Patricia Vieira Dos Santos & Vitor Gabriel C. de Oliveira**

Projeto desenvolvido para fins acadêmicos e aprendizado em desenvolvimento web utilizando PHP, MySQL e Arquitetura MVC.
