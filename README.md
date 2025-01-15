# super-nac
20 exercícios resolvidos na aula de "computational logical using python"


# exercício 1

v1 = float(input("Qual o valor do cigarro que você fuma? \n"))
anos = float(input("Há quantos anos você fuma? \n"))
quantidade = float(input("Quantos cigarros você fuma por dia?\n "))

valor = (v1/20)*quantidade*365*anos

print("Você já gastou um total de R$",valor)

# Exerc’cio 2

custo = float(input("Qual o custo de fábrica do carro? \n"))

impostocarro = custo*0.45
lucro = custo*0.12
valortotal = custo + impostocarro + lucro

print("O valor do carro para o consumidor é de: R$ ", valortotal)

# exercício 3

n1 = float(input("Entre com a nota da primeira prova \n "))
n2 = float(input("Entre com a nota da segunda prova \n "))
n3 = float(input("Entre com a nota da terceira prova \n "))
media = (n1+n2+n3)/3
faltas = int(input("Quantas faltas o aluno tem? \n"))
if(faltas >=15):
    print("REPROVADO POR FALTA!")
else:
    if(media >= 6):
        print("APROVADO!")
    elif(media >=3):
        print("RECUPERAÇÃO!")
    else:
        print("REPROVADO!")

#exercício 4

n1 = float(input("Insira 3 números reais e veremos se o primeiro é maior que a soma dos outros dois. \n \n Insira o primeiro número: \n"))
n2 = float(input("Insira o segundo número: \n"))
n3 = float(input("Insira o terceiro número: \n"))

if(n1 > n2 + n3):
    print("É maior que a soma dos outros 2!")
else:
    print("Não é maior que a soma dos outros dois!")    

#exercício 5

produto = input("Digite o nome do produto: \n ")
descricao = input("Digite a descrição do produto: \n ")
preco = float(input("Digite o preço do produto: \n "))
validade = input("Digite a validade do produto: \n ")

print("\nDados do produto:")
print("Nome:", produto)
print("Descrição:", descricao)
print("Preço: R$",preco)
print("Validade:", validade)

# exercício 6

total = 0
for num in range(1, 101):
    total += num
print("A soma total dos números de 1 a 100 é: \n", total)

# exercício 7

n = int(input("Entre com um número para descobrirmos a sua tabuada: \n "))
for num in range(1, 11): 
    resultado = n * num
    print(n,"x", num, "=", resultado)
    
# exercício 8

tot_ele = int(input("Digite o número total de eleitores: \n "))
vb = int(input("Digite o número de votos brancos: \n"))
vn = int(input("Digite o número de votos nulos: \n"))
vv = int(input("Digite o número de votos válidos: \n"))

perc_b=((vb/tot_ele)*100)
perc_n=((vn/tot_ele)*100)
perc_v=((vv/ tot_ele)*100)

print("Percentual de votos brancos: \n", perc_b, "%")
print("Percentual de votos nulos: \n", perc_n, "%")
print("Percentual de votos válidos: \n", perc_v, "%")

# exercício 9

v1=int(input("Digite um número: \n"))
if (v1<0):
    print("Esse número é negativo")

else:
    print("Esse número é positivo")

#exercício  10

hrs_sem=40
hrs_mes=160

hrs_trab_mes=float(input("Horas trabalhadas no mês: \n"))
sal_hrs=float(input("Salário por hora: \n"))

if (hrs_trab_mes<hrs_mes):
    sal_total = hrs_trab_mes*sal_hrs
    
else:
    hrs_extra=hrs_trab_mes-hrs_mes
    sal_extra=hrs_extra*(sal_hrs*1.5)
    sal_total =+ sal_extra

print("Salário total: \n", sal_total)

# exercício 11

sal_fixo = float(input("Digite o salário fixo do vendedor: \n"))
valor_venda = float(input("Digite o valor das vendas feitas pelo vendedor:  \n"))

comissao = min(valor_venda, 1500) * 0.03  
comissao_bonus= max(valor_venda - 1500, 0) * 0.05  
comissao_total = comissao + comissao_bonus  
sal_total = sal_fixo + comissao_total  

print("O salário do vendedor é de:", sal_total)


# exercício 12

qtd_atual=int(input("Quantidade atual em estoque:\n"))
qtd_max=int(input("Quantidade máxima em estoque:\n"))
qtd_min=int(input("Quantidade mínima em estoque:\n"))

qtd_media=(qtd_max+qtd_min)/2

if (qtd_atual>=qtd_media):
    print("Não efetuar compra")
    
else:
    print("Efetuar compra")

#exercício 13 
n1 = float(input("Digite o primeiro número: "))
n2 = float(input("Digite o segundo número: "))
n3 = float(input("Digite o terceiro número: "))

soma_maiores_numeros = n1+n2+n3 - min(n1+n2+n3)

print("A soma dos 2 maiores valores é:", soma_maiores_numeros)


# exercício 14

time1=str(input("Nome do primeiro time:\n"))
gols1=int(input("Quantos gols ele marcou?\n"))
time2=str(input("Nome do segundo time:\n"))
gols2=int(input("Quantos gols ele marcou?\n"))

if (gols1>gols2):
    print( "O vencedor foi: ",time1)
    
elif(gols1>gols2):
    print("O vencedor foi: ",time2)
    
else:
    print("EMPATE!")
               
#exercício 15

preco_gasolina = 4.89
preco_alcool = 3.39


lts_vendidos = float(input("Digite o número de litros vendidos: "))
combustivel = str(input("Digite o tipo de combustível (A para álcool, G para gasolina): "))

if combustivel.upper() == A:
    if lts_vendidos <= 20:
        desc_por_lto = 0.03
    else:
        desc_por_lto = 0.05 
    valor_total = lts_vendidos * (preco_alcool - (preco_alcool * desc_por_lto))
else: 
    combustivel.upper() == G
    if lts_vendidos <= 20:
        desc_por_lto = 0.04  
    else:
        desc_por_lto = 0.06  
    valor_total = lts_vendidos * (preco_gasolina - (preco_gasolina * desc_por_lto))

#exercício 16

cod_empregado = int(input("Digite o código do empregado: \n"))
ano_nasc = int(input("Digite o ano de nascimento do empregado: \n"))
ano_ing_emp = int(input("Digite o ano de ingresso na empresa do empregado: \n"))


idade = 2024 - ano_nasc
tempo_trabalho = 2024 - ano_ing_emp


if idade >= 65 or tempo_trabalho >= 30 or (idade >= 60 and tempo_trabalho >= 35):
    mensagem = 'Requerer aposentadoria'
else:
    mensagem = 'Não requerer'

print("Idade do empregado:", idade, "anos")
print("Tempo de trabalho na empresa:", tempo_trabalho, "anos")
print("Resultado:", mensagem)

 #exercício 17

cont = 0
while(cont<10):
    cont=cont+1
    print(cont,"\n")

#exercício 18

cont=11
while(cont>0):
    cont=cont-1
    print(cont,"\n")

#exercício 19

qtd_neg = 0

for num in range(100):
    valor = float(input("Digite um valor: "))
    if valor < 0:
        qtd_neg += 1


print("Quantidade de valores negativos:", qtd_neg)


#exercício 20

v1=int(input("Digite um valor: "))
v2=int(input("Digite um valor: "))
v3=int(input("Digite um valor: "))
v4=int(input("Digite um valor: "))
v5=int(input("Digite um valor: "))
v6=int(input("Digite um valor: "))

soma=v1+v2+v3+v4+v5+v6

print("O resultado é: ",soma)
    
         





    





    

    
