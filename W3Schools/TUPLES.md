# Tuples

### Sumário:

- [Tuple](#tuple)
- [Itens Tuple](#itens-tuple)
- [Ordenação](#ordenação)
- [Imutável](#imutável)
- [Permite duplicatas](#permite-duplicatas)
- [Comprimento Tuple](#comprimento-tuple)
- [Crie Tuple com um item](#crie-tuple-com-um-item)
- [Itens Tuple - Tipos de dados](#itens-tuple---tipos-de-dados)
- [type()](#type)
- [O construtor tuple()](#o-construtor-tuple)
- [Coleções Python (Arrays)](#coleções-python-arrays)
---
- [Acessar itens de Tuple](#acessar-itens-de-tuple)
- [Indexação Negativa](#indexação-negativa)
- [Intervalo de Índices](#intervalo-de-índices)
- [Intervalo de Índices Negativos](#intervalo-de-índices-negativos)
- [Verifique se o item existe](#verifique-se-o-item-existe)
---
- [Alterar valores de Tuple](#alterar-valores-de-tuple)
- [Adicionar itens](#adicionar-itens)
- [Remover itens](#remover-itens)
---
- [Descompactando uma Tuple](#descompactando-uma-tuple)
- [Usando Asterisk *](#usando-asterisk)
---
- [Loops nos itens da Tuple](#loops-nos-itens-da-tuple)
- [Loops consultando os números de índice](#loops-consultando-os-números-de-índice)
- [Usando um loop while](#usando-um-loop-while)
---
- [Juntando duas Tuples](#juntando-duas-tuples)
- [Multiplicar Tuples](#multiplicar-tuples)
---
- [Métodos de Tuple](#métodos-de-tuple)

---

```
mytuple = ("apple", "banana", "cherry")
```

## Tuple

_Tuples_ são usadas para **armazenar vários itens** em uma _única variável_.

**Tuple** é um dos 4 _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**, os outros 3 são **``List``**, **``Set``** e **``Dictionary``**.

- Uma _Tuple_ é uma **coleção ordenada** e **imutável**.
- _Tuples_ são escritas entre **parênteses** ``()``.

```
# Criando uma 'tuple'

thistuple = ("apple", "banana", "cherry")
print(thistuple)  # Retorna: ('apple', 'banana', 'cherry')
```

## Itens Tuple

Os _itens da Tuple_ são **ordenados**, **imutáveis** e permitem **valores duplicados**.

Os _itens da Tuple_ são **indexados**, o _primeiro item_ possui **index** ``[0]``, o _segundo item_ possui **index** ``[1]`` etc.

## Ordenação

_Tuples_ são **ordenadas**, isso significa que os _itens_ tem uma _ordem definida_ e essa _ordem não mudará_.

## Imutável

_Tuples_ são **imutáveis**, o que significa que _não pode ser alterada_, **adicionar** ou **remover** _itens_ após a criação da _Tuple_.

## Permite duplicatas

- Como _Tuples_ são **indexadas**, elas podem ter _itens com o mesmo valor_:
    ```
    # Tuples permitem valores duplicados

    thistuple = ("apple", "banana", "cherry", "apple", "cherry")
    print(thistuple)  # Retorna: ('apple', 'banana', 'cherry', 'apple', 'cherry')
    ```

## Comprimento Tuple

Para determinar quantos _itens_ um _Tuple_ possui, basta utilizar a **função** ``len()``.

```
# Imprimindo o número de itens na Tuple

thistuple = ("apple", "banana", "cherry")
print(len(thistuple))  # Retorna: 3
```

## Crie Tuple com um item

- Para criar uma _Tuple_ com _apenas um item_, deve-se **adicionar uma vírgula (``,``) após o item**, caso contrário o Python _não reconhecerá como uma _Tuple_:
    ```
    # Tuple de 'um item', lembre-se da vírgula

    thistuple = ("apple",)
    print(type(thistuple))  # Retorna: <class 'tuple'>

    # Não é uma Tuple
    thistuple1 = ("apple")
    print(type(thistuple1))  # Retorna: <class 'str'>
    ```

## Itens Tuple - Tipos de dados

- Os _itens da Tuple_ podem ser de **qualquer tipo de dados**:
    ```
    # String
    tuple1 = ("apple", "banana", "cherry")

    # Int
    tuple2 = (1, 5, 7, 9, 3)

    # Boolean
    tuple3 = (True, False, False)
    ```

- Uma _Tuple_ pode conter **diferentes tipos de dados**:
    ```
    # Tuple com strings, ints e booleans
    tuple1 = ("abc", 34, True, 40, "male")
    ```

## ``type()``

Da perspectiva do Python, as _Tuples_ são definidas como **objetos** com o _tipo de dados_ ``tuple``.

```
<class 'tuple'>
```

```
mytuple = ("apple", "banana", "cherry")
print(type(mytuple))  # Retorna: <class 'tuple'>
```

## O construtor ``tuple()``

- É possível usar o **construtor** ``tuple()`` para _criar uma Tuple_:
    ```
    # Usando o método 'tuple()' para criar uma Tuple
    thistuple = tuple(("apple", "banana", "cherry"))  # Note os duplos parênteses.

    print(thistuple)  # Retorna: ('apple', 'banana', 'cherry')
    ```

## Coleções Python (Arrays)

Existem quatro _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**:

- ``List``: É uma _coleção ordenada_ e **mutável**. Permite _membros duplicados_.
- ``Tuple``: É uma _coleção ordenada_ e **imutável**. Permite _membros duplicados_.
- ``Set``: É uma _coleção não ordenada_, **imutável** e _não indexada_. Nenhum _membro duplicado_.
    - Os itens do ``Set`` não podem ser alterados, mas é possível remover e adicionar itens sempre que desejar.
- ``Dictionary``: É uma _coleção ordenada_ e **mutável**. Nenhum _membro duplicado_.

> Ao escolher um _tipo de dado integrado_ para **armazenar coleções de dados** é útil compreender as _propriedades_ desse tipo. Escolher o tipo certo para uma determinado conjunto de dados pode significar retenção de significado e um aumento na eficiência ou segurança.

---

## Acessar itens de Tuple

É possível _acessar itens_ da **Tuple** consultando o _número do índice_, entre **colchetes** (``[]``).

```
# Imprimindo o segundo item (1) da Tuple.

thistuple = ("apple", "banana", "cherry")
print(thistuple[1])  # Retorna: banana
```

> **Nota**: O _primeiro item_ possui **índice** ``0``.

## Indexação Negativa

_Indexação negativa_ significa **começar do fim**.

- ``-1`` refere-se ao _último item_, ``-2`` refere-se ao _penúltimo item_ etc:
    ```
    # Imprimindo o último item da Tuple

    thistuple = ("apple", "banana", "cherry")
    print(thistuple[-1])  # Retorna: cherry
    ```

## Intervalo de Índices

É possível _especificar um intervalo de índices_ especificando onde **começar** e onde **terminar** o _intervalo_.

Ao _especificar um intervalo_, o **valor de retorno** será uma _nova Tuple_ com os _itens especificados_.

```
# Imprimindo o terceiro, quarto e quinto item (2, 3, 4)

thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])  # Retorna: ('cherry', 'orange', 'kiwi')
```

> **Nota**: A _pesquisa_ começará no _índice_ ``2`` (**incluído**) e terminará no _índice_ ``5`` (**não incluído**).

> **Nota**: O _primeiro item_ possui **índice** ``0``.

- Ao **omitir** o _valor inicial_, o intervalo começará no _primeiro item_:
    ```
    thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
    print(thistuple[:4])  # Retorna: ('apple', 'banana', 'cherry', 'orange')
    ```

    > **Nota**: A _pesquisa_ começará no _índice_ ``0`` (**incluído**) e terminará no _índice_ ``4`` (**não incluído**).

- Ao **omitir** o _valor final_, o intervalo irá para o _final da Tuple_:
    ```
    # Imprimindo os itens de "cherry" (2) até o final.

    thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
    print(thistuple[2:])  # Retorna: ('cherry', 'orange', 'kiwi', 'melon', 'mango')
    ```

    > **Nota**: A _pesquisa_ começará no _índice_ ``2`` (**incluído**) e terminará no _último índice_ (**incluído**).

## Intervalo de Índices Negativos

Especifique _índices negativos_ se quiser **iniciar** a pesquisa do _final da Tuple_.

```
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[-4:-1])  # Retorna: ('orange', 'kiwi', 'melon')
```

> **Nota**: A _pesquisa_ começará no _índice_ ``-4`` (**incluído**) e terminará no _índice_ ``-1`` (**não incluído**).

## Verifique se o item existe

Para determinar se um _item especificado_ está **presente** em uma _Tuple_, basta utilizar a _palavra-chave_ ``ìn``.

```
# Verificando se "apple" está presente na Tuple

thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
    print("Yes, 'apple' is in the fruits tuple")

# Retorna: Yes, 'apple' is in the fruits tuple
```

---

As _Tuples_ são **imutáveis**, o que significa que _não podem ser alteradas_, **adicionar** ou **remover** _itens_ depois que a _Tuple_ for criada não é mais possível.

> Mas existem algumas _soluções alternativas_.

## Alterar valores de Tuple

Depois que uma _Tuple_ é criada, **não pode alterar seus valores**. As _Tuples_ são **imutáveis**.

- É possível _converter uma Tuple_ em uma **lista**, _alterar a lista_ e **converter a lista** novamente em uma _Tuple_:
    ```
    # Convertendo uma Tuple em uma Lista para alterá-la

    thistuple = ("apple", "banana", "cherry")
    thislist = list(thistuple)  # Convertendo de 'Tuple' para 'List'

    thislist[1] = "kiwi"
    thistuple = tuple(thislist)  # Convertendo de 'List' para 'Tuple'

    print(thistuple)  # Retorna: ('apple', 'kiwi', 'cherry')
    ```

## Adicionar itens

Como as _Tuples_ são **imutáveis**, elas _não possuem_ um "método integrado" ``append()``, mas existem outras maneiras de _adicionar itens_ a uma _Tuple_.

- **Converter em uma _List_** - É possível _converter_ uma _Tuple_ em uma **List**, _adicionar seu(s) item(s)_ e **convertê-la** novamente em uma _Tuple_:
    ```
    # Convertendo uma 'Tuple' em uma 'List', adicionando "orange" e convertendo novamente em uma 'Tuple'

    thistuple = ("apple", "banana", "cherry")
    thislist = list(thistuple)  # Convertendo de 'Tuple' para 'List'

    thislist.append("orange")
    thistuple = tuple(thislist)  # Convertendo de 'List' para 'Tuple'

    print(thistuple)  # Retorna: ('apple', 'banana', 'cherry', 'orange')
    ```

- **Adicione _Tuple_ a uma _Tuple_** - É possível **adicionar** _Tuples_ a _Tuples_, então se quiser **adicionar** um _item (ou vários)_, crie uma **nova Tuple** com os _itens_ e **adicione** a _Tuple_ existente:
    ```
    # Criando uma nova 'Tuple' com o valor "orange" e adicionando essa 'Tuple'

    thistuple = ("apple", "banana", "cherry")
    newtuple = ("orange",)

    thistuple += newtuple

    print(thistuple)  # Retorna: ('apple', 'banana', 'cherry', 'orange')
    ```

    > **Nota**: Ao criar uma _Tuple_ com **apenas um item**, lembre-se de _incluir uma vírgula (``,``) após o item_, caso contrário não será identificado como _Tuple_.

## Remover itens

> **Nota**: Não é possível _remover itens_ de uma **Tuple**.

- As _Tuples_ são **imutáveis**, portanto não é possível _remover itens_ delas, mas pode usar a mesma solução de _alterar_ e _adicionar_ **itens da Tuple**:
    ```
    # Convertendo a 'Tuple' em uma 'List', removendo "apple" e convertendo novamente em uma 'Tuple'

    thistuple = ("apple", "banana", "cherry")
    thislist = list(thistuple)  # Convertendo de 'Tuple' para 'List'

    thislist.remove("apple")
    thistuple = tuple(thislist)  # Convertendo de 'List' para 'Tuple'

    print(thistuple)  # Retorna: ('banana', 'cherry')
    ```

- Também é possível **excluir** uma _Tuple_ completamente:
    ```
    # A palavra-chave 'del' pode excluir a 'Tuple' completamente

    thistuple = ("apple", "banana", "cherry")
    del thistuple

    print(thistuple)  # Gerará um erro porque a 'Tuple' não existe mais
    ```

---

## Descompactando uma Tuple

Quando uma _Tuple_ é criada, normalmente é **atribuído valores** a ela. Isso é chamado "packing" (_empacotar_) uma _Tuple_.

```
# Empacotando uma 'Tuple'
fruits = ("apple", "banana", "cherry")
```

- Em Python, também é possível _extrair os valores_ de volta para **variáveis**. Isso é chamado "unpacking" (_descompactar_):
    ```
    # Descompactando uma 'Tuple'
    fruits = ("apple", "banana", "cherry")

    (green, yellow, red) = fruits

    print(green)   # Retorna: apple
    print(yellow)  # Retorna: banana
    print(red)     # Retorna: cherry
    ```

    > **Nota**: O _número de variáveis_ deve **corresponder** ao _número de valores na Tuple_, caso contrário, deve-se usar um **asterisco** para _coletar os valores restantes_ como uma **lista**.

## Usando Asterisk ``*``

Se o _número de variáveis_ for **menor** que o _número de valores_, é possível **adicionar** um ``*`` ao _nome da variável_ e os **valores serão atribuídos a variável** como uma _lista_.

```
# Atribuindo o restante dos valores em uma lista chamada 'red'

fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")

(green, yellow, *red) = fruits

print(green)   # Retorna: apple
print(yellow)  # Retorna: banana
print(red)     # Retorna: ['cherry', 'strawberry', 'raspberry']
```

- Se o **asterisco** for _adicionado_ a **outro nome de variável** que _não o último_, o Python atribuirá valores à variável até que o _número de valores restantes_ corresponda ao _número de variáveis restantes_:
    ```
    # Adicionando uma 'lista' de valores à variável "tropic"

    fruits = ("apple", "mango", "papaya", "pineapple", "cherry")

    (green, *tropic, red) = fruits

    print(green)   # Retorna: apple
    print(tropic)  # Retorna: ['mango', 'papaya', 'pineapple']
    print(red)     # Retorna: cherry
    ```

---

## Loops nos itens da Tuple

É possível _percorrer os itens_ da **Tuple** usando um _loop_ ``for``.

```
# Iterando pelos itens e imprimindo os valores

thistuple = ("apple", "banana", "cherry")
for x in thistuple:
    print(x)

"""Retorna:
    apple
    banana
    cherry
"""
```

## Loops consultando os números de índice

É possível _percorrer os itens_ da **Tuple** consultando seu _número de índice_.

- Utilizando as **funções** ``range()`` e ``len()`` para _criar um iterável_ adequado:
    ```
    # Imprimindo todos os itens referindo-se ao seu número de índice

    thistuple = ("apple", "banana", "cherry")

    for i in range(len(thistuple)):
        print(thistuple[i])

    """Retorna:
        apple
        banana
        cherry
    """
    ```

## Usando um loop while

É possível _percorrer os itens_ da **Tuple** usando um _loop_ ``while``.

- Utilize a **função** ``len()`` para determinar o _comprimento da Tuple_, então _comece_ em **0** e _percorra os itens da Tuple_ consultando seus **índices**:
    ```
    # Imprimindo todos os itens, usando um loop 'while' para percorrer todos os números de índice

    thistuple = ("apple", "banana", "cherry")

    i = 0
    while i < len(thistuple):
        print(thistuple[i])
        i = i + 1

    """Retorna:
        apple
        banana
        cherry
    """
    ```

    > **Nota**: Lembre-se de _aumentar o índice_ em ``1`` após **cada iteração**.

---

## Juntando duas Tuples

Para _juntar_ duas ou mais **Tuples** é possível usar o _operador_ ``+``.

```
# Juntando duas Tuples

tuple1 = ("a", "b", "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3)  # Retorna: ('a', 'b', 'c', 1, 2, 3)
```

## Multiplicar Tuples

É possível _multiplicar o conteúdo_ de uma **Tuple** um _determinado número de vezes_, basta utilizar o _operador_ ``*``.

```
# Multiplicando a Tuple "fruits" por 2

fruits = ("apple", "banana", "cherry")
mytuple = fruits * 2

print(mytuple)  # Retorna: ('apple', 'banana', 'cherry', 'apple', 'banana', 'cherry')
```

---

## Métodos de Tuple

Python possui _dois métodos integrados_ que podem ser usados em **Tuples**.

- ``count()``: Retorna o número de vezes que um _valor especificado_ ocorre em uma **Tuple**.
- ``index()``: Pesquisa na **Tuple** um _valor especificado_ e retorna a posição onde ele foi encontrado.

---