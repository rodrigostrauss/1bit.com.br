# rodrigostrauss.github.io
1bit.com.br
# Desafio n°1 JOGO JOKENPO

from random import randint
joken = ('Pedra', 'Papel', 'Tesoura')
rival = randint(0,2)
print(''' Suas Opções:
[0] Pedra
[1] Papel
[2] Tesoura''')
jogador = int(input('O que você escolhe? '))
print('===' *20)
print ('Rival jogou {}'.format(joken[rival]))
print ('você jogou {}'.format(joken[jogador]))
if rival == 0: #rival jogou pedra
    if jogador == 0:
        print ('Empatou')
    elif jogador == 1:
        print ('Você venceu')
    elif jogador == 2:
        print ('Seu Rival venceu')
    else:
        print ('Jogada Invalida')
elif rival == 1: # rival jogou papel
    if jogador == 0:
        print ('Seu Rival venceu')
    elif jogador == 1:
        print ('Empatou')
    elif jogador == 2:
        print ('Você venceu')
    else:
        print ('Jogada Invalida')
elif rival == 2: # rival jogou tesoura
    if jogador == 0:
        print ('Você venceu')
    elif jogador == 1:
        print ('Seu Rival venceu')
    elif jogador == 2:
        print ('Empatou')
    else:
        print ('Jogada Invalida')
        
        
#Desafio n°2 Banco da Intelitrader
print('{:^30}'.format('BANCO INTELITRADER'))
print ('=' *30)
valor = int(input('Qual valor a ser sacado? R$ '))
total = valor
cedulas = 100
totcedulas = 0
while True:
    if total >= cedulas:
        total -= cedulas
        totcedulas += 1
    else:
        if totcedulas > 0:
            print(f'Total de {totcedulas} cedulas de R${cedulas}')
        if cedulas == 100:
            cedulas = 50
        elif cedulas == 50:
            cedulas = 20
        elif cedulas == 20:
            cedulas = 10
        elif cedulas == 10:
            cedulas = 5
        elif cedulas == 5:
            cedulas = 1
        totcedulas = 0
        if total == 0:
            break



#Desafio n°3 FizzBuzz
num = 1
while (num <= 100):
    if (num % 3 == 0) and (num % 5 == 0):
        print('FizzBuzz')
    elif (num % 3 == 0):
        print('Fizz')
    elif (num % 5 == 0):
        print('Buzz')
    else:
        print(num)
    num += 1
