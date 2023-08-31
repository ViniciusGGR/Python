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
- []()

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

## 