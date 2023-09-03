# Sets

### Sumário:

- [Set](#set)
- [Set itens](#set-itens)
- [Não ordenado](#não-ordenado)
- [Imutável](#imutável)
- [Duplicatas não permitidas](#duplicatas-não-permitidas)
- [Obtendo o comprimento de um Set](#obtendo-o-comprimento-de-um-set)
- [Set itens - Tipos de Dados](#set-itens---tipos-de-dados)
- [type()](#type)
- [O construtor set()](#o-construtor-set)
- [Coleções Python (Arrays)](#coleções-python-arrays)
---
- [Acessar itens](#acessar-itens)
- [Alterar itens](#alterar-itens)
---
- [Adicionar itens](#adicionar-itens)
- [Adicionar Sets](#adicionar-sets)
- [Adicione qualquer iterável](#adicione-qualquer-iterável)
---
- [Remover item](#remover-item)
---
- [Loop Items](#loop-items)
---
- [Juntando dois Sets](#juntando-dois-sets)
- [Mantenha SOMENTE as duplicatas](#mantenha-somente-as-duplicatas)
- [Mantenha tudo, mas NÃO as duplicatas](#mantenha-tudo-mas-não-as-duplicatas)
---
- [Métodos Set](#métodos-set)

---

```
myset = {"apple", "banana", "cherry"}
```

## Set

**Sets** são usados para _armazenar vários itens_ em uma **única variável**.

**Set** é um dos 4 _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**, os outros 3 são **``Tuple``**, **``List``** e **``Dictionary``**.

Um **Set** é uma coleção _não ordenada_, _imutável_ e _não indexada_.

> **Observação**: Os _itens_ do **Set** **não podem ser alterados**, mas é possível _remover itens_ e _adicionar novos itens_.

- Os **Sets** são escritos entre _colchetes_ (``{}``):
    ```
    # Criando um Set
    
    thisset = {"apple", "banana", "cherry"}
    print(thisset)  # Retorna: {'cherry', 'apple', 'banana'}
    ```

    > **Nota**: Os **Sets** _não são ordenados_, portanto os **itens podem ser apresentados em ordem diferente**.

## Set itens

Os _itens_ do **Set** são _desordenados_, _imutáveis_ e **não permitem** _valores duplicados_.

## Não ordenado

**Não ordenado** significa que os _itens_ de um **Set** _não possuem uma ordem definida_.

- Os _itens_ do **Set** podem aparecer em uma _ordem diferente_ sempre que forem utilizados e _não podem_ ser **referenciados por _índice_ ou _chave_**.

## Imutável

Os _itens_ do **Set** _não podem ser alterados_, o que significa que não podem ser alterados após a **criação do Set**.

> Depois que um **Set** é criado, **não é possível** _alterar seus itens_, mas é possível **remover itens e adicionar novos itens**.

## Duplicatas não permitidas

Os **Sets** não podem ter _dois itens_ com o mesmo valor.

```
# Valores duplicados serão ignorados

thisset = {"apple", "banana", "cherry", "apple"}
print(thisset)  # Retorna: {'banana', 'cherry', 'apple'}
```

> **Nota**: Os _valores_ ``True`` e ``1`` são considerados o _mesmo valor_ em **Sets** e são _tratados como duplicados_.

```
# 'True' e '1' são considerados o mesmo valor

thisset = {"apple", "banana", "cherry", True, 1, 2}
print(thisset)  # Retorna: {True, 2, 'banana', 'cherry', 'apple'}
```

## Obtendo o comprimento de um Set

Para _determinar_ quantos **itens um Set** possui, basta utilizar a **função** ``len()``.

```
# Obtendo o número de itens em um Set

thisset = {"apple", "banana", "cherry"}
print(len(thisset))  # Retorna: 3
```

## Set itens - Tipos de Dados

Os _itens_ de **Set** podem ser de qualquer _tipo de dados_.

```
# string
set1 = {"apple", "banana", "cherry"}
print(set1)  # Retorna: {'cherry', 'apple', 'banana'}

# int
set2 = {1, 5, 7, 9, 3}
print(set2)  # Retorna: {1, 3, 5, 7, 9}

# boolean
set3 = {True, False, False}
print(set3)  # Retorna: {False, True}
```

- Um **Set** pode conter _diferentes tipos de dados_:
    ```
    # Um Set com 'strings', 'inteiros' e 'booleanos'
    
    set1 = {"abc", 34, True, 40, "male"}
    print(set1)  # Retorna: {True, 34, 40, 'male', 'abc'}
    ```

## ``type()``

Da perspectiva do Python, **Sets** são definidos como _objetos_ com o **tipo de dados** '``set``':

```
<class 'set'>
```

```
myset = {"apple", "banana", "cherry"}
print(type(myset))  # Retorna: <class 'set'>
```

## O construtor ``set()``

É possível usar o _construtor_ ``set()`` para fazer um **Set**.

```
# Usando o construtor 'set()' para fazer um Set

thisset = set(("apple", "banana", "cherry"))
print(thisset)  # Retorna: {'apple', 'banana', 'cherry'}
```

> **Nota**: Observe os _parênteses_ **duplos** com o uso do _construtor_ ``list()``.

## Coleções Python (Arrays)

Existem quatro _tipos de dados integrados_ em Python usados para **armazenar coleções de dados**:

- ``List``: É uma _coleção ordenada_ e **mutável**. Permite _membros duplicados_.
- ``Tuple``: É uma _coleção ordenada_ e **imutável**. Permite _membros duplicados_.
- ``Set``: É uma _coleção não ordenada_, **imutável** e _não indexada_. Nenhum _membro duplicado_.
    - Os itens do ``Set`` não podem ser alterados, mas é possível remover e adicionar itens sempre que desejar.
- ``Dictionary``: É uma _coleção ordenada_ e **mutável**. Nenhum _membro duplicado_.

> Ao escolher um _tipo de dado integrado_ para **armazenar coleções de dados** é útil compreender as _propriedades_ desse tipo. Escolher o tipo certo para uma determinado conjunto de dados pode significar retenção de significado e um aumento na eficiência ou segurança.

---

## Acessar itens

Não é possível _acessar itens_ de um **Set** consultando um _índice_ ou uma _chave_.

- É possível _percorrer os itens_ de um **Set** usando um **loop** ``for`` ou "_perguntar se um valor especificado_" está presente em um **Set** usando a _palavra-chave_ ``in``.
    ```
    # Fazendo um loop pelo Set e Imprimindo os valores
    
    thisset = {"apple", "banana", "cherry"}

    for x in thisset:
        print(x)

    """Retorna:
        apple
        cherry
        banana
    """
    ```

    ```
    # Verificando se "banana" está presente no Set

    thisset = {"apple", "banana", "cherry"}

    print("banana" in thisset)  # Retorna: True
    ```

## Alterar itens

> Depois que um **Set** é criado, não é possível _alterar seus itens_, mas poderá _adicionar novos itens_.

---

## Adicionar itens

> Depois que um **Set** é criado, não é possível _alterar seus itens_, mas poderá _adicionar novos itens_.

- Para _adicionar um item_ a um **Set**, basta utilizar o **método** ``add()``:
    ```
    # Adicionando um item a um Set, usando o método 'add()'

    thisset = {"apple", "banana", "cherry"}
    thisset.add("orange")

    print(thisset)  # Retorna: {'orange', 'apple', 'cherry', 'banana'}
    ```

## Adicionar Sets

- Para _adicionar itens_ de **outro Set** ao **Set atual**, basta utilizar o **método** ``update()``:
    ```
    # Adicionando elementos de 'tropical' em 'thisset'

    thisset = {"apple", "banana", "cherry"}
    tropical = {"pineapple", "mango", "papaya"}

    thisset.update(tropical)

    print(thisset)  # Retorna: {'apple', 'mango', 'cherry', 'pineapple', 'banana', 'papaya'}
    ```

## Adicione qualquer iterável

O _objeto_ no **método** ``update()`` _não precisa ser_ um **Set**, pode ser _qualquer objeto iterável_ (**tuples**, **lists**, **dictionaries** etc.).

```
# Adicionando elementos de uma List ao Set

thisset = {"apple", "banana", "cherry"}
mylist = ["kiwi", "orange"]

thisset.update(mylist)

print(thisset)  # Retorna: {'banana', 'cherry', 'apple', 'orange', 'kiwi'}
```

---

## Remover item

- Para _remover um item_ de um **Set**, basta utilizar o **método** ``remove()`` ou ``discard()``:
    ```
    # Removendo "banana" usando o método 'remove()'

    thisset = {"apple", "banana", "cherry"}
    thisset.remove("banana")

    print(thisset)  # Retorna: {'apple', 'cherry'}
    ```

    > **Nota**: Se o **item** a ser _removido não existir_, o ``remove()`` gerará um **erro**.

    ```
    # Removendo "banana" usando o método 'discard()'

    thisset = {"apple", "banana", "cherry"}
    thisset.discard("banana")

    print(thisset)  # Retorna: {'apple', 'cherry'}
    ```

    > **Nota**: Se o **item** a ser _removido não existir_, o ``discard()`` **NÃO** gerará um **erro**.

Também é possível usar o **método** ``pop()`` para _remover um item_, mas esse **método** _removerá um item aleatório_, portanto não será possível ter certeza de qual _item será removido_.

- O _valor de retorno_ do **método** ``pop()`` é o _item removido_:
    ```
    thisset = {"apple", "banana", "cherry"}
    x = thisset.pop()

    print(x)  # Retorna: cherry (exemplo aleatório - poderia ser qualquer outro valor)
    print(thisset)  # Retorna: {'banana', 'apple'}
    ```

    > **Nota**: Os **Sets** _não são ordenados_, portanto, ao usar o **método** ``pop()``, não se sabe qual _item será removido_.

```
# O método 'clear()' esvazia o Set

thisset = {"apple", "banana", "cherry"}
thisset.clear()

print(thisset)  # Retorna: set()
```

```
# A palavra-chave 'del' excluirá o Set completamente

thisset = {"apple", "banana", "cherry"}
del thisset

print(thisset)  # Retorna: NameError: name 'thisset' is not defined
```

---

## Loop Items

É possível _percorrer os itens_ definidos usando um **loop** ``for``.

```
# Fazendo um loop pelo Set e Imprimindo os valores

thisset = {"apple", "banana", "cherry"}

for x in thisset:
    print(x)

"""Retorna:
    apple
    banana
    cherry
"""
```

---

## Juntando dois Sets

Existem _várias maneiras_ de **unir dois ou mais Sets** em Python.

- É possível usar o **método** ``union()`` que retorna um _novo_ **Set** contendo _todos os itens_ de ambos os **Sets**, ou o **método** ``update()`` que _insere todos os itens_ de um **Set** em outro:
    ```
    # O método 'union()' retorna um novo Set com todos os itens de ambos os Sets

    set1 = {"a", "b", "c"}
    set2 = {1, 2, 3}

    set3 = set1.union(set2)
    print(set3)  # Retorna: {'b', 2, 'a', 'c', 3, 1}
    ```

    ```
    # O método 'update()' insere os itens do 'set2' no 'set1'

    set1 = {"a", "b", "c"}
    set2 = {1, 2, 3}

    set1.update(set2)
    print(set1)  # Retorna: {'c', 'a', 3, 2, 1, 'b'}
    ```

    > **Nota**: _Ambos_ ``union()`` e ``update()`` **excluirão** quaisquer _itens duplicados_.

## Mantenha SOMENTE as duplicatas

O **método** ``intersection_update()`` manterá apenas os _itens_ que estão presentes em **ambos os Sets**.

```
# Mantendo os itens que existem em Set 'x' e Set 'y'

x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

x.intersection_update(y)

print(x)  # Retorna: {'apple'}
```

O **método** ``intersection()`` retornará um _novo_ **Set**, que contém apenas os _itens_ que estão presentes em **ambos os Sets**.

```
# Retornando um Set que contém os itens que existem em Set 'x' e Set 'y'

x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

z = x.intersection(y)

print(z)  # Retorna: {'apple'}
```

## Mantenha tudo, mas NÃO as duplicatas

- O **método** ``symmetric_difference_update()`` manterá _apenas os elementos_ que **NÃO** estão presentes em **ambos os Sets**:
    ```
    # Mantendo os itens que não estão presentes em ambos os Sets

    x = {"apple", "banana", "cherry"}
    y = {"google", "microsoft", "apple"}

    x.symmetric_difference_update(y)

    print(x)  # Retorna: {'google', 'banana', 'microsoft', 'cherry'}
    ```

- O **método** ``symmetric_difference()`` retornará um **novo Set**, que contém _apenas os elementos_ que **NÃO** estão presentes em **ambos os Sets**:
    ```
    x = {"apple", "banana", "cherry"}
    y = {"google", "microsoft", "apple"}

    z = x.symmetric_difference(y)

    print(z)  # Retorna: {'google', 'banana', 'microsoft', 'cherry'}
    ```

> **Nota**: Os valores ``True`` e ``1`` são considerados o _mesmo valor_ em **Sets** e são tratados como _duplicados_.

```
# 'True' e '1' são considerados o mesmo valor

x = {"apple", "banana", "cherry", True}
y = {"google", 1, "apple", 2}

z = x.symmetric_difference(y)

print(z)  # Retorna: {2, 'google', 'cherry', 'banana'}
```

---

## Métodos Set

Python possui um _conjunto_ de **métodos** integrados que podem ser usados em **Set**.

- ``add()``: Adiciona um _elemento_ ao **Set**.
- ``clear()``: Remove _todos os elementos_ do **Set**.
- ``copy()``: Retorna uma _cópia_ do **Set**.
- ``difference()``: Retorna um **Set** contendo a _diferença_ entre dois ou mais **Sets**.
- ``difference_update()``: Remove os _itens_ deste **Set** que também estão incluídos em outro **Set** especificado.
- ``discard()``: Remove o _item_ especificado.
- ``intersection()``: Retorna um **Set**, que é a _intersecção_ de dois outros **Sets**.
- ``intersection_update()``: Remove os _itens_ deste **Set** que não estão presentes em outro(s) **Sets** especificado(s).
- ``isdisjoint()``: Retorna se dois **Sets** têm _intersecção_ ou **não**.
- ``issubset()``: Retorna se outro **Set** contém este **Set** ou **não**.
- ``issuperset()``: Retorna se este **Set** contém outro **Set** ou **não**.
- ``pop()``: Remove um _elemento_ do **Set**.
- ``remove()``: Remove o _elemento_ especificado.
- ``symmetric_difference()``: Retorna um **Set** com as _diferenças simétricas_ de dois **Sets**.
- ``symmetric_difference_update()``: Insere as _diferenças simétricas_ deste **Set** e de outro.
- ``union()``: Retorne um **Set** contendo a _união_ de **Sets**.
- ``update()``: Atualize o **Set** com a _união_ deste **Set** e de outros.

---