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
- [Muitos valores para várias variáveis](#muitos-valores-para-várias-variáveis)
- [Um valor para várias variáveis](#um-valor-para-várias-variáveis)
- [Descompactar uma coleção](#descompactar-uma-coleção)
---
- [Variáveis de Saída](#variáveis-de-saída)

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

## Muitos valores para várias variáveis

- O Python permite a _atribuição de valores_ a **várias variáveis** em uma linha:
    ```
    x, y, z = "Orange", "Banana", "Cherry"

    print(x)  # Retorna: Orange
    print(y)  # Retorna: Banana
    print(z)  # Retorna: Cherry
    ```

    > **Nota**: Certifique-se de que o _número de variáveis_ corresponda ao _número de valores_, caso contrário, ocorrerá um erro.

## Um valor para várias variáveis

- O Python permite _atribuir o mesmo valor_ a **várias variáveis** em uma linha:
    ```
    x = y = z = "Orange"

    print(x)  # Retorna: Orange
    print(y)  # Retorna: Orange
    print(z)  # Retorna: Orange
    ```

## Descompactar uma coleção

Se existir uma _coleção de valores_ em uma **lista**, **tupla** etc. O Python permite a _extração dos valores_ em **variáveis**. Isso é chamado de _descompactação_ (``unpacking``).

```
# Descompactar uma lista:

fruits = ["apple", "banana", "cherry"]
x, y, z = fruits

print(x)  # Retorna: apple
print(y)  # Retorna: banana
print(z)  # Retorna: cherry
```

---

## Variáveis de Saída

- No Python a _função_ ``print()`` é frequentemente usada para **variáveis de saída**.
    ```
    x = "Python is awesome"

    print(x)  # Retorna: Python is awesome
    ```

- Na _função_ ``print()``, você "gera/imprime/printa" _várias variáveis_, separadas por vírgula:
    ```
    x = "Python"
    y = "is"
    z = "awesome"

    print(x, y, z)  # Retorna: Python is awesome
    ```

    - Também é possível usar o _operador_ ``+`` para "gerar/imprimir/printar" _várias variáveis_.

    ```
    x = "Python "
    y = "is "
    z = "awesome"

    print(x + y + z)  # Retorna: Python is awesome
    ```

    > **Nota**: Observe o _caractere de espaço_ após ``"Python "`` e ``"is "``, sem eles o **resultado** seria: **``Pythonisawesome``**.

- Para **números**, o _caractere_ ``+`` funciona como um **operador matemático**:
    ```
    x = 5
    y = 10

    print(x + y)  # Retorna: 15
    ```

- Na _função_ ``print()``, ao tentar "combinar" uma **string** e um **número** com o _operador_ ``+``, o Python vai te dar um **_erro_**:
    ```
    x = 5
    y = "John"

    print(x + y)

    # Retorna: TypeError: unsupported operand type(s) for +: 'int' and 'str'
    ```

- A "melhor maneira" de "gerar/imprimir/printar" _várias variáveis_ na _função_ ``print()`` é **separá-las com vírgulas**, que até suportam _diferentes tipos de dados_:
    ```
    x = 5
    y = "John"

    print(x, y)  # Retorna: 5 John
    ```

---

