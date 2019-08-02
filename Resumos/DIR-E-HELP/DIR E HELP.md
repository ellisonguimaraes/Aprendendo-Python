# DIR E HELP

As funções `dir` e `help` são de grande ajuda, não somente para iniciantes como também para quem já programa em *python*. O propósito é obter informações sobre determinado tipos, classes ou funções.

Essas funções geralmente são usadas no modo interativo, somente para obter informações rápidas.



## DIR

O `dir()` retorna todas as propriedades e métodos do objeto especificado. Vamos tentar entender através de exemplos:



> ***Exemplos:***
>
> Pode pode exemplo, usar o `dir` para obter informações dos métodos do `int` ou `input`:
>
> ```python
> >>> dir(int)
> ['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__', '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__', '__float__', '__floor__', '__floordiv__', '__format__', '__ge__', '__getattribute__', '__getnewargs__', '__gt__', '__hash__', '__index__', '__init__', '__init_subclass__', '__int__', '__invert__', '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__', '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__', '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__', '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'numerator', 'real', 'to_bytes']
> 
> >>> dir(input)
> ['__call__', '__class__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__name__', '__ne__', '__new__', '__qualname__', '__reduce__', '__reduce_ex__', '__repr__', '__self__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__text_signature__']
> ```
>
> Ou, caso você tenha importado uma biblioteca, poderá saber quais métodos ela implementa:
>
> ```python
> >>> import math as ma
> 
> >>> dir(ma)
> ['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
> ```
>
> Se você precisar saber todos os métodos utilizados para string:
>
> ```python
> >>> dir("Hello World")
> 
> ['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
> ```



E assim, você pode obter quais métodos/funções estão disponível para aquele tipo de dado.





## HELP

Com o `dir()` você obtém todos os métodos que aquele tipo de dado tem, mas e se você precisar saber o que aquele método/função faz?

Para isso temos o `help()`. Ele nos fornece uma breve explicação de como implementa e do que faz aquele método/função específica. 



> ***Exemplo:***
>
> Nos exemplos do `dir` obtemos informações dos métodos da biblioteca `math`. Com a função `help` agora podemos saber o que cada uma faz:
>
> ```python
> >>> import math as ma
> 
> >>> dir(ma)
> ['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
> 
> >>> help(ma.sqrt)
> 
> Help on built-in function sqrt in module math:
> sqrt(x, /)
>     Return the square root of x.
> >>> 
> ```
>
> Obtemos que na biblioteca `math` a função `sqrt` retorna a raiz do número passado por argumento.
>
> Podemos também, verificar o que faz o método `.lower()` do tipo de dados `string`:
>
> ```python
> >>> help("Hello World".lower)
> Help on built-in function lower:
> 
> lower() method of builtins.str instance
>     Return a copy of the string converted to lowercase.
> 
> >>> 
> ```



Com isso, a função `help()` nos auxilia quando necessitamos de informações sobre determinada função ou método disponível. 



## Conclusão

Com essas duas funções você poderá obter informações sem ter que pesquisar sobre o assunto, principalmente quando se trata de bibliotecas importadas. A rapidez é o que torna essas funções extremamente uteis.