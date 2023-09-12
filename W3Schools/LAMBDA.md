# Lambda

### Sumário:

- [Sintaxe](#sintaxe)
- [Por que usar funções Lambda](#por-que-usar-funções-lambda)

---

Uma **função _Lambda_** é uma pequena **função _anônima_**.

Uma **função _Lambda_** pode receber qualquer número de _argumentos_, mas só pode ter **uma expressão**.

## Sintaxe

```
lambda arguments : expression
```

A **expressão** é executada e o _resultado_ é retornado.

```
# Adicionando 10 ao argument 'a' e retornando o resultado

x = lambda a : a + 10
print(x(5))  # Retorna: 15
```

As **funções _Lambda_** podem receber qualquer número de _argumentos_.

```
# Multiplicando argumento 'a' por argumento 'b' e retornando o resultado

x = lambda a, b : a * b
print(x(5, 6))  # Retorna: 30
```

```
# Somando os argumentos 'a', 'b' e 'c' e retornando o resultado

x = lambda a, b, c : a + b + c
print(x(5, 6, 2))  # Retorna: 13
```

## Por que usar funções Lambda

O poder do _Lambda_ é melhor demonstrado quando utilizado como uma **função _anônima_** dentro de outra **função**.

- Por exemplo, uma _definição_ de **função** que receba um _argumento_ e esse _argumento_ será **multiplicado por um _número desconhecido_**:
    ```
    def myfunc(n):
        return lambda a : a * n
    ```

    Utilizando essa _definição_ de **função** para "criar" uma **função** que sempre _dobre o **número** enviado_:

    ```
    def myfunc(n):
        return lambda a : a * n

    mydoubler = myfunc(2)

    print(mydoubler(11))  # Retorna: 22
    ```

    - Utilizando a mesma _definição_ de **função** para "criar" uma **função** que sempre _triplique o **número** enviado_:
        ```
        def myfunc(n):
            return lambda a : a * n

        mytripler = myfunc(3)

        print(mytripler(11))  # Retorna: 33
        ```

    Utilizando a mesma _definição_ de **função** para "criar" _ambas as **funções**_, no mesmo programa:

    ```
    def myfunc(n):
        return lambda a : a * n

    mydoubler = myfunc(2)
    mytripler = myfunc(3)

    print(mydoubler(11))  # Retorna: 22
    print(mytripler(11))  # Retorna: 33
    ```

> **Dica**: Utilize **funções** _Lambda_ quando uma **função anônima** for necessária por um curto período de tempo.

---