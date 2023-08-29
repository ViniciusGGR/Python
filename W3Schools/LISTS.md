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
- []()

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

## 