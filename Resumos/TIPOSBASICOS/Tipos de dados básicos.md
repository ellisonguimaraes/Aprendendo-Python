# Tipos de dados básicos e operadores booleanos, aritméticos, comparação e lógicos

Nesta sessão veremos os tipos básicos e operadores do Python. Os tipos de dados básicos do Python são:

- `int`: Que representa os inteiros.
- `float`: Representa os números decimais.
- `boolean`: Representa os lógicos `True` e `False`.
- `string`: Representa as strings/textos.
- `complex`: Representa números complexos. (Contém um j no final: `x = 11j`).



E os operadores em Python são:

- Aritméticos: Responsáveis por cálculos matemáticos.
- Atribuição: Responsável por atribuir um valor a uma variável.
- Booleanos: Como deve ser feita a combinação entre os termos ou expressões(`and`, `or`, `not`).
- Comparativos: Comparações entre variáveis/valores. 



> Os operadores booleanos e comparativos estão entre o conteúdo **Booleano** por retornarem um valor **booleano**. Assim como os operadores aritméticos para o conteúdo **Numéricos** abaixo.





## Numéricos

Os tipos numéricos em Python se resume a três, o `int`, o `float` e o `complex`. Declaramos da seguinte forma: 



> ***Declaração:***
>
> ```python
> >>> i = 21
> >>> f = 3.1415
> >>> c = 3.14j
>  
> >>> i
> 21
> 
> >>> f
> 3.1415
> 
> >>> c
> 3.14j
> ```

O número complexo necessita de um `j` no final da declaração.



> **Features Python 3**
>
> Ao inicializar um número inteiro, o Python facilitou ao adicionar o underscore. Agora você pode declarar o número da seguinte forma:
>
> ```python
> x = 1_000_000_000_000
> y = 1000000000000
> ```
>
> Isso foi implementado somente para a leitura humana ficar mais fácil. No intuito de você conseguir entender qual o número que foi digitado e nada mais além disso.



### Operadores aritméticos

Há os seguintes operadores aritméticos em Python: 

| Descrição        | Operador | Exemplo |
| ---------------- | -------- | ------- |
| Soma             | +        | 15 + 5  |
| Subtração        | -        | 15 - 5  |
| Multiplicação    | *        | 15 * 5  |
| Divisão          | /        | 15 / 5  |
| Potenciação      | **       | 15 ** 2 |
| Resto da divisão | %        | 15 % 2  |
| Divisão inteira  | //       | 15 // 2 |



### Operadores de atribuição

Há os seguintes operadores de atribuição no Python:

| Descrição                       | Operador    | Resultante       |
| ------------------------------- | ----------- | ---------------- |
| Atribuição com soma             | x += 5      | x = x + 5        |
| Atribuição com subtração        | x -= 5      | x = x - 5        |
| Atribuição com multiplicação    | x*= 2       | x = x * 2        |
| Atribuição com divisão          | x /= 2      | x = x / 2        |
| Atribuição com potenciação      | x **= 2     | x = x ** 2       |
| Atribuição com resto da divisão | x %= 2      | x = x % 2        |
| Atribuição com divisão inteira  | x //= 2     | x = x // 2       |
| Atribuição normal               | x = 259     | x = 259          |
| Atribuição múltipla             | a, b = 5, 9 | a = 5<br />b = 9 |





## Boleanos

As variáveis booleanas representam `True` ou `False`, verdadeiro ou falso respectivamente.

> ***Declaração:***
>
> ```python
> Ativado = True
> Autenticado = False
> 
> if(Ativado and Autenticado):
>     pass
> ```



### Operadores booleanos

Em Python os operadores booleanos são:

| Descrição | Operador | Exemplo         |
| --------- | -------- | --------------- |
| E         | and      | `True and True` |
| OU        | or       | `True or False` |
| NOT       | not      | `not Ativo`     |

> ***Exemplos:***
>
> ```python
> >>> Ativo = True
> >>> Autenticado = False
> 
> >>> not Ativo
> False
> 
> >>> not Autenticado
> True
> 
> >>> not(Ativo)
> False
> 
> >>> Ativo and Autenticado
> False
> 
> >>> Ativo or Autenticado
> True
> ```

Observe que o operador `not` também pode ser usado entre parênteses `not(True)`.



### Operadores de comparação

Em Python, os operadores de comparação não são diferentes:

| Descrição   | Operador | Exemplo  |
| ----------- | -------- | -------- |
| Maior       | >        | 15 > 10  |
| Maior igual | >=       | 15 >= 15 |
| Menor       | <        | 14 < 12  |
| Menor Igual | <=       | 14 <= 12 |
| Igual       | ==       | 14 == 12 |
| Diferente   | !=       | 14 != 12 |







## String

Vamos agora falar um pouco sobre *strings* em *python*. *String* em *python* é tudo o que é delimitado por: 

- Aspas simples: `'Hello World'`
- Aspas duplas: `"Hello World"`
- Aspas simples tripla: `'''Hello World'''`
- Aspas duplas tripla: `"""Hello World"""`



> ***Obs:*** Geralmente as *strings* declaradas com aspas triplas são para múltiplas linhas:
>
> ```python
> >>> poema = """Quando te vi de longe
> Jurei amor eterno
> Quando te vi de perto
> Vai ser feio assim
> Lá no inferno!"""
> 
> >>> print(poema)
> Quando te vi de longe
> Jurei amor eterno
> Quando te vi de perto
> Vai ser feio assim
> Lá no inferno!
> ```
>
> As aspas triplas respeitam as quebras de linha, assim, imprimindo da mesma maneira digitada.



> ***Algumas dicas: Caracteres de escape***
>
> Não é possível fazer `'Camila's Restaurant'` pois há um `'` dentro da delimitação de string `''`.  Assim também acontece com aspas duplas.
>
> Para resolver esse problema, podemos delimitar a string com aspas duplas e utilizar as aspas simples no interior: `"Camila's Restaurant"`. Ainda, ao contrário: `'Esse é "um" exemplo.'`. 
>
> Além dessa solução, há os caracteres de escape:
>
> | Caractere | Descrição            |
> | --------- | -------------------- |
> | `\'`      | Aspas simples        |
> | `\"`      | Aspas duplas         |
> | `\\`      | Barra invertida      |
> | `\t`      | Tabulação horizontal |
> | `\n`      | Quebra de linha      |
>
> Com os caracteres de escape você pode manter o primeiro exemplo, porém, com uma barra invertida: `'Camila\'s Restaurant'`.



### Slices (fatia)

*Slice* assim como o nome já sugere, podemos fazer fatias das string através dos seus índices. **Como assim?** 

Temos uma *string* `nome = "Ellison William"` e queremos somente a parte `William`. Sabemos que o índice da primeira letra começa em 8 e termina em 14, então é só usarmos a *sintax* `nome[inicio:fim:pulos]`, que no nosso caso se torna `nome[8:15]` ou simplesmente `nome[8:]`. 

- Quando você omite o `inicio`, então automaticamente começa do início  
- Quando você omite o `fim`, então automaticamente termina no fim da palavra.
- Quando você omite os pulos, por padrão é 1.
- Quando você omite tudo `nome[:]` ele cria uma cópia nova de toda a palavra.
- Quando o pulo é negativo, retorna a string invertida: `nome[::-1]`.
- O `fim` deve ser o índice do fim + 1, já que é um intervalo aberto.



***Veremos alguns exemplos:***

```python
>>> nome = "Ellison William"

>>> nome[::-1]
'mailliW nosillE'

>>> nome[0:len(nome):2]
'ElsnWlim'

>>> nome[:7]
'Ellison'

>>> nome[:8]
'Ellison '

>>> nome[8:]
'William'
```



### Métodos para manipulação

O *python* há diversos métodos para a manipulação de *string*. Dando um `dir('')` podemos observar todos eles: 

```python
>>> dir('')
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
```

A seguir verá a tabela com alguns desses métodos mais usados:

| Descrição                                                    | Método                            | Exemplo IIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIII |
| ------------------------------------------------------------ | --------------------------------- | ------------------------------------------------------------ |
| Transformar a string em minúscula                            | `.lower()`                        | `>>> "Hello World".lower()`<br />`'hello world'`             |
| Transformar a string em maiúscula                            | `.upper()`                        | `>>> "Hello World".upper()`<br />`'HELLO WORLD'`             |
| Remove espaços em branco dos extremos                        | `.strip()`                        | `>>> ' Ellison   W.  '.strip()`<br />`Ellison   W.`          |
| Remove espaços em branco a esquerda                          | `.lstrip()`                       | `>>> "  Ellison  W.  ".lstrip()`<br/>`'Ellison  W.  '`       |
| Remove espaços em branco a direita                           | `.rstrip()`                       | `>>> "  Ellison  W.  ".rstrip()`<br/>`'  Ellison  W.'`       |
| Troca todos os valores A de uma string, por um valor B.      | `.replace(a,b)`                   | `>>> x = 'O Rato Roeu a Roupa do Rei de Roma'`<br/>`>>> x.replace('R', 'Pr')`<br/>`'O Prato Proeu a Proupa do Prei de Proma'` |
| Divide a string em substrings se encontrar instâncias do separador `a`. | `.split(a)`                       | `>>> x = 'O Rato Roeu'`<br/>`>>> x.split()`<br/>`['O', 'Rato', 'Roeu']`<br />`>>> y = 'Maça, banana, manga'`<br/>`>>> y.split(',')`<br/>`['Maça', ' banana', ' manga']`<br />`>>> z = 'Maça!!Banana!!Manga'`<br/>`>>> z.split('!!')`<br/>`['Maça', 'Banana', 'Manga']` |
| Retorna o número de vezes que um valor especificado ocorre em uma string | `.count(str)`                     | `>>> x = "O rato roeu a roupa do rei de roma"`<br/>`>>> x.count('ro')`<br />`3` |
| Pesquisa a string por um valor especificado e retorna a posição de onde foi encontrada | `.find(str)`<br />`.index(str)`   | `>>> x = "O rato roeu a roupa do rei de roma"`<br />`>>> x.find('ro')`<br />`7`<br />`>>> x.index('ro')`<br />`7` |
| Pesquisa a string por um valor especificado e retorna a última posição de onde foi encontrada | `.rfind(str)`<br />`.rindex(str)` | `>>> x = "O rato roeu a roupa do rei de roma"`<br/>`>>> x.rfind('ro')`<br/>`30`<br />`>>> x.rindex('ro')`<br />`30` |



A seguir alguns outros métodos: 

| Método           | Descrição                                                    |
| :--------------- | :----------------------------------------------------------- |
| `isalnum()`      | Retorna `True` se todos os caracteres da string forem alfanuméricos |
| `isalpha()`      | Retorna `True` se todos os caracteres da string estiverem no alfabeto |
| `isdecimal()`    | Retorna `True` se todos os caracteres na string forem decimais |
| `isdigit()`      | Retorna `True` se todos os caracteres na string forem dígitos |
| `isidentifier()` | Retorna `True` se a string for um identificador              |
| `expandtabs()`   | Define o tamanho do tab da string                            |
| `islower()`      | Retorna `True` se todos os caracteres da string estiverem em minúsculas |
| `isnumeric()`    | Retorna `True` se todos os caracteres da string forem numéricos |
| `isprintable()`  | Retorna `True` se todos os caracteres na string forem imprimíveis |
| `isspace()`      | Retorna `True` se todos os caracteres na string forem espaços em branco |
| `istitle()`      | Retorna `True` se a string segue as regras de um título      |
| `isupper()`      | Retorna `True` se todos os caracteres da string forem maiúsculos |
| `capitalize()`   | Converte o primeiro caractere em maiúsculo                   |
| `title()`        | Converte o primeiro caractere de cada palavra em maiúscula   |
| `splitlines()`   | Divide a string nas quebras de linha e retorna uma lista     |
| `startswith()`   | Retorna `True` se a string começar com o valor especificado  |
| `endswith()`     | Retorna `True` se a string terminar com o valor especificado. |
| `swapcase()`     | Troca de casos, minúsculas, maiúsculas e vice-versa          |
| `join()`         | Junta os elementos de um iterável ao final da string         |
| `zfill()`        | Preenche a string com um número especificado de 0 no início  |
| `casefold()`     | Converte string em letras minúsculas                         |
| `encode()`       | Retorna uma versão codificada da string                      |
| `translate()`    | Retorna uma string traduzida                                 |
| `maketrans()`    | Retorna uma tabela de tradução a ser usada nas traduções     |
| `partition()`    | Retorna uma tupla onde a string é dividida em três partes    |
| `rpartition()`   | Retorna uma tupla onde a string é dividida em três partes    |
| `rsplit()`       | Divide a string no separador especificado e retorna uma lista |
| `ljust()`        | Retorna uma versão justificada à esquerda da string          |
| `rjust()`        | Retorna uma versão justificada à direita da string           |
| `center()`       | Retorna uma string centrada                                  |

Para mais informações dos métodos aqui citados, acesse a página da W3S Schools: [Python String Methods](https://www.w3schools.com/python/python_ref_string.asp).








## Type

A função `type()` retorna o tipo da variável informada por parâmetro. 

> ***Exemplo:***
>
> ```python
> >>> a = 18
> >>> b = 3.1415
> >>> c = "Hello World"
> >>> d = True
> 
> >>> type(a)
> <class 'int'>
> 
> >>> type(b)
> <class 'float'>
> 
> >>> type(c)
> <class 'str'>
> 
> >>> type(d)
> <class 'bool'>
> 
> >>> type(a) == type(b)
> False
> 
> >>> type(a) == type(1)
> True
> ```







