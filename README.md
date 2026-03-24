# Cadastro
Fiz meu primeiro programa para cadastrar pessoas

cadastrar = []

def cadastro():
    nome = input("Digite seu nome: ")
    idade = input("Digite sua idade: ")
    sexo = input("Digite seu sexo: ")
    estado_civil = input("Digite seu estado civil: ")

    registro = {
        "nome": nome,
        "idade": idade,
        "sexo": sexo,
        "estado_civil": estado_civil
    }
    cadastrar.append(registro)
    print("Usuário cadastrado com sucesso!")


     

def listar_usuarios():
    if not cadastrar:
        print("Nenhum usuário cadastrado ainda.")
        return

    print("\n--- Usuários Cadastrados ---")
    for i, usuario in enumerate(cadastrar):
        print(f"Usuário {i+1}:")
        for chave, valor in usuario.items():
            print(f"  {chave.replace('_', ' ').capitalize()}: {valor}")
    print("--------------------------")
