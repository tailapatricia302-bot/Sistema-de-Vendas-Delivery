# PROJETO FINAL – SISTEMA INTEGRADO DE PDV E DELIVERY

## 1. Descrição Geral

O projeto consiste no desenvolvimento de um sistema web integrado entre um Ponto de Venda (PDV) e uma plataforma de Delivery, permitindo o gerenciamento centralizado de vendas presenciais e pedidos online.

O sistema tem como objetivo proporcionar maior praticidade para clientes e funcionários, automatizando processos de venda, controle de pedidos e gerenciamento operacional.

A aplicação será desenvolvida utilizando PHP 8, MySQL, PDO, Programação Orientada a Objetos (POO) e arquitetura MVC.

---

## 2. Objetivos

### Objetivo Geral

Desenvolver um sistema integrado de PDV e Delivery capaz de gerenciar vendas, pedidos online e controle operacional de forma segura e eficiente.

### Objetivos Específicos

* Disponibilizar um catálogo online de produtos para os clientes;
* Permitir a realização de pedidos pela internet;
* Integrar os pedidos online ao sistema de PDV;
* Controlar permissões de acesso de acordo com o perfil do usuário;
* Garantir maior segurança em operações críticas;
* Facilitar o gerenciamento de produtos, vendas e pedidos.

---

## 3. Funcionalidades do Cliente

O cliente poderá acessar a área pública do sistema para:

* Visualizar os produtos disponíveis;
* Consultar preços e descrições;
* Selecionar produtos e quantidades;
* Adicionar produtos ao pedido;
* Escolher a forma de recebimento:

  * Retirada no local;
  * Entrega delivery;
* Selecionar a forma de pagamento;
* Finalizar pedidos;
* Acompanhar o status do pedido.

---

## 4. Integração com o PDV

Todos os pedidos realizados pelo sistema de delivery serão enviados automaticamente para o módulo de PDV.

Através do PDV será possível:

* Receber pedidos realizados online;
* Aceitar ou rejeitar pedidos;
* Atualizar o status do pedido;
* Registrar vendas presenciais;
* Finalizar vendas;
* Consultar histórico de vendas;
* Gerenciar produtos cadastrados;
* Controlar estoque.

---

## 5. Controle de Permissões

O sistema contará com controle de acesso baseado em perfis de usuário.

### Funcionário

O perfil Funcionário possuirá permissões limitadas para operações do dia a dia.

Poderá:

* Registrar vendas;
* Consultar produtos;
* Consultar pedidos;
* Atualizar status de pedidos.

Não poderá:

* Cancelar vendas finalizadas sem autorização;
* Executar operações administrativas restritas.

### Supervisor

O perfil Supervisor terá acesso ampliado ao sistema.

Poderá:

* Autorizar cancelamentos;
* Validar operações críticas;
* Gerenciar funcionários;
* Gerenciar produtos;
* Acessar relatórios administrativos;
* Supervisionar operações do sistema.

---

## 6. Regras de Negócio

1. Apenas usuários autenticados poderão acessar o sistema administrativo.
2. Senhas serão armazenadas utilizando a função password_hash().
3. Todo pedido deverá possuir pelo menos um item.
4. Um cliente poderá realizar vários pedidos.
5. Cada pedido deverá possuir um status.
6. O estoque será atualizado automaticamente após a confirmação da venda.
7. Cancelamentos de vendas finalizadas exigirão autorização de um supervisor.
8. Produtos inativos não poderão ser vendidos.
9. O sistema registrará data e hora de todas as operações importantes.

---

## 7. Principais Entidades do Sistema

O sistema será composto, no mínimo, pelas seguintes entidades:

### Usuário

* id
* nome
* email
* senha
* perfil

### Cliente

* id
* nome
* telefone
* email
* endereço

### Produto

* id
* nome
* descrição
* preço
* estoque
* imagem

### Pedido

* id
* cliente_id
* data
* status
* valor_total

### ItemPedido

* id
* pedido_id
* produto_id
* quantidade
* valor_unitário

### Venda

* id
* usuário_id
* data
* valor_total
* forma_pagamento

---

## 8. Funcionalidades Extras

Para atender aos requisitos do projeto serão implementadas as seguintes funcionalidades adicionais:

* Busca de produtos;
* Upload de imagens de produtos;
* Controle de estoque;
* Dashboard administrativo;
* Carrinho de compras;
* Filtro de produtos por categoria;
* Histórico de pedidos;
* Relatório de vendas.

---

## 9. Benefícios Esperados

O sistema proporcionará:

* Maior agilidade no atendimento;
* Integração entre vendas presenciais e online;
* Melhor controle de estoque;
* Segurança operacional;
* Facilidade no gerenciamento administrativo;
* Melhor experiência para o cliente final.
