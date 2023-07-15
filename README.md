# Exercicio056.py

somaidade = 0
mediaidade = 0
maioridadehomem = 0
nomevelho = 0
totmulher20 = 0
for p in range(1,5):
    nome = str(input('Digite o nome da pessoa: ')).strip()
    idade = int(input('Digite a idade da pessoa:'))
    sexo = str(input('Sexo: [M/F]:')).strip()
    somaidade += idade
    if p == 1 and sexo in 'Mm':
        maioridadehomem = idade
        nomevelho = nome
    if sexo in 'Mm' and idade > maioridadehomem:
        maioridadehomem = idade
        nomevelho = nome
    if sexo in 'fF' and idade < 20:
        totmulher20 += 1

mediaidade = somaidade / 4
print('A media do grupo é:',mediaidade)
print('O mais velho tem {} e se chama {}'.format(maioridadehomem, nomevelho))
print('Sao {} mulheres com menos de 20 anos')
