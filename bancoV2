def menu():
    print("\n=== MENU ===")
    print("[1] Depositar")
    print("[2] Sacar")
    print("[3] Extrato")
    print("[4] Novo Usuário")
    print("[5] Nova Conta")
    print("[6] Listar Contas")
    print("[0] Sair")

def depositar(saldo, extrato):
    valor = float(input("Informe o valor do depósito: R$ "))
    if valor > 0:
        saldo += valor
        extrato += f"Depósito: R$ {valor:.2f}\n"
        print("Depósito realizado com sucesso!")
    else:
        print("Valor inválido para depósito.")
    return saldo, extrato

def sacar(saldo, extrato, limite, saques_realizados, LIMITE_SAQUES):
    valor = float(input("Informe o valor do saque: R$ "))
    
    excedeu_saldo = valor > saldo
    excedeu_limite = valor > limite
    excedeu_saques = saques_realizados >= LIMITE_SAQUES

    if excedeu_saldo:
        print("Você não tem saldo suficiente.")
    elif excedeu_limite:
        print("O valor do saque excede o limite por operação.")
    elif excedeu_saques:
        print("Número máximo de saques diários excedido.")
    elif valor > 0:
        saldo -= valor
        extrato += f"Saque:    -R$ {valor:.2f}\n"
        saques_realizados += 1
        print("Saque realizado com sucesso!")
    else:
        print("Valor inválido para saque.")
    
    return saldo, extrato, saques_realizados

def mostrar_extrato(saldo, extrato):
    print("\n=== EXTRATO ===")
    print(extrato if extrato else "Não foram realizadas movimentações.")
    print(f"\nSaldo atual: R$ {saldo:.2f}")

def cadastrar_usuario(usuarios):
    cpf = input("Informe o CPF (somente números): ")
    usuario = filtrar_usuario(cpf, usuarios)

    if usuario:
        print("Usuário já cadastrado.")
        return

    nome = input("Informe o nome completo: ")
    data_nascimento = input("Informe a data de nascimento (dd-mm-aaaa): ")
    endereco = input("Informe o endereço (logradouro, número - bairro - cidade/estado): ")

    usuarios.append({
        "nome": nome,
        "data_nascimento": data_nascimento,
        "cpf": cpf,
        "endereco": endereco
    })

    print("Usuário cadastrado com sucesso!")

def filtrar_usuario(cpf, usuarios):
    usuarios_filtrados = [usuario for usuario in usuarios if usuario["cpf"] == cpf]
    return usuarios_filtrados[0] if usuarios_filtrados else None

def criar_conta(agencia, numero_conta, usuarios, contas):
    cpf = input("Informe o CPF do usuário: ")
    usuario = filtrar_usuario(cpf, usuarios)

    if usuario:
        conta = {
            "agencia": agencia,
            "numero_conta": numero_conta,
            "usuario": usuario
        }
        contas.append(conta)
        print("Conta criada com sucesso!")
    else:
        print("Usuário não encontrado. Cadastre o usuário primeiro.")

def listar_contas(contas):
    for conta in contas:
        print(f"\nAgência: {conta['agencia']}")
        print(f"Conta: {conta['numero_conta']}")
        print(f"Titular: {conta['usuario']['nome']}")

# Programa principal
saldo = 0.0
limite = 500.0
extrato = ""
LIMITE_SAQUES = 3
saques_realizados = 0
usuarios = []
contas = []
AGENCIA = "0001"

while True:
    menu()
    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        saldo, extrato = depositar(saldo, extrato)

    elif opcao == "2":
        saldo, extrato, saques_realizados = sacar(saldo, extrato, limite, saques_realizados, LIMITE_SAQUES)

    elif opcao == "3":
        mostrar_extrato(saldo, extrato)

    elif opcao == "4":
        cadastrar_usuario(usuarios)

    elif opcao == "5":
        numero_conta = len(contas) + 1
        criar_conta(AGENCIA, numero_conta, usuarios, contas)

    elif opcao == "6":
        listar_contas(contas)

    elif opcao == "0":
        print("Obrigado por usar nosso sistema bancário!")
        break

    else:
        print("Opção inválida. Por favor, escolha uma opção válida.")