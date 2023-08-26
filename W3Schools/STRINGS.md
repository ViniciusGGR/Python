# Strings

### Sumário:

- [Strings](#strings-1)
- [Atribuir String a uma variável](#atribuir-string-a-uma-variável)
- [Strings multilinhas](#strings-multilinhas)
- [Strings são Arrays](#strings-são-arrays)
- [Percorrendo uma String](#percorrendo-uma-string)
- [Comprimento da String](#comprimento-da-string)
- [Verificar String](#verificar-string)
- [Verifique se NÃO](#verifique-se-não)
---
- [Slicing](#slicing)
- [Slice desde o início](#slice-desde-o-início)
- [Slice até o Fim](#slice-até-o-fim)
- [Indexação Negativa](#indexação-negativa)
---
- [Modificar Strings](#modificar-strings)
    - [Maiúsculas - Upper Case](#maiúsculas---upper-case)
    - [Minúsculas - Lower Case](#minúsculas---lower-case)
    - [Remover espaço em branco - Remove Whitespace](#remover-espaço-em-branco---remove-whitespace)
    - [Replace String](#replace-string)
    - [Split String](#split-string)
---
- [Concatenação de Strings](#concatenação-de-strings)
---
- [String Format](#string-format)
---
- [Escape Character](#escape-character)
---
- []()

---

## Strings

- **Strings** em Python são colocadas entre _aspas simples ou duplas_.
    - ``'olá'`` é o mesmo que ``"olá"``.

É possível exibir uma _string literal_ com a **função** ``print()``.

```
print("Hello")  # Retorna: Hello
print('Hello')  # Retorna: Hello
```

## Atribuir String a uma variável

A _atribuição de uma string_ a uma **variável** é feita com o _nome da variável_ seguido por um _sinal de igual_ e a **string**:

```
a = "Hello"
print(a)  # Retorna: Hello
```

## Strings multilinhas

- É possível _atribuir uma string de várias linhas_ a uma **variável** usando _três aspas_:
    - **Três aspas duplas**:
        ```
        a = """Lorem ipsum dolor sit amet,
        consectetur adipiscing elit,
        sed do eiusmod tempor incididunt
        ut labore et dolore magna aliqua."""
        
        print(a)
        ```

    - **Três aspas simples**:
        ```
        a = '''Lorem ipsum dolor sit amet,
        consectetur adipiscing elit,
        sed do eiusmod tempor incididunt
        ut labore et dolore magna aliqua.'''
        
        print(a)
        ```

    > **Observação**: No resultado, as _quebras de linha_ são inseridas na **mesma posição do código**.

## Strings são Arrays

**Strings** em Python são _arrays de bytes_ que representam **caracteres Unicode**.

No entanto, Python _não possui um tipo de dados_ de **caractere** (``char``), um _único caractere_ é simplesmente uma **string** com comprimento 1.

- **Colchetes** podem ser usados para _acessar elementos_ da **string**:
    ```
    # Acessando o 'caractere' na posição 1.

    a = "Hello, World!"
    print(a[1])  # Retorna: e
    ```

    > **Nota**: O _primeiro caractere_ tem a posição ``0``.

## Percorrendo uma String

- Como **strings** são _arrays_, é possível _percorrer os caracteres_ de uma **string**, com um **loop** ``for``:
    ```
    for x in "Hello, World!"
        print(x)

    """
    Retorna:
        H
        e
        l
        l
        o
        ,

        W
        o
        r
        l
        d
        !
    """
    ```

## Comprimento da String

- Obtendo o _comprimento_ de uma **string** com a **função** ``len()``:
    ```
    # A função 'len()' retorna o comprimento de uma string:

    a = "Hello, World!"
    print(len(a))  # Retorna: 13
    ```

## Verificar String

- Verificando se _determinada frase ou caractere_ está presente em uma **string** com o uso da _palavra-chave_ ``in``:
    ```
    # Verificando se "free" está presente na string 'txt'.

    txt = "The best things in life are free!"
    print("free" in txt)  # Retorna: True - (Boolean value)
    ```

    Utilizando o ``in`` em uma _declaração_ ``if``

    ```
    # Imprimindo/exibindo apenas se "free" estiver presente na string 'txt'.

    txt = "The best things in life are free!"

    if "free" in txt:
        print("Yes, 'free' is present.")
    
    # Retorna: Yes, 'free' is present.
    ```

## Verifique se NÃO

- Verificando se uma _determinada frase ou caractere_ **NÃO** está presente em uma **string** com o uso da _palavra-chave_ ``not in``:
    ```
    # Verificando se "expensive" NÃO está presente na string 'txt'.

    txt = "The best things in life are free!"
    print("expensive" not in txt)  # Retorna: True - (Boolean value)
    ```

    Utilizando o ``not in`` em uma _declaração_ ``if``

    ```
    # Imprimindo/exibindo apenas se "expensive" NÃO estiver presente na string 'txt'.

    txt = "The best things in life are free!"

    if "expensive" not in txt:
        print("No, 'expensive' is NOT present.")

    # Retorna: No, 'expensive' is NOT present.
    ```

---

## Slicing

É possível "retornar" um _intervalo de caracteres_ usando a sintaxe **slice**.

- Especifique o _índice inicial_ e o _índice final_, separados por **dois pontos**, para _retornar_ uma **parte da string**.
    ```
    # Obtendo as 'letras' da posição 2 para a posição 5 (não incluído).

    b = "Hello, World!"
    print(b[2:5])

    # Retorna: llo
    ```

    - O _índice final_ não é incluído no "intervalo de caracteres".

    > **Nota**: O _primeiro caractere_ de uma **string** possui índice 0.

## Slice desde o início

Ao **omitir** o _índice inicial_, o **intervalo** começará no _primeiro caractere_:

```
# Obtendo as 'letras' da primeira posição até a posição 5 (não incluído).

b = "Hello, World!"
print(b[:5])

# Retorna: Hello
```

- O _índice final_ **``5``** não é incluído no "intervalo de caracteres".

## Slice até o Fim

Ao **omitir** o _índice final_, o **intervalo** irá até o _final_ (último caractere).

```
Obtendo as 'letras' da 2 posição até a última posição (incluído).

b = "Hello, World!"
print(b[2:])

# Retorna: llo, World!
```

## Indexação Negativa

- Utilizando _índices negativos_ para iniciar o **slice** do _final da string_:
    ```
    # Obtendo as letras:
    # De: "o" em 'World!' (posição -5)
    # Para, mas (não incluído): "d" em 'World!' (posição -2):

    b = "Hello, World!"
    print(b[-5:-2])

    # Retorna: orl
    ```

---

## Modificar Strings

Python possui um _conjunto de métodos integrados_ que podem ser utilizados em **strings**.

### Maiúsculas - Upper Case

- O _método_ ``upper()`` retorna a **string** em _letras maiúsculas_:
    ```
    a = "Hello, World!"
    print(a.upper())  # Retorna: HELLO, WORLD!
    ```

### Minúsculas - Lower Case

- O _método_ ``lower()`` retorna a **string** em _letras minúsculas_:
    ```
    a = "Hello, World!"
    print(a.lower())  # Retorna: hello, world!
    ```

### Remover espaço em branco - Remove Whitespace

É possível _remover_ **espaços em branco antes/depois** de uma **string**.

- O _método_ ``strip()`` _remove qualquer espaço em branco_ do **início/fim** de uma **string**:
    ```
    a = " Hello, World! "
    print(a.strip())  # Retorna: Hello, World!
    ```

### Replace String

- O _método_ ``replace()`` _substitui_ uma **string/caractere** _por outra_ **string/caractere**:
    ```
    a = "Hello, World!"
    print(a.replace("H", "J"))  # Retorna: Jello, World!
    ```

### Split String

O _método_ ``split()`` retorna uma _lista_ onde o texto entre o **separador especificado** se torna os _itens da lista_.

- O _método_ ``split()`` **divide a string** em _substrings_ se encontrar instâncias do **separador**:
    ```
    a = "Hello, World!"
    print(a.split(","))  # Retorna: ['Hello', 'World!']
    ```

---

## Concatenação de Strings

Para _concatenar/combinar_ duas **strings** é possível usar o _operador_ ``+``.

- _Concatenar_ **variável** ``a`` com **variável** ``b`` em **variável** ``c``:
    ```
    a = "Hello"
    b = "World!"

    # Concatenando variáveis
    c = a + b

    print(c)  # Retorna: HelloWorld!
    ```

    Adicionando um _espaço em branco_ entre os valores de cada **variável**.

    ```
    a = "Hello"
    b = "World!"

    # Primeira maneira:
    c = a + " " + b
    print(c)  # Retorna: Hello World!

    # Segunda maneira:
    print("{} {}".format(a, b))  # Retorna: Hello World!
    ```

---

## String Format

> Não é possível combinar **strings** e **números** da seguinte forma:

```
age = 36
txt = "My name is John, I am " + age

print(txt)  # Gera um erro

"""Retorna:
Traceback (most recent call last):
  File "demo_string_format_error.py", line 2, in <module>
    txt = "My name is John, I am " + age
TypeError: must be str, not int
"""
```

- É possível _combinar_ **strings** e **números** usando o _método_ ``format()``.
- O _método_ ``format()`` pega os _argumentos_ passados, **formata** e os coloca na **string** onde ``{}`` estão os _espaços reservados_:
    ```
    # Utilizando o método 'format()' para inserir números em string:
    age = 36
    txt = "My name is John, and I am {}"

    print(txt.format(age))  # Retorna: My name is John, and I am 36
    ```

- O _método_ ``format()`` aceita um _número ilimitado_ de **argumentos** e são colocados nos respectivos _espaços reservados_:
    ```
    quantity = 3
    itemno = 567
    price = 49.95

    myorder = "I want {} pieces of item {} for {} dollars."
    print(myorder.format(quantity, itemno, price))  # Retorna: I want 3 pieces of item 567 for 49.95 dollars.
    ```

- É possível usar **números de índice** ``{0}, {1}, {2}...`` para garantir que os _argumentos_ sejam colocados nos _espaços reservados_ corretos:
    ```
    quantity = 3
    itemno = 567
    price = 49.95

    myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
    print(myorder.format(quantity, itemno, price))  # Retorna: I want to pay 49.95 dollars for 3 pieces of item 567.
    ```

---

## Escape Character

Um **caractere de escape** é uma _barra invertida_ ``\`` seguida pelo caractere que deseja inserir.

- Para inserir um "caractere ilegal" em uma **string**, basta utilizar um **caractere de escape**.
    - Um exemplo de "caractere ilegal" são _aspas duplas_ dentro de uma **string** entre _aspas duplas_:
    
    ```
    # Retornará um 'erro' se usar "aspas duplas" dentro de uma 'string' entre "aspas duplas"

    txt = "We are the so-called "Vikings" from the north."

    """Retorna:
      File "demo_string_escape_error.py", line 1
        txt = "We are the so-called "Vikings" from the north."
                                       ^
    SyntaxError: invalid syntax
    """
    ```

- Para corrigir esse problema, basta usar o **caractere de escape** ``\"``:
    ```
    txt = "We are the so-called \"Vikings\" from the north."  # Retorna: We are the so-called "Vikings" from the north.
    ```

    > **Nota**: O **caractere de escape** ``\"`` permite o uso de _aspas duplas_ quando normalmente não seria permitido.

- Outros **caracteres de escape** usados em Python:
    ```
    \'      # Single Quote
    \\      # Backslash
    \n      # New Line
    \r      # Carriage Return
    \t      # Tab
    \b      # Backspace
    \f      # Form Feed
    \ooo    # Octal value
    \xhh    # Hex value
    ```

---

## 