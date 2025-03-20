# revisao2Python

def matriz(linhas, colunas):
    matrizOficial =[]
    qtd = 1
    for i in range(linhas):
        linhas =[]
        for j in range(colunas):
            linhas.append(qtd)
            qtd += 1
        matrizOficial.append(linhas)
    return matrizOficial

print(matriz(3,2))


m = [[1,2,3], [4,5,6], [7,8,9]]
def soma_matriz(m):
    soma = 0
    for i in range(len(m)):
        for j in range(len(m[0])):
            soma += m[i][j]
    return soma
print(soma_matriz(m)) #o parametro é a própria matriz

#transposta
def transposta(m):
    t = []
    for j in range(len(m[0])):
        linhas = []
        for i in range(len(m)):
            linhas.append(m[i][j])
        t.append(linhas)
    return t
print(transposta(m))

#calcular a soma de cada linha & coluna da matriz e armazenar em lista
m = [[1,2,3], [4,5,6], [5,8,9]]
def soma_linha(m):
    soma = 0
    resultado = []
    for i in range(len(m)):
        soma = 0
        for j in range(len(m)):
            soma += m[i][j]
        resultado.append(soma)
    return resultado
print(soma_linha(m))

def soma_coluna(m):
    soma = 0
    resultado = []
    for i in range(len(m[0])):
        soma = 0
        for j in range(len(m[0])):
            soma += m[j][i]
        resultado.append(soma)
    return resultado
print(soma_coluna(m))

#cada coluna da matriz e armazenar em lista
#da diagonal principal
def diagonal_matriz(m):
    soma = 0
    for i in range(len(m)):
        linhas=[]
        soma += m[i][i]
        linhas.append(soma)
    return soma
print(diagonal_matriz(m))
#da diagonal secundária????

def diagonalsec_matriz(m):
    soma = 0
    for i in range(len(m)):
        linhas=[]
        soma += m[i][len(m)-1-i]
        linhas.append(soma)
    return soma
print(diagonalsec_matriz(m))


#A matriz identidade é uma matriz quadrada onde os elementos da diagonal principal são iguais a 1
# e os demais são iguais a 0.

matriz = [[1,0,0], [0,1,0]]
def identidade(matriz):
    for i in range(len(matriz)):
        for j in range(len(matriz[0])):
            if matriz[i][i] != 1 and matriz[j] != 0:
                return False
    return True
print(identidade(matriz))

#simetrica (tem que ser igual a transporta ???
def simetrica(m):
    for i in range(len(m)):
        for j in range(len(m[0])):
            if m[i][j] != m[j][i]: #if m != transposta(m) para conferir
                return False
    return True

print(simetrica(m))

#dado uma matriz de 0 e 1, crie uma função que conte quantos vizinhos 1 um determinado elemento m[i][j] tem
