# 💳 Sistema Bancário - Versão bancoV3 (POO)

Este projeto simula um sistema bancário simples utilizando **Programação Orientada a Objetos (POO)** em Python. Ele foi desenvolvido como exercício prático para consolidar os conceitos de classes, herança, encapsulamento e polimorfismo.

---

## 📌 Funcionalidades

- Criar usuários (clientes pessoas físicas)
- Criar contas bancárias do tipo corrente
- Realizar depósitos
- Realizar saques com regras de limite e quantidade
- Exibir extrato da conta
- Listar contas cadastradas

---

## 🧱 Modelo de Classes (UML)

O sistema foi modelado com as seguintes classes:

- `Cliente` (classe base)
- `PessoaFisica` (herda de `Cliente`)
- `Conta` (classe base)
- `ContaCorrente` (herda de `Conta`)
- `Transacao` (abstrata)
  - `Deposito` e `Saque` (herdam de `Transacao`)
- `Historico` (armazena transações de uma conta)

---

## 🖥️ Como utilizar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/sistema-bancario.git
   cd sistema-bancario
