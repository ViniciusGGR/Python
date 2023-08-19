# Comments

### Sumário:

- [Criando um comentário](#criando-um-comentário)
- [Comentários multilinha](#comentários-multilinha)

---

- Os **comentários** podem ser usados para explicar o código Python.
- **Comentários** podem ser usados para tornar o código mais legível.
- Os **comentários** podem ser usados para impedir a execução ao testar o código.

## Criando um comentário

Os **comentários** começam com um (``#``), e o Python irá ignorá-los.

```
# Isso é um comentário

print("Hello, World!")
```

- Os **comentários** podem ser colocados no final de uma linha e o Python ignorará o restante da linha:
    ```
    print("Hello, World!") # Isso é um comentário
    ```

- Um **comentário** não precisa ser um texto que explique o código, ele também pode ser usado para impedir que o Python execute o código:
    ```
    # print("Hello, World!")
    print("Olá, mundo!")
    ```

## Comentários multilinha

Python não tem uma sintaxe para _comentários multilinha_.

- Para adicionar um _comentário multilinha_, é preciso inserir um (``#``) para cada linha:
    ```
    # Isso é um comentário
    # escrito em
    # mais do que apenas uma linha

    print("Hello, World!")
    ```

É possível usar uma **string multilinha** como _comentário multilinha_.

- O Python ignorará **string literais** que não são atribuídas a uma variável, é possível adicionar uma **string** de "várias linhas" (``""" """``) no código e colocar o **comentário** dentro dela:
    ```
    """
    Isso é um comentário
    escrito em
    mais do que apenas uma linha
    """

    print("Hello, World!")
    ```

    > Contanto que a _string_ não seja atribuída a uma variável, o Python lerá o código, mas o ignorará e assim foi feito um _comentário multilinha_.

---