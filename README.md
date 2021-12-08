# Descobrindo-2-digitos-CPF


guardar = []
contador = 0


while contador <= 8:
    cpf = input('Digite cada numero do seu CPF, 1 (Um) por vez: ')
    while len(cpf) > 1:
               print('Você precisa digitar apenas um número por vez!')
               cpf = input('Digite cada numero do seu CPF, 1 (Um) por vez: ')
               while not cpf.isnumeric():
                        print('Você precisa digitar um número!')
                        cpf = input('Digite cada numero do seu CPF, 1 (Um) por vez: ')
                        while cpf == '':
                          print('Seu número não pode ser vazio e não pode conter mais de dois digitos por vez!')
                          cpf = input('Digite cada numero do seu CPF, 1 (Um) por vez: ')

    guardar.append(int(cpf))
    contador = contador + 1


n1, n2, n3, n4, n5, n6, n7, n8, n9 = guardar

conta_digito = (n1*10) + (n2*9) + (n3*8) + (n4*7) + (n5*6) + (n6*5) + (n7*4) + (n8*3) + (n9*2)

digitox = conta_digito % 11


if digitox == 1 or digitox == 0:
    digito1 = 0
    guardar.append(digito1)
else:
    digito1 = 11 - digitox
    guardar.append(digito1)


m1,m2,m3,m4,m5,m6,m7,m8,m9,m10 = guardar

conta_digito2 = (m1*11) + (m2*10) + (m3*9) + (m4*8) + (m5*7) + (m6*6) + (m7*5) + (m8*4) + (m9*3) + (m10*2)

digitoy = conta_digito2 % 11


if digitoy == 1 or digitoy == 0:
    digito2 = 0
    guardar.append(digito2)

else:
    digito2 = 11 - digitoy
    guardar.append(digito2)

print(f'O seu CPF completo é {guardar}')




