# Variables

### Sumário

- [Criando Variáveis](#criando-variáveis)
- [Casting](#casting)
- [Obter o tipo](#obter-o-tipo)
- [Aspas Simples ou Duplas?](#aspas-simples-ou-duplas)
- [Maiúsculas e minúsculas](#maiúsculas-e-minúsculas)

---

Variáveis são "recipientes" para **armazenar valores de dados**.

## Criando Variáveis

- Python não tem "comando" para _declarar uma variável_.
- Uma **variável** é criada no momento em que se _atribui um valor_ a ela.

```
x = 5
y = "John"

print(x)
print(y)
```

As **variáveis** não precisam ser _declaradas_ com nenhum _tipo_ específico e podem até mudar de tipo depois de terem sido definidas.

```
x = 4        # 'x' é do tipo 'int'.
x = "Sally"  # 'x' é agora do tipo 'str'.

print(x)
```

## Casting

- Se deseja _especificar o tipo de dados_ de uma **variável**, isso pode ser feito com a _conversão_ (Casting):
    ```
    x = str(3)    # 'x' vai ser '3'.
    y = int(3)    # 'y' vai ser 3.
    z = float(3)  # 'z' vai ser 3.0.
    ```

## Obter o tipo

- É possível obter o _tipo de dados_ de uma **variável** com a _função_ ``type()``:
    ```
    x = 5
    y = "John"

    print(type(x))  # Retorna: <class 'int'>
    print(type(y))  # Retorna: <class 'str'>
    ```

## Aspas Simples ou Duplas?

- As **variáveis** do _tipo_ ``string`` podem ser declaradas usando aspas simples ou duplas:
    ```
    # Funcionam da mesma forma:
    x = "John"
    x = 'John'
    ```

## Maiúsculas e minúsculas

- Os nomes das **variáveis** _diferenciam_ maiúsculas de minúsculas.
    ```
    # 'A' não vai sobrescrever 'a'
    a = 4
    A = "Sally"

    print(a)  # Retorna: 4
    print(A)  # Retorna: Sally
    ```

---

