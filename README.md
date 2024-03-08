# Respostas Desafio Target Sistemas

## 1°)  Observe o trecho de código abaixo:

int INDICE = 13, SOMA = 0, K = 0;

enquanto K < INDICE faça

{

K = K + 1;

SOMA = SOMA + K;

}

imprimir(SOMA);

Ao final do processamento, qual será o valor da variável SOMA?

### Resposta: 91
____


## 2°) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.


### Resposta (Foi utilizada a linguagem Python):

````
numero = int(input("Digite um número para verificar se pertence à sequência de Fibonacci: "))

def fibonacci(numero):
    fib = [0, 1]  # Inicia a sequência com os dois primeiros valores: 0 e 1
    while fib[-1] < numero:  # Continua gerando a sequência até que o último valor seja maior que o número fornecido
        fib.append(fib[-1] + fib[-2])  # Adiciona o próximo valor à sequência (soma dos dois últimos valores)
    
    if numero in fib:  # Verifica se o número fornecido está na sequência de Fibonacci
        return f"O número {numero} pertence à sequência de Fibonacci."
    else:
        return f"O número {numero} não pertence à sequência de Fibonacci."

print(fibonacci(numero))
````
___

## 3°) Descubra a lógica e complete o próximo elemento:


a) 1, 3, 5, 7, ___

b) 2, 4, 8, 16, 32, 64, ____

c) 0, 1, 4, 9, 16, 25, 36, ____

d) 4, 16, 36, 64, ____

e) 1, 1, 2, 3, 5, 8, ____

f) 2,10, 12, 16, 17, 18, 19, ____

### Resposta:

a) 1, 3, 5, 7, <font color="\green\"> 9 </font>

b) 2, 4, 8, 16, 32, 64, <font color=green> 128 </font><br>

c) 0, 1, 4, 9, 16, 25, 36, <font color=green> 49 </font><br>

d) 4, 16, 36, 64, <font color=green> 100 </font><br>

e) 1, 1, 2, 3, 5, 8, <font color=green> 13 </font><br>

f) 2,10, 12, 16, 17, 18, 19, <font color=green> 200 </font><br>
___

## 4°) Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada. Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?

### Resposta:

Ligaria o primeiro interruptor e aguardaria alguns minutos.
Desligo o primeiro interruptor e ligo o segundo interruptor.
Deixo o terceiro interruptor desligado.

Vou na primeira sala e observo a lâmpada:

- Se a lâmpada estiver acesa:

- - O segundo interruptor que está ligado na sala controla a lâmpada acesa.
Vou na segunda sala e toco na lâmpada: se estiver quente, está conectada ao primeiro interruptor, se estiver fria, está conectada ao terceiro interruptor, em ambos os casos não se faz necessário a visita a última sala pois sobraria um interruptor apenas para ligar.

- Se a lâmpada estiver apagada:
  
- - Toco na lâmpada para verificar a temperatura, caso esteja quente, então ela é ligada pelo primeiro interruptor que ficou ligado alguns minutos, se estiver fria, ela é ligada pelo terceiro interruptor que permaneceu todo o tempo apagado. 
- - Vou na segunda sala e verifica a segunda lâmpada: se a lâmpada estiver acesa ela é controlada pelo segundo interruptor e consequentemente a lâmpada da terceira sala é controlada pelo interruptor que sobrou. Caso a lampada esteja apagada repito o processo acima de verificar a temperatura: está quente? é controlada pelo primeiro interruptor, está fria? terceiro interruptor.
<br>

## 5°) Escreva um programa que inverta os caracteres de um string.

### Resposta (utilizando a linguagem python):

```
def inverter_string(string):
    # Inicializa uma string vazia para armazenar a string invertida
    string_invertida = ""

    # Percorre a string de trás para frente e adiciona cada caractere à string invertida
    for i in range(len(string) - 1, -1, -1):
        string_invertida += string[i]

    return string_invertida

string_original = input("Digite um texto ou sequência numérica para ser invertida: ")
string_invertida = inverter_string(string_original)
print("String invertida:", string_invertida)```
