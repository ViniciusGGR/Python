# Polymorphism

### Sumário:

- [Polimorfismo de Função](#polimorfismo-de-função)
    - [String](#string)
    - [Tuple](#tuple)
    - [Dictionary](#dictionary)
- [Polimorfismo de Classe](#polimorfismo-de-classe)
- [Polimorfismo de Classe de Herança](#polimorfismo-de-classe-de-herança)

---

A palavra ``Polimorfismo`` significa "_muitas formas_" e em programação refere-se a **métodos**, **funções** e **operadores** com o mesmo nome que podem ser _executados em muitos objetos_ ou _classes_.

## Polimorfismo de Função

- Um exemplo de **função** Python que pode ser usada em _diferentes objetos_ é a **função** ``len()``.

### String

Para _Strings_ a **função** ``len()`` retorna o _número de caracteres_.

```
x = "Hello World!"

print(len(x))  # Retorna: 12
```

### Tuple

Para _Tuples_ a **função** ``len()`` retorna o _número de itens_ na _Tuple_.

```
mytuple = ("apple", "banana", "cherry")

print(len(mytuple))  # Retorna: 3
```

### Dictionary

Para _Dictionaries_ a **função** ``len()`` retorna o _número de pares **chave/valor**_ no _Dictionary_.

```
thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

print(len(thisdict))  # Retorna: 3
```

## Polimorfismo de Classe

O ``Polimorfismo`` é frequentemente usado em **métodos de classe**, onde é possível ter _várias **classes**_ com o mesmo _nome de **método**_.

- Por exemplo, caso tenha _três **classes**_: ``Car``, ``Boat`` e ``Plane``, e todas elas têm um **método** chamado ``move()``:
    ```
    # Classes diferentes com o mesmo método

    class Car:
        def __init__(self, brand, model):
            self.brand = brand
            self.model = model

        def move(self):
            print("Drive!")

    class Boat:
        def __init__(self, brand, model):
            self.brand = brand
            self.model = model

        def move(self):
            print("Sail!")

    class Plane:
        def __init__(self, brand, model):
            self.brand = brand
            self.model = model

        def move(self):
            print("Fly!")

    car1 = Car("Ford", "Mustang")        # Criando a 'class' Car
    boat1 = Boat("Ibiza", "Touring 20")  # Criando a 'class' Boat
    plane1 = Plane("Boeing", "747")      # Criando a 'class' Plane

    for x in (car1, boat1, plane1):
        x.move()

        """Retorna:
            Drive!
            Sail!
            Fly!
        """
    ```

    > **Nota**: O _loop_ ``for`` no final executa o **mesmo método** para todas as _três **classes**_ devido ao ``Polimorfismo``.

## Polimorfismo de Classe de Herança

- Criando uma _class **pai**_ chamada ``Vehicle`` e tornando as **classes** ``Car``, ``Boat`` e ``Plane`` _classes **filhas**_ de ``Vehicle``, as _classes **filhas**_ "**herdarão**" os **métodos** ``Vehicle``, mas poderão _substituí-los_:
    ```
    class Vehicle:
        def __init__(self, brand, model):
            self.brand = brand
            self.model = model

        def move(self):
            print("Move!")

    class Car(Vehicle):
        pass

    class Boat(Vehicle):
        def move(self):
            print("Sail!")

    class Plane(Vehicle):
        def move(self):
            print("Fly!")
    
    car1 = Car("Ford", "Mustang")        # Criando a 'object' Car
    boat1 = Boat("Ibiza", "Touring 20")  # Criando a 'object' Boat
    plane1 = Plane("Boeing", "747")      # Criando a 'object' Plane

    for x in (car1, boat1, plane1):
        print(x.brand)
        print(x.model)
        x.move()
        print("\n")
    
    """Retorna:
        Ford
        Mustang
        Move!

        Ibiza
        Touring 20
        Sail!

        Boeing
        747
        Fly!
    """
    ```

    - As _classes **filhas**_ "**herdam**" as **propriedades** e **métodos** da _classe **pai**_.
    - No exemplo acima a _classe_ ``Car`` está "vazia", mas "**herda**" ``brand``, ``model`` e ``move()`` de ``Vehicle``.
    - As _classes_ ``Boat`` e ``Plane`` também "**herdam**" ``brand``, ``model`` e ``move()`` de ``Vehicle``, mas ambas _substituem_ o **método** ``move()``.
    - Devido ao ``Polimorfismo`` é possível _executar o mesmo **método**_ para todas as _classes_.

---