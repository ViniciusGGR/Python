# Syntax

### Sumário:

- [Executar a sintaxe do Python](#executar-a-sintaxe-do-python)
- [Indentação do Python](#indentação-do-python)
- [Variáveis Python](#variáveis-python)
- [Comentários](#comentários)

---

## Executar a sintaxe do Python

A sintaxe do Python pode ser executada escrevendo diretamente na _linha de comando_.

```
>>> print("Hello, World!")
Hello, World!
```

Ou criando um arquivo Python, usando a _extensão_ de arquivo (``.py``) e **executando-o** na _linha de comando_.

```
>>> python myfile.py
```

## Indentação do Python

**Indentação** refere-se aos _espaços_ no **início de uma linha de código**.

- Onde em outras _linguagens de programação_ o **recuo** no código é apenas para facilitar a leitura, o **recuo** no Python é muito importante.

Python usa indentação para indicar um bloco de código.

```
if 5 > 2:
    print("Five is greater than two!")
```

- O Python fornecerá um erro se pular o **recuo**:
    ```
    # Erro de sintaxe:

    if 5 > 2:
    print("Five is greater than two!")
    ```

    > O _número de espaços_ fica a seu critério como programador, o uso mais comum é **quatro**, mas tem que ser pelo menos um.

    ```
    if 5 > 2:
     print("Five is greater than two!")
    if 5 > 2:
            print("Five is greather than two!")
    ```

- Deve-se usar o mesmo número de espaços no mesmo bloco de código, caso contrário, o Python fornecerá um erro:
    ```
    # Erro de sintaxe:

    if 5 > 2:
     print("Five is greater than two!")
            print("Five is greater than two!")
    ```

## Variáveis Python

Em Python, as _variáveis_ são criadas quando se atribui um valor a elas.

```
x = 5
y = "Hello, World!"
```

- Python não tem comando para declarar uma _variável_.

## Comentários

O Python tem capacidade de **comentários** para fins de documentação no código.

- Os **comentários** começam com um (``#``) e o Python renderizará o restante da linha como um **comentário**.
    ```
    # Isso é um comentário.
    
    print("Hello, World!")
    ```

---