# Operators

### Sumário

- [Operadores Python](#operadores-python)
- [Operadores Aritméticos Python](#operadores-aritméticos-python)
- [Operadores de Atribuição Python](#operadores-de-atribuição-python)
- [Operadores de Comparação Python](#operadores-de-comparação-python)
- [Operadores Lógicos Python](#operadores-lógicos-python)
- [Operadores de Identidade Python](#operadores-de-identidade-python)
- [Operadores de Associação Python](#operadores-de-associação-python)
- [Operadores bit a bit Python](#operadores-bit-a-bit-python)
- [Precedência do Operador](#precedência-do-operador)

---

## Operadores Python

_Operadores_ são usados para **realizar operações** em _variáveis_ e _valores_.

- No exemplo abaixo, foi utilizado o _operador_ ``+`` para **somar dois valores**:
    ```
    print(10 + 5)  # Retorna: 15
    ```

- Python divide os _operadores_ nos seguintes grupos:
    - Operadores **Aritméticos**.
    - Operadores de **Atribuição**.
    - Operadores de **Comparação**.
    - Operadores **Lógicos**.
    - Operadores de **Identidade**.
    - Operadores de **Associação**.
    - Operadores **bit a bit**.

## Operadores Aritméticos Python

_Operadores Aritméticos_ são usados com **valores numéricos** para realizar _operações matemáticas comuns_:

| Operador | Name             | Exemplo |
| -------- | ---------------- | ------- |
| ``+``    | Adição           | x + y   |
| ``-``    | Subtração        | x - y   |
| ``*``    | Multiplicação    | x * y   |
| ``/``    | Divisão          | x / y   |
| ``%``    | Módulo           | x % y   |
| ``**``   | Exponenciação    | x ** y  |
| ``//``   | Resto da divisão | x // y  |

## Operadores de Atribuição Python

_Operadores de Atribuição_ são usados para **atribuir valores** a _variáveis_:

| Operador | Exemplo | Igual a    |
| -------- | ------- | ---------- |
| ``=``    | x = 5   | x = 5      |
| ``+=``   | x += 3  | x = x + 3  |
| ``-=``   | x -= 3  | x = x - 3  |
| ``*=``   | x *= 3  | x = x * 3  |
| ``/=``   | x /= 3  | x = x / 3  |
| ``%=``   | x %= 3  | x = x % 3  |
| ``//=``  | x //= 3 | x = x // 3 |
| ``**=``  | x **= 3 | x = x ** 3 |
| ``&=``   | x &= 3  | x = x & 3  |
| ``I=``   | x I= 3  | x = x I 3  |
| ``^=``   | x ^= 3  | x = x ^ 3  |
| ``>>=``  | x >>= 3 | x = x >> 3 |
| ``<<=``  | x <<= 3 | x = x << 3 |

## Operadores de Comparação Python

_Operadores de Comparação_ são usados para **comparar dois valores**:

| Operador | Nome                 | Exemplo |
| -------- | -------------------- | ------- |
| ``==``   | Igual                | x == y  |
| ``!=``   | Não Igual            | x != y  |
| ``>``    | Maior que            | x > y   |
| ``<``    | Menor que            | x < y   |
| ``>=``   | Maior que ou igual a | x >= y  |
| ``<=``   | Menor que ou igual a | x <= y  |

## Operadores Lógicos Python

_Operadores Lógicos_ são usados para **combinar instruções condicionais**:

| Operador | Descrição                                 | Exemplo               |
| -------- | ----------------------------------------- | --------------------- |
| ``and``  | True - se ambas as declarações são 'true' | x < 5 and x < 10      |
| ``or``   | True - se uma das declarações for 'true'  | x < 5 or x < 4        |
| ``not``  | Inverte o resultado                       | not(x < 5 and x < 10) |

## Operadores de Identidade Python

Os _Operadores de Identidade_ são usados para **comparar os objetos**, não se forem iguais, mas se forem realmente o _mesmo objeto_, com a mesma localização de memória.

| Operador   | Descrição                                        | Exemplo    |
| ---------- | ------------------------------------------------ | ---------- |
| ``is``     | True - se ambas variáveis são o mesmo objeto     | x is y     |
| ``is not`` | True - se ambas variáveis não são o mesmo objeto | x is not y |

## Operadores de Associação Python

_Operadores de Associação_ são usados para _testar_ se uma **sequência** é apresentada em um objeto.

| Operador   | Exemplo    |
| ---------- | ---------- |
| ``in``     | x in y     |
| ``not in`` | x not in y |

## Operadores bit a bit Python

_Operadores bit a bit_ são usados para **comparar números** (_binários_).

| Operador | Nome                 | Exemplo |
| -------- | -------------------- | ------- |
| ``&``    | AND                  | x & y   |
| ``I``    | OR                   | x I y   |
| ``^``    | XOR                  | x ^ y   |
| ``~``    | NOT                  | ~x      |
| ``<<``   | Zero fill left shift | x << 2  |
| ``>>``   | Signed right shift   | x >> 2  |

## Precedência do Operador

A _Precedência do Operador_ descreve a _ordem_ em que as **operações** são _executadas_.

- Os _parênteses_ ``()`` tem a **precedência mais alta**, o que significa que as _expressões entre parênteses_ devem ser avaliadas primeiro.
    ```
    print((6 + 3) - (6 + 3))  # Retorna: 0
    ```

- A _multiplicação_ ``*`` tem **maior precedência** que a _adição_ ``+`` e, portanto, as _multiplicações_ são avaliadas antes das _adições_:
    ```
    print(100 + 5 * 3)  # Retorna: 115
    ```

Tabela descritiva da _Ordem de Precedência_, começando com a _precedência mais alta_:

| Operador                                                                    |
| --------------------------------------------------------------------------- |
| ``()``                                                                      |
| ``**``                                                                      |
| ``+x`` ``-x`` ``~x``                                                        |
| ``*`` ``/`` ``//`` ``%``                                                    |
| ``+`` ``-``                                                                 |
| ``<<`` ``>>``                                                               |
| ``&``                                                                       |
| ``^``                                                                       |
| ``I``                                                                       |
| ``==`` ``!=`` ``>`` ``>=`` ``<`` ``<=`` ``is`` ``is not`` ``in`` ``not in`` |
| ``not``                                                                     |
| ``and``                                                                     |
| ``or``                                                                      |

- Se _dois operadores_ tiverem a **mesma precedência**, a expressão será _avaliada da esquerda para a direita_.
- _Adição_ ``+`` e _Subtração_ ``-`` tem a **mesma precedência** e, portanto, a expressão é avaliada da esquerda para a direita:
    ```
    print(5 + 4 - 7 + 3)  # Retorna: 5
    ```

---