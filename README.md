# Calculadora

def formatar_valor(valor_str):
    # Suporta vírgula ou ponto como separador decimal
    return float(valor_str.replace(',', '.'))

def calculadora():
    print("=== CALCULADORA SIMPLES ===")
    print("Operações disponíveis: +  -  *  /")
    
    # Entrada dos valores
    num1 = formatar_valor(input("Digite o primeiro número: "))
    operacao = input("Digite a operação (+, -, *, /): ")
    num2 = formatar_valor(input("Digite o segundo número: "))

    # Processamento
    if operacao == '+':
        resultado = num1 + num2
    elif operacao == '-':
        resultado = num1 - num2
    elif operacao == '*':
        resultado = num1 * num2
    elif operacao == '/':
        if num2 == 0:
            print("Erro: divisão por zero!")
            return
        resultado = num1 / num2
    else:
        print("Operação inválida!")
        return

    # Resultado
    print(f"Resultado: {resultado:.2f}")

# Executar a calculadora
calculadora()
