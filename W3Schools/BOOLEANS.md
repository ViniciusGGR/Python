# Booleans

### Sumário

- [Valores Booleanos](#valores-booleanos)
- [Avalie Valores e Variáveis](#avalie-valores-e-variáveis)
- [A maioria dos Valores são Verdadeiros](#a-maioria-dos-valores-são-verdadeiros)
- [Alguns Valores são Falsos](#alguns-valores-são-falsos)
- [Funções podem retornar um Booleano](#funções-podem-retornar-um-booleano)

---

**Booleanos** representam um de _dois valores_: ``True`` ou ``False``.

## Valores Booleanos

Na programação, as vezes é preciso saber se uma _expressão_ é ``True`` ou ``False``.

- É possível _avaliar_ qualquer **expressão** em Python e obter uma de duas respostas, ``True`` ou ``False``.
- Quando _comparado dois valores_, a **expressão** é avaliada e o Python retorna a resposta _booleana_:
    ```
    print(10 > 9)   # Retorna: True
    print(10 == 9)  # Retorna: False
    print(10 < 9)   # Retorna: False
    ```

- Quando _executada_ uma **condição** em uma _instrução_ ``if``, Python retorna ``True`` ou ``False``:
    ```
    # Imprimindo uma mensagem com base se a 'condição' é "True" ou "False"

    a = 200
    b = 33

    if b > a:
        print("'b' is grater than 'a'")
    else:
        print("'b' is not greater than 'a'")

    # Retorna: 'b' is not greater than 'a'
    ```

## Avalie Valores e Variáveis

A _função_ ``bool()`` permite avaliar qualquer valor e fornecer ``True`` ou ``False``.

```
# Avaliando uma 'string' e um 'int'

print(bool("Hello"))  # Retorna: True
print(bool(15))       # Retorna: True
```

```
# Avaliando duas 'variáveis'

x = "Hello"
y = 15

print(bool(x))  # Retorna: True
print(bool(y))  # Retorna: True
```

## A maioria dos Valores são Verdadeiros

- Quase qualquer _valor_ é avaliado ``True`` se tiver algum tipo de _conteúdo_.
- Qualquer **string** é ``True``, exceto **strings vazias**.
- Qualquer **int** é ``True``, exceto **0**.
- Qualquer **list**, **tuple**, **set** e **dictionarie** são ``True``, exceto os _vazios_.

```
bool("abc")                          # Retorna: True
bool(123)                            # Retorna: True
bool(["apple", "cherry", "banana"])  # Retorna: True
```

## Alguns Valores são Falsos

Não há muitos _valores_ avaliados como ``False``, exceto **valores vazios**, como ``()``, ``[]``, ``{}``, ``""``, o número ``0`` e o valor ``None``. E é claro que o valor ``False`` é _avaliado_ como ``False``.

```
bool(False)  # Retorna: False
bool(None)   # Retorna: False
bool(0)      # Retorna: False
bool("")     # Retorna: False
bool(())     # Retorna: False
bool([])     # Retorna: False
bool({})     # Retorna: False
```

- Mais um _valor_, ou _objeto_ neste caso, é avaliado como ``False``, e isso se tiver um _objeto_ feito de uma **classe** com uma **função** ``__len__`` que retorna ``0`` ou ``False``:
    ```
    class myclass():
        def __len__(self):
            return 0

    myobj = myclass()
    print(bool(myobj))  # Retorna: False
    ```

## Funções podem retornar um Booleano

- É possível criar **funções** que retornem um _valor_ **booleano**:
    ```
    def myFunction():
        return True

    print(myFunction())  # Retorna: True
    ```

    É possível _executar o código_ com base na **resposta booleana** de uma **função**.

    ```
    # Imprima "YES!" se a função retornar 'True', caso contrário imprima "NO!"

    def myFunction():
        return True

    if myFunction():
        print("YES!")
    else:
        print("NO!")

    # Retorna: YES!
    ```

Python também possui muitas _funções integradas_ que retornam um **valor booleano**, como a **função** ``isinstance()``, que pode ser usada para determinar se um _objeto_ é de determinado _tipo de dados_.

```
# Verificando se um objeto é um número inteiro ou não

x = 200
print(isinstance(x, int))    # Retorna: True
print(isinstance(x, float))  # Retorna: False
```

---