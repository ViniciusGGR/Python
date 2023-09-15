# Iterators

### Sumário:

- [Iteradores Python](#iteradores-python)
- [Iterador vs Iterável](#iterador-vs-iterável)
- [Loop através de um Iterador](#loop-através-de-um-iterador)
- [Criar um Iterador](#criar-um-iterador)
- [Parar Iteração](#parar-iteração)

---

## Iteradores Python

Um _iterador_ é um _object_ que contém um **número _contável_ de valores**.

Um _iterador_ é um _object_ que pode ser **iterado**, o que significa que é possível _percorrer todos os valores_.

Tecnicamente, em Python, um _iterador_ é um _object_ que **implementa o protocolo do _iterador_**, que consiste nos **métodos** ``__iter__()`` e ``__next__()``.

## Iterador vs Iterável

**Lists**, **Tuples**, **Dictionaries** e **Sets** são todos _objects iteráveis_. Eles são **contêineres** _iteráveis_ dos quais se pode obter um _iterador_.

- Todos esses _objects_ possuem um **método** ``__iter__()`` que é usado para obter um _iterador_:
    ```
    # Retornando um 'iterador' de uma tuple e imprimindo cada valor

    mytuple = ("apple", "banana", "cherry")
    myit = iter(mytuple)

    print(next(myit))  # Retorna: apple
    print(next(myit))  # Retorna: banana
    print(next(myit))  # Retorna: cherry
    ```

- Até mesmo **strings** são _objects **iteráveis**_ e podem retornar um _iterador_:
    ```
    # Strings também são objects iteráveis, contendo uma sequência de caracteres

    mystr = "banana"
    myit = iter(mystr)

    print(next(myit))  # Retorna: b
    print(next(myit))  # Retorna: a
    print(next(myit))  # Retorna: n
    print(next(myit))  # Retorna: a
    print(next(myit))  # Retorna: n
    print(next(myit))  # Retorna: a
    ```

## Loop através de um Iterador

Também é possível usar um _loop_ ``for`` para _iterar_ através de um _object iterável_.

```
# Iterando os valores de uma 'tuple'

mytuple = ("apple", "banana", "cherry")

for x in mytuple:
    print(x)

"""Retorna:
    apple
    banana
    cherry
"""
```

```
# Iterando os caracteres de uma 'string'

mystr = "banana"

for x in mystr:
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

- Na verdade, o _loop_ ``for`` cria um _object iterador_ e executa o **método** ``next()`` para cada _loop_.

## Criar um Iterador

Para criar um _object/class_ como um _iterador_ deve-se implementar os **métodos** ``__iter__()`` e ``__next__()`` no _object_.

Todas as _classes_ têm uma **função** ``__init__()``, que permite fazer _algumas inicializações_ quando o _object_ está sendo **criado**.

- O **método** ``__iter__()`` age de forma semelhante, é possível fazer **operações** (inicializar, etc.), mas deve sempre _retornar o próprio object iterador_.
- O **método** ``__next__()`` também permite fazer **operações**, devendo retornar o _próximo item da sequência_.

```
# Criando um iterador que retorne números, começando com '1', e cada sequência aumentará em um (retornando 1, 2, 3, 4, 5, etc.)

class MyNumbers:
    def __iter__(self):
        self.a = 1
        return self

    def __next__(self):
        x = self.a
        self.a += 1
        return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))  # Retorna: 1
print(next(myiter))  # Retorna: 2
print(next(myiter))  # Retorna: 3
print(next(myiter))  # Retorna: 4
print(next(myiter))  # Retorna: 5
print(next(myiter))  # Retorna: 6
print(next(myiter))  # Retorna: 7
print(next(myiter))  # Retorna: 8
print(next(myiter))  # Retorna: 9
print(next(myiter))  # Retorna: 10
```

## Parar Iteração

O exemplo acima **continuaria para sempre** se tivesse _instruções_ ``next()`` suficientes ou se fosse usado em um _loop_ ``for``.

Para evitar que a _iteração_ continue para sempre, basta utilizar a _instrução_ ``StopIteration``.

- No **método** ``__next__()``, é possível adicionar uma **condição de terminação** para _gerar um erro_ se a _iteração_ for feita um **determinado número de vezes**:
    ```
    # Parar após 20 iterações

    class MyNumbers:
        def __iter__(self):
            self.a = 1
            return self

        def __next__():
            if self.a <= 20:
                x = self.a
                self.a += 1
                return x
            else:
                raise StopIteration
        
    myclass = MyNumbers()
    myiter = iter(myclass)

    for x in myiter:
        print(x)

    """Retorna:
        1
        2
        3
        4
        5
        6
        7
        8
        9
        10
        11
        12
        13
        14
        15
        16
        17
        18
        19
        20
    """
    ```

---