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
- [Acessando Itens](#acessando-itens)
- [Obter as Keys](#obter-as-keys)
- [Obter os Values](#obter-os-values)
- [Obter Items](#obter-items)
- [Verifique se a Key existe](#verifique-se-a-key-existe)
---
- [Mudar valores](#mudar-valores)
- [Atualizar Dictionary](#atualizar-dictionary)
---
- [Adicionando itens](#adicionando-itens)
- [Atualizar Dictionary](#atualizar-dictionary-1)
---
- [Removendo Itens](#removendo-itens)
---
- [Loop em um Dictionary](#loop-em-um-dictionary)
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

## Acessando Itens

É possível _**acessar os itens** de um Dictionary_ referindo-se ao **nome da chave**, entre _colchetes_ ``[]``.

```
# Obtendo o valor da chave 'model'

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

x = thisdict["model"]
print(x)  # Retorna: Mustang
```

- Existe também um **método** chamado ``get()`` que "retorna" o mesmo _resultado_:
    ```
    # Obtendo o valor da chave 'model'

    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    x = thisdict.get("model")
    print(x)  # Retorna: Mustang
    ```

## Obter as Keys

O **método** ``keys()`` retornará uma _lista_ de **todas as chaves** do _Dictionary_.

```
# Obtendo uma lista de chaves

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

x = thisdict.keys()
print(x)  # Retorna: dict_keys(['brand', 'model', 'year'])
```

- A _lista_ de **chaves** é uma _visualização do **Dictionary**_, o que significa que quaisquer **alterações** feitas no _Dictionary_ serão _refletidas na **lista de chaves**_:
    ```
    # Adicionando um novo item ao Dictionary original e visualizando a lista de chaves também sendo atualizada

    car = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    x = car.keys()
    print(x)  # Retorna: dict_keys(['brand', 'model', 'year'])

    car["color"] = "white"

    print(x)  # Retorna: dict_keys(['brand', 'model', 'year', 'color'])
    ```

## Obter os Values

O **método** ``values()`` retornará uma _lista_ de **todas os valores** do _Dictionary_.

```
# Obtendo uma lista dos valores

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

x = thisdict.values()
print(x)  # Retorna: dict_values(['Ford', 'Mustang', 1964])
```

- A _lista_ de **valores** é uma _visualização do **Dictionary**_, o que significa que quaisquer **alterações** feitas no _Dictionary_ serão _refletidas na **lista de valores**_:
    ```
    # Fazendo uma alteração no Dictionary original e visualizando a lista de valores também sendo atualizada

    car = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    x = car.values()
    print(x)  # Retorna: dict_values(['Ford', 'Mustang', 1964])

    car["year"] = 2020

    print(x)  # Retorna: dict_values(['Ford', 'Mustang', 2020])
    ```

    Adicionando um **novo item** ao _Dictionary_ original e visualizando a **lista de valores** também sendo atualizada.

    ```
    car = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    x = car.values()
    print(x)  # Retorna: dict_values(['Ford', 'Mustang', 1964])

    car["color"] = "red"

    print(x)  # Retorna: dict_values(['Ford', 'Mustang', 1964, 'red'])
    ```

## Obter Items

O **método** ``items()`` retornará **cada item** de um _Dictionary_, como **tuples** em uma **lista**.

```
# Obtendo uma lista dos pares chave-valor

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

x = thisdict.items()
print(x)  # Retorna: dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])
```

- A _lista_ retornada é uma _visualização dos itens do **Dictionary**_, o que significa que quaisquer **alterações** feitas no _Dictionary_ serão _refletidas na **lista de itens**_:
    ```
    # Fazendo uma alteração no Dictionary original e visualizando a lista de itens também sendo atualizada

    car = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    x = car.items()
    print(x)  # Retorna: dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])

    car["year"] = 2020

    print(x)  dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 2020)])
    ```

    Adicionando um **novo item** ao _Dictionary_ original e visualizando a **lista de itens** também sendo atualizada.

    ```
    car = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    x = car.items()
    print(x)  # Retorna: dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])

    car["color"] = "red"

    print(x)  dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964), ('color', 'red')])
    ```

## Verifique se a Key existe

Para _determinar_ se uma **chave especificada** está _presente_ em um _Dictionary_, basta utilizar a **palavra-chave** ``in``.

```
# Verificando se 'model' está presente no Dictionary

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

if "model" in thisdict:
    print("Yes, 'model' is one of the keys in the 'thisdict' dictionary")

# Retorna: Yes, 'model' is one of the keys in the thisdict dictionary
```

---

## Mudar valores

- É possível _alterar o valor_ de um _item especificado_ consultando seu **nome chave**:
    ```
    # Alterando o 'year' para 2018

    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict["year"] = 2018

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 2018}
    ```

## Atualizar Dictionary

O **método** ``update()`` _atualizará o Dictionary_ com os **itens** do _argumento_ fornecido.

- O _argumento_ deve ser um _Dictionary_ ou um **objeto iterável** com pares _chave:valor_:
    ```
    # Atualizando o 'year' do carro usando o método 'update()'

    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict.update({"year": 2020})

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 2020}
    ```

---

## Adicionando itens

- A _adição_ de um _item ao Dictionary_ é feita usando uma **nova chave** de _índice_ e **atribuindo um valor** a ela:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict["color"] = "red"

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 'red'}
    ```

## Atualizar Dictionary

O **método** ``update()`` _atualizará o Dictionary_ com os _itens_ de um determinado **argumento**. Se o _item_ não existir, o _item_ será adicionado.

- O **argumento** deve ser um _Dictionary_ ou um **objeto iterável** com pares _chave:valor_:
    ```
    # Adicionando um item 'color' ao Dictionary usando o método 'update()'

    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict.update({"color": "red"})

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 'red'}
    ```

---

## Removendo Itens

Existem _vários métodos_ para **remover itens** de um _Dictionary_.

- O **método** ``pop()`` _remove o item_ com o **nome de chave** especificado:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict.pop("model")

    print(thisdict)  # Retorna: {'brand': 'Ford', 'year': 1964}
    ```

- O **método** ``popitem()`` _remove o **último** item_ inserido:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict.popitem()

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang'}
    ```

- A _palavra-chave_ ``del`` _remove o item_ com o **nome de chave** especificado:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    del thisdict["model"]

    print(thisdict)  # Retorna: {'brand': 'Ford', 'year': 1964}
    ```

    A _palavra-chave_ ``del`` também pode _excluir completamente o Dictionary_:

    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    del thisdict

    print(thisdict)  # Retorna: NameError: name 'thisdict' is not defined
    ```

- O **método** ``clear()`` _esvazia o Dictionary_:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    print(thisdict)  # Retorna: {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

    thisdict.clear()

    print(thisdict)  # Retorna: {}
    ```

---

## Loop em um Dictionary

É possível "_percorrer_" um _Dictionary_ usando um **loop** ``for``.

Ao "_percorrer_" um _Dictionary_, o **valor de retorno** são as _**chaves** do Dictionary_, mas também existem **métodos** para **retornar** os _valores_.

- Imprimindo todos os _nomes de chaves_ do _Dictionary_, um por um:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    for x in thisdict:
        print(x)

    """Retorna:
        brand
        model
        year
    """
    ```

- Imprimindo todos os _valores_ do _Dictionary_, um por um:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    for x in thisdict:
        print(thisdict[x])
    
    """Retorna:
        Ford
        Mustang
        1964
    ```

- O **método** ``values()`` também pode ser usado para **retornar** _valores_ de um _Dictionary_:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    for x in thisdict.values():
        print(x)

    """Retorna:
        Ford
        Mustang
        1964
    """
    ```

- O **método** ``keys()`` também pode ser usado para **retornar** as _chaves_ de um _Dictionary_:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    for x in thisdict.keys():
        print(x)

    """Retorna:
        brand
        model
        year
    ```

- Fazendo um **loop** por _chaves_ e _valores_, usando o **método** ``items()``:
    ```
    thisdict = {
        "brand": "Ford",
        "model": "Mustang",
        "year": 1964
    }

    for x, y in thisdict.items():
        print(x, y)

    """Retorna:
        brand Ford
        model Mustang
        year 1964
    """
    ```

---

## 