# JSON

### Sumário:

- [JSON em Python](#json-em-python)
- [Analisar JSON - Converter de JSON para Python](#analisar-json---converter-de-json-para-python)
- [Converter de Python para JSON](#converter-de-python-para-json)
- [Formatando o resultado](#formatando-o-resultado)
- [Ordenando o resultado](#ordenando-o-resultado)

---

**JSON** é uma _sintaxe_ para **armazenar** e **trocar dados**.

**JSON** é _texto_, escrito com **notação de objeto JavaScript**.

## JSON em Python

Python possui um _pacote integrado_ chamado ``json``, que pode ser usado para **trabalhar com dados JSON**.

```
# Importando o 'Module' 'json'

import json
```

## Analisar JSON - Converter de JSON para Python

Caso tenha uma **string JSON**, poderá _analisá-la_ usando o **método** ``json.loads()``.

> O resultado será um _Dictionary_ Python.

```
# Convertendo de JSON para Python

import json

# Um JSON
x = '{"name":"John", "age":30, "city":"New York"}'

# Analisar 'x'
y = json.loads(x)

# O resultado é um 'Dictionary' Python
print(y["age"])  # Retorna: 30
```

## Converter de Python para JSON

Caso tenha um _object_ Python, poderá **convertê-lo** em uma **string JSON** usando o **método** ``json.dumps()``.

```
# Convertendo de Python para JSON

import json

# Um 'object' Python (dict)
x = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

# Convertendo para JSON
y = json.dumps(x)

# O resultado é uma string JSON
print(y)  # Retorna: {"name": "John", "age": 30, "city": "New York"}
```

- É possível _converter objects_ Python dos seguintes tipos em **strings JSON**:
    - ``dict``.
    - ``list``.
    - ``tuple``.
    - ``string``.
    - ``int``.
    - ``float``.
    - ``True``.
    - ``False``.
    - ``None``.

```
# Converta 'objects' Python em 'strings JSON' e imprimindo os valores

import json

print(json.dumps({"name": "John", "age": 30}))  # Retorna: {"name": "John", "age": 30}
print(json.dumps(["apple", "bananas"]))         # Retorna: ["apple", "bananas"]
print(json.dumps(("apple", "bananas")))         # Retorna: ["apple", "bananas"]
print(json.dumps("hello"))                      # Retorna: "hello"
print(json.dumps(42))                           # Retorna: 42
print(json.dumps(31.76))                        # Retorna: 31.76
print(json.dumps(True))                         # Retorna: true
print(json.dumps(False))                        # Retorna: false
print(json.dumps(None))                         # Retorna: null
```

- Ao _converter_ de Python para **JSON**, os _objects_ Python são _convertidos_ no equivalente **JSON** (_JavaScript_):
    | Python    | JSON       |
    | --------- | ---------- |
    | ``dict``  | ``Object`` |
    | ``list``  | ``Array``  |
    | ``tuple`` | ``Array``  |
    | ``str``   | ``String`` |
    | ``int``   | ``Number`` |
    | ``float`` | ``Number`` |
    | ``True``  | ``true``   |
    | ``False`` | ``false``  |
    | ``None``  | ``null``   |

```
# Convertendo um 'object' Python contendo todos os tipos de dados legais

import json

x = {
    "name": "John",
    "age": 30,
    "married": True,
    "divorced": False,
    "children": ("Ann", "Billy"),
    "pets": None,
    "cars": [
        {"model": "BMW 230", "mpg": 27.5},
        {"model": "Ford Edge", "mpg": 24.1}
    ]
}

# Convertendo para JSON:
y = json.dumps(x)

# O resultado é uma string JSON
print(y)

# Retorna: {"name": "John", "age": 30, "married": true, "divorced": false, "children": ["Ann","Billy"], "pets": null, "cars": [{"model": "BMW 230", "mpg": 27.5}, {"model": "Ford Edge", "mpg": 24.1}]}
```

## Formatando o resultado

- O **método** ``json.dumps()`` possui _parâmetros_ para **facilitar a leitura do resultado**:
    ```
    # Utilizando o parâmetro 'indent' para definir o número de recuos

    import json

    x = {
        "name": "John",
        "age": 30,
        "married": True,
        "divorced": False,
        "children": ("Ann","Billy"),
        "pets": None,
        "cars": [
            {"model": "BMW 230", "mpg": 27.5},
            {"model": "Ford Edge", "mpg": 24.1}
        ]
    }

    # Utilizando quatro 'indent' para facilitar a leitura do resultado
    print(json.dumps(x, indent=4))

    """Retorna:
        {
            "name": "John",
            "age": 30,
            "married": true,
            "divorced": false,
            "children": [
                "Ann",
                "Billy"
            ],
            "pets": null,
            "cars": [
                {
                    "model": "BMW 230",
                    "mpg": 27.5
                },
                {
                    "model": "Ford Edge",
                    "mpg": 24.1
                }
            ]
        }
    """
    ```

Também é possível definir os _separadores_, o **valor padrão** é (``, ``, ``. ``, ``: ``), o que significa usar _uma vírgula e um espaço_ para **separar cada objeto**, e _dois pontos e um espaço_ para **separar as chaves dos valores**.

```
# Utilizando o parâmetro 'separators' para alterar o separador padrão

import json

x = {
    "name": "John",
    "age": 30,
    "married": True,
    "divorced": False,
    "children": ("Ann", "Billy"),
    "pets": None,
    "cars": [
        {"model": "BMW 230", "mpg": 27.5},
        {"model": "Ford Edge", "mpg": 24.1}
    ]
}

print(json.dumps(x, indent=4, separators=(". ", " = ")))

"""Retorna:
    {
        "name" = "John".
        "age" = 30.
        "married" = true.
        "divorced" = false.
        "children" = [
            "Ann".
            "Billy"
        ].
        "pets" = null.
        "cars" = [
            {
                "model" = "BMW 230".
                "mpg" = 27.5
            }.
            {
                "model" = "Ford Edge".
                "mpg" = 24.1
            }
        ]
    }
"""
```

## Ordenando o resultado

O **método** ``json.dumps()`` possui **parâmetros** para _ordenar as chaves no resultado_.

```
# Utilizando o 'parâmetro' 'sort_keys' para especificar se o resultado deve ser classificado ou não

import json

x = {
    "name": "John",
    "age": 30,
    "married": True,
    "divorced": False,
    "children": ("Ann", "Billy"),
    "pets": None,
    "cars": [
        {"model": "BMW 230", "mpg": 27.5},
        {"model": "Ford Edge", "mpg": 24.1}
    ]
}

# Classificando o resultado em 'ordem alfabética' por chaves
print(json.dumps(x, indent=4, sort_keys=True))

"""Retorna:
    {
        "age": 30,
        "cars": [
            {
                "model": "BMW 230",
                "mpg": 27.5
            },
            {
                "model": "Ford Edge",
                "mpg": 24.1
            }
        ],
        "children": [
            "Ann",
            "Billy"
        ],
        "divorced": false,
        "married": true,
        "name": "John",
        "pets": null
    }
"""
```

---