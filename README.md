# calculadora-simples
uma calculadora simples que crie com ajuda de algumas pessoas já que estou iniciando dentro do mundo de ADS.
essa calculadora foi criada no código python.

def calculadora():
    print("Bem-vindo à calculadora simples!")
    print("Selecione a operação:")
    print("1. Adição")
    print("2. Subtração")
    print("3. Multiplicação")
    print("4. Divisão")
    
    operacao = input("Digite o número da operação (1/2/3/4): ")

    if operacao not in ['1', '2', '3', '4']:
        print("Entrada inválida. Por favor, reinicie o programa e digite um número de 1 a 4.")
        return

    try:
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
    except ValueError:
        print("Entrada inválida. Por favor, digite apenas números.")
        return

    if operacao == '1':
        resultado = num1 + num2
        print(f"O resultado da adição é: {resultado}")
    elif operacao == '2':
        resultado = num1 - num2
        print(f"O resultado da subtração é: {resultado}")
    elif operacao == '3':
        resultado = num1 * num2
        print(f"O resultado da multiplicação é: {resultado}")
    elif operacao == '4':
        if num2 == 0:
            print("Erro: Divisão por zero não é permitida.")
        else:
            resultado = num1 / num2
            print(f"O resultado da divisão é: {resultado}")

calculadora()
