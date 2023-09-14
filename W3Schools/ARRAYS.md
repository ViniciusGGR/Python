# Arrays

### Sumário:

- [Arrays](#arrays-1)
- [O que é um Array?](#o-que-é-um-array)
- [Acesse os Elementos de um Array](#acesse-os-elementos-de-um-array)
- [O comprimento de um Array](#o-comprimento-de-um-array)
- [Loop nos Elementos do Array](#loop-nos-elementos-do-array)
- [Adicionando Elementos no Array](#adicionando-elementos-no-array)
- [Removendo Elementos do Array](#removendo-elementos-do-array)
- [Métodos Array](#métodos-array)

---

> **Nota**: Python _não tem suporte integrado_ para **Arrays**, mas **List** pode ser _usado em seu lugar_.

## Arrays

> **Nota**: Mostrando como usar ``List`` como ``Array``, porém, para trabalhar como ``Arrays`` em Python "deve-se" _importar uma **biblioteca**_, como a **biblioteca** ``NumPy``.

- ``Arrays`` são usados para _armazenar vários valores_ em uma única **variável**:
    ```
    # Criando um 'array' contendo nomes de carros

    cars = ["Ford", "Volvo", "BMW"]
    print(cars)  # Retorna: ['Ford', 'Volvo', 'BMW']
    ```

## O que é um Array?

Um ``Array`` é uma **variável** especial que pode conter _mais de um valor_ por vez.

- Caso tenha uma **List** de _itens_ (**List** de _nomes de carros_, por exemplo), _armazenar_ os carros em **variáveis** únicas poderia ser assim:
    ```
    car1 = "Ford"
    car2 = "Volvo"
    car3 = "BMW"
    ```
    
    A solução é um ``Array``!

    - Um ``Array`` pode conter _muitos valores_ sob um **único nome** e é possível _acessar os valores_ referindo-se a um **número de índice**.

## Acesse os Elementos de um Array

É possível _acessar um Elemento_ do ``Array`` referindo-se ao _número do índice_.

```
# Obtendo o valor do primeiro item do Array

cars = ["Ford", "Volvo", "BMW"]

x = cars[0]

print(x)  # Retorna: Ford
```

```
# Modificando o valor do primeiro item do Array

cars = ["Ford", "Volvo", "BMW"]

cars[0] = "Toyota"

print(cars)  # Retorna: ['Toyota', 'Volvo', 'BMW']
```

## O comprimento de um Array

O **método** ``len()`` retorna o _comprimento_ de um ``Array`` (o _número de elementos_ em um ``Array``).

```
# Retornando o número de elementos do Array 'cars'

cars = ["Ford", "Volvo", "BMW"]

x = len(cars)

print(x)  # Retorna: 3
```

> **Nota**: O _comprimento_ de um ``Array`` é sempre **um a mais** que o _índice mais alto_ do ``Array``.

## Loop nos Elementos do Array

- É possível utilizar o **loop** ``for in`` para _percorrer todos os elementos_ de um ``Array``:
    ```
    # Imprimindo cada item do Array 'cars'

    cars = ["Ford", "Volvo", "BMW"]

    for x in cars:
        print(x)

    """Retorna:
        Ford
        Volvo
        BMW
    """
    ```

## Adicionando Elementos no Array

- É possível utilizar o **método** ``append()`` para _adicionar um elemento_ a um ``Array``:
    ```
    # Adicionando mais um elemento ao Array 'cars'

    cars = ["Ford", "Volvo", "BMW"]

    cars.append("Honda")

    print(cars)  # Retorna: ['Ford', 'Volvo', 'BMW', 'Honda']
    ```

## Removendo Elementos do Array

- É possível utilizar o **método** ``pop()`` para _remover um elemento_ do ``Array``:
    ```
    # Excluindo o segundo elemento do Array 'cars'

    cars = ["Ford", "Volvo", "BMW"]

    cars.pop(1)

    print(cars)  # Retorna: ['Ford', 'BMW']
    ```

    Também é possível utilizar o **método** ``remove()`` para _remover um elemento_ do ``Array``:

    ```
    # Excluindo o elemento que possui o valor "Volvo"

    cars = ["Ford", "Volvo", "BMW"]

    cars.remove("Volvo")

    print(cars)  # Retorna: ['Ford', 'BMW']
    ```

    > **Nota**: O **método** de **List** ``remove()`` _remove_ apenas a **primeira ocorrência** do _valor especificado_.

## Métodos Array

Python possui um _conjunto de métodos integrados_ para usar em **Lists/Arrays**:

- ``append()``: Adiciona um _elemento_ no final da **List**.
- ``clear()``: Remove _todos os elementos_ da **List**.
- ``copy()``: Retorna uma _cópia_ da **List**.
- ``count()``: Retorna o _número de elementos_ com o **valor especificado**.
- ``extend()``: Adiciona os _elementos_ de uma **List** (ou qualquer _iterável_) ao final da **List** atual.
- ``index()``: Retorna o _índice_ do **primeiro elemento** com o _valor especificado_.
- ``insert()``: Adiciona um _elemento_ na **posição especificada**.
- ``pop()``: Remove o _elemento_ na **posição especificada**.
- ``remove()``: Remove o _primeiro item_ com o **valor especificado**.
- ``reverse()``: Inverte a ordem da **List**.
- ``sort()``: Classifica a **List**.

> **Nota**: Python _não tem suporte integrado_ para **Arrays**, mas **List** pode ser _usado em seu lugar_.

---