# Create Database

### Sumário:

- [Criando um banco de dados](#criando-um-banco-de-dados)
- [Verifique se o banco de dados existe](#verifique-se-o-banco-de-dados-existe)

---

## Criando um banco de dados

Para criar um **banco de dados** no ``MySQL``, basta utilizar a _instrução_ "``CREATE DATABASE``".

```
import mysql.connector

mydb = mysql.connector.connect(
    host="localhost",
    user="test",
    password="123456789"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE DATABASE mydatabase")
```

## Verifique se o banco de dados existe

É possível "verificar" se existe um **banco de dados** _listando todos os **bancos de dados** no sistema_ usando a **instrução** "``SHOW DATABASES``".

```
import mysql.connector

mydb = mysql.connector.connect(
    host="localhost",
    user="test",
    password="123456789"
)

mycursor = mydb.cursor()

mycursor.execute("SHOW DATABASES")

for x in mycursor:
    print(x)
```

É possível _acessar o **banco de dados** ao fazer a conexão_.

```
import mysql.connector

mydb = mysql.connector.connect(
    host="localhost",
    user="test",
    password="123456789",
    database="mydatabase"
)
```

> **Nota**: Se o **banco de dados** não existir será retornado um _erro_.

---