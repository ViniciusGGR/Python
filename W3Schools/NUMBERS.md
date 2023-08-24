# Numbers

### Sumário:

- [Números Python](#números-python)
- [Int](#int)
- [Float](#float)
- [Complex](#complex)
- [Conversão de tipo](#conversão-de-tipo)
- [Random Number](#random-number)

---

## Números Python

- Existem três _tipos numéricos_ em Python:
    - ``int``.
    - ``float``.
    - ``complex``.

**Variáveis** de _tipos numéricos_ são criadas quando se atribui um valor a elas.

```
x = 1    # int.
y = 2.8  # float.
z = 1j   # complex.
```

- Para verificar o _tipo_ de qualquer objeto em Python, utilize a **função** ``type()``:
    ```
    x = 1    # int.
    y = 2.8  # float.
    z = 1j   # complex.

    print(type(x))  # Retorna: <class 'int'>
    print(type(y))  # Retorna: <class 'float'>
    print(type(z))  # Retorna: <class 'complex'>
    ```

## Int

``int``, ou _inteiro (integer)_, é um **número inteiro**, positivo ou negativo, sem decimais, de comprimento ilimitado.

```
x = 1                  # int.
y = 35653222554887711  # int.
z = -3255522           # int.

print(type(x))  # Retorna: <class 'int'>
print(type(y))  # Retorna: <class 'int'>
print(type(z))  # Retorna: <class 'int'>
```

## Float

``float``, ou "_número de ponto flutuante_" é um número, positivo ou negativo, contendo **uma ou mais casas decimais**.

```
x = 1.10    # float.
y = 1.0     # float.
z = -35.59  # float.

print(type(x))  # Retorna: <class 'float'>
print(type(y))  # Retorna: <class 'float'>
print(type(z))  # Retorna: <class 'float'>
```

- ``float`` também pode ser um _número científico_ com um "``e``" para **indicar a potência de 10**:
    ```
    x = 35e3       # float.
    y = 12E4       # float.
    z = -87.7e100  # float.

    print(type(x))  # Retorna: <class 'float'>
    print(type(y))  # Retorna: <class 'float'>
    print(type(z))  # Retorna: <class 'float'>
    ```

## Complex

Os **números complexos** são escritos com um "``j``" como _parte imaginária_.

```
x = 3+5j  # complex.
y = 5j    # complex.
z = -5j   # complex.

print(type(x))  # Retorna: <class 'complex'>
print(type(y))  # Retorna: <class 'complex'>
print(type(z))  # Retorna: <class 'complex'>
```

## Conversão de tipo

- É possível **converter** de um _tipo para outro_ com os **métodos**: ``int()``, ``float()`` e ``complex()``:
    ```
    # Convertendo de um tipo para outro:

    x = 1    # int.
    y = 2.8  # float.
    z = 1j   # complex.

    # Convertendo de 'int' para 'float'.
    a = float(x)  # Retorna: 1.0

    # Convertendo de 'float' para 'int'.
    b = int(y)  # Retorna: 2

    # Convertendo de 'int' para 'complex'.
    c = complex(x) # Retorna: (1+0j)

    print(a)  # 1.0
    print(b)  # 2
    print(c)  # (1+0j)

    print(type(x))  # Retorna: <class 'float'>
    print(type(y))  # Retorna: <class 'int'>
    print(type(z))  # Retorna: <class 'complex'>
    ```

> **Nota**: Não é possível converter números complexos em outro tipo de número.

## Random Number

Python _não tem_ uma **função** ``random()`` para criar _números aleatórios_, mas Python _possui_ um **módulo interno** chamado ``random`` que pode ser usado para criar _números aleatórios_.

```
import random

print(random.randrange(1, 10))  # Imprime/Printa um número aleatório entre '1' e '10'.
```

---