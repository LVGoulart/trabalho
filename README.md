import math
def tang():
    global xr, yr, tgx, tgy
    tgx = math.sin(xr)/math.cos(xr)
    tgy = math.sin(yr) / math.cos(yr)

def tangente_cotangente(tgx, tgy):
    global resultado
    resultado=tgx + (1 / tgy)

def graus(): #transfroma os valores dados em graus para radianos
    global xr , yr
    xr= x*math.pi/180
    yr = y * math.pi / 180

def numeros_impares(x):
    return [i for i in range(1, x + 1) if i % 2 != 0]

def numeros_pares(y):
    return [i for i in range(2, y + 1) if i % 2 == 0]

def hipotenusa(x, y):
    return math.sqrt(x ** 2 + y ** 2)

def x_elevado_a_y(x, y):
    return x ** y

X=0
Y=0
xr=0
yr=0
tgx=0
tgy=0
resultado=0
print('\nCom esse programa você será capaz de: \n1 – Soma de X e Y \n2 – Produto de X e Y\n3 – Seno (X) + Cosseno (Y)\n4 – Tangente (X) + Cotangente (Y)\n5 – Raiz quadrada de X – Raiz quadrada de Y\n6 – Números ímpares de 1 a X\n7 – Números pares de 2 a Y\n8 – Hipotenusa, considerando X e Y como catetos de um triângulo retângulo\n9 – X elevado a Y\n')

x = float(input('Sendo assim, insira um valor para X - '))
y = float(input('Sendo assim, insira um valor para Y - '))
graus()
tang()
print('Muito bem agora o que vamos fazer com esses números?')
op=0

while op!= 10:
    print('')
    print('1 – Soma de X e Y ')
    print('2 – Produto de X e Y')
    print('3 – Seno(X) + Cosseno(Y)')
    print('4 – Tangente (X) + Cotangente (Y)')
    print('5 – Raiz quadrada de X – Raiz quadrada de Y')
    print('6 – Números ímpares de 1 a X')
    print('7 – Números pares de 2 a Y')
    print('8 – Hipotenusa, considerando X e Y como catetos de um triângulo retângulo')
    print('9 – X elevado a Y')
    print('10-sair')

    op = int(input('\nSelecione uma opçção - '))
    print('')

    if op == 1: #1 – Soma de X e Y
        print('a soma é', x+y)

    elif op == 2: #2 – Produto de X e Y
        print('o produto é', x*y)

    elif op == 3: #3 – Seno(X) + Cosseno(Y)
        print(f'a soma do seno de {x} e cosseno de {y} é', round(math.sin(xr)+math.cos(yr),2))

    elif op == 4: #4 – Tangente (X) + Cotangente (Y)'
        tangente_cotangente(tgx, tgy)
        #print(resultado)
        print(f'A tangente de {x} é {round(tgx, 2)}')
        print(f'A cotangente de {y} é {round(1 / tgy, 2)}')
        print(f'O resultado da soma da tangente e cotangente é {round(resultado, 2)}')
# trabalho
