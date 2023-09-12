# Functions

### Sumário:

- [Criando uma Função](#criando-uma-função)
- [Chamando uma Função](#chamando-uma-função)
- [Argumentos](#argumentos)
- [Parâmetros ou Argumentos?](#parâmetros-ou-argumentos)
- [Número de Argumentos](#número-de-argumentos)
- [Argumentos Arbitrários, *args](#argumentos-arbitrários-args)
- [Argumentos de palavras-chave](#argumentos-de-palavras-chave)
- [Argumentos de palavras-chave Arbitrárias, **kwargs](#argumentos-de-palavras-chave-arbitrárias-kwargs)
- [Valor de Parâmetro padrão](#valor-de-parâmetro-padrão)
- [Passando uma Lista como Argumento](#passando-uma-lista-como-argumento)
- [Valores de Retorno](#valores-de-retorno)
- [A declaração pass](#a-declaração-pass)
- [Recursão](#recursão)

---

Uma **função** é um _bloco de código_ que só é **executado** quando é _chamado_.

É possível passar _dados_, conhecidos como "**parâmetros**", para uma **função**.

- Uma **função** pode _retornar dados_ como **resultado**.

## Criando uma Função

Em Python, uma **função** é _definida_ usando a _palavra-chave_ ``def``.

```
def my_function():
    print("Hello from a function")
```

## Chamando uma Função

Para "_chamar_" uma **função**, basta utilizar o _nome da **função**_ seguido de **parênteses** ``()``.

```
def my_function():
    print("Hello from a function")

my_function()

# Retorna: Hello from a function
```

## Argumentos

As "_informações_" podem ser passadas para **funções** como _argumentos_.

Os _argumentos_ são **especificados após** o _nome da **função**_, entre **parênteses** ``()``. É possível adicionar quantos _argumentos_ quiser, basta separá-los com **vírgula** ``,``.

- O exemplo a seguir possui uma **função** com um _argumento_ (``fname``). Quando a **função** é "_chamada_", é passado um "**primeiro nome**, que é usado dentro da **função** para _imprimir o **nome completo**_:
    ```
    def my_function(fname):
        print(fname + " Refsnes")

    my_function("Emil")    # Retorna: Emil Refsnes
    my_function("Tobias")  # Retorna: Tobias Refsnes
    my_function("Linus")   # Retorna: Linus Refsnes
    ```

> **Nota**: Os _argumentos_ são frequentemente abreviados para ``args`` nas documentações do Python.

## Parâmetros ou Argumentos?

Os termos _parâmetros_ e _argumentos_ podem ser usados para a mesma coisa: **informações** que são passadas para uma **função**.

- Da perspectiva de uma **função**:
    - Um _parâmetro_ é a **variável** listada entre **parênteses** na _definição_ da **função**.
    - Um _argumento_ é o **valor** enviado à **função** quando ela é _chamada_.

## Número de Argumentos

Por padrão, uma **função** _deve ser chamada_ com o _número correto de **argumentos**_. O que significa que se a **função** "espera" _2 argumentos_, deve-se "chamar" a **função** com _2 argumentos_, nem mais, nem menos.

```
# Esta função espera 2 argumentos e obtém 2 argumentos

def my_function(fname, lname):
    print(fname + " " + lname)

my_function("Emil", "Refsnes")  # Retorna: Emil Refsnes
```

- Caso tente "chamar" uma **função** que espera _2 argumentos_ com ``1`` ou ``3`` _argumentos_, receberá um **erro**:
    ```
    # Esta função espera 2 argumentos, mas obtém apenas 1

    def my_function(fname, lname):
        print(fname + " " + lname)

    my_function("Emil")

    # Retorna: my_function() missing 1 required positional argument: 'lname'
    ```

## Argumentos Arbitrários, *args

Se não se sabe quantos _argumentos_ serão passados para uma **função**, adicione um ``*`` **antes do nome do _parâmetro_** na _definição da **função**_.

- Desta forma a **função** receberá uma **tuple de _argumentos_**, e poderá acessar os _itens_ de acordo:
    ```
    # Se o número de argumentos for desconhecido, adicione um '*' antes do nome do parâmetro

    def my_function(*kids):
        print("The youngest child is " + kids[2])

    my_function("Emil", "Tobias", "Linus")

    # Retorna: The youngest child is Linus
    ```

> **Nota**: Os _argumentos arbitrários_ são frequentemente abreviados para ``*args`` nas documentações do Python.

## Argumentos de palavras-chave

É possível "enviar" _argumentos_ com a **sintaxe** _chave = valor_.

- Desta forma, a **ordem dos _argumentos_** não importa:
    ```
    def my_function(child3, child2, child1):
        print("The youngest child is " + child3)

    my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")

    # Retorna: The youngest child is Linus
    ```

> **Nota**: Os _argumentos de palavra-chave_ são frequentemente abreviados para ``kwargs`` nas documentações do Python.

## Argumentos de palavras-chave Arbitrárias, **kwargs

Se não se sabe quantos _argumentos de palavra-chave_ serão passados para uma **função**, adicione dois ``**`` **antes do nome do _parâmetro_** na _definição da **função**_.

- Desta forma a **função** receberá um **dictionary de _argumentos_**, e poderá acessar os _itens_ de acordo:
    ```
    # Se o número de argumentos de palavra-chave for desconhecido, adicione um duplo '**' antes do nome do parâmetro

    def my_function(**kid):
        print("His last name is " + kid["lname"])

    my_function(fname = "Tobias", lname = "Refsnes")

    # Retorna: His last name is Refsnes
    ```

> **Nota**: Os _argumentos Kword arbitrários_ são frequentemente abreviados para ``**kwargs`` nas documentações do Python.

## Valor de Parâmetro padrão

O exemplo a seguir mostra como usar um _valor de **parâmetro** padrão_.

Se uma **função** for "chamada" _sem argumentos_, ela usará o **valor padrão**.

```
def my_function(country = "Norway"):
    print("I am from " + country)

my_function("Sweden")  # Retorna: I am from Sweden
my_function("India")   # Retorna: I am from India
my_function()          # Retorna: I am from Norway
my_function("Brazil")  # Retorna: I am from Brazil
```

## Passando uma Lista como Argumento

É possível enviar _qualquer **tipo** de argumento de dados_ para uma **função** (string, number, list, dictionary, etc.), e ele será tratado como o mesmo _tipo de dados_ dentro da **função**.

- Por exemplo, se for enviado uma **List como _argumento_**, ela ainda será uma **List** quando chegar à **função**:
    ```
    def my_function(food):
        for x in food:
            print(x)

    fruits = ["apple", "banana", "cherry"]

    my_function(fruits)

    """Retorna:
        apple
        banana
        cherry
    """
    ```

## Valores de Retorno

Para permitir que uma **função** _retorne um valor_, basta utilizar a **instrução** ``return``.

```
def my_function(x):
    return 5 * x

print(my_function(3))  # Retorna: 15
print(my_function(5))  # Retorna: 25
print(my_function(9))  # Retorna: 45
```

## A declaração pass

As _definições_ ``function`` não podem ficar **vazias**, mas se por algum motivo tiver uma _definição_ ``function`` sem conteúdo, coloque-a na _instrução_ ``pass`` para **evitar erro**.

```
def my_function():
    pass
```

## Recursão

Python também aceita _recursão de **função**_, o que significa que uma **função** definida pode "chamar" a si mesma.

A _recursão_ é um **conceito matemático** e de **programação** comum. Isso significa que uma **função** "chama" a si mesma. Isso tem a vantagem de significar que é possível _percorrer os dados_ para chegar a um **resultado**.

Deve-se ter **muito cuidado** com a _recursão_, pois pode ser muito fácil escrever uma **função** que _nunca termina_ ou que _usa quantidades excessivas de memória ou potência do processador_. No entanto, a _recursão_ pode ser uma **abordagem de programação muito _eficiente_ e matematicamente elegante**.

- Neste exemplo, ``tri_recursion()`` é uma **função** que foi definida para "chamar" a si mesma ("**recurse**"). Foi utilizado a _variável_ ``k`` como dados, que diminui (``-1``) toda vez que é recorrida. A _recursão_ termina quando a **condição** não é _maior que ``0``_ (ou seja, **quando é ``0``**):
    ```
    # Exemplo de recursão

    def tri_recursion(k):
        if(k > 0):
            result = k + tri_recursion(k - 1)
            print(result)
        else:
            result = 0
        return result
    
    print("\n\nRecursion Example Results")
    tri_recursion(6)

    """Retorna:
        Recursion Example Results
        1
        3
        6
        10
        15
        21
    """
    ```

---