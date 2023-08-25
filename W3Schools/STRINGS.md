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

