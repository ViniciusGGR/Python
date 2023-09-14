# Classes/Objects

### Sumário:

- [Classes/Objects Python](#classesobjects-python)
- [Criando uma Class](#criando-uma-class)
- [Criando um Object](#criando-um-object)
- [A Função __init__()](#a-função-init)
- [A Função __str__()](#a-função-str)
- [Métodos de Object](#métodos-de-object)
- [O Parâmetro self](#o-parâmetro-self)
- [Modificar Propriedades do Object](#modificar-propriedades-do-object)
- [Excluir Propriedades do Object](#excluir-propriedades-do-object)
- [Excluir Objects](#excluir-objects)
- [A Declaração pass](#a-declaração-pass)

---

## Classes/Objects Python

Python é uma _linguagem de programação_ **orientada a objetos**.

Quase tudo em Python é um _Object_, com suas **propriedades** e **métodos**.

Uma _class_ é como um **construtor de _Objects_** ou um "modelo" para criar _Objects_.

## Criando uma Class

Para criar uma _class_, basta utilizar a **palavra-chave** ``class``.

```
# Criando uma 'class' chamada 'MyClass', com uma propriedade chamada 'x'

class MyClass:
    x = 5
```

## Criando um Object

Utilizando a _class_ chamada **MyClass** para criar _Objects_.

```
# Criando um 'object' chamado 'p1' e imprimindo o valor de 'x'

class MyClass:
    x = 5

p1 = MyClass()
print(p1.x)  # Retorna: 5
```

## A Função __init__()

> **Nota**: Os exemplos acima são _classes_ e _objects_ em sua **forma mais simples** e não são realmente úteis em aplicações da vida real.

- Para entender o significado das _classes_, é preciso entender a **função integrada** ``__init__().
- Todas as _classes_ possuem uma **função** chamada ``__init__()``, que é sempre **executada** quando a _class_ está sendo **iniciada**.
- A **função** ``__init__()`` é utilizada para _atribuir valores_ as **propriedades** do _object_ ou outras _operações_ que sejam necessárias quando o _object_ estiver sendo **criado**.

```
# Criando uma class chamada 'Person', utilizando a função '__init__()' para atribuir valores para 'name' e 'age'

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p1 = Person("John", 36)

print(p1.name)  # Retorna: John
print(p1.age)   # Retorna: 36
```

> **Nota**: A **função** ``__init__()`` é chamada automaticamente sempre que a _class_ está sendo usada para _criar um **novo objeto**_.

## A Função __str__()

A **função** ``__str__()`` _controla_ o que deve ser retornado quando o _object_ da _class_ é representado como uma **string**.

Se a **função** ``__str__()`` não estiver _definida_, a representação em **string** do _object_ será retornada.

```
# A representação de 'string' de um object SEM a função '__str__()'

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p1 = Person("John", 36)

print(p1)  # Retorna: <__main__.Person object at 0x15039e602100>
```

```
# A representação de 'string' de um object COM a função '__str__()'

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name} ({self.age})"

p1 = Person("John", 36)

print(p1)  # Retorna: John (36)
```

## Métodos de Object

_Objects_ também podem conter **métodos**. **Métodos** em _objects_ são **funções** que pertencem ao _object_.

- Criando um **método** na _class_ **Person**:
    ```
    # Inserindo uma função que imprima uma saudação e execute-a no object 'p1'

    class Person:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def myfunc(self):
            print("Hello my name is {}".format(self.name))

    p1 = Person("John", 36)
    p1.myfunc()  # Retorna: Hello my name is John
    ```

## O Parâmetro self

O **parâmetro** ``self`` é uma _referência à instância atual_ da _class_ e é usado para **acessar variáveis** que pertencem à _class_.

- O **parâmetro** _não precisa_ ter o nome ``self``, pode ser **qualquer nome**, mas tem que ser o _primeiro **parâmetro**_ de qualquer **função** da _class_.
    ```
    # Utilizando as palavras 'mysillyobject' e 'abc' em vez de 'self'

    class Person:
        def __init__(mysillyobject, name, age):
            mysillyobject.name = name
            mysillyobject.age = age
        
        def myfunc(abc):
            print("Hello my name is {}".format(abc.name))

    p1 = Person("John", 36)
    p1.myfunc()  # Retorna: Hello my name is John
    ```

## Modificar Propriedades do Object

- É possível **modificar propriedades** em _objects_:
    ```
    # Definindo 'age' de 'p1' para 40

    class Person:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def myfunc(self):
            print("Hello my name is {}".format(self.name))

    p1 = Person("John", 36)

    p1.age = 40
    print(p1.age)  # Retorna: 40
    ```

## Excluir Propriedades do Object

- É possível **excluir propriedades** de _objects_ usando a **palavra-chave** ``del``:
    ```
    # Excluindo a propriedade 'age' do object 'p1'

    class Person:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def myfunc(self):
            print("Hello my name is {}".format(self.name))

    p1 = Person("John", 36)

    del p1.age
    print(p1.age)  # Retorna: AttributeError: 'Person' object has no attribute 'age'
    ```

## Excluir Objects

- É possível **excluir _objects_** usando a **palavra-chave** ``del``:
    ```
    # Excluindo o object 'p1'

    class Person:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def myfunc(self):
            print("Hello my name is {}".format(self.name))

    p1 = Person("John", 36)

    del p1
    print(p1)  # Retorna: NameError: 'p1' is not defined
    ```

## A Declaração pass

As **definições** _class_ não podem ficar vazias, mas se por algum motivo existir uma **definição** _class_ sem conteúdo, basta colocar uma **instrução** ``pass`` para evitar erro.

```
class Person:
    pass

# Ter uma definição de classe vazia como esta geraria um erro sem a instrução pass
```

---