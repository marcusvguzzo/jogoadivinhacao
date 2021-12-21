import random # BIBLIOTECA

print(37*'*')
bem_vindo = ('Bem-Vindo para o jogo da adivinhação!')
print(bem_vindo)
print(37*'*')

numero_secreto = random.randrange(1,51)
tentativa_total = 0

print('Nível de Dificuldade: ')
print('(1) - Fácil ** (2) Médio ** (3) Difícil')


nivel_dificuldade = int(input('Defina um nível: '))
 
if nivel_dificuldade == 1:
  tentativa_total = 8
elif nivel_dificuldade == 2:
  tentativa_total = 5
else:
  tentativa_total = 3


for  rodada in range(1, tentativa_total + 1):
  print(f'Tentativa {rodada} de {tentativa_total}: ')
  
  chute_ = input('Digite seu número de 1 a 50: ')
  chute = int(chute_)

  
  if chute < 1 or chute > 50:
    print('Você deve digitar um valor entre 1 e 50!')
    continue
  acertou = chute == numero_secreto
  maior = chute < numero_secreto
  if acertou:
    print(f'Parabéns, você acertou certou: {chute}')
    break
  elif maior:
    print(f'O número secreto é maior que {chute}')
  else:
    print(f'O número secreto é menor que {chute}')
  rodada = rodada + 1

print('FIM DE JOGO!')
  
