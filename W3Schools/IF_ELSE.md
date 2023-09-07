# If...Else

### Sumário:

- [Condições Python e Instruções If](#condições-python-e-instruções-if)
- [Indentação](#indentação)
- [Elif](#elif)
- [Else](#else)
- [Short Hand If](#short-hand-if)
- [Short Hand If...Else](#short-hand-ifelse)
- [And](#and)
- [Or](#or)
- [Not](#not)
- [If Aninhado](#if-aninhado)
- [A Declaração pass](#a-declaração-pass)

---

## Condições Python e Instruções If

Python suporta as _condições lógicas_ usuais da **matemática**:

- Igual a: ``a == b``.
- Não é igual: ``a != b``.
- Menor que: ``a < b``.
- Menor ou igual a: ``a <= b``.
- Maior que: ``a > b``.
- Maior ou igual a: ``a >= b``.

Essas _condições_ podem ser usadas de **diversas maneiras**, mais comumente em "_instruções ``if``_" e _loops_.

- Uma "_instrução ``if``_" é escrita usando a **palavra-chave** ``if``:
    ```
    # Testando se 'b' é maior que 'a'
    a = 33
    b = 200

    if b > a:
        print("'b' is greater than 'a'")

    # Retorna: 'b' is greater than 'a'
    ```

## Indentação

Python **depende** de _indentação_ (recuo - **espaço em branco** no _início de uma linha_) para **definir** o _escopo no código_.

> **Nota**: Outras linguagens de programação costumam usar _colchetes_ para essa finalidade.

```
# Instrução if, sem recuo (irá gerar um erro)

a = 33
b = 200

if b > a:
print("'b' is greater than 'a'")

# Retorna: you will get an error - IndentationError: expected an indented block
```

## Elif

A **palavra-chave** ``elif`` é a maneira do Python dizer "_se as condições anteriores não eram verdadeiras, tente esta condição_".

```
a = 33
b = 33

if b > a:
    print("'b' is greater than 'a'")
elif a == b:
    print("'a' and 'b' are equal")

# Retorna: 'a' and 'b' are equal
```

- Neste exemplo ``a`` é _igual a_ ``b``, então a **primeira condição _não é verdadeira_**, mas a **condição** ``elif`` é _verdadeira_.

## Else

A **palavra-chave** ``else`` captura _qualquer coisa_ que **não** seja capturada pelas _condições anteriores_.

```
a = 200
b = 33

if b > a:
    print("'b' is greater than 'a'")
elif a == b:
    print("'a' and 'b' are equal")
else:
    print("'a' is greater than 'b'")

# Retorna: 'a' is greater than 'b'
```

- Neste exemplo ``a`` é _maior que_ ``b``, então a **primeira condição _não é verdadeira_**, também a **condição** ``elif`` _não é verdadeira_.
- É possível ter um ``else`` sem ``elif``:
    ```
    a = 200
    b = 33

    if b > a:
        print("'b' is greater than 'a'")
    else:
        print("'b' is not greater than 'a'")

    # Retorna: 'b' is not greater than 'a'
    ```

## Short Hand If

Se tiver _apenas uma **instrução**_ para **executar**, poderá colocá-la na _mesma linha_ da **instrução** ``if``.

```
# Declaração 'if' de uma linha

a = 200
b = 33

if a > b: print("'a' is greater than 'b'")

# Retorna: 'a' is greater than 'b'
```

## Short Hand If...Else

Se tiver _apenas uma **instrução**_ para **executar**, uma para ``if`` e outra para ``else``, poderá colocar _tudo na mesma linha_.

```
# Instrução 'if' 'else' de uma linha

a = 2
b = 330

print("A") if a > b else print("B")

# Retorna: B
```

> **Nota**: Esta técnica é conhecida como **Operadores Ternários** ou **Expressões Condicionais**.

- É possível ter _várias instruções_ ``else`` na **mesma linha**:
    ```
    a = 330
    b = 330

    print("A") if a > b else print("=") if a == b else print("B")

    Retorna: =
    ```

## And

A **palavra-chave** ``and`` é um _operador lógico_ e é usada para **combinar instruções condicionais**.

```
# Testando se 'a' é maior que 'b' e se 'c' é maior que 'a'

a = 200
b = 33
c = 500

if a > b and c > a:
    print("Both conditions are 'True'")

# Retorna: Both conditions are 'True'
```

## Or

A **palavra-chave** ``or`` é um _operador lógico_ é usada para **combinar instruções condicionais**.

```
# Testando se 'a' é maior que 'b', OU se 'a' é maior que 'c'

a = 200
b = 33
c = 500

if a > b or a > c:
    print("At least one of the conditions is 'True'")

# Retorna: At least one of the conditions is 'True'
```

## Not

A **palavra-chave** ``not`` é um _operador lógico_ e é usada para **reverter o resultado da _instrução condicional_**.

```
# Testando se 'a' NÃO é maior que 'b'

a = 33
b = 200

if not a > b:
    print("'a' is NOT greater than 'b'")

# Retorna: 'a' is NOT greater than 'b'
```

## If Aninhado

É possível ter _instruções_ ``if`` **dentro** de _instruções_ ``if``, isso é chamado de _instruções ``if`` **aninhadas**_.

```
x = 41

if x > 10:
    print("Above ten,")
    if x > 20:
        print("and also above 20!")
    else:
        print("but not above 20.")

"""Retorna:
    Above ten,
    ando also above 20!
```

## A Declaração pass

As _instruções_ ``if`` **não podem estar vazias**, mas se por algum motivo tiver uma _instrução_ ``if`` **sem conteúdo**, coloque ``pass`` na _instrução_ para **evitar erros**.

```
a = 33
b = 200

if b > a:
    pass
```

---