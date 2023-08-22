# Variables

### Sumário

- [Criando Variáveis](#criando-variáveis)
- [Casting](#casting)
- [Obter o tipo](#obter-o-tipo)
- [Aspas Simples ou Duplas?](#aspas-simples-ou-duplas)
- [Maiúsculas e minúsculas](#maiúsculas-e-minúsculas)
---
- [Nomes de Variáveis](#nomes-de-variáveis)
- [Nomes de Variáveis com várias palavras](#nomes-de-variáveis-com-várias-palavras)
    - [Camel Case](#camel-case)
    - [Pascal Case](#pascal-case)
    - [Snake Case](#snake-case)

---

Variáveis são "recipientes" para **armazenar valores de dados**.

## Criando Variáveis

- Python não tem "comando" para _declarar uma variável_.
- Uma **variável** é criada no momento em que se _atribui um valor_ a ela.

```
x = 5
y = "John"

print(x)
print(y)
```

As **variáveis** não precisam ser _declaradas_ com nenhum _tipo_ específico e podem até mudar de tipo depois de terem sido definidas.

```
x = 4        # 'x' é do tipo 'int'.
x = "Sally"  # 'x' é agora do tipo 'str'.

print(x)
```

## Casting

- Se deseja _especificar o tipo de dados_ de uma **variável**, isso pode ser feito com a _conversão_ (Casting):
    ```
    x = str(3)    # 'x' vai ser '3'.
    y = int(3)    # 'y' vai ser 3.
    z = float(3)  # 'z' vai ser 3.0.
    ```

## Obter o tipo

- É possível obter o _tipo de dados_ de uma **variável** com a _função_ ``type()``:
    ```
    x = 5
    y = "John"

    print(type(x))  # Retorna: <class 'int'>
    print(type(y))  # Retorna: <class 'str'>
    ```

## Aspas Simples ou Duplas?

- As **variáveis** do _tipo_ ``string`` podem ser declaradas usando aspas simples ou duplas:
    ```
    # Funcionam da mesma forma:
    x = "John"
    x = 'John'
    ```

## Maiúsculas e minúsculas

- Os nomes das **variáveis** _diferenciam_ maiúsculas de minúsculas.
    ```
    # 'A' não vai sobrescrever 'a'
    a = 4
    A = "Sally"

    print(a)  # Retorna: 4
    print(A)  # Retorna: Sally
    ```

---

## Nomes de Variáveis

Uma **variável** pode ter um _nome curto_ (como ``x`` e ``y``), ou um _nome mais descritivo_ (``age``, ``carname``, ``total_volume``).

- Regras para **variáveis** Python:
    - **Nome de variável** deve _começar_ com uma **letra** ou o caractere de **sublinhado**. 
    - **Nome de variável** _não pode começar_ com um **número**.
    - **Nome de variável** pode conter _apenas_ **caracteres alfanuméricos** e **sublinhados** (``Az``, ``0-9`` e ``_``).
    - **Nome de variável** _diferenciam_ **maiúsculas** de **minúsculas** (``age``, ``Age`` e ``AGE`` são _três_ **variáveis** diferentes).
    - **Nome de variável** _não pode_ ser nenhuma das **palavras-chave** do Python.

```
# Nomes de variáveis "legais":

myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"
```

```
# Nomes de variáveis "ilegais":

2myvar = "John"
my-var = "John"
my var = "John"
```

> **Nota**: _Nomes de variáveis_ diferenciam maiúsculas de minúsculas.

## Nomes de Variáveis com várias palavras

- **Nomes de variáveis** com mais de uma palavra podem ser difíceis de ler.

Existem várias técnicas que tornam os nomes mais legíveis.

### Camel Case

- Cada palavra, exceto a primeira, _começa_ com letra **maiúscula**:
    ```
    myVariableName = "John"
    ```

### Pascal Case

- Cada palavra _começa_ com uma letra **maiúscula**:
    ```
    MyVariableName = "John"
    ```

### Snake Case

Cada palavra é _separada_ por um caractere de **sublinhado** (``_``):
    ```
    my_variable_name = "John"
    ```

---

