# Lists

### Sumário

- [Lista](#lista)
- [Itens da Lista](#itens-da-lista)
- [Ordenamento](#ordenamento)
- [Mutável](#mutável)
- [Permitir Duplicatas](#permitir-duplicatas)
- [Comprimento da Lista](#comprimento-da-lista)
- [Itens da Lista - Tipos de Dados](#itens-da-lista---tipos-de-dados)
- [type()](#type)
- [O Construtor list()](#o-construtor-list)
- [Coleções Python (Arrays)](#coleções-python-arrays)
---
- [Acessar itens](#acessar-itens)
    - [Indexação Negativa](#indexação-negativa)
    - [Intervalo de Índices](#intervalo-de-índices)
    - [Intervalo de Índices Negativos](#intervalo-de-índices-negativos)
- [Verifique se o item existe](#verifique-se-o-item-existe)
---
- [Alterar valor do item](#alterar-valor-do-item)
- [Alterar valores em um intervalo de itens](#alterar-valores-em-um-intervalo-de-itens)
- [Inserir itens](#inserir-itens)
---
- [Anexar Itens](#anexar-itens)
- [Inserir Itens](#inserir-itens-1)
- [Estender Lista](#estender-lista)
- [Adicione qualquer iterável](#adicione-qualquer-iterável)
---
- [Remover item específico](#remover-item-específico)
- [Remover índice específico](#remover-índice-específico)
- [Limpe a lista](#limpe-a-lista)
---
- [Loop nos itens da lista](#loop-nos-itens-da-lista)
- [Loop consultando os números de índice](#loop-consultando-os-números-de-índice)
- [Usando um Loop While](#usando-um-loop-while)
- [Loop usando compreensão de lista](#loop-usando-compreensão-de-lista)
---
- [Compreensão de lista](#compreensão-de-lista)
- [A Sintaxe](#a-sintaxe)
    - [Condição](#condição)
    - [Iterável](#iterável)
    - [Expressão](#expressão)

---

```
mylist = ["apple", "banana", "cherry"]
```

## Lista

**Listas** são usadas para _armazenar vários itens_ em uma **única variável**.

**Lista** é um dos 4 _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**, os outros 3 são **``Tuple``**, **``Set``** e **``Dictionary``**.

- **Listas** são criadas usando _colchetes_ (``[]``):
    ```
    thislist = ["apple", "banana", "cherry"]
    print(thislist)  # Retorna: ['apple', 'banana', 'cherry']
    ```

## Itens da Lista

- Os _itens da lista_ são **ordenados**, **alteráveis** e é permitido _valores duplicados_.
- Os _itens da lista_ são **indexados**, o _primeiro item_ possui **index** ``[0]``, o _segundo item_ possui **index** ``[1]``...

## Ordenamento

**Listas** são _ordenadas_, portanto, os **itens** tem uma _ordem definida_ e essa _ordem_ não mudará.

Se _adicionado novos itens_ a uma **lista**, os _novos itens_ serão colocados no **final da lista**.

> **Nota**: Existem alguns _métodos de lista_ que irão **alterar a ordem**, mas em geral: a _ordem dos itens não serã alterada_.

## Mutável

**Listas** são _mutáveis_, o que significa que podem ser _alteradas_, **adicionar** e **remover itens** de uma lista após ela ter sido criada.

## Permitir Duplicatas

Como as **listas** são _indexadas_ as **listas** podem ter _itens com o mesmo valor_.

```
# Listas permitem valores duplicados
thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)  # Retorna: ['apple', 'banana', 'cherry', 'apple', 'cherry']
```

## Comprimento da Lista

- Para determinar _quantos itens_ uma **lista** possui, basta utilizar a **função** ``len()``:
    ```
    # Imprimindo o número de itens da lista
    thislist = ["apple", "banana", "cherry"]
    print(len(thislist))  # Retorna: 3
    ```

## Itens da Lista - Tipos de Dados

Os _itens da lista_ podem ser de qualquer **tipo de dados**.

```
# Tipos de dados 'string', 'int' e 'boolean'

# string:
list1 = ["apple", "banana", "cherry"]
print(list1)  # Retorna: ['apple', 'banana', 'cherry']

# int:
list2 = [1, 5, 7, 9, 3]
print(list2)  # Retorna: [1, 5, 7, 9, 3]

# boolean
list3 = [True, False, False]
print(list3)  # Retorna: [True, False, False]
```

- Uma **lista** pode conter diferentes _tipos de dados_:
    ```
    # Uma lista com 'string', 'int' e 'boolean':
    list1 = ["abc", 34, True, 40, "male"]
    print(list1)  # Retorna: ['abc', 34, True, 40, 'male']
    ```

## ``type()``

- **Listas** são definidas como _objetos_ com o _tipo de dados_ ``'list'``:
    ```
    <class 'list'>
    ```

```
mylist = ["apple", "banana", "cherry"]
print(type(mylist))  # Retorna: <class 'list'>
```

## O Construtor ``list()``

É possível usar o _construtor_ ``list()`` ao **criar uma nova lista**.

```
# Usando o construtor 'list()' para fazer uma lista
thislist = list(("apple", "banana", "cherry"))
print(thislist)  # Retorna: ['apple', 'banana', 'cherry']
```

> **Nota**: Observe os _parênteses_ **duplos** com o uso do _construtor_ ``list()``.

## Coleções Python (Arrays)

Existem quatro _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**:

- ``List``: É uma _coleção ordenada_ e **mutável**. Permite _membros duplicados_.
- ``Tuple``: É uma _coleção ordenada_ e **imutável**. Permite _membros duplicados_.
- ``Set``: É uma _coleção não ordenada_, **imutável** e _não indexada_. Nenhum _membro duplicado_.
    - Os itens do ``Set`` não podem ser alterados, mas é possível remover e adicionar itens sempre que desejar.
- ``Dictionary``: É uma _coleção ordenada_ e **mutável**. Nenhum _membro duplicado_.

> Ao escolher um _tipo de dado integrado_ para **armazenar coleções de dados** é útil compreender as _propriedades_ desse tipo. Escolher o tipo certo para uma determinado conjunto de dados pode significar retenção de significado e um aumento na eficiência ou segurança.

---

## Acessar itens

- Os _itens da lista_ são **indexados** e é possível acessá-los consultando o **número do índice**:
    ```
    # Imprimindo o segundo item da lista
    thislist = ["apple", "banana", "cherry"]
    print(thislist[1])  # Retorna: banana
    ```

    > **Nota**: O _primeiro item_ possui **índice** ``0``.

### Indexação Negativa

_Indexação negativa_ significa **começar do fim**.

- ``-1`` refere-se ao _último item_, ``-2`` refere-se ao _penúltimo item_ etc:
    ```
    # Imprimindo o último item da lista
    thislist = ["apple", "banana", "cherry"]
    print(thislist[-1])  # Retorna: cherry
    ```

### Intervalo de Índices

É possível _especificar um **intervalo de índices**_ especificando **onde começar** e **onde terminar** o _intervalo_.

Ao _especificar um intervalo_, o valor de retorno será uma **nova lista** com os itens especificados.

```
# Imprimindo terceiro, quarto e quinto item
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])  # Retorna: ['cherry', 'orange', 'kiwi']
```

> **Nota**: A "pesquisa" começará no _índice_ ``2`` (**incluído**) e terminará no _índice_ ``5`` (**não incluído**).

> **Nota**: O _primeiro item_ possui **índice** ``0``.

- Ao _omitir o valor inicial_, o **intervalo começará no primeiro item**:
    ```
    # Imprimindo desde o primeiro item, mas NÃO incluindo, "kiwi".
    thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(thislist[:4])  # Retorna: ['apple', 'banana', 'cherry', 'orange']
    ```

- Ao _omitir o valor final_, o **intervalo irá para o final da lista**:
    ```
    # Imprimindo os itens de "cherry" até o final.
    thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(thislist[2:])  # Retorna: ['cherry', 'orange', 'kiwi', 'melon', 'mango']
    ```

### Intervalo de Índices Negativos

- Especifique _índices negativos_ se desejar **iniciar a pesquisa do final da lista**:
    ```
    # Imprimindo os itens de "orange" (-4) até, mas NÃO inclui "mango" (-1).
    thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(thislist[-4:-1])  # Retorna: ['orange', 'kiwi', 'melon']
    ```

## Verifique se o item existe

Para _determinar_ se um **item especificado** está _presente em uma lista_, basta utilizar a **palavra-chave** ``in``.

```
# Verificando se "apple" está presente na lista:
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
    print("Yes, 'apple' is in the fruits list")

# Retorna: Yes, 'apple' is in the fruits list
```

---

## Alterar valor do item

Para _alterar o valor_ de um **item específico**, consulte o _número do índice_.

```
# Alterando de "banana" para "blackcurrant"

thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"

print(thislist)  # Retorna: ['apple', 'blackcurrant', 'cherry']
```

## Alterar valores em um intervalo de itens

Para _alterar o valor dos itens_ dentro de um **intervalo específico**, defina uma lista com os _novos valores_ e consulte o **intervalo de números de índice** onde deseja _inserir os novos valores_.

```
# Alterando de "banana" para "blackcurrant" e de "cherry" para "watermelon"

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]

print(thislist)  # Retorna: ['apple', 'blackcurrant', 'watermelon', 'orange', 'kiwi', 'mango']
```

> **Nota**: O _índice_ ``3`` (**não incluído**), portanto o seu valor se mantém o mesmo.

- Se for _inserido mais itens_ do que **substitui**, os _novos itens_ serão inseridos onde foram **especificados** e os _itens restantes_ serão **movidos de acordo**:
    ```
    # Alterando o "segundo valor" (1) substituindo-o por "dois novos valores"

    thislist = ["apple", "banana", "cherry"]
    thislist[1:2] = ["blackcurrant", "watermelon"]  # "blackcurrant" (índice - 1) e "watermelon" (índice 2)

    print(thislist)  # Retorna: ['apple', 'blackcurrant', 'watermelon', 'cherry']
    ```

    > **Nota**: O _comprimento da lista_ mudará quando o **número de itens** inseridos não corresponder ao número de itens substituídos.

- Se for _inserido menos itens_ do que **substitui**, os _novos itens_ serão inseridos onde foram **especificados** e os _itens restantes_ serão **movidos de acordo**:
    ```
    # Alterando o "segundo" (1) e "terceiro" (2) valores substituindo-os por "um valor"

    thislist = ["apple", "banana", "cherry"]
    thislist[1:3] = ["watermelon"]  # "watermelon" - (índices 1 e 2)

    print(thislist)  # Retorna: ['apple', 'watermelon']
    ```

## Inserir itens

Para _inserir um novo item na lista_, **sem substituir nenhum dos valores existentes**, pode-se utilizar o **método** ``insert()``

- O **método** ``insert()`` insere um _item no índice especificado_:
    ```
    # Inserindo "watermelon" como terceiro item (2)

    thislist = ["apple", "banana", "cherry"]
    thislist.insert(2, "watermelon")

    print(thislist)  # Retorna: ['apple', 'banana', 'watermelon', 'cherry']
    ```

    > **Nota**: Como _resultado_ do exemplo acima, a lista conterá agora **4 itens**.

---

## Anexar Itens

- Para _adicionar um item_ ao **final da lista**, basta utilizar o **método** ``append()``:
    ```
    # Usando o método 'append()' para anexar um item

    thislist = ["apple", "banana", "cherry"]
    thislist.append("orange")

    print(thislist)  # Retorna: ['apple', 'banana', 'cherry', 'orange']
    ```

## Inserir Itens

Para _inserir um item na lista_ em um **índice especificado**, basta usar o **método** ``insert()``.

- O **método** ``ìnsert()`` insere um _item_ no **índice especificado**:
    ```
    # Inserindo um item na segunda posição (1)

    # Inserindo "orange" como segundo item (1)
    thislist = ["apple", "banana", "cherry"]
    thislist.insert(1, "orange")

    print(thislist)  # Retorna: ['apple', 'orange', 'banana', 'cherry']
    ```

    > **Nota**: Como _resultado_ do exemplo acima, a lista conterá agora **4 itens**.

## Estender Lista

Para _acrescentar elementos de outra lista_ à **lista atual**, basta usar o **método** ``extend()``.

```
# Adicionando os elementos da lista "tropical" a lista "thislist"

thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]

thislist.extend(tropical)
print(thislist)  # Retorna: ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']
```

- Os _elementos_ serão adicionados ao **final da lista**.

## Adicione qualquer iterável

O **método** ``extend()`` não precisa _anexar listas_, é possível adicionar qualquer objeto iterável (**tuples**, **sets**, **dictionaries** etc).

```
# Adicionando elementos de um 'tuple' a uma 'lista'

thislist = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")

thislist.extend(thistuple)
print(thislist)  # Retorna: ['apple', 'banana', 'cherry', 'kiwi', 'orange']
```

---

## Remover item específico

O **método** ``remove()`` remove o _item especificado_.

```
# Removendo 'banana'

thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")

print(thislist)  # Retorna: ['apple', 'cherry']
```

- Se houver _mais de um item com o valor especificado_, o **método** ``remove()`` remove a _primeira ocorrência_:
    ```
    # Removendo a primeira ocorrência de 'banana'

    thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
    thislist.remove("banana")

    print(thislist)  # Retorna: ['apple', 'cherry', 'banana', 'kiwi']
    ```

## Remover índice específico

O **método** ``pop()`` remove o _índice especificado_.

```
# Removendo o segundo item (1)

thislist = ["apple", "banana", "cherry"]
thislist.pop(1)

print(thislist)  # Retorna: ['apple', 'cherry']
```

- Se **não** for _especificado o índice_, o **método** ``pop()`` _removerá o último item_:
    ```
    # Removendo o último item

    thislist = ["apple", "banana", "cherry"]
    thislist.pop()

    print(thislist)  # Retorna: ['apple', 'banana']
    ```

A _palavra-chave_ ``del`` também **remove o índice especificado**.

```
# Removendo o primeiro item (0)

thislist = ["apple", "banana", "cherry"]
del thislist[0]

print(thislist)  # Retorna: ['banana', 'cherry']
```

- A _palavra-chave_ ``del`` também pode **excluir completamente a lista**:
    ```
    # Excluindo a lista inteira

    thislist = ["apple", "banana", "cherry"]
    del thislist

    print(thislist)  # Retorna: NameError: name 'thislist' is not defined
    ```

## Limpe a lista

O **método** ``clear()`` _esvazia a lista_.

A _lista_ ainda permanece, mas **não tem conteúdo**.

```
# Limpando o conteúdo da lista

thislist = ["apple", "banana", "cherry"]
thislist.clear()

print(thislist)  # Retorna: []
```

---

## Loop nos itens da lista

É possível _percorrer os itens_ de uma **lista** usando um _loop_ ``for``.

```
# Imprimindo 'todos os itens' da lista, um por um

thislist = ["apple", "banana", "cherry"]
for x in thislist:
    print(x)

"""Retorna:
    apple
    banana
    cherry
"""
```

## Loop consultando os números de índice

Também é possível _percorrer os itens_ de uma **lista** consultando seu **número de índice**.

- Utilize as **funções** ``range()`` e ``len()`` para criar um _iterável_ adequado:
    ```
    # Imprimindo 'todos os itens' referindo-se ao seu 'número de índice'

    thislist = ["apple", "banana", "cherry"]
    for i in range(len(thislist)):
        print(thislist[i])

    """Retorna:
        apple
        banana
        cherry
    """
    ```

    O _iterável_ criado no exemplo acima é: ``[0, 1, 2]``.

## Usando um Loop While

É possível _percorrer os itens_ de uma **lista** usando um _loop_ ``while``.

Utilize a **função** ``len()`` para determinar o _comprimento da lista_, então comece em **0** e _percorra os itens da lista_ consultando seus **índices**.

> Lembre-se de _aumentar o índice_ em **1** após cada _iteração_.

```
# Imprimindo 'todos os itens', usando um loop while para 'percorrer todos os números de índice'

thislist = ["apple", "banana", "cherry"]

i = 0
while i < len(thislist):
    print(thislist[i])
    i = i + 1

"""Retorna:
    apple
    banana
    cherry
"""
```

## Loop usando compreensão de lista

A _compreensão de lista_ oferece uma **sintaxe** mais curta para _percorrer listas_.

```
# Um pequeno loop for manul que imprimirá todos os itens de uma lista

thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist]

"""Retorna:
    apple
    banana
    cherry
"""
```

---

## Compreensão de lista

A _compreensão de lista_ oferece uma **sintaxe** mais curta quando se deseja criar uma _nova lista com base nos valores_ de uma **lista existente**.

Exemplo:

- Com base em uma _lista de frutas_, deseja-se uma **nova lista**, contendo _apenas as frutas_ com a **letra** ``a`` no nome.
- Sem _compreensão de lista_ será necessário escrever uma **declaração** ``for`` com um _teste condicional_ dentro:
    ```
    fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
    newlist = []

    for x in fruits:
        if "a" in x:
            newlist.append(x)
    
    print(newlist)  # Retorna: ['apple', 'banana', 'mango']
    ```

    Com a _compreensão de lista_ é possível fazer tudo isso com **apenas uma linha de código**:

    ```
    fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

    newlist = [x for x in fruits if "a" in x]

    print(newlist)  # Retorna: ['apple', 'banana', 'mango']
    ```

## A Sintaxe

> newlist = [_expression_ for _item_ in _iterable_ if _condition_ == True]

- O _valor de retorno_ é uma **nova lista**, deixando a _lista antiga_ **inalterada**.

### Condição

A _condição_ é como um "filtro" que aceita _apenas os itens_ com valor igual a ``True``.

```
# Aceita apenas itens que não sejam (diferente de) "apple"

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if x != "apple"]

print(newlist)  # Retorna: ['banana', 'cherry', 'kiwi', 'mango']
```

- A _condição_ ``if x != "apple"`` retornará ``True`` para _todos os elementos_ "exceto" **apple**, fazendo com que a _nova lista_ contenha todas as frutas, "exceto" **apple**.

A _condição_ é **opcional** e pode ser _omitida_.

```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits]

print(newlist)  # Retorna: ['apple', 'banana', 'cherry', 'kiwi', 'mango']
```

### Iterável

O _iterável_ pode ser **qualquer objeto iterável**, como um **list**, **tuple**, **set** etc.

```
# É possível usar a função 'range()' para criar um iterável

newlist = [x for x in range(10)]

print(newlist)  # Retorna: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

- Mesmo exemplo, mas com uma _condição_:
    ```
    # Aceita apenas números menores que 5

    newlist = [x for x in range(10) if x < 5]

    print(newlist)  # Retorna: [0, 1, 2, 3, 4]
    ```

### Expressão

A _expressão_ é o **item atual** na _iteração_, mas também é o _resultado_, que pode ser "manipulado" antes que acabe como um _item de lista_ na **nova lista**.

```
# Defina os valores na nova lista para 'letras maiúsculas'

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x.upper() for x in fruits]

print(newlist)  # Retorna: ['APPLE', 'BANANA', 'CHERRY', 'KIWI', 'MANGO']
```

- É possível _definir o resultado_ como quiser:
    ```
    # Definindo todos os valores na nova lista como 'hello'

    fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
    newlist = ['hello' for x in fruits]

    print(newlist)  # Retorna: ['hello', 'hello', 'hello', 'hello', 'hello']
    ```

A _expressão_ também pode conter **condições**, não como "filtro", mas como uma forma de _manipular o resultado_:

```
# Retornando "orange" em vez de "banana"

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x if x != "banana" else "orange" for x in fruits]

print(newlist)  # Retorna: ['apple', 'orange', 'cherry', 'kiwi', 'mango']
```

- A _expressão_ no exemplo acima diz:
    - Devolva o item _se não for ``banana``_, _se for ``banana`` devolva ``orange``_.

---

## 