# Data Types

### Sumário:

- [Tipos de dados integrados](#tipos-de-dados-integrados)
- [Obtendo o tipo de dados](#obtendo-o-tipo-de-dados)
- [Definindo o tipo de dados](#definindo-o-tipo-de-dados)
- [Definindo o tipo de dados específico](#definindo-o-tipo-de-dados-específico)

---

## Tipos de dados integrados

**Variáveis** podem _armazenar dados de diferentes tipos_, e diferentes tipos podem fazer coisas diferentes.

- O Python tem os seguintes _tipos de dados integrados_ por padrão:
    - **Tipo de Texto**: ``str``.
    - **Tipos Numéricos**: ``int``, ``float``, ``complex``.
    - **Tipos de Sequência**: ``list``, ``tuple``, ``range``.
    - **Tipo de Mapeamento**: ``dict``.
    - **Tipos de Conjunto**: ``set``, ``frozenset``.
    - **Tipo Booleano**: ``bool``
    - **Tipos Binários**: ``bytes``, ``bytearray``, ``memoryview``.
    - **Nenhum Tipo**: ``NoneType``.

## Obtendo o tipo de dados

- É possível **obter o tipo de dados** de qualquer _objeto_ usando a _função_ ``type()``:
    ```
    # Imprimindo o 'tipo de dados' da variável 'x':

    x = 5
    print(type(x))  # Retorna: <class 'int'>
    ```

## Definindo o tipo de dados

- Em Python, o _tipo de dados_ é **definido** quando um _valor é atribuido a uma variável_:
    ```
    a = "Hello World"                             # Type: str
    b = 20                                        # Type: int
    c = 20.5                                      # Type: float
    d = 1j                                        # Type: complex
    e = ["apple", "banana", "cherry"]             # Type: list
    f = ("apple", "banana", "cherry")             # Type: tuple
    g = range(6)                                  # Type: range
    h = {"name": "John", "age": 36}               # Type: dict
    i = {"apple", "banana", "cherry"}             # Type: set
    j = frozenset({"apple", "banana", "cherry"})  # Type: frozenset
    k = True                                      # Type: bool
    l = b"Hello"                                  # Type: bytes
    m = bytearray(5)                              # Type: bytearray
    n = memoryview(bytes(5))                      # Type: memoryview
    o = None                                      # Type: NoneType
    ```

## Definindo o tipo de dados específico

- Para _especificar o tipo de dados_, é possível usar as seguintes **funções construtoras**:
    ```
    a = str("Hello World")
    b = int(20)
    c = float(20.5)
    d = complex(1j)
    e = list(("apple", "banana", "cherry"))
    f = tuple(("apple", "banana", "cherry"))
    g = range(6)
    h = dict("name": "John", "age": 36)
    i = set(("apple", "banana", "cherry"))
    j = frozenset(("apple", "banana", "cherry"))
    k = bool(5)
    l = bytes(5)
    m = bytearray(5)
    n = memoryview(bytes(5))
    ```

---