# For Loops

### Sumário:

- [Python For Loops](#python-for-loops)
- [Loop através de uma string](#loop-através-de-uma-string)
- [A declaração break](#a-declaração-break)
- [A declaração continue](#a-declaração-continue)
- [A função range()](#a-função-range)
- [Else em For Loop](#else-em-for-loop)
- [Loops aninhados](#loops-aninhados)
- [A declaração pass](#a-declaração-pass)

---

## Python For Loops

Um _loop_ ``for`` é usado para **iterar uma sequência** (que é uma **List**, **Tuple**, **Dictionary**, **Set** ou uma **string**).

- Isso é _menos parecido_ com a **palavra-chave** ``for`` em _outras **linguagens de programação**_ e funciona mais como um "_método iterador_" encontrado em _outras **linguagens de programação** orientadas a objetos_.

Com o _loop_ ``for`` é possível **executar um _conjunto de instruções_**, uma vez para _cada item_ de uma **List**, **Tuple**, **Set**, **Dictionary** etc.

```
# Imprimindo cada fruta em uma lista de frutas

fruits = ["apple", "banana", "cherry"]

for x in fruits:
    print(x)

"""Retorna:
    apple
    banana
    cherry
"""
```

- O _loop_ ``for`` não requer que uma **variável de indexação** seja definida antecipadamente.

## Loop através de uma string

As **strings** são _objetos iteráveis_, elas contêm uma _sequência de caracteres_.

```
# Percorrendo as letras da palavra "banana"

for x in "banana":
    print(x)

"""Retorna:
    b
    a
    n
    a
    n
    a
"""
```

## A declaração break

- Com a _instrução_ ``break`` é possível **parar o _loop_** antes que ele percorra _todos os itens_:
    ```
    # Saindo do loop quando 'x' for "banana"

    fruits = ["apple", "banana", "cherry"]

    for x in fruits:
        print(x)

        if x == "banana":
            break

    """Retorna:
        apple
        banana
    """
    ```

    - Saindo do _loop_ quando ``x`` for "**banana**", mas dessa vez o ``break`` vem _antes_ do ``print(x)``:
        ```
        fruits = ["apple", "banana", "cherry"]

        for x in fruits:
            if x == "banana":
                break
            
            print(x)
        
        """Retorna:
            apple
        """
        ```

## A declaração continue

- Com a _instrução_ ``continue`` é possível **parar a iteração atual** do _loop_ e **continuar com a próxima**:
    ```
    # Não imprimindo "banana"

    fruits = ["apple", "banana", "cherry"]

    for x in fruits:
        if x == "banana":
            continue
        
        print(x)
    
    """Retorna:
        apple
        cherry
    """
    ```

## A função ``range()``

Para _percorrer um **conjunto de códigos**_ um determinado _número de vezes_, é possível usar a **função** ``range()``.

- A **função** ``range()`` retorna uma _sequência de números_, começando em **0** (por padrão), e _incrementando_ em **1** (por padrão), e termina em um número especificado:
    ```
    for x in range(6):
        print(x)

    """Retorna:
        0
        1
        2
        3
        4
        5
    """
    ```

    > **Nota**: Em ``range(6)`` **não são valores** de ``0`` a ``6``, mas os **valores** de ``0`` a ``5``.

- A **função** ``range()`` tem como _padrão_ ``0`` como **valor inicial**, porém é possível _especificar o **valor inicial**_ adicionando um **parâmetro** - ``range(2, 6)``, que significa valores de ``2`` a ``6`` (mas _não incluindo_ ``6``):
    ```
    # Usando o parâmetro inicial

    for x in range(2, 6):
        print(x)

    """Retorna:
        2
        3
        4
        5
    """
    ```

- A **função** ``range()`` tem como (padrão) _incrementar a sequência em ``1``_, porém é possível **especificar o valor do _incremento_** adicionando um _terceiro **parâmetro**_ - ``range(2, 30, 3)``:
    ```
    # Aumentando a sequência com '3' (o padrão é '1')

    for x in range(2, 30, 3):
        print(x)

    """Retorna:
        2
        5
        8
        11
        14
        17
        20
        23
        26
        29
    ```

## Else em For Loop

A **palavra-chave** ``else`` em um _loop_ ``for`` especifica um **bloco de código** a ser _executado_ quando o _loop **terminar**_.

```
# Imprimindo todos os números de '0' a '5' e imprimindo uma mensagem quando o loop terminar

for x in range(6):
    print(x)
else:
    print("Finally finished!")

"""Retorna:
    0
    1
    2
    3
    4
    5
    Finally finished!
```

> **Nota**: O bloco ``else`` **NÃO _será executado_** se o _loop_ for interrompido por uma _instrução_ ``break``,

- Quebrando o _loop_ quando ``x`` for **3** e vendo o que acontece com o _bloco_ ``else``:
    ```
    for x in range(6):
        if x == 3:
            break
        print(x)
    else:
        print("Finally finished!")

    """Retorna:
        0
        1
        2
    """
    ```

    > Se o _loop_ é **interrompido**, o _bloco_ ``else`` **não é executado**.

## Loops aninhados

Um _loop **aninhado**_ é um _loop_ **dentro** de um _loop_.

- O "_loop **interno**_", será _executado uma vez_ para **cada iteração** do "_loop **externo**_":
    ```
    # Imprimindo cada adjetivo para cada fruta

    adj = ["red", "big", "tasty"]
    fruits = ["apple", "big", "tasty"]

    for x in adj:
        for y in fruits:
            print(x, y)
    
    """Retorna:
        red apple
        red banana
        red cherry
        big apple
        big banana
        big cherry
        tasty apple
        tasty banana
        tasty cherry
    """
    ```

## A declaração pass

Os _loops_ ``for`` não podem estar _vazios_, mas se por algum motivo tiver um _loop_ ``for`` **sem conteúdo**, basta colocar a _instrução_ ``pass`` para **evitar erro**.

```
for x in [0, 1, 2]:
    pass
```

> **Nota**: Ter um _loop_ ``for`` **vazio** como este _geraria um erro_ sem a **instrução** ``pass``.

---