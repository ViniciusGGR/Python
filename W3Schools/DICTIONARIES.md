# Dictionaries

### Sumário:

- [Dictionary](#dictionary)
- [Itens do Dictionary](#itens-do-dictionary)
- [Ordenado ou Não ordenado?](#ordenado-ou-não-ordenado)
- [Mutável](#mutável)
- [Duplicatas não permitidas](#duplicatas-não-permitidas)
- [Comprimento do Dictionary](#comprimento-do-dictionary)
- [Itens do Dictionary - Tipos de Dados](#itens-do-dictionary---tipos-de-dados)
- [type()](#type)
- [O construtor dict()](#o-construtor-dict)
- [Coleções Python (Arrays)](#coleções-python-arrays)
---
- []()

---

```
thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
```

## Dictionary

_Dictionaries_ são usados para **armazenar valores de dados** em **pares** _chave:valor_.

Um _Dictionary_ é uma **coleção ordenada**, **mutável** e que **não permite duplicatas**.

- Os _Dictionaries_ são escritos entre **chaves** e possuem _chaves e valores_:
    ```
    # Criando e imprimindo um Dictionary

    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
    ```

## Itens do Dictionary

Os _itens do Dictionary_ são **ordenados**, **alteráveis** e **não permitem duplicatas**.

- Os _itens do Dictionary_ são **apresentados** em _pares chave:valor_ e podem ser **referenciados** usando o _nome da chave_:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict["brand"])  # Retorna: Ford
    ```

## Ordenado ou Não ordenado?

_Dictionaries_ são **ordenados**, isso significa que os _itens_ tem uma **ordem definida** e essa _ordem não mudará_.

> **Não ordenado** significa que os _itens não possuem_ uma **ordem definida**, não é possível se referir a um item usando um índice.

## Mutável

Os _Dictionaries_ são **mutáveis**, o que significa que _podem ser alterados_, **adicionar ou remover itens** após a criação do _Dictionary_.

## Duplicatas não permitidas

- Os _Dictionaries_ **não podem** ter _dois itens_ com a mesma _chave_:
    ```
    # Valores duplicados substituirão os valores existentes

    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964,
        "year": 2020
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 2020}
    ```

## Comprimento do Dictionary

Para **determinar** quantos _itens um Dictionary_ possui, basta utilizar a **função** ``len()``.

```
# Imprimindo o número de itens no Dictionary

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
    "year": 2020
}

print(len(thisdict))  # Retorna: 3
```

> **Nota**: Valores duplicados substituirão os valores existentes, por isso a **função** ``len()`` considera só ``3`` itens no _Dictionary_.

## Itens do Dictionary - Tipos de Dados

- Os **valores** nos _itens do Dictionary_ podem ser de _qualquer **tipo de dados**_:
    ```
    # Tipos de dados 'string', 'int', 'boolean' e 'list'

    thisdict = {
        "brand": "Ford",
        "electric": False,
        "year": 1964,
        "colors": ["red", "white", "blue"]
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'electric': False, 'year': 1964, 'colors': ['red', 'white', 'blue']}
    ```

## ``type()``

Da perspectiva do Python, os _Dictionaries_ são definidos como **objetos** com o _tipo de dados_ ``'dict'``.

```
<class 'dict'>
```

```
# Imprimindo o tipo de dados de um Dictionary

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

print(type(thisdict))  # Retorna: <class 'dict'>
```

## O construtor ``dict()``

- É possível usar o **construtor** ``dict()`` para fazer um _Dictionary_:
    ```
    # Usando o método 'dict' para fazer um Dictionary

    thisdict = dict(name = "John", age = 36, country = "Norway")
    
    print(thisdict)  # Retorna: {'name': 'John', 'age': 36, 'country': 'Norway'}
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