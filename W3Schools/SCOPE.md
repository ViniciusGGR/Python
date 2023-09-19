# Scope

### Sumário:

- [Escopo Local](#escopo-local)
    - [Função dentro da Função](#função-dentro-da-função)
- [Escopo Global](#escopo-global)
    - [Nomeando Variáveis](#nomeando-variáveis)
- [Palavra-chave global](#palavra-chave-global)

---

Uma **variável** só está disponível dentro da "**região**" em que foi _criada_. Isso é chamado de ``Escopo - (Scope)``.

## Escopo Local

Uma **variável** _criada dentro_ de uma **função** pertence ao _``Escopo`` local_ dessa **função** e só pode ser "usada" dentro dessa **função**.

```
# Uma variável criada dentro de uma função está disponível dentro dessa função

def myfunc():
    x = 300
    print(x)

myfunc()

# Retorna: 300
```

### Função dentro da Função

- Uma **variável** ``x`` _não está disponível fora de uma **função**_, mas está _disponível para qualquer **função** dentro da **função**_:
    ```
    # A variável local pode ser acessada a partir de uma função dentro da função

    def myfunc():
        x = 300
        def myiinerfunc():
            print(x)
        myinnerfunc()

    myfunc()

    # Retorna: 300
    ```

## Escopo Global

Uma **variável** _criada_ no "corpo principal" do código Python é uma **variável ``global``** e pertence ao _Escopo ``global``_.

**Variáveis ``globais``** estão disponíveis em qualquer _Escopo_, ``global`` e ``local``.

```
# Criando uma variável fora de uma função, portanto ela é 'global' e pode ser usada por qualquer pessoa

x = 300

def myfunc():
    print(x)

myfunc()  # Retorna: 300

print(x)  # Retorna: 300
```

### Nomeando Variáveis

- É possível **operar** com o _mesmo nome de **variável** dentro e fora_ de uma **função**, o Python irá tratá-las como _duas **variáveis** separadas_, uma disponível no _Escopo ``global``_ (fora da **função**) e outra disponível no _Escopo ``local``_ (dentro da **função**):
    ```
    # A função imprimirá o "local" 'x' e então o código imprimirá o "global" 'x'

    x = 300

    def myfunc():
        x = 200
        print(x)

    myfunc()  # Retorna: 200

    print(x)  # Retorna: 300
    ```

## Palavra-chave ``global``

Caso precise _criar_ uma **variável ``global``**, mas esteja "preso" no _Escopo ``local``_, basta usar a **palavra-chave** ``global``.

- A **palavra-chave** ``global`` torna a **variável ``global``**:
    ```
    # Se utilizar a palavra-chave 'global', a variável pertence ao escopo 'global'

    def myfunc():
        global x
        x = 300

    myfunc()

    print(x)  # Retorna: 300
    ```

- Também é possível utilizar a **palavra-chave** ``global`` se quiser fazer uma _alteração em uma **variável** ``global``_ dentro de uma **função**:
    ```
    # Para alterar o valor de uma variável 'global' dentro de uma função, consulte a variável usando a palavra-chave 'global'

    x = 300

    def myfunc():
        global x
        x = 200

    myfunc()

    print(x)  # Retorna: 200
    ```

---