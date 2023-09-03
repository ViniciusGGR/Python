# Sets

### Sumário:

- [Set](#set)
- [Set itens](#set-itens)
- [Não ordenado](#não-ordenado)
- [Imutável](#imutável)
- [Duplicatas não permitidas](#duplicatas-não-permitidas)
- [Obtendo o comprimento de um Set](#obtendo-o-comprimento-de-um-set)
- [Set itens - Tipos de Dados](#set-itens---tipos-de-dados)
- [type()](#type)
- [O construtor set()](#o-construtor-set)
- [Coleções Python (Arrays)](#coleções-python-arrays)
---
- []()

---

```
myset = {"apple", "banana", "cherry"}
```

## Set

**Sets** são usados para _armazenar vários itens_ em uma **única variável**.

**Set** é um dos 4 _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**, os outros 3 são **``Tuple``**, **``List``** e **``Dictionary``**.

Um **Set** é uma coleção _não ordenada_, _imutável_ e _não indexada_.

> **Observação**: Os _itens_ do **Set** **não podem ser alterados**, mas é possível _remover itens_ e _adicionar novos itens_.

- Os **Sets** são escritos entre _colchetes_ (``{}``):
    ```
    # Criando um Set
    
    thisset = {"apple", "banana", "cherry"}
    print(thisset)  # Retorna: {'cherry', 'apple', 'banana'}
    ```

    > **Nota**: Os **Sets** _não são ordenados_, portanto os **itens podem ser apresentados em ordem diferente**.

## Set itens

Os _itens_ do **Set** são _desordenados_, _imutáveis_ e **não permitem** _valores duplicados_.

## Não ordenado

**Não ordenado** significa que os _itens_ de um **Set** _não possuem uma ordem definida_.

- Os _itens_ do **Set** podem aparecer em uma _ordem diferente_ sempre que forem utilizados e _não podem_ ser **referenciados por _índice_ ou _chave_**.

## Imutável

Os _itens_ do **Set** _não podem ser alterados_, o que significa que não podem ser alterados após a **criação do Set**.

> Depois que um **Set** é criado, **não é possível** _alterar seus itens_, mas é possível **remover itens e adicionar novos itens**.

## Duplicatas não permitidas

Os **Sets** não podem ter _dois itens_ com o mesmo valor.

```
# Valores duplicados serão ignorados

thisset = {"apple", "banana", "cherry", "apple"}
print(thisset)  # Retorna: {'banana', 'cherry', 'apple'}
```

> **Nota**: Os _valores_ ``True`` e ``1`` são considerados o _mesmo valor_ em **Sets** e são _tratados como duplicados_.

```
# 'True' e '1' são considerados o mesmo valor

thisset = {"apple", "banana", "cherry", True, 1, 2}
print(thisset)  # Retorna: {True, 2, 'banana', 'cherry', 'apple'}
```

## Obtendo o comprimento de um Set

Para _determinar_ quantos **itens um Set** possui, basta utilizar a **função** ``len()``.

```
# Obtendo o número de itens em um Set

thisset = {"apple", "banana", "cherry"}
print(len(thisset))  # Retorna: 3
```

## Set itens - Tipos de Dados

Os _itens_ de **Set** podem ser de qualquer _tipo de dados_.

```
# string
set1 = {"apple", "banana", "cherry"}
print(set1)  # Retorna: {'cherry', 'apple', 'banana'}

# int
set2 = {1, 5, 7, 9, 3}
print(set2)  # Retorna: {1, 3, 5, 7, 9}

# boolean
set3 = {True, False, False}
print(set3)  # Retorna: {False, True}
```

- Um **Set** pode conter _diferentes tipos de dados_:
    ```
    # Um Set com 'strings', 'inteiros' e 'booleanos'
    
    set1 = {"abc", 34, True, 40, "male"}
    print(set1)  # Retorna: {True, 34, 40, 'male', 'abc'}
    ```

## ``type()``

Da perspectiva do Python, **Sets** são definidos como _objetos_ com o **tipo de dados** '``set``':

```
<class 'set'>
```

```
myset = {"apple", "banana", "cherry"}
print(type(myset))  # Retorna: <class 'set'>
```

## O construtor ``set()``

É possível usar o _construtor_ ``set()`` para fazer um **Set**.

```
# Usando o construtor 'set()' para fazer um Set

thisset = set(("apple", "banana", "cherry"))
print(thisset)  # Retorna: {'apple', 'banana', 'cherry'}
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

## 