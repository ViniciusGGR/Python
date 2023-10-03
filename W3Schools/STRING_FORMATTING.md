# String Formatting

### Sumário:

- [String format()](#string-format)
- [Vários valores](#vários-valores)
- [Números de índice](#números-de-índice)
- [Índices Nomeados](#índices-nomeados)

---

Para _garantir_ que uma **string** seja exibida conforme esperado, é possível _formatar o resultado_ com o **método** ``format()``.

## String format()

O **método** ``format()`` permite _formatar partes selecionadas_ de uma **string**.

Às vezes há "**partes de um texto**" que não é possível controlar, talvez elas venham de um _banco de dados_ ou de _entrada do usuário_. Para "**controlar**" tais _valores_, adicione **espaços reservados** (colchetes ``{}``) no texto e execute os _valores_ através do **método** ``format()``.

```
# Adicionando um 'espaço reservado' onde deseja exibir o 'price'

price = 49

txt = "The price is {} dollars."
print(txt.format(price))  # Retorna: The price is 49 dollars.
```

- É possível adicionar **parâmetros** entre _chaves_ para especificar como _converter o valor_:
    ```
    price = 49

    txt = "The price is {:.2f} dollars."
    print(txt.format(price))  # Retorna: The price is 49.00 dollars.
    ```

## Vários valores

- Se quiser usar mais _valores_, basta adicionar mais _valores_ ao **método** ``format()``:
    ```
    print(myorder.format(price, itemno, quantity))
    ```

    E adicione mais **espaços reservados**:

    ```
    quantity = 3
    itemno = 567
    price = 49

    myorder = "I want {} pieces of item number {} for {:.2f} dollars."
    print(myorder.format(quantity, itemno, price))

    # Retorna: I want 3 pieces of item number 567 for 49.00 dollars.
    ```

## Números de índice

É possível usar _números de índice_ (um **número entre chaves** ``{0}``) para "_garantir_" que os _valores_ sejam colocados nos **espaços reservados** corretos.

```
quantity = 3
itemno = 567
price = 49

myorder = "I want {0} pieces of item number {1} for {2:.2f} dollars."
print(myorder.format(quantity, itemno, price))

# Retorna: I want 3 pieces of item number 567 for 49.00 dollars.
```

- Além disso, é possível "referir-se" ao _mesmo valor **mais de uma vez**_, utilizando o _número do índice_:
    ```
    age = 36
    name = "John"

    txt = "His name is {1}. {1} is {0} years old."
    print(txt.format(age, name))

    # Retorna: His name is John. John is 36 years old.
    ```

## Índices Nomeados

É possível usar _índices nomeados_ inserindo um **nome** entre "chaves" ``{carname}``, mas então deve-se usar _nomes_ ao passsar os _valores_ dos **parâmetros**: ``txt.format(carname = "Ford")``.

```
myorder = "I have a {carname}, it is a {model}."
print(myorder.format(carname = "Ford", model = "Mustang"))

# Retorna: I have a Ford, it is a Mustang.
```

---