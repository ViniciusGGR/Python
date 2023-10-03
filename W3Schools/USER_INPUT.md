# User Input

### Sumário

- [User Input](#user-input-1)

---

## User Input

Python _permite_ a **entrada do usuário** (User Input). Isso significa que é possível "**pedir informações**" ao _usuário_.

- O **método** é um pouco diferente no Python ``3.6`` e no Python ``2.7``:
    - O Python ``3.6`` usa o **método** ``input()``.
    - O Python ``2.7`` usa o **método** ``raw_input()``.

O exemplo a seguir "pede" o _nome de usuário_ e, quando digitado o _nome de usuário_, ele é **impresso** na tela.

```
# Python 3.6

username = input("Enter username: ")
print("Username is: {}".format(username))
```

```
# Python 2.7

username = raw_input("Enter username: ")
print("Username is: " + username)
```

> **Nota**: Python _para de executar_ quando se trata da **função** ``input()`` e **continua** quando o _usuário fornece_ alguma **entrada**.

---