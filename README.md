# 📘 Fundamentos da Biblioteca NumPy

Bem-vindo ao repositório de estudo do curso de **Fundamentos da biblioteca NumPy**. 
Este material cobre a base essencial para computação científica e manipulação de dados em Python.

> **Status do Projeto:** 🚧 Branch: `topico1` (Fundamentos Iniciais)

---

## 📋 Tabela de Conteúdos

1. [Conhecer a biblioteca e nossos dados](#1-conhecer-a-biblioteca-e-nossos-dados)
2. [Exploração dos dados](#2-exploração-dos-dados)
3. [Operação entre arrays](#3-operação-entre-arrays)
4. [Números aleatórios](#4-números-aleatórios)

---

## 1. Conhecer a biblioteca e nossos dados

O **NumPy** (Numerical Python) é a base para a Ciência de Dados em Python. Sua principal estrutura é o `ndarray` (N-dimensional array), que é mais eficiente que as listas nativas do Python.

### Conceitos Chave:
* **Importação:** `import numpy as np`
* **Performance:** Arrays são armazenados em blocos contíguos de memória.
* **Tipagem:** Arrays são homogêneos (todos os elementos têm o mesmo tipo).

```python
import numpy as np

# Lista Python (lenta, tipos mistos)
lista = [1, 2, 3]

# Array NumPy (rápido, tipagem estática)
array = np.array(lista)

print(array)        # [1 2 3]
print(array.dtype)  # int64 (ou int32 dependendo do sistema)


2. Exploração dos dados
Antes de manipular dados, é necessário entender a "forma" (shape) da matriz. Isso evita erros de dimensionalidade em algoritmos de IA.

Atributos Principais:
.shape: Retorna uma tupla com (linhas, colunas).

.ndim: Retorna o número de dimensões (ex: 1D, 2D, 3D).

.size: Retorna o número total de elementos.

Python

dados = np.array([
    [10, 20, 30],
    [40, 50, 60]
])

print(f"Formato: {dados.shape}")   # (2, 3) -> 2 linhas, 3 colunas
print(f"Dimensões: {dados.ndim}")  # 2
3. Operação entre arrays
O maior poder do NumPy é a Vetorização. Ela permite realizar cálculos matemáticos em todo o array de uma vez, sem a necessidade de laços for explícitos.

Funcionalidades:
Aritmética: Soma, subtração, multiplicação e divisão direta entre arrays.

Estatística: Métodos otimizados como .mean(), .sum(), .max().

Python

custo = np.array([10, 20])
venda = np.array([15, 30])

# Operação vetorizada (elemento a elemento)
lucro = venda - custo 
print(lucro) # [5 10]

# Média
print(f"Média de Venda: {venda.mean()}")
4. Números aleatórios
A geração de números aleatórios é crucial para inicializar pesos em redes neurais, dividir datasets e criar simulações. O sub-módulo numpy.random gerencia isso.

Funções Principais:
np.random.seed(): Garante reprodutibilidade (gera sempre os mesmos números).

np.random.rand(): Gera números float entre 0 e 1.

np.random.randint(): Gera números inteiros em um intervalo.

Python

np.random.seed(42)

# Gera 3 números entre 0 e 1
print(np.random.rand(3)) 

# Gera 5 inteiros entre 10 e 100
print(np.random.randint(10, 100, 5))            "# curso_matematica_IA" 
