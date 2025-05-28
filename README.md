# 💰 Sistema Bancário em Python

Este é um projeto desenvolvido como parte do desafio da Formação Python oferecida pela [DIO - Digital Innovation One](https://www.dio.me/). O objetivo é implementar um sistema bancário simples com as operações de saque, depósito e visualização de extrato.

## 🚀 Funcionalidades

- [x] **Depósito** com validação de valor positivo
- [x] **Saque** com:
  - Limite de valor por saque (R$ 500)
  - Limite de 3 saques diários
  - Verificação de saldo suficiente
- [x] **Extrato** com listagem de todas as transações
- [x] Interface no terminal (linha de comando)

## 🛠️ Tecnologias utilizadas

- Python 3.x
- VS Code
- Git e GitHub

## ▶️ Como executar o projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/Rogerio99ga/sistema-bancario-python.git

   # 💰 Sistema Bancário em Python - Desafio 2 (V2)

Este projeto é uma continuação do **Desafio 1** da Formação Python da DIO. Agora, além de sacar, depositar e visualizar extrato, o sistema também permite:

✅ Cadastrar usuários (clientes)  
✅ Cadastrar contas bancárias vinculadas aos usuários  
✅ Listar contas existentes  

---

## 🧠 Funcionalidades

### 📥 Depositar
- Permite que o usuário informe um valor positivo para depósito.
- Atualiza o saldo e registra no extrato.

### 💸 Sacar
- Limite de até **R$ 500 por saque**.
- Limite de **3 saques por dia**.
- Valida saldo, limite e número de saques.

### 📄 Extrato
- Mostra todas as movimentações (depósitos e saques).
- Mostra o saldo final da conta.

### 👤 Cadastrar Usuário
- Cadastro com: **nome, data de nascimento, CPF e endereço**.
- CPF não pode se repetir (usado como identificador único).

### 🏦 Cadastrar Conta
- Cria uma nova conta vinculada a um usuário existente.
- Cada conta tem número, agência e CPF do titular.

### 📋 Listar Contas
- Exibe todas as contas bancárias cadastradas com seus dados.

---

## 🛠️ Tecnologias

- Python 3.x
- Execução via terminal / prompt de comando

---

## 🚀 Como usar

1. Clone o repositório:
```bash
git clone https://github.com/Rogerio99ga/sistema-bancario-python.git

