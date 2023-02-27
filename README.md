# fibonacci.py

2) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

# Função para calcular a sequência de Fibonacci
def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2) 
# Função para verificar se um número pertence à sequência de Fibonacci
def is_fibonacci(num):
    for i in range(num):
        if fibonacci(i) == num:
            return True
    return False 
# Solicita ao usuário que informe um número
num = int(input("Informe um número: ")) 
# Verifica se o número informado pertence à sequência de Fibonacci
if is_fibonacci(num):
    print("O número informado pertence à sequência de Fibonacci.")
else:
    print("O número informado não pertence à sequência de Fibonacci.")
