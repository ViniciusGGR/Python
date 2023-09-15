# Inheritance

### Sumário:

- [Herança Python](#herança-python)
- [Criar uma Class pai](#criar-uma-class-pai)
- [Criar uma Class filha](#criar-uma-class-filha)
- [Adicionar a Função __init__()](#adicionar-a-função-init)
- [Usar a Função super()](#usar-a-função-super)
- [Adicionar Propriedades](#adicionar-propriedades)
- [Adicionar Métodos](#adicionar-métodos)

---

## Herança Python

A _Herança_ permite **definir uma _class_** que "herda" todos os **métodos** e **propriedades** de outra _class_.

- _Class **pai**_ é a _class_ da qual está sendo "herdada", também chamada de _Class **base**_.
- _Class **filha**_ é a _class_ que "herda" de outra _class_, também chamada de _Class **derivada**_.

## Criar uma Class pai

Qualquer _class_ pode ser uma _Class **pai**_, então a **sintaxe** é a mesma da criação de qualquer outra _class_.

```
# Criando uma class chamada 'Person', com propriedades 'firstname' e 'lastname' e um método 'printname'

class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

# Utilizando a class 'Person' para criar um object e então executar o método 'printname'

x = Person("John", "Doe")
x.print(name)  # Retorna: John Doe
```

## Criar uma Class filha

Para criar uma _class_ que "herda" a **funcionalidade** de outra _class_, basta enviar a _Class **pai**_ como **parâmetro** ao criar a _Class **filha**_.

```
# Criando uma class chamada 'Student', que herdará as propriedades e métodos da class 'Person'

class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    pass
```

> **Nota**: Utilizando a **palavra-chave** ``pass`` para não _adicionar outras **propriedades** ou **métodos** à class_.

- Agora a _class_ **Student** possui as mesmas **propriedades** e **métodos** da _class_ **Person**:
    ```
    # Utilizando a class 'Student' para criar um object e depois executar o método 'printname'

    class Person:
        def __init__(self, fname, lname):
            self.firstname = fname
            self.lastname = lname

        def printname(self):
            print(self.firstname, self.lastname)

    class Student(Person):
        pass

    x = Student("Mike", "Olsen")
    x.printname()  # Retorna: Mike Olsen
    ```

## Adicionar a Função __init__()

- Até agora foi criado uma _Class **filha**_ que "herda" as **propriedades** e **métodos** de sua _Class **pai**_.

Adicionando a **função** ``__init__()`` à _Class **filha**_ (em vez da **palavra-chave** ``pass``).

> **Nota**: A **função** ``__init__()`` é chamada automaticamente sempre que a _class_ está sendo usada para criar um **novo _object_**.

```
# Adicionando a função '__init__()' à class 'Student'

class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    def __init__(self, fname, lname):
        # Adicione as propriedades aqui.
```

Quando adicionado a **função** ``__init__()``, a _Class **filha**_ "não herdará" mais a **função** ``__init__()`` da _Class **pai**_.

> **Nota**: A **função** ``__init__()`` da _Class **filha**_ **substitui** a "_herança_" da **função** ``__init__()`` da _Class **pai**_.

- Para "manter a herança" da **função** ``__init__()`` da _Class **pai**_, basta adicionar uma **chamada à função** ``__init__()`` da _Class **pai**_:
    ```
    class Person:
        def __init__(self, fname, lname):
            self.firstname = fname
            self.lastname = lname

        def printname(self):
            print(self.firstname, self.lastname)

    class Student(Person):
        def __init__(self, fname, lname):
            Person.__init__(self, fname, lname)

    x = Student("Mike", "Olsen")
    x.printname()  # Retorna: Mike Olsen
    ```

    Foi adicionado com sucesso a **função** ``__init__()`` e foi mantido a "herança" da _Class **pai**_.

## Usar a Função super()

Python também possui uma **função** ``super()`` que fará com que a _Class **filha**_ "herde" todos os **métodos** e **propriedades** de sua _Class **pai**_.

```
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    def __init__(self, fname, lname):
        super().__init__(fname, lname)

x = Student("Mike", "Olsen")
x.printname()  # Retorna: Mike Olsen
```

- Ao usar a **função** ``super()``, não é preciso usar o _nome do elemento_ "**pai**", ela "herdará" automaticamente os **métodos** e **propriedades** de seu "**pai**".

## Adicionar Propriedades

```
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

# Adicionando uma propriedade chamada 'graduationyear' à class 'Student'

class Student(Person):
    def __init__(self, fname, lname):
        super().__init__(fname, lname)
        self.graduationyear = 2019

x = Student("Mike", "Olsen")
print(x.printname() + x.graduationyear)

"""Retorna:
    Mike Olsen
    None 2019
"""
```

- No exemplo abaixo, o _year_ ``2019`` deve ser uma **variável** e passado para a _class_ ``Student`` na _criação dos objects_ **student**. Para fazer isso, basta adicionar outro **parâmetro na função** ``__init__()``:
    ```
    class Person:
        def __init__(self, fname, lname):
            self.firstname = fname
            self.lastname = lname

        def printname(self):
            print(self.firstname, self.lastname)

    # Adicionando uma propriedade chamada 'graduationyear' à class 'Student'

    class Student(Person):
        def __init__(self, fname, lname, year):
            super().__init__(fname, lname)
            self.graduationyear = year

    x = Student("Mike", "Olsen", 2019)
    print(x.printname() + x.graduationyear)

    """Retorna:
        Mike Olsen
        None 2019
    """
    ```

## Adicionar Métodos

```
# Adicionando um método chamado 'welcome' à class 'Student'

class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    def __init__(self, fname, lname, year):
        super().__init__(fname, lname)
        self.graduationyear = year

    def welcome(self):
        print("Welcome {} {} to the class of {}".format(self.firstname, self.lastname, self.graduationyear))

x = Student("Mike", "Olsen", 2019)
x.welcome()  # Retorna: Welcome Mike Olsen to the class of 2019
```

- Se for adicionado um **método** na _Class **filha**_ com o **mesmo nome de uma função** na _Class **pai**_, a "herança" do **método pai** será _substituida_.

---