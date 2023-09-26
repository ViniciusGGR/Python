# RegEx

### Sumário:

- [Módulo RegEx](#módulo-regex)
- [RegEx em Python](#regex-em-python)
- [Funções RegEx](#funções-regex)
- [Metacaracteres](#metacaracteres)
- [Sequências Especiais](#sequências-especiais)
- [Conjuntos](#conjuntos)
- [A Função findall()](#a-função-findall)
- [A Função search()](#a-função-search)
- [A Função split()](#a-função-split)
- [A Função sub()](#a-função-sub)
- [Objeto de correspondência](#objeto-de-correspondência)

---

Um ``RegEx``, ou **Expressão Regular**, é uma _sequência de caracteres_ que forma um **padrão de pesquisa**.

``RegEx`` pode ser usado para "verificar" se uma **string _contém o padrão de pesquisa especificado_**.

## Módulo RegEx

Python possui um **pacote interno** chamado ``re``, que pode ser usado para _trabalhar_ com **Expressões Regulares**.

- Importando o **Module** ``re``:
    ```
    import re
    ```

## RegEx em Python

Após _importar_ o **Module** ``re``, é possível começar a usar **Expressões Regulares**.

```
# Pesquisando a string para ver se ela começa com "The" e termina com "Spain".

import re

txt = "The rain in Spain"
x = re.search("^The. *Spain$", txt)

if x:
    print("YES! We have a match!")
else:
    print("No match")

# Retorna: YES! We have a match!
```

## Funções RegEx

O **Module** ``re`` oferece um _conjunto de **funções**_ que permitem _procurar uma correspondência em uma **string**_.

- ``findall``: Retorna uma **List** contendo todas as correspondências.
- ``search``: Retorna um **Object** "Match" se houver uma correspondência em qualquer lugar da **string**.
- ``split``: Retorna uma **List** onde a **string** foi dividida em cada parte.
- ``sub``: Substitui uma ou mais correspondências por uma **string**.

## Metacaracteres

**Metacaracteres** são caracteres com um _significado especial_.

- ``[]``: Um **Set** de **caracteres**.
- ``\``: Sinaliza uma _sequência especial_ (também pode ser usada para "escapar" de **caracteres especiais**).
- ``.``: Qualquer **caractere** (exceto **caractere** de _nova linha_).
- ``^``: Começa com.
- ``$``: Termina com.
- ``*``: Zero ou mais _ocorrências_.
- ``+``: Uma ou mais _ocorrências_.
- ``?``: Zero ou uma _ocorrência_.
- ``{}``: Exatamente o **número especificado** de _ocorrências_.
- ``|``: Ou.
- ``()``: Capturar e agrupar.

## Sequências Especiais

Uma **sequência especial** é ``\`` seguida por um dos **caracteres** da lista abaixo e tem um _significado especial_.

- ``\A``: Retorna uma _correspondência_ se os **caracteres especificados** estiverem no _início_ da **string**.
- ``\b``: Retorna uma _correspondência_ onde os **caracteres especificados** estão no _início_ ou no _final_ de uma **palavra** (o "``r``" no _início_ garante que a **string** está sendo "tratada" como uma "**string bruta**").
- ``\B``: Retorna uma _correspondência_ onde os **caracteres especificados** estão "presentes", mas _NÃO no início_ (ou no _final_) de uma **palavra** (o "``r``" no _início_ garante que a **string** está sendo "tratada" como uma "**string bruta**").
- ``\d``: Retorna uma _correspondência_ onde a **string** _contém dígitos_ (números de ``0`` a ``9``).
- ``\D``: Retorna uma _correspondência_ onde a **string** _NÃO contém dígitos_.
- ``\s``: Retorna uma _correspondência_ onde a **string** contém um _caractere de **espaço em branco**_.
- ``\S``: Retorna uma _correspondência_ onde a **string** _NÃO_ contém um _caractere de **espaço em branco**_.
- ``\w``: Retorna uma _correspondência_ em que a **string** contém _qualquer caractere de palavra_ (**caracteres** de ``a`` a ``Z``, **dígitos** de ``0`` a ``9`` e o **caractere sublinhado** ``_``).
- ``\W``: Retorna uma _correspondência_ onde a **string** _NÃO_ contém **nenhum caractere de palavra**.
- ``\Z``: Retorna uma _correspondência_ se os **caracteres especificados** estiverem no _final da **string**_.

## Conjuntos

Um **Set** é um _conjunto de **caracteres**_ dentro de um **par de colchetes** ``[]`` com um _significado especial_.

- ``[arn]``: Retorna uma _correspondência_ onde um dos **caracteres especificados** (``a``, ``r`` ou ``n``) está _presente_.
- ``[a-n]``: Retorna uma _correspondência_ para qualquer **caractere minúsculo**, em _ordem alfabética_ entre ``a`` e ``n``.
- ``[^arn]``: Retorna uma _correspondência_ para _qualquer **caractere**_, **EXCETO** ``a``, ``r`` e ``n``.
- ``[0123]``: Retorna uma _correspondência_ onde _qualquer um dos **dígitos especificados**_ (``0``, ``1``, ``2`` ou ``3``) está _presente_.
- ``[0-9]``: Retorna uma _correspondência_ para _qualquer **dígito**_ entre ``0`` e ``9``.
- ``[0-5][0-9]``: Retorna uma _correspondência_ para _qualquer **número** de dois dígitos_ entre ``00`` e ``59``.
- ``[a-zA-Z]``: Retorna uma _correspondência_ para _qualquer **caractere**_ em _ordem alfabética_ entre ``a`` e ``z``, **minúsculo** OU **maiúsculo**.
- ``[+]``: Em **Sets**, ``+``, ``*``, ``.``, ``|``, ``()``, ``$``, ``{}`` _não tem **significado especial**_, então **``[+]``** significa: Retornar uma _correspondência_ para _qualquer **caractere**_ ``+`` na **string**.

## A Função ``findall()``

A **Função** ``findall()`` retorna uma **List** contendo _todas as correspondências_.

```
# Imprimindo uma 'List' de todas as correspondências

import re

txt = "The rain in Spain"
x = re.findall("ai", txt)

print(x)  # Retorna: ['ai', 'ai']
```

A **List** contém as _correspondências_ na **ordem** em que são _encontradas_.

Se _nenhuma correspondências_ for "encontrada", uma **List vazia** será retornada.

```
# Retorna uma 'List vazia' se nenhuma correspondência for encontrada

import re

txt = "The rain in Spain"

x = re.findall("Portugal", txt)
print(x)

if (x):
    print("Yes, there is at least one match!")
else:
    print("No match")

"""Retorna:
    []
    No match
"""
```

## A Função ``search()``

A **Função** ``search()`` "procura" uma _correspondência_ na **string** e retorna um _Object Match_ se houver uma _correspondência_.

Se houver _mais de uma correspondência_, **apenas a primeira ocorrência** da _correspondência_ será retornada.

```
# Procurando o primeiro caractere de espaço em branco na string

import re

txt = "The rain in Spain"
x = re.search("\s", txt)

print("The first white-space character is located in position:", x.start())

# Retorna: The first white-space character is located in position: 3
```

- Se **nenhuma _correspondência_** for encontrada, o _valor_ ``None`` será retornado:
    ```
    import re

    txt = "The rain in Spain"
    x = re.search("Portugal", txt)

    print(x)  # Retorna: None
    ```

## A Função ``split()``

A **Função** ``split()`` retorna uma **List** onde a **string** foi _dividida em cada parte_.

```
# Dividir em cada caractere de 'espaço em branco'

import re

txt = "The rain in Spain"
x = re.split("\s", txt)

print(x)  # Retorna: ['The', 'rain', 'in', 'Spain']
```

- É possível _controlar o número de **ocorrências**_ especificando o **parâmetro** ``maxsplit``:
    ```
    # Dividindo a string apenas na primeira ocorrência

    import re

    txt = "The rain in Spain"
    x = re.split("\s", txt, 1)

    print(x)  # Retorna: ['The', 'rain in Spain']
    ```

## A Função ``sub()``

A **Função** ``sub()`` _substitui as correspondências_ pelo **texto** de sua escolha.

```
# Substituindo cada caractere de 'espaço em branco' pelo número '9'

import re

txt = "The rain in Spain"
x = re.sub("\s", "9", txt)

print(x)  # Retorna: The9rain9in9Spain
```

- É possível _controlar o número de **substituições**_ especificando o **parâmetro** ``count``:
    ```
    # Substituindo as '2 primeiras' ocorrências

    import re

    txt = "The rain in Spain"
    x = re.sub("\s", "9", txt, 2)

    print(x)  # Retorna: The9rain9in Spain
    ```

## Objeto de correspondência

Um _Match Object_ é um **object** que contém _informações_ sobre a **pesquisa** e o **resultado**.

> **Nota**: Se _não houver correspondência_, o **valor** ``None`` será retornado, em vez do _Match Object_.

```
# Fazendo uma 'pesquisa' que retornará um 'Match Object'

import re

txt = "The rain in Spain"
x = re.search("ai", txt)

print(x)  # Retorna: <_sre.SRE_Match object; span=(5, 7), match='ai'>
```

O _Match Object_ possui **propriedades** e **métodos** usados para _recuperar informações_ sobre a **pesquisa** e o **resultado**.

- ``span()``: Retorna uma **Tuple** contendo as _posições **inicial** e **final**_.
    ```
    # Imprimindo a posição (inicial e final) da primeira ocorrência de correspondência.

    # A 'Expressão Regular' procura qualquer palavra que comece com "S" maiúsculo

    import re

    txt = "The rain in Spain"
    x = re.search(r"\bS\w+", txt)

    print(x.span())  # Retorna: (12, 17)
    ```

- ``string``: Retorna uma **string** passada para a **Função**.
    ```
    # Imprimindo a 'string' passada para a função

    import re

    txt = "The rain in Spain"
    x = re.search(r"\bS\w+", txt)

    print(x.string)  # Retorna: The rain in Spain
    ```

- ``group()``: Retorna a _parte_ da **string** onde houve uma _correspondência_.
    ```
    # Imprimindo a parte da 'string' onde houve correspondência.

    # A 'Expressão Regular' procura qualquer palavra que comece com "S" maiúsculo

    import re

    txt = "The rain in Spain"
    x = re.search(r"\bS\w+", txt)

    print(x.group())  # Retorna: Spain
    ```

---