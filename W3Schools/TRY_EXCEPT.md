# Try...Except

### Sumário:

- [Manipulação de Exception](#manipulação-de-exception)
- [Muitas Exceptions](#muitas-exceptions)
- [Else](#else)
- [Finally](#finally)
- [Raise an Exception](#raise-an-exception)

---

- O _bloco_ ``try`` permite **testar um _bloco de código_ em busca de _erros_**.
- O _bloco_ ``except`` permite **lidar com _erro_**.
- O _bloco_ ``else`` permite **executar código quando _não há erro_**.
- O _bloco_ ``finally`` permite **executar código**, independentemente do _resultado dos blocos_ ``try`` e ``except``.

## Manipulação de Exception

Quando ocorre um _erro_, ou _exceção_, o Python normalmente irá **parar e gerar uma _mensagem de erro_**.

- Essas _exceções_ podem ser "**tratadas**" usando a _instrução_ ``try``:
    ```
    # O bloco 'try' irá gerar uma 'exceção', pois 'x' não está definido

    try:
        print(x)
    except:
        print("An exception occurred.")

    # Retorna: An exception occurred.
    ```

    - Como o _bloco_ ``try`` **gera um erro**, o _bloco_ ``except`` será **executado**.
    
    Sem o _bloco_ ``try``, o programa irá **travar e gerar um erro**:
    
    ```
    # Gerando um erro, pois 'x' não está definido

    print(x)  # Retorna: NameError: name 'x' is not defined
    ```

## Muitas Exceptions

- É possível definir _quantos blocos_ ``except`` desejar, por exemplo, se quiser **executar um _bloco de código especial_ para um _tipo especial de erro_**:
    ```
    # Imprimindo uma mensagem se o bloco 'try' gerar um 'NameError' e outra para outros 'erros'

    try:
        print(x)
    except NameError:
        print("Variable 'x' is not defined.")
    except:
        print("Something else went wrong.")

    # Retorna: Variable 'x' is not defined.
    ```

## Else

- É possível usar a **palavra-chave** ``else`` para _definir um bloco de código_ a ser **executado** se nenhum _erro_ for gerado:
    ```
    # O bloco 'try' não gera nenhum erro

    try:
        print("Hello!")
    except:
        print("Something went wrong.")
    else:
        print("Nothing went wrong.")

    """Retorna:
        Hello!
        Nothing went wrong.
    """
    ```

## Finally

O _bloco_ ``finally``, se especificado, será **executado** independentemente de o _bloco_ ``try`` **gerar um erro _ou não_**.

```
try:
    print(x)
except:
    print("Something went wrong.")
finally:
    print("The 'try except' is finished.")

"""Retorna:
    Something went wrong.
    The 'try except' is finished.
```

- Isto pode ser "_útil_" para **fechar _objects_ e limpar recursos**:
    ```
    # Tentando abrir e grevar em um arquivo que não seja gravável

    try:
        f = open("demofile.txt")
        try:
            f.write("Lorem Ipsum")
        except:
            print("Something went wrong when writing to the file.")
        finally:
            f.close()
    except:
        print("Something went wrong when opening the file.")

    # Retorna: Something went wrong when opening the file.
    ```

    O programa pode _continuar_ sem deixar o _**arquivo** object_ aberto. 

## Raise an Exception

É possível "optar" por _lançar_ um **Exception** se ocorrer uma **condição**.

- Para _lançar/levantar_ uma **Exception**, basta utilizar a **palavra-chave** ``raise``:
    ```
    # Gerando um 'erro' e parando o programa se 'x' for menor que '0'

    x = -1

    if x < 0:
        raise Exception("Sorry, no numbers below zero")

    # Retorna: Exception: Sorry, no numbers below zero
    ```

- A **palavra-chave** ``raise`` é usada para _gerar_ uma **Exception**.
- É possível definir que o _tipo de erro gerar_ e o _texto_ a ser "impresso" para o usuário:
    ```
    # Gerando um 'TypeError' se 'x' não for um número inteiro

    x = "hello"

    if not type(x) is int:
        raise TypeError("Only integers are allowed.")

    # Retorna: TypeError: Only integers are allowed
    ```

---