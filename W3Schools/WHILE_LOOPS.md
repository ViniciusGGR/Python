# While Loops

### Sumário:

- [Loops Python](#loops-python)
- [O loop while](#o-loop-while)
- [A declaração break](#a-declaração-break)
- [A declaração continue](#a-declaração-continue)
- [A declaração else](#a-declaração-else)

---

## Loops Python

Python tem _dois comandos_ de **loop primitivos**:

- ``while`` loops.
- ``for`` loops.

## O loop while

Com o _loop_ ``while`` é possível **executar** um _conjunto de instruções_, desde que uma **condição seja _verdadeira_**.

```
# Imprimindo 'i' desde que 'i' seja menor que 6

i = 1

while i < 6:
    print(i)
    i += 1

"""Retorna:
    1
    2
    3
    4
    5
"""
```

> **Nota**: Lembre-se de _incrementar_ ``i``, caso contrário o _loop_ continuará para **sempre**.

O _loop_ ``while`` requer que **variáveis** relevantes estejam prontas, neste exemplo é preciso _definir uma **variável**_ de indexação ``i``, que foi definida como **1**.

## A declaração break

Com a _instrução_ ``break`` é possível **parar o _loop_** mesmo se a _condição ``while`` for **verdadeira**_.

```
# Saindo do loop quando 'i' for 3

i = 1

while i < 6:
    print(i)
    if i == 3:
        break
    i += 1

"""Retorna:
    1
    2
    3
"""
```

## A declaração continue

Com a _instrução_ ``continue`` é possível **parar a _iteração_ atual** e _continuar com a próxima_.

```
# Continuando para a próxima iteração se 'i' for 3

i = 0

while i < 6:
    i += 1
    if i == 3:
        continue
    print(i)

"""Retorna:
    1
    2
    4
    5
    6
"""

# Observe que o número '3' está faltando no resultado.
```

## A declaração else

Com a _instrução_ ``else`` é possível **executar um _bloco de código_ uma vez quando a _condição não for mais_ verdadeira**.

```
# Imprimindo uma mensagem quando a condição for falsa

i = 1

while i < 6:
    print(i)
    i += 1
else:
    print("'i' is no longer less than 6")

"""Retorna:
    1
    2
    3
    4
    5
    'i' is no longer less than 6
"""
```

---