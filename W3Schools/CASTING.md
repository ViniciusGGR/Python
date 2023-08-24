# Casting

### Sumário:

- [Especifique um tipo de variável](#especifique-um-tipo-de-variável)
    - [Int](#int)
    - [Float](#float)
    - [String](#string)

---

## Especifique um tipo de variável 

Especificando um _tipo_ para uma **variável**. Isso pode ser feito com **casting**. Python é uma linguagem _orientada a objetos_ e, como tal, usa **classes** para definir _tipos de dados_, incluindo seus **tipos primitivos**.

- A _conversão_ em Python é, portanto, feita usando **funções construtoras**:
    - ``int()`` - Constrói um _número inteiro_ a partir de um **literal inteiro**, um **literal float** (removendo todos os decimais) ou um **literal de string** (desde que a **string** represente um _número inteiro_).
    - ``float()`` - Constrói um _número float_ a partir de um **literal inteiro**, um **literal float** ou um **literal string** (desde que a **string** represente um _float_ ou um _inteiro_).
    - ``str()`` - Constrói uma _string_ a partir de uma ampla variedade de _tipos de dados_, incluindo **strings**, **literais inteiros** e **literais float**.

### Int

```
x = int(1)    # 'x' vai ser: 1
y = int(2.8)  # 'y' vai ser: 2
z = int("3")  # 'z' vai ser: 3
```

### Float

```
x = float(1)      # 'x' vai ser: 1.0
y = float(2.8)    # 'y' vai ser: 2.8
z = float("3")    # 'z' vai ser: 3.0
w = float("4.2")  # 'w' vai ser: 4.2
```

### String

```
x = str("s1")  # 'x' vai ser: 's1'
y = str(2)     # 'y' vai ser: '2'
z = str(3.0)   # 'z' vai ser: '3.0'
```

---