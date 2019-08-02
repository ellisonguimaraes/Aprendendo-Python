# Entrada e Saída de Dados



## Print (Saída de dados)

A função `print` é responsável por imprimir uma mensagem na tela. Iremos ver nesse  tutorial como formatar as mensagens de saída. 

A instrução `print` funciona da seguinte maneira:

> ```python
> print("Hello World!")
> print('Tudo bem com você?')
> ```

Dentro dos parênteses é digitado a mensagem em aspas simples ou aspas duplas.





### Formatando variáveis na instrução

Existem diversas formas de formatar o `print` para receber variáveis. Vamos ver alguma delas a seguir. 



#### Formatted String Literals

A forma mais nova de formatar uma string, para usar deve-se usar o prefixo `f` antes das aspas e para referenciar uma variável dentro das aspas é necessário usar o formato: `{n:e.cT}`, onde:

- `n`: Nome identificador da variável
- `e`: Quantidade de espaço desejado para a impressão daquela variável
- `c`: Quantidade de casas decimais
- `T`: Tipo da impressão. (`f` para *float*, `d` para inteiro, `s` para string)



Lembrando, que nesse formato a única coisa obrigatória é o `n` e todos os outros (`e`, `c`, `T`) opcionais.

> ***Exemplos:***
>
> ```python
> >>> import math as m
> 
> >>> print(f"O pi é: {m.pi:10.3f}")
> O pi é:      3.142
>     
> >>> idade = 21
> >>> print(f"Você tem {idade} anos.")
> Você tem 21 anos.
> 
> >>> print(f"Você tem {idade:10} anos.")
> Você tem         21 anos.
> 
> >>> table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}
> >>> for name, phone in table.items():
> 		print(f'{name:10} ==> {phone:10d}')
> 
> Sjoerd     ==>       4127
> Jack       ==>       4098
> Dcab       ==>       7678
> 
> ```



#### .format()

Basicamente, é usado a `str.format()`. O formato usado entre `{}` segue o padrão da anterior, porém, o `n` não é mais o nome da variável e sim o número do índice dos argumentos do `.format(0, 1, 2, ..., n)`.



A seguir veremos alguns exemplos:

> ***Exemplo:***
>
> ```python
> >>> print("{} + {} = {}".format(5, 3, 8))
> 5 + 3 = 8
> 
> >>> print("{0} + {1} = {2}".format(5, 3, 8))
> 5 + 3 = 8
> 
> >>> print("{1} + {0} = {2}".format(5, 3, 9))
> 3 + 5 = 9
> 
> >>> print("{nome} tem {idade} anos.".format(nome="Ellison", idade=21))
> Ellison tem 21 anos.
> 
> >>> print("O pi é: {0:.3f}".format(m.pi))
> O pi é: 3.142
> ```



#### Formatação antiga

Usada no Python 2, mas que ainda é utilizada em larga escala. A formatação dela dentro da string se assemelha aos anteriores, porém é delimitado pelo `%` no inicio. 

Já no final da string é usado um `%var` ou `%(var1, var2, var3)` para múltiplas variáveis.

> ***Exemplos:***
>
> ```python
> >>> print("O pi é: %10.3f" % m.pi)
> O pi é:      3.142
> 
> >>> print("Meu nome é %s e eu tenho %d anos." %("Ellison", 19))
> Meu nome é Ellison e eu tenho 19 anos.
> ```





## Input (Entrada de dados)

A entrada de dados no Python é feita pela função `input()` de forma fácil:

> ***Exemplo:***
>
> ```python
> nome = input("Digite seu nome: ")
> ```

Nesse caso o `input()` retorna a string digitada para a variável nome. 



> Pode usar as *strings* de formatação vistas no `print` no `input`?
>
> ```python
> >>> nome = "Ellison"
> >>> idade = int(input(f"{nome}, digite sua idade: "))
> Ellison, digite sua idade: 21
> ```
>
> Sim. Pode!



Toda leitura feita por `input` retorna uma string. É necessário o uso de **CASTING** para a conversão para outros tipos de dados.



### Casting

O **CAST** é usado para converter tipos de dados em outro. O `input` por exemplo, retorna sempre uma string. E quando for necessário receber um inteiro ou um float? 

- `int(var)`: Converte uma variável para inteiro. (Se *var* for do tipo float, o número é truncado).
- `float(var:` Converte uma variável em float.
- `str(var):` Converte uma variável em string.



> ***Exemplo:***
>
> ```python
> >>> int(m.pi)
> 3
> 
> >>> float(15)
> 15.0
> 
> >>> str(1.568)
> '1.568'
> ```