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
