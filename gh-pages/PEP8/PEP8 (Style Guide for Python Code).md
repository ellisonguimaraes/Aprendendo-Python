# PEP8 (Style Guide for Python Code)

O *PEP*8 é uma convenção para a escrita de códigos *python*. Algumas regras devem ser seguidas para facilitar a compreensão dos códigos.

A seguir, discutimos sobre algumas regras: 



## *CamelCase* para o nome das classes

O nome das classes devem ter a primeira letra maiúscula e todas as outras minúsculas da palavra. Se tratar de palavras compostas, cada palavra segue a mesma ideia, a primeira letra maiúscula e as demais minúsculas. Além disso, não podem ser separadas por *underline* ( _ ) nem traços ( - ).



> ***Exemplo:***
>
> ```python
> class Calculadora:
>         pass
> 
> class CalculadoraCientifica:
>         pass
> ```





## Nome de variáveis e funções

O nome das variáveis e de funções devem ser totalmente minúsculas. E se tratar de palavras compostas, devem ser separadas por *underline*. 



> ***Exemplo:***
>
> ```python
> def soma():
> 	pass
> 
> def soma_dois():
>         pass 
> 
> numero_impar = 5
> 
> ```





## Indentação

Para a indentação, é necessário a utilização de 4 espaços. Não devem ser misturados **tab** com **espaço**.





## Linhas em branco entre instruções

Entre as instruções devem ter linhas de separação para legibilidade do código. 



### Declaração de classes, funções, métodos e fim de todas as instruções

As classes e funções devem conter 2 linhas em branco entre suas declarações, ou seja, se você declarou uma classe A e deseja declarar a classe B, é necessário que você pule duas linhas para declarar a classe B.

Além disso, dentro da classe entre métodos, deve-se ter a distância de 1 espaço no fim do arquivo. 



> ***Exemplo:***
>
> ```python
> class A:
>     def __init__(self):
>         print("Estou dentro da classe.")
> 	#1
>     def hi_print(self, name):
>         print(f"Oi {name}!")
> #1	
> #2	
> def B():
> 	pass
> #1
> #2
> test = A()
> test.hi_print("Ellison")
> #1
> ```



Podemos observar distância de 2 espaços entre a classe A e classe B, e entre os métodos `__init__` e `hi_print` distância de 1.

No final do arquivo, a última linha não pode ser uma instrução, deve ser uma linha em branco.



### Importação

`Imports` devem ser feitas em linhas separadas e antes de qualquer instrução, até mesmo de comentários.



> ***Exemplos***:
>
> ```python
> #Não fazer:
> import os, sys
> 
> #Correto:
> import os
> import sys
> 
> #É permitido fazer:
> from types import StringType, ListType
> 
> #Caso tenha muitos imports no caso acima:
> from types import (
> 	StringType,
>     ListType,
>     SetType,
>     OutroType
> )
> 
> #Evitar
> from sys import *
> ```



Deve-se evitar a última instrução, pois ela trás todas a funções da biblioteca para o contexto atual.





## Comprimento máximo de linha

Devido ao tamanho da tela e dos editores, a *PEP8* limita a quantidade de **79 colunas** a uma linha. Caso a instrução ultrapasse esse limite é usado a barra invertida (**\\**) para a continuação na linha posterior.

Caso a instrução seja separada por vírgulas, pode ser feita a quebra de linha sem a necessidade de colocar a barra invertida.

**Para comentários é limitada em 72 colunas.**



> ***Exemplo:***
>
> ```python
> class Rectangle(Blob):
>     def __init__(self, width, height,
>         color='black', emphasis=None, highlight=0):
>         if width == 0 and height == 0 and \
>             color == 'red' and emphasis == 'strong' or \
>             highlight > 100:
>             raise(ValueError, "sorry, you lose")
> 
>         if width == 0 and height == 0 and (color == 'red' or 
>                                            emphasis is None):
>             raise ValueError, "I don't think so"
>             
>         Blob.__init__(self, width, height,
>                       color, emphasis, highlight)
> 
> ```





## Quando usar *underscores* nos nomes

Os *underscores* são usados em nomes nos seguintes casos:

- `_underscore_no_inicio`: Costuma indicar que o atributo é de uso interno, ou seja, quando usado um `from sys import *` não importam objetos cujo o nome começam com underline _.
- `underscore_no_fim_`: usado para evitar conflitos com palavras-chave. Por
  exemplo: `Tkinter.Toplevel(master, class _='ClassName')`. 
- `__dois_underscore_no_inicio`: Atributo privado de classe.
- `__dois_underscore_no_inicio_e_no_fim__`: Atributos ou objetos especiais. `__init__`, `__import__` ou `__file__`.





## Comparações com Singletons

Singletons como o `None`, `True` e `False` devem sempre ser feitas com `is` ou `is not`.



> ***Exemplo:***
>
> ```python
> x = None
> 
> if x is not None:
> 	print("Não é None!")
> ```





## Conclusão

Podemos utilizar essas regras básicas para escrever um código cada vez mais legível para diversos programadores.

Além dessas, existem outras regras que podem ser encontradas em [Python.org](https://www.python.org/dev/peps/pep-0008/).

